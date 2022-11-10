# AWSサービスまとめ

# コンピューティングサービス
### EC2
> ネットワークに迅速にサーバーを作成できるサービス。アンマネージド型。12か月間無料。    

### Lambda
> サーバーレスでコードを生成・実行できるコンピューティングサービス。1か月100万リクエストが無料。  

# データベース
### ElastiCache
> リアルタイムな高速処理に利用可能。クラウド内のインメモリデータストアまたはキャッシュを簡単にデプロイ・操作・スケーリングできるデータベース。  
RedisまたはMemcachedに互換性があり、ミリ秒未満のレイテンシーを実現し、リアルタイムアプリケーションを強化できる。  

### ESC
> EC2インスタンスにアタッチして使われるAWSのストレージサービス。タイプはSSDとHDDの2種類がある。
ボリュームタイプは4種類あるが今回は省略。

### EFS
> インターネットからアクセスできず、複数のEC2インスタンスからアクセスできることができるストレージ。  

### S3
> 大量のデータの保存に向いている。また、高い可用性や耐久性・低価格・容量無制限などのメリットがある。(1ファイル5TBまで)  
Availability Zoneを指定せずにリージョンに直接サービスが設置される。
[詳細はこちら](https://business.ntt-east.co.jp/content/cloudsolution/column-try-43.html#section-03)

### Aurora
> クラウド専用の分散型RDB。通常のMySQLデータベースとくらべて最大5倍、PosgreDBと比べて最大3倍高速。
商用データベースと同等のセキュリティ、可用性、信頼性を10分の1のコストで実現できる。

### RDS on Putposts
> RDSのフルマネージドべーす

# コンテナオーケストレーションサービス
### ECS
> Dockerコンテナをサポートする、拡張性とパフォーマンスに優れたサービスで、コンテナ化されたアプリケーションを実行できる。  

### ECR
> 作成したDockerコンテナをAWS内に移行するためのGitクラウド。

# ネットワーク
### AWS VPC
> クラウドを論理的に分離してプロビジョニングして、ユーザー専用のネットワーク領域を作成する。  

### Route53
> DNSサービス。ドメインを登録してルーティングすることができる。その際にDNSヘルスチェックを構成トラフィックを正常なエンドポイントにルーティングしたり、アプリケーションやそのエンドポイントの正常性をモニタリングすることができる。


# Firewall
### Route 53 Resolver DNS Firewall
サイトへのサクセスを制御し、DNSレベルの脅威を防ぐことができる。

# トラフィック関係
### CloudFront
> 世界中の視聴者に安全にデータや動画などのコンテンツを配信する高速コンテンツ配信ネットワークサービス。  

### ELB
> アプリケーションへのトラフィックを複数のターゲットに移動的に分散するサービス。  
ELBはインスタンスのヘルスチェックを行うことができるので、正常なインスタンスにのみトラフィックを送信することも可能。

### スティッキーセッション
> ELBがサーバーにリクエストを振り分ける際、特定のCookieを確認することでクライアントからのリクエストを特定のサーバーに紐づけることができる機能。

### 

# モニタリグサービス
### AWS CloudWatch
> AWSリソースとAWSで実行するアプリケーションを監視することができる。また、AWSサービスの閾値によるアラームを設定することができる。詳しくは[こちら](https://www.acrovision.jp/service/aws/?p=2222)  

### AWS CloudWatch Logs
> AWSマネージドサービスのログやEC2インスタンス上のOS/アプリケーションのログを取得できる。  

### AWS Cloud Events
> AWSリソースの変更をトリガーとしてアクションを実行できるサービス  

### AWS CloudTrail
> AWSサービスを記録し、いつ・だれが・何をしたのかを残すサービスでAWSアカウントで発生したAPIコールの記録を行っています。**→ユーザーに対する監視サービス**  

### AWS Config
> アクセスログなどの取得と監視ができるサービス。AWSアカウントのガバナンス、コインプライアンス、運用監査、リスク監査を行うことができる。**→リソースに対する監視サービス**  

[AWS CloudTrailとAWS Configの違い](https://qiita.com/miyuki_samitani/items/da7ececd52af9aa94280)

### AWS Sysyems Manager
> AWSで利用しているインフラストラクチャを可視化し、制御するためのサービス。

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

# セキュリティ
### セキュリティグループ
> AWSリソースごとにアタッチするファイアーウォール  
ステートフルなのでインバウンドを許可すれば、アウトバウンドでも許可される(許可のみを設定する)。  

### NACL
> サブネット・VPC単位でアタッチする。s
ステートレスなのでインバウンドアウトバウンドを設定する。(許可/拒否を設定する)

セキュリティグループとNACLの違いは[こちら](https://zenn.dev/rrk347/articles/e6baff41e04c37)  

# インスタンス購入オプション
### オンデマンドインスタンス
> 長期間なコミットメントなしで1時間ごとにコンピューティング容量を支払うことで、コストを最適化する。  

### リザーブドインスタンス
> 1年間または3年間の長期使用をする場合、割引価格で使用することができる。

### Dedicate host
> オンデマンドインスタンスを物理的に占有する場合に選択するオプション

# 移行サービス
### AWS Database Migration Service(DMS)
> データベースに悪影響を与えずにオンプレ環境・AWS間の移行ができる。 
移行中も利用可能な状態に保たれるためダウンタイムを最小限に抑えられる。  

### AWS Application Migration Service(MGN)
> オンプレのサーバー、仮想インフラおよびAzureなどの他のクラウドサービスにあるサーバーや仮想マシンのサーバーソフトウェアをAWSクラウドで利用可能なように変換し、移行を自動化するサービス。  

### AWS Migration Hub
> 大規模な移行を実施している際に、以降実施状況を把握するためのサービス。  

# サポートサービス
### AWS Application Discovery Service(ADS)
> オンプレのデータセンターに関する情報を収集することによって、移行プロジェクト計画を立案するのをサポートするサービス。  

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

# 料金
### AWS Pricing Calculator
> AWS請求額を効率的に見積もる際に利用するツール。このサービスでベストケースとワーストケースのシナリオを決定して利用するAWSリソース構成に応じた見積もりを算出することができる。

### TCO計算ツール(廃止済み)
> AWSを利用する際の総コストを算出することができる。

### Cost Explorer
> 月額コストの予測分析が可能な分析ツール。カスタムレポートを作成して、コストと使用量のデータを分析できる。

# その他サービス
### Amazon Elastic Transcoder
> 簡単かつ低コストでメディアファイルをさまざまなデバイスで再生できるように変換するサービス  

### Amazon Interactive Video Service
> インライなどのようなライブストリーミング機能をアプリケーションに実装する際などに利用するサービス






