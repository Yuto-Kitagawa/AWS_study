# AWSサービスまとめ






# コンピューティングサービス
### EC2
> ネットワークに迅速にサーバーを作成できるサービス。アンマネージド型。12か月間無料。    

### Lambda
> サーバーレスでコードを生成・実行できるコンピューティングサービス。1か月100万リクエストが無料。  

### Lightsail
> コンテナなどのクラウドリソースを予測可能な低価格で簡単に管理できる使いやすい仮想プライベートサーバー

### Amazon WorkSpaces
> 様々なデバイスからオンデマンドでアクセスできるWindowsおよびLinux向けフルマネージドデスクトップ仮想サービス。

### Dedicated Hosts
> EC2インスタンスを利用する際にユーザーが占有できる物理EC2サーバー。


### Amazon EC2　ベアメタルインスタンス
> IntelXeonスケーラブルプロセッサとメモリリソースに直接アクセスできるインスタンス。






# インスタンス購入オプション
### オンデマンドインスタンス
> 長期間なコミットメントなしで1時間ごとにコンピューティング容量を支払うことで、コストを最適化する。  

### リザーブドインスタンス
> 1年間または3年間の長期使用をする場合、インスタンスを指定して継続利用することで割引価格で使用することができる。
>> 1. スタンダード
>> ![スタンダード表](https://img-c.udemycdn.com/redactor/raw/test_question_description/2021-12-15_00-03-23-36ecf074ba26ec5564cfdd2f11e702f2.png)
>> 途中でインスタンスタイプを交換できない。マーケットプレイスでの販売。購入ができる。
>> 2. コンバーティブル  
>> 途中でインスタンスタイプを交換できる。マーケットプレイスでの販売・購入はできない。
>> ![コンバーティブル表](https://img-c.udemycdn.com/redactor/raw/test_question_description/2021-12-15_00-03-23-36ecf074ba26ec5564cfdd2f11e702f2.png)

### Dedicate host
> オンデマンドインスタンスを物理的に占有する場合に選択するオプション

### Saving Plans
> 1時間あたりの一定の費用を1年・3年分支払うことで割引されるオプション。インスタンス構成ではなく時間によって料金がかわる。






# データベース
### ElastiCache
> リアルタイムな高速処理に利用可能。クラウド内のインメモリデータストアまたはキャッシュを簡単にデプロイ・操作・スケーリングできるデータベース。  
RedisまたはMemcachedに互換性があり、ミリ秒未満のレイテンシーを実現し、リアルタイムアプリケーションを強化できる。  

### インスタンスストア
> EC2の内臓ストレージ。EC2を停止するとデータが消滅する。追加料金は発生しない。

### EBS
> EC2インスタンスにアタッチして使われるAWSのストレージサービス。アタッチするのでインスタンスがなくなってもデータは消滅しないが、追加料金はかかる。
インターネットからはアクセスできない。タイプはSSDとHDDの2種類がある。
ボリュームタイプは4種類あるが今回は省略。


### S3
> 大量のデータの保存に向いている。また、高い可用性や耐久性・低価格・容量無制限などのメリットがある。(1ファイル5TBまで)  
Availability Zoneを指定せずにリージョンに直接サービスが設置される。
[詳細はこちら](https://business.ntt-east.co.jp/content/cloudsolution/column-try-43.html#section-03)

### Aurora
> クラウド専用の分散型RDB。通常のMySQLデータベースとくらべて最大5倍、PosgreDBと比べて最大3倍高速。
商用データベースと同等のセキュリティ、可用性、信頼性を10分の1のコストで実現できる。

### DynamoDB
> シームレスで
拡張性のあるデータベース。NoSQLデータベースで、セッションデータの処理に向いている。

### RDS on Outposts
> RDSのフルマネージドデータベース

### Redshift
> クラウド内にデータウェアハウスを構築できる。

### EFS
> シンプルでスケーラブル、かつ伸縮自在な完全マネージド型ファイルシステム。インターネットからアクセスできず、複数のEC2インスタンスからアクセスできることができるストレージ。  

### Amazon FSx for Windows File Server
> Windows File Serverと互換性があり、Windwowsやソフトウェアとの連携が豊富に可能なファイルシステム

### Amazon FSx for Lustre
> 1秒間に最大でテラバイトのスループットを達成できる、スーパーコンピューターに利用可能なサービス。

### Amazon FSx for NetApp ONTAP

### Amazon FSx for OpenZFS








# データ分析
### Amazon Athena
> S3内のデータを標準SQLを使用して簡単に分析できる。

### Amazon Kinesis
> ストリーミングデータをリアルタイムで収集、処理、分析するデータ処理

### Amazon SageMaker
> トレーニングデータの前処理、教師データの作成、機械学習モデルの構築・学習、学習済みモデルのデプロイなどの一連のプロセスを提供するサービス。








# コード管理

### Codestar
> CI/CD環境の構築と、開発環境をすばやく構築することができる。

### CodeBuild
> CI/CDを担うサービス。自動でビルド、テスト、デリバリー、デプロイを実行する。

### CodeCommit
> フルマネージド型のソース管理サービス。企業が安全に閣僚性の高いプライベートGitリポジトリを簡単にホストできる。

### CodeArtifact
> フルマネージド型のアーティファクトリポジトリサービス。ソフトウェア開発プロセスで使用されるソフトウェアパッケージを安全に保存・公開・および共有することができる。Java,JavaScript,.NET,Pythonなどの一般的なパッケージマネージャーおよびビルドツールと連携して動作する。

#### CodeCommit CodeArtifactの違い
> CodeArtifactはパッケージマネージャーを使ったコード管理。CodeCommitはgitリポジトリ

### AWS CodeGuru
> 機械学習を使ったコードレビューを行うサービス。  100行で0.5$。脆弱性やパフォーマンスにも対応している。








# コンテナオーケストレーションサービス
### ECS
> Dockerコンテナをサポートする、拡張性とパフォーマンスに優れたサービスで、コンテナ化されたアプリケーションを実行できる。  

### ECR
> 完全マネージド型コンテナレジストリ。作成したDockerコンテナをAWS内に移行するためのGitクラウド。

### Fargate
> サーバーレスでコンテナを実行できるサービス。ECSやEKSと組み合わせて利用する。
コンテナの起動時間・使用リソースに応じた従量課金







# ネットワーク
### AWS VPC
> クラウドを論理的に分離してプロビジョニングして、ユーザー専用のネットワーク領域を作成する。  

### Route53
> DNSサービス。ドメインを登録してルーティングすることができる。その際にDNSヘルスチェックを構成トラフィックを正常なエンドポイントにルーティングしたり、アプリケーションやそのエンドポイントの正常性をモニタリングすることができる。

### リードレプリカ
> RDSのマスタデータベースインスタンスの読み取り処理を分散化させることができる。

### リージョナルエッジキャッシュ
> エッジロケーションとオリジンの間に存在する1段容量の多いキャッシュサーバー群を保持したロケーション
エッジロケーションだけを利用するよりもキャッシュ利用率を効率化する。

### AWS Local Zones
> リージョンやAZが遠いユーザーに対して、レイテンシーの影響を受けやすいアプリケーションをエンドユーザーにより近い場所で実行可能にするために作られた特別なゾーン

### AWS Global Accelerator
> 世界中のユーザーに対して地理的に近いエンドポイントにおいて、アプリケーションのトラフィックを高速に処理するため使用される。

### AWS S3 Transfer Acceleration
> S3との間で高速データ転送を実現するためのサービス

### CloudFront
> 世界中の視聴者に安全にデータや動画などのコンテンツを配信する高速コンテンツ配信ネットワークサービス。  


### ELB
> アプリケーションへのトラフィックを複数のターゲットに移動的に分散するサービス。  
ELBはインスタンスのヘルスチェックを行うことができるので、正常なインスタンスにのみトラフィックを送信することも可能。

>> ### ALB
>> レイヤー7に対応。1つのALBで複数のサーバー群にトラフィックを制御できる。

>> ### CLB
>> レイヤー4,7に対応。古いタイプなのでALB/NLBを優先。

>> ### NLB
>> レイヤー4に対応。TCP,UDPなどのプロトコルでの通信に関してトラフィック分散が可能。


### スティッキーセッション
> ELBがサーバーにリクエストを振り分ける際、特定のCookieを確認することでクライアントからのリクエストを特定のサーバーに紐づけることができる機能。

### AWS CloudShell
> Webブラウザ経由でコマンドラインを実行できるサービス。

### AWS Outposts
> AWSサービスをオンプレ環境で実行することができる。






# Firewall
### Route 53 Resolver DNS Firewall
> サイトへのサクセスを制御し、DNSレベルの脅威を防ぐことができる。

### AWS Network Firewall
> VPCに不可欠なネットワークファイアーウォールや侵入防止システムをデプロイするマネージドサービス

### WAF
> 可用性・セキュリティ侵害・リソースの過剰消費に影響を与えるようなウェブの脆弱性を利用した一般的な攻撃野暮っとからウェブアプリケーションを保護するファイアーウォール。SQLインジェクションやクロスサイトスクリプティングなど一般的な攻撃をブロックできる。

### AWS Fiewall Manager
> 一元敵にファイアーウォールのルールを設定・管理できるサービス





# モニタリグサービス

### Amazon GuardDuty
> 機械学習で攻撃を検知して通知するサービス。

### AWS CloudWatch
> AWSリソースとAWSで実行するアプリケーションを監視することができる。また、AWSサービスの閾値によるアラームを設定することができる。詳しくは[こちら](https://www.acrovision.jp/service/aws/?p=2222)  

> ### AWS CloudWatch Events
>> 変更イベントを認識することができる。

> ### AWS CloudWatch Logs
>> AWSマネージドサービスのログやEC2インスタンス上のOS/アプリケーションのログを取得できる。  

> ### CloudWatch Logs Insights
>> ログに対してクエリを作成して検索できるサービス  
>> スキャンしたデータ 1GB あたり 0.0076USD

> ### CloudWatch Alarm
>> EC2インスタンスのCPU使用率などのメトリクスに対してアラームを設定できる。

### AWS Cloud Events
> AWSリソースの変更をトリガーとしてアクションを実行できるサービス  

### AWS CloudTrail
> AWSサービスを記録し、いつ・だれが・何をしたのかを残すサービスでAWSアカウントで発生したAPIコールの記録を行っています。**→ユーザーに対する監視サービス**  

### AWS Config
> アクセスログなどの取得と監視ができるサービス。AWSアカウントのガバナンス、コインプライアンス、運用監査、リスク監査を行うことができる。**→リソースに対する監視サービス**  

### Credential Report
> 利用日時などが記録されたIAM認証情報のレポートファイルを取得できる。

### Access Advisor
> IAMエンティティが、最後にAWSサービスにアクセスした日付と時刻が表示される。

>> ### CloudTrail insights
>> CloudTrailで設定した管理イベントを自動的に分析して、異常な動作パターンを検出した際に通知するサービス。


[AWS CloudTrailとAWS Configの違い](https://qiita.com/miyuki_samitani/items/da7ececd52af9aa94280)

### AWS Sysyems Manager
> AWSで利用しているインフラストラクチャを可視化し、制御するためのサービス。

### AWS Security Hub
> Amazon GuardDutyによる監視監視結果を収集して、分析・レポーティングすることができるサービス。

### Amazon Detective
> Amazon GuardDutyによる監視監視結果を収集して、分析・レポーティングすることができるサービス。

### AWS Personal Health Dashboard
> AWSリソースの正常・異常に関するデータを提供するダッシュボード。







# ゲートウェイ
### インターネットゲートウェイ
> AWSネットワークにインターネットからアクセスするためにVPC内に配置するコンポーネント

### NATゲートウェイ
> プライベートサブネットからインターネットヘアクスするためのゲートウェイ

### 仮想プライベートゲートウェイ
> VPNに使用するAmazon側にあるルーター

### Egress-Only Internet Gateway
> IPv6用のインターネットゲートウェイ

### カスタマーゲートウェイ
> オンプレ環境と接続する際に使用するゲートウェイ

### AWS Strage Gateway
> オンプレのデータセンターにあるストレージを拡張してデータのバックアップに使用できる費用対効果の高いサービス。

### AWS Direct Connect
> VPCとオンプレ環境を接続する専用接続サービス。

### AWS Transit Gateway
> 複数のVPCと、オンプレのネットワークを連結させるVPC間のサービス。VPCが複数あるとき、HUBのような役割を果たすことができる(設定が簡単になったりするメリットがある)






# セキュリティ
### セキュリティグループ
> AWSリソースごとにアタッチするファイアーウォール  
ステートフルなのでインバウンドを許可すれば、アウトバウンドでも許可される(許可のみを設定する)。  

### NACL
> サブネット・VPC単位でアタッチする。s
ステートレスなのでインバウンドアウトバウンドを設定する。(許可/拒否を設定する)

セキュリティグループとNACLの違いは[こちら](https://zenn.dev/rrk347/articles/e6baff41e04c37)  

### AWS Security Hub
> セキュリティのベストプラクティスのチェックを行い、アラートを集約し、自動修復を可能にするセキュリティ体制管理サービス。

### Amazon Inspectator
> EC2インスタンスにおける、現在ホストされているアプリケーションなどを分析して、脆弱性がないかをtyっくすることができるサービス。






# アプリケーション構築
### AWS Device Farm
> 様々なデバイスへの対応ができているかを検証することができる。

### AWS Mobile Hub
> Cognito,Lambda,Device Farm,PinpointなどのAWSサービスと連携してアプリケーション構築・テスト・モニタリングを実施することができるサービス。

### AWS Amplify
> クラウド向けWEB/モバイル開発向けのJavaScript/iOS/Androidライブラリ。WebアプリケーションのCICDおよびホスティングを実施することができる。

### AWS Launch Wizard
> AWSベストプラクティスに従ったアプリケーションを簡単にデプロイできるサービス。

### Amazon EventBridge
> イベントを通じて大規模なアプリケーションを構築することができる。AWSのサービス、独自のアプリケーション、Saasアプリケーションを接続し、イベント型アプリケーションを簡単に構築、管理できる。

### AWS Elastic BeanStalk
> ソースコードをアップロードするたびに、アプリケーションバージョンを作成し、使い慣れたサーバーでデプロイおよびスケーリングができる。ばーじょｎ変更を実施すると、影響を受けるすべてのリソースに対して変更内容を自動的に帝王することができる。

### Amazon OpenSearch Service
> リアルタイムのアプリケーションモニタリング、ログ分析、ウェブサイト検索などができる。アプリケーション運用向けの分析サービス。

### Amazon Interactive Video Service
> インライなどのようなライブストリーミング機能をアプリケーションに実装する際などに利用するサービス

### Cognito
> 開発するWEBアプリケーションやモバイルアプリに認証機能を提供するサービス。

### AWS Private Links
> 独自のアプリケーションと、AWS上のサービスを安全に接続するための機能。

### Amazon Rekognition
> 画像分析と動画分析をアプリケーションに簡単に追加できる。顔認識や、不適切なコンテンツを検出することもできる。









# 移行サービス
### AWS Database Migration Service(DMS)
> データベースに悪影響を与えずにオンプレ環境・AWS間の移行ができる。 
移行中も利用可能な状態に保たれるためダウンタイムを最小限に抑えられる。  

### AWS Application Migration Service(MGN)
> オンプレのサーバー、仮想インフラおよびAzureなどの他のクラウドサービスにあるサーバーや仮想マシンのサーバーソフトウェアをAWSクラウドで利用可能なように変換し、移行を自動化するサービス。  

### AWS Migration Hub
> DMSやServer Migration Service、CloudEndureなどで移行を実施している際に、移行実施状況を把握するためのサービス。  

### Snowball edge strage optimized
> データ移行とエッジコンピューティングのデバイス。一台で80TBのサイズがあり、50TBのデータを一台で可能にする。

### Snowball edge compute  optimized
> 一台で40TBのデータを移行できる。52個のvCPU、オプションのGPUなどを提供できるので断続的な接続となる環境にあるデータや極度な遠隔地にあるデータの収集、機械学習、処理、保存をAWSに返送する前に実行できる。

### Snowmobile
> エクサバイト規模のデータ移動ができる。

### AWS Transfer Family
> SFTP,FTPS,FTPプロトコルを使用して、S3やEFSへの企業間ファイル転送を実施することができる。











# アカウント
### ルートユーザー
> デフォルトでAWSアカウントのすべてのリソースを完全に管理できる。
ルートユーザーはEメールとパスワードを初期設定する必要がある。

### 管理者権限
> 管理者権限の許可が付与されたIMAユーザー。ルートユーザーでしかできない、請求処理など一部以外の権限をすべて所有する。

### パワーユーザー
> 管理者操作以外のAWSリソースへのアクセス権限をすべて保有しているユーザー。





# データ変換

### AWS Lake Formation
> データレイクを数日で簡単にセットアップできるサービス。  
データレイクとは様々なデータを保存できる安全な一元的リポジトリ。元の形式と分析用のデータに処理されたデータすべてが保存される。分析はAWS Glueが行っているので、あくまでデータの保存先のことを指す。

### AWS Glue
> データ分析用に抽出したIoTデータの変換作業ができる
> ### AWS Glue Data Catalog  
>> 必要なデータを検出し、アクセスすることができる
> ### AWS Glue Studio
>> 視覚的にETL(抽出・変換・読み込み)の処理を作成して実行する。
> ### AWS Glue DataBrew
>> 機械学習前のデータを正規化できる。(ノーコード)

### Amazon Elastic Transcoder
> 簡単かつ低コストでメディアファイルをさまざまなデバイスで再生できるように変換するサービス  

### Amazon Polly
> 自然言語処理と音声識別によって文章をリアルな音声に変換するサービス。

### Amazon Transcribe
> 音声をテキストに変換する文字起こしサービス

### Amazon Lex
> 音声やテキストを使用して任意のアプリケーションに対話型インターフェースを構築するサービス。音声のテキスト変換は自動音声認識(ASR)、テキストの意図認識は自然言語理解(NLU)が使用できる。

### Amazon Ttextract
> PDFやOCRドキュメントからテキストやデータを自動抽出するサービス。






# サポートサービス
### Trusted Advisor
> ユーザーが利用しているリソースを評価して、コスト削減、パフォーマンス向上、セキュリティ向上などの推奨を提供するサービス。

### Amazonマネージドサービス
> 運用管理をAWS側で監視、インシデント検出と管理、セキュリティ、パッチ、バックアップ、コスト最適化などを提供する。

### TAM
> AWSを導入している企業や個人に対して効率よく運用するための、技術的視点でサポートを行うサポーター。
ビジネス成果に対するサポートはしていない。

### コンシェルジュサポート
> ユーザー側と連携して、請求及びアカウントのベストプラクティスを実装するエキスパート

### AWSインフラストラクチャイベント管理(IEM)
> 買い物で忙しくなる時期や休日時期、予定イベントの準や実行時にアーキテクチャとスケーリングのガイダンスと運用サポートするサービス

### サポートプラン
> ベーシックプラン、開発者、ビジネス、エンタープライズ、エンタープライズ On-Rampの4つのタイプがある。ビジネスはアカウント支援以外のサポート、エンタープライズ以上はすべてのサポートが含まれる。

### AWSパートナーパス
> AWSパートナーネットワークに参加後、パートナーとなった会社がソフトウェア、ハードウェア、サービス、トレーニング、ディストリビューションなどの領域ごとに最適なパスに登録することで、パートナーとして利用してもらう対象ユーザーに対して幅広いオファリングを実施することができるサービス。

### AWS Application Discovery Service(ADS)
> オンプレのデータセンターに関する情報を収集することによって、移行プロジェクト計画を立案するのをサポートするサービス。  

### AWSプロフェッショナルサービス
> AWSを利用したクラウド移転などで、目標となるビジネス成果を達成するために利用する支援プログラム





# メッセージングサービス
### Amazon SNS
> 分散型システム、およびサーバーレスアプリケーションの分離を可能にする高可用性で耐久性に優れた完全マネージド型メッセージングサービス。コンポーネント間のメッセージ通知やメッセージング処理、プッシュ通知を利用できる。  

### Amazon SES
> デベロッパーが任意のアプリでの電子メールの送信を可能にし、費用対効果が高く、高可用性・柔軟で、スケーラブルなSESサービス  

### Amazon SQS
> 完全マネージド型のメッセージキューイングサービス。AWS上でキューイング処理・タスク並列分散処理・ポーリング/Pull型の通知をする場合に利用する。  






# 自動化
### CloudFormation
> AWSリソースを利用したインフラ攻勢をコードとして記述し、一括で起動し設定できる構成管理ツール

### OpsWorks
> PuppetやChefのマネージド型インスタンスを利用した構成管理サービス。コードを利用してEC2インスタンスの構成を自動化するためのオートメーションプラットフォーム。CloudFormationとの違いは、リソース全体かEC2インスタンスの構成かの違い。

### CodeDeplay
> EC2,Fargate,Lambdaなどのコンピューティングサービスへのソフトウェアのデプロイを自動化するサービス。

### CodePipeline
> アプリケーションを素早く確実性のあるデプロイの方法を可視化・自動化できるサービス。






# 料金
### AWS Pricing Calculator
> AWS請求額を効率的に見積もる際に利用するツール。このサービスでベストケースとワーストケースのシナリオを決定して利用するAWSリソース構成に応じた見積もりを算出することができる。

### TCO計算ツール(廃止済み)
> AWSを利用する際の総コストを算出することができる。

### Cost Explorer
> 月額コストの予測分析が可能な分析ツール。カスタムレポートを作成して、コストと使用量のデータを分析できる。







# その他サービス
### AWS Batch
> 数十万件にも及ぶような大規模なバッチコンピューティングジョブを効率的に実行できる。大規模な計算処理を実行するワークロードを整備できる。


### WaveLengthゾーン
> 東京リージョンにおいて5Gを利用したVRアプリケーションを構築する際に利用するべきロケーション

### AWS KMS
> EBSボリュームの暗号化に使用されるサービス。暗号化をする時がKMSカスタマーマスターキー(CMK)を指定して、EC2インスタンスにボリュームを接続するとデーターキーを使用してボリュームへのすべてのディスクI/Oを暗号化する。

### AWS マーケットプレイス
> サードパーティのソフトバンクソリューションやサービスを検索するために利用するサービス

### EC2 Instance Connect
> SSHを使用してLinuxインスタンスに接続する方法。ユーザー間でSSHキーを管理する必要がなく、簡単に接続できる。

### Step Functions
> AWSリソースを利用したワークフローを作成できる。

### AWS X-Ray
> 本番環境や分散アプリケーションを分析およびデバッグできるサービス。

### Amazon Health Lake
> ライフサイエンス企業に個人または患者の集団ヘルスデータを完全にかしかし、大規模なクエリと分析を行うことができるサービス。






# AI
### 自然言語系AI
![自然言語系AI](https://img-c.udemycdn.com/redactor/raw/test_question_description/2022-01-15_10-32-45-af585acf056b6fcd1c767b004d803e79.png)  

### 音声系AI
![音声系AI](https://img-c.udemycdn.com/redactor/raw/test_question_description/2022-01-15_10-26-23-ca6d5c935342c1b205485e936b733a57.png)  


### 予測系AI
![予測系AI](https://img-c.udemycdn.com/redactor/raw/test_question_description/2022-01-15_10-26-49-6f0106da345811598bca1910e55788eb.png)  


### 画像系AI
![画像系AI](https://img-c.udemycdn.com/redactor/raw/test_question_description/2022-01-15_10-27-20-a198e28fde72df822e8abeaf3be27656.png)  


### AI開発ツール
![AI開発ツール](https://img-c.udemycdn.com/redactor/raw/test_question_description/2022-01-15_10-27-53-5b9873cdc36e9cdbeef151e9668a503b.png)








# AWS制度関連
### AWS Well-Architected Framework
1. オペレーションエクセレンスの柱(運用上の優秀性)
> システムを運用する上での、設計や原則について。また、ビジネスでの成果やそれに対してどのように取り組むべきかのベストプラクティスが書かれている。

2. 

### AWS ベストプラクティス
> 1. 

### Pay-as-you-go
> 使った分だけライセンス料を支払う課金方法