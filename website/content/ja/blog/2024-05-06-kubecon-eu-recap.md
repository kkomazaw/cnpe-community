---
title:  KubeCon EU 2024におけるプラットフォームエンジニアリング - 振り返り
slug:   platform-engineering-at-kubecon-eu-2024-recap
date:   2024-05-06 12:00:00 +0000
author: Atulpriya Sharma
categories:
- Article
tags:
- Event
- WG Platforms
- Community Contribution
---

ちょうど1ヶ月前、Kubernetesユーザーと専門家たちが光の都パリに集結し、KubeConのヨーロッパ版が開催されました。[12,000人以上の現地参加者を集め、このKubeConは近年最大規模の大会の一つとなりました](https://www.cncf.io/blog/2024/03/28/missed-kubecon-cloudnativecon-europe-2024-heres-everything-you-need-to-know/)。

人工知能（AI）や生成AIへの注目と話題が非常に多かった一方で、プラットフォームエンジニアリングも十分な存在感を示しました。今回初めて「プラットフォームエンジニアリング・デイ」が設けられ、熱心な参加者がプラットフォームエンジニアリングに関連するあらゆる事柄を議論する専用の場が提供されました。

本記事では、KubeCon 2024で開催されたプラットフォームエンジニアリング関連の講演と議論を解説します。

## KubeCon EUにおけるTAG App Delivery & WG-Platforms

TAG App Deliveryは、クラウドネイティブアプリケーションの構築、パッケージング、デプロイ、管理、運用を含むデリバリーに関連するプロジェクトやイニシアチブを支援することを目的としています。TAGのイニシアチブの一つであるPlatformsワーキンググループは、プラットフォームエンジニアリングの取り組みを支援し、改善し、推進することに専念しています。

KubeCon EUでは、同グループの活動認知度向上のため、ブースにて講演やセッションが開催されました。詳細は[前回のブログ記事](https://tag-app-delivery.cncf.io/blog/tag-app-delivery-at-kubecon-eu-2024/)をご覧ください。TAGアプリデリバリーまたはプラットフォームワーキンググループについて初めて知る方は、以下の講演動画をご覧ください：

* [ミームで探るApp Deliveryの奥深さ](https://sched.co/1YhhV)
* [TAG App Delivery プラットフォームワーキンググループ最新情報](https://sched.co/1ZiQB)

## Platform Engineering Day
まずは、初開催となったPlatform Engineering Dayの素晴らしい講演をご紹介します。会場に少し遅れて入った時、満席で立ち見の人々も講演に耳を傾けている光景が印象的でした。
![Platform Engineering Day - KubeCon EU 2024](/images/platform-engineering-day-kubecon-eu-2024.png)

### トーク

* [TAG App Deliveryプラットフォームワーキンググループ最新情報](https://colocatedeventseu2024.sched.com/event/1ZiQB) - KrumwareのColin Griffinが、プラットフォームワーキンググループの概要と参加方法について説明します。

* [時には、口紅こそが豚に必要なものなのだ！](https://colocatedeventseu2024. sched.com/event/1YFdf/sometimes-lipstick-is-exactly-what-a-pig-needs-abby-bangser-syntasso-whitney-lee-vmware) - SyntassoのAbby BangserとVMwareのWhitney Leeが、基盤技術の完成以上に、内部開発者プラットフォームにおけるユーザーインターフェースと採用への投資の重要性を強調。

* [Ritchie Brothersにおけるプラットフォーム思考の超越 - 誰も予想しない場所で、誰も予想しないものを構築する](https://colocatedeventseu2024. sched.com/event/1YFe7/beyond-platform-thinking-at-ritchie-brothers-build-things-no-one-expects-in-a-place-no-one-expect-bryan-oliver-thoughtworks-ranbir-chawla-ritchie-bros) - ThoughtworksのBryan OliverとRitchie BrosのRanbir Chawlaが、Ritchie BrosがKubernetesの機能を単なる配信プラットフォームを超えて拡張し、中核事業を推進した方法を議論します。

* [イノベーションの設計図：ユーザーフレンドリーな開発者プラットフォームへの道筋を整備するエンジニアリング](https://colocatedeventseu2024. sched.com/event/1YFek/cl-lightning-talk-blueprints-of-innovation-engineering-paved-paths-for-a-user-friendly-developer-platform-ahmed-bebars-the-new-york-times)- ニューヨーク・タイムズのAhmed Bebars - クラウドにおけるプラットフォームエンジニアリングの微妙なニュアンスに関する貴重な洞察を提供し、組織内で戦略を実装するための青写真を示します。

* [kcpによるプラットフォームエンジニアリングAPIレイヤーの構築](https://colocatedeventseu2024.sched.com/event/1YFfY/building-a-platform-engineering-api-layer-with-kcp-marvin-beckers-kubermatic-gmbh) - Kubermatic GmbHのMarvin Beckersが、kcpが全内部サービス向けグローバル制御プレーンでプラットフォームエンジニアリングを強化する方法を解説。

* [型破りなアプローチ：Platform as a Productにおけるアンチアーキテクチャパターンの解明](https://colocatedeventseu2024.sched.com/event/1YFgi/cl-lightning-talk-breaking-the-mold-unveiling-anti-architectural-patterns-in-platform-as-a-product-vamshi-krishna-samudrala-american-airlines) - アメリカン航空のVamshi Krishna Samudrala氏 - 効果的なプラットフォームの設計と実装における複雑な状況について議論します。

* [巨人を強化する：運用技術選択におけるCNOEで企業を導く](https:// colocatedeventseu2024.sched.com/event/1YFgu/cl-lightning-talk-empowering-giants-guide-your-enterprise-with-cnoe-in-operational-tech-choices-engin-diri-pulumi) - PulumiのEngin DiriがCNOEフレームワークを紹介し、参加が組織の課題克服にどう貢献するかを探ります。

* [成功を導く設計：内部開発者プラットフォームのためのUX原則](https://colocatedeventseu2024.sched.com/event/1YFhD/designing-for-success-ux-principles-for-internal-developer-platforms-kirsten-schwarzer-octopus-deploy) - Octopus DeployのKirsten Schwarzerが、開発者が愛用する内部開発者プラットフォーム（IDP）を設計するための実践的なUX原則とツールを紹介します。

* [プロダクト思考で開発者プラットフォームチームを強化する](https://colocatedeventseu2024.sched.com/event/1YFhg/boosting-developer-platform-teams-with-product-thinking-samantha-coffman-spotify) - SpotifyのSamantha Coffmanが、プラットフォーム構築におけるプロダクトアプローチの有効性について語ります。

* [クラウドネイティブOSSで構築するAI駆動の舗装済み道路プラットフォーム](https://colocatedeventseu2024.sched.com/event/1YFi2/building-an-ai-powered-paved-road-platform-with-cloud-native-oss-todd-ekenstam-avni-sharma-intuit) - IntuitのTodd Ekenstam氏とAvni Sharma氏が、Open Application Model、Istio、Karpenter、Argo Rolloutsなどのオープンソースプロジェクトを統合・拡張し、AIネイティブアプリケーションプラットフォームを構築する方法について解説します。

* [イノベーションの解き放ち：NatWest銀行がクラウドネイティブツールを活用しPlatform as a Productを実現する方法](https://colocatedeventseu2024.sched.com/event/1YFif/unlocking-innovation-how-natwest-bank-uses-cloud-native-tools -to-deliver-platform-as-a-product-chris-plank-natwest-group-derik-evangelista-syntasso) - NatWest GroupのChris PlankとSyntassoのDerik Evangelistaが、GitOpsアプローチに焦点を当て、プラットフォームユーザーがシームレスな開発者体験を得られるよう様々なツールを組み込んだ手法について議論します。

* [K8Sを超えて－プラットフォームエンジニアリングの成熟化](https://colocatedeventseu2024.sched.com/event/1YFj9/to-k8s-and-beyond-maturing-your-platform-engineering-initiative-nicki-watt-opencredo) - OpenCredoのNicki Wattが、最近公開されたCNCFプラットフォーム成熟度モデルをツールボックスの一部として活用し、組織が考え抜く手助けをする方法についての洞察を共有します。

### パネルディスカッション

* [パネル：プラットフォームエンジニアリングの卓越性への道筋：包括的ガイド](https://colocatedeventseu2024.sched.com/event/1YFjf/panel-navigating-the-path-to-platform-engineering-excellence-a-comprehensive-guide-cortney-nickerson-kubeshop-william-rizzo-suse-abby-bangser-syntasso-areti-panou-sap-se-aparna-subramanian-shopify)- KubeshopのCortney Nickerson氏; SUSEのWilliam Rizzo、SyntassoのAbby Bangser、SAP SEのAreti Panou、ShopifyのAparna Subramanianが、効果的なプラットフォームエンジニアリングを確保するための実践的なステップと、自社プラットフォームへの投資を検討するすべての人にとって重要な考慮事項を分析しました。

* [パネルディスカッション: プラットフォームのじゃんけん：構築、採用、購入](https://colocatedeventseu2024.sched.com/event/1YFgB/panel-the-platform-rock-paper-scissors-build-adopt-buy-jorge-lainfiesta-independent-contributor-leena-mooneeram-chainalysis-victor-araujo-wolt-jinhong-brejnholt-saxo-bank-edgaras-petovradzius-lego-group) - Jorge Lainfiesta（独立寄稿者）、Leena Mooneeram（Chainalysis）、Victor Araujo（Wolt）、Jinhong Brejnholt（Saxo Bank）、Edgaras Petovradžius（LEGO）が、プラットフォーム基盤構築における予算・ロックイン・ライセンスの調整と意思決定について見解を共有しました。

## KubeConにおける講演とパネルディスカッション

プラットフォームエンジニアリングはKubeCon 2024で最も注目を集めた併催イベントの一つでしたが、[BackstageCon](https://colocatedeventseu2024.sched.com/overview/type/BackstageCon)、 [AppDevCon](https://colocatedeventseu2024.sched.com/overview/type/AppDeveloperCon)、[ArgoCon](https://colocatedeventseu2024.sched.com/overview/type/ArgoCon)、[MultitenancyCon](https://colocatedeventseu2024.sched.com/overview/type/Multi-TenancyCon)、[OpenShift Commons](https://commons.openshift) 、[MultitenancyCon](https://colocatedeventseu2024.sched.com/overview/type/Multi-TenancyCon)、[OpenShift Commons](https://commons.openshift.org/gatherings/kubecon-24-mar-19/)など、数多くのイベントが開催されました。

以下にそれらをまとめてご紹介します：

### 1日目 - 3月20日

* [Bloombergのマルチクラスタワークフローオーケストレーションプラットフォームへの道程](https://kccnceu2024.sched.com/event/1YeLy/bloombergs-journey-to-a-multi-cluster-workflow-orchestration-platform-yao-lin-reinhard-tartler-bloomberg) - BroombergのYao Lin氏とReinhard Tartler氏が、関連プロジェクトの調査方法と、KarmadaやOCMなどから得たインスピレーションを基に自社オーケストレーションプラットフォームを構築した経緯を解説します。

* [Kubernetesコントローラーを用いた大規模マルチクラウド・マルチリージョンSaaSプラットフォームの構築](https://kccnceu2024.sched.com/event/1YeML/building-a-large-scale-multi-cloud-multi-region-saas-platform-with-kubernetes-controllers-sebastien-guilloux-elastic) - ElasticのSébastien Guillouxが、数百のKubernetesクラスターで構成されるアーキテクチャを説明し、マルチクラウド・マルチリージョンプラットフォーム構築の過程で直面した課題について語ります。

* [クラウドネイティブ開発者の内側と外側のループを簡素化する](https://kccnceu2024.sched.com/event/1YeMJ/simplified-inner-and-outer-cloud-native-developer-loops-oleg-selajev-atomicjar-alice-gibbons-diagrid) - AtomicJarのOleg ŠelajevとDiagridのAlice Gibbonsが、プラットフォームエンジニアリングとポリグロットアプローチを通じて開発者の生産性を簡素化・向上させるツールを探求します。

* [AI対応プラットフォーム構築 - 開発者とプラットフォームエンジニアのためのシンフォニー](https://kccnceu2024.sched.com/event/1YeMm/building-ai-ready-platforms-symphony-for-developer-and-platform-engineer-thomas-vitale-systematic-lize-raes-langchain4j) - SystematicのThomas Vitale氏とLangChain4jのLize Raes氏が、プラットフォームエンジニアと開発者の間のギャップを埋める詳細を共有。AI対応プラットフォームへの適応と、スムーズな開発者体験の提供に焦点を当てています。

* [ノルウェー公共部門におけるプラットフォーム成熟度の現状](https://kccnceu2024.sched.com/event/1YeMj/state-of-platform-maturity-in-the-norwegian-public-sector-hans-kristian-flaatten-norwegian-labor-and-welfare-administration) - ノルウェー労働福祉庁のハンス・クリスティアン・フラッテンは、新たに公開されたCNCFプラットフォームエンジニアリング成熟度モデルを用いて、自組織のプラットフォームの成熟度と選択した技術を測定しています。

* [文化の変革：プラットフォームエンジニアリングにおけるカオスファースト思考の醸成](https://kccnceu2024.sched.com/event/1YeNB/cultural-shifts-fostering-a-chaos-first-mindset-in-platform-engineering-sayan-mondal-harness-raj-vadheraju-fis) - HarnessのSayan MondalとFISのRaj Vadherajuが、カオスファーストの原則を活用して組織がプラットフォームエンジニアリングの実践を強化する方法について語ります。

### 2日目 - 3月21日

* [オープンインターフェースによる新たなプラットフォーム体験の実現](https://kccnceu2024.sched.com/event/1YeOr/unlocking-new-platform-experiences-with-open-interfaces-thomas-vitale-systematic-mauricio-salaboy-salatino-diagrid) - SystematicのThomas VitaleとDiagridのMauricio 「Salaboy」 サラティーノが既存のCNCFプロジェクトを探索し、プラットフォーム構築のためのエンドツーエンド体験を実装する方法を解説します。

* [ブロックの流れを維持する： 製造向けプラットフォームエンジニアリングへのLEGOグループのアプローチ](https://kccnceu2024.sched.com/event/1YePF/keeping-the-bricks-flowing-the-lego-groups-approach-to-platform-engineering-for-manufacturing-mads-hogstedt-danquah-jeppe-lund-andersen-the-lego-group)
 
- LEGOグループのMads Høgstedt Danquah氏とJeppe Lund Andersen氏が、24時間365日の生産、限定的なインターネット接続、高い耐障害性と低遅延といった制約に対応するプラットフォームと製品をレゴグループが構築する手法について語ります。

* [プラットフォームにKubernetesが不適切な理由と改善方法](https://kccnceu2024.sched.com/event/1YePC/why-kubernetes-is-inappropriate-for-platforms-and-how-to-make-it-better-stefan-schimanski-upbound-mangirdas-judeikis-cast-ai-sebastian-scheele-kubermatic).- UpboundのStefan Schimanski、Cast AIのMangirdas Judeikis、 KubermaticのSebastian Scheele - Kubeの拡張と、プラットフォームに適したアーキテクチャへの適応について語ります。

### 3日目 - 3月22日

* [AutodeskにおけるIDP機能の迅速な開発と自動テスト](https://kccnceu2024.sched.com/event/1YeRp/rapid-idp-capability-development-and-automated-testing-at-autodesk-jesse-sanford-greg-haynes-autodesk) - AutodeskのJesse Sanford と Greg Haynesが、IDPBuilderがDocker以外の事前依存関係なしで数分でCNOEリファレンスアーキテクチャを構築する方法を示します。

* [Shopifyでの検索: データ耐障害性とコンプライアンスのための高可用性プラットフォーム](https://kccnceu2024.sched.com/event/1YeSk/search-at-shopify-highly-available-platform-for-data-resilience-and-compliance-leila-vayghan-shopify) - ShopifyのLeila Vayghanが、毎分数百万件のドキュメントを順序通りかつリアルタイムにインデックス化し高可用性を実現するKafkaの活用例を紹介します。

### パネルディスカッションとブース内トーク

_KubeConではプラットフォームエンジニアリングに関する話題が非常に盛り上がっていましたが！_
メインカンファレンスの講演に加え、パネルディスカッションや併催イベント、TAG App Deliveryブースでのトークも開催されました。全講演の動画は公開されていませんが、Backstageを活用したセルフサービス型インフラやKubernetes開発者体験のパターンなど、興味深いトピックがいくつかありました。

Lian, Thomas, Mauricio, Atulは、Red Hat OpenCommons併催イベントにてパネルディスカッション「プラットフォームエンジニアリングから開発者成功へ」(https://www.youtube.com/watch?v=PfrUObDwvyQ)に参加しました。

KubeConへの参加経験から言えるのは、プラットフォームエンジニアリング分野において、今回が最も充実した内容の一つだったということです。講演は魅力的で、プラットフォームワーキンググループは活発に活動し、ブースは活気に満ちていました。

[KubeCon NA 2024のCFP募集が既に開始されています](https://events.linuxfoundation.org/kubecon-cloudnativecon-north-america/program/cfp/) が始まっているので、プラットフォームエンジニアリングに関する興味深い提案を共有し、皆さんが取り組んでいる素晴らしいことを世界に知らせてください。

## プラットフォームコーヒーミートアップ - パリ編

プラットフォームワーキンググループで私が特に気に入っているのは、KubeCon開催中に企画する対面式の**コーヒーミートアップ**です。初めて参加したのはKubeConシカゴで、このコンセプトに魅了されました。

コーヒーを片手に、プラットフォームとプラットフォームエンジニアリングに関するあらゆる話題を、どなたでも自由に議論できる場です。プラットフォームエンジニアリングの世界で起きていることを学び、その背景にいる素晴らしい人々と出会える、素晴らしい体験です。
<blockquote class="twitter-tweet"><p lang="en" dir="ltr">プラットフォームリーンコーヒーミートアップ開催中。今日は本当に素晴らしいトピックを議論しています。<br><br>この企画を提案してくれた<a href="https://twitter.com/CNCFTAGApp?ref_src=twsrc%5Etfw">@CNCFTAGApp</a>のWG-Platformsグループに感謝します。<br><br>スポンサーの<a href="https://twitter.com/syntasso?ref_src=twsrc%5Etfw">@syntasso</a> <a href="https://twitter.com/krumware?ref_src=twsrc%5Etfw">@ krumware</a><a href="https://twitter.com/gitpod?ref_src=twsrc%5Etfw">@gitpod</a> 🙏🏻😇 <a href="https://t.co/NPMHZBlgQo">pic.twitter.com/NPMHZBlgQo</a></p>&mdash; Atulmaharaj 🥑 (@TheTechMaharaj) <a href="https://twitter.com/ TheTechMaharaj/status/1770713303167193378?ref_src=twsrc%5Etfw">2024年3月21日</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

今回は4日間にわたり開催され、毎日大勢の参加者が集まりました。クロワッサン、パン・オ・ショコラ、カフェ・オ・レを囲みながら、プラットフォームの真の意味から成功基準まで、あらゆる話題について議論を交わしました。非常に示唆に富む議論の数々でした。

## 主な学び

今回が私にとって2度目の対面式KubeCon、通算4回目の参加となりました。プラットフォームワーキンググループのメンバーと直接会うのも2度目です。私たちは毎月電話会議で連携し、[Platform Whitepaper](https://tag-app-delivery.cncf.io/whitepapers/platforms/)や
 [Platform Maturity Model](https://tag-app-delivery.cncf.io/whitepapers/platform-eng-maturity-model/)、進行中の[Platform as a Product paper](https://github.com/cncf/tag-app-delivery/issues/553)といった刺激的なプロジェクトに取り組んでいますが、直接会うのは格段に良いものです。

さらに、KubeCon開催発表当初からKubeCon期間中まで精力的に支援してくれたTAGアプリデリバリーおよびWGプラットフォームのメンバーに心から感謝します。また、初のPlatform Engineering Dayは大成功を収め、満員の会場はプラットフォームエンジニアリングの重要性と関心の高さを証明しています。

プラットフォームエンジニアリングパネルへの参加に加え、プラットフォームエンジニアリングの迷路をどう切り抜けるかについて、興味深い講演をいくつか聴講しました。特に、プラットフォームの成功をカスタマイズして測定する方法や、AI対応プラットフォームに関する議論に強く惹かれました。議論の中で最も楽しんだ点は、開発者体験とその生産性への広範な影響に焦点が当てられていたことです。  

## ぜひご参加ください！

この楽しく知的なグループの一員として、これが最も双方向的で有益なグループの一つだと保証できます。プラットフォームエンジニアリングを学んだばかりの方でも、長年プラットフォーム構築に携わるプロフェッショナルでも、プラットフォームワーキンググループに参加し、プラットフォームの未来を共に形作るお手伝いをお待ちしています。

まずは[WG-Platforms Slack](https://cloud-native.slack.com/archives/C020RHD43BP)にご参加ください。自己紹介と参加目的を簡単に伝えていただければ、チームメンバーがサポートします :)
