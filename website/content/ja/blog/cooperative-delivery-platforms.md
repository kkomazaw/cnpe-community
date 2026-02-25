---
title:  "アプリケーションのためのインフラストラクチャ：協調的配信のためのプラットフォーム"
date:   2022-09-22 00:00:00 +0000
author: Josh Gavant
categories:
- Announcement
tags:
- WG Platforms
- Event
---

![インフラストラクチャの統合](/images/infrastructure-integration.png)

TAG App Delivery は、インフラストラクチャ機能とアプリケーションの協調的なデリバリーに関する新たなトレンドを収集し、報告するために、2021 年後半に Cooperative Delivery ワーキンググループを設立しました。TAG は、インフラストラクチャチームはソフトウェア開発手法をうまく採用し、GitOps や IaC (Infrastructure as Code) などを通じて機能や修正を継続的にデプロイしている一方で、インフラストラクチャ機能のデリバリーは、そのインフラストラクチャを使用するアプリケーションのデリバリーとよく調整されていないことが多いと指摘しました。つまり、アプリケーションとインフラストラクチャのデリバリーには*ギャップ*があり、そのギャップを埋めるためには調整/協力が必要なのです。

本グループの主な目的は、a) ギャップの存在という仮説の確認、b) エンドユーザーへの影響の明確化、c) 連携促進のための新たな動向の特定と推進です。例えば、グループの[最初の仮説](https://github.com/Cloud-Native-Platform-Engineering/cnpe-community/blob/main/cooperative-delivery-wg/charter/README.md#examples-of-known-patterns-aimed-to-deploy-applications)では、以下の既存のトレンドが言及されています：

- GitOps：宣言型記述子からの設定を恒等的に継続的に調整
- オペレーター：調整指向のサービス
- パイプライン：サービスとアプリケーションの命令型オーケストレーション

本稿では、エンドユーザーやBackstage、Crossplane、Dapr、KubeVelaなどの新興[CNCFプロジェクト](https://landscape.cncf.io/card-mode?category=application-definition-image-build,continuous-integration-delivery&grouping=no)から学んだ新たな動向を検証します。

また、過去1年間で「インフラチームとアプリケーションチームの協力」こそが目指すべき目標である一方、「協調的デリバリー」という用語は多くの貢献者にとって馴染みの薄いものであることも判明しました。この協力関係が「内部開発者プラットフォーム（IDP）」や新興のプラットフォームエンジニアリング運動の目標でもあることを踏まえ、ワーキンググループの名称を「Platforms」に変更する準備を進めています。

ユーザーや貢献者の皆様からのご意見をお待ちしております。組織におけるアプリケーションとインフラストラクチャのデリバリー連携方法について、[こちらのGitHubフォーム](https://github.com/Cloud-Native-Platform-Engineering/cnpe-community/issues/new/choose)からご共有いただき、ご意見は [GitHub](https://github.com/Cloud-Native-Platform-Engineering/cnpe-community/discussions) または [Slack](https://cloud-native.slack.com/archives/CL3SL0CP5) でご意見をお聞かせください。

## プラットフォームエンジニアリング

当初の仮説を超え、インフラとアプリケーションの連携において顕在化した新たな潮流がプラットフォームエンジニアリング（PE）であり、特にその核心となる**セルフサービス可能な機能**の原則です。例えば[Backstage](https://www.cncf.io/projects/backstage/)は、こうした新興プラットフォーム向けの代表的なポータルフレームワークです。Humanitecのリーダーである[Luca Galante](https://platformengineering.org/authors/luca-galante)によれば、プラットフォームエンジニアリングとは「クラウドネイティブ時代におけるソフトウェアエンジニアリング組織に**セルフサービス**機能を実現するツールチェーンとワークフローを設計・構築する分野である（[リンク](https://platformengineering.org/blog/what-is-platform-engineering)）」と定義されています。*セルフサービス*とは、協調的デリバリー（協働的提供）の仕組みを指します。開発者が文書化された手順に従い、オンデマンドでアプリ内の機能をプロビジョニング（調達）し利用する形態です。

セルフサービスというパラダイムに加え、プラットフォームエンジニアリングは**アプリケーション開発者や運用担当者（プラットフォーム利用者）のニーズに焦点を当てます**。これにより、PE（プラットフォームエンジニア）は開発者や他のプラットフォーム利用者への共感を高め、フィードバックを収集し、製品開発者がエンドユーザーに対して行うように、反復的に改善してニーズを満たすことができます。この焦点の移行により、プラットフォーム開発はインフラチームが帯域外コストセンターとなるのではなく、企業の真の価値ストリームとより適切に連携します。厳密には技術的ではありませんが、**プラットフォームエンジニアリングとアプリケーションチーム間の共感的な関係性**が、インフラ機能とアプリ要件のより良い調整につながります。

こうしたプラットフォームは通常、Kubernetes、Helm、Prometheus、Backstage、Istio、Knative、KeptnなどCNCFの基盤プロジェクトを用いて構築されます。

## 万能のKubernetes

[Crossplane](https://www.cncf.io/projects/crossplane/)のようなプロジェクトで確認されたもう一つの傾向は、あらゆる種類のインフラ機能やアプリケーションコンポーネントの設定・管理にKubernetesリソースモデルが採用されていることです。ユーザーはもはや、デプロイメント、ボリューム、イングレスだけを Kubernetes API 経由でプロビジョニングするわけではありません。カスタムリソース定義 (CRD) により、データベース、ID、メッセージブローカー、可観測性システムなど、さらに多くのものをプロビジョニングできるようになりました。

[GitOps](https://www.cncf.io/projects/opengitops/) の動きは、アプリケーションの継続的な調整の価値を実証しました。利用可能なリソースタイプが非常に多くなったことで、開発者はアプリケーションと同じ方法でインフラストラクチャを調整できるようになりました。独自のインフラストラクチャ機能を提供するユーザーにとって、[Operator Framework](https://www.cncf.io/projects/operator-framework/) は、カスタム Kubernetes ベースのリコンサイラー実装のための人気のある基盤です。

## 機能注入

最後に、[Dapr](https://www.cncf.io/projects/dapr/) や [KubeVela](https://www.cncf.io/projects/kubevela/) といったプロジェクトに注目しています。これらは推論と遅延解決・機能注入を通じて、アプリケーション向けのインフラ機能を調整することを目指しています。これらのプロジェクトでは、アプリ開発者にデータベースやメッセージブローカーなど必要な機能を宣言させ、実行時にサイドカーコンテナやeBPFプログラムを用いて実際の実装を解決することが多いです。Istio(https://www.redhat.com/en/blog/istio-service-mesh-applies-become-cncf-project)のようなプロジェクトでは、アプリ開発者に対して機能を透過的に注入することさえ可能です。

レイト・リゾリューションとインジェクションは、アプリケーションとインフラストラクチャの結合を緩め、「協調的」なデリバリーのもう一つの形です。アプリケーションのコンテキストに応じて、AWS の RDS インスタンス、GCP の CloudSQL インスタンス、オンプレミスの [CloudNativePG](https://cloudnative-pg.io/) インスタンスなど、さまざまなプロバイダからデータベースを取得することを想像してみてください。

## 結論

Cooperative Delivery WG（まもなく Platforms WG に名称変更予定）の使命は、インフラストラクチャ機能とアプリケーションの連携におけるギャップに対処します、新たなトレンドに関するフィードバックを収集し、その重要性を強調することです。このトピックや、アプリケーションおよびプラットフォームの開発者や運用者に関連するその他のトピックを推進するために、TAG App Delivery にぜひご参加ください（https://github.com/cncf/tag-app-delivery）。

<sub>画像クレジット https://www.cleo.com/blog/knowledge-base-cloud-integration-platform</sub>
