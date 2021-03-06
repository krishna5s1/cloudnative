---

copyright:
  years: 2016, 2017
lastupdated: "2017-06-12"

---
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:codeblock: .codeblock}
{:pre: .pre}

# Web ベーシック・スターターのエンドツーエンド・チュートリアル
{: #tutorial}

以下のエンドツーエンド・チュートリアルでは、Web ベーシック・スターターからプロジェクトを作成するための手順を段階的に説明します。ステップには、前提条件ツールのインストールと、プロジェクト・コードの実行方法が含まれます。


## 開発者ツールのインストール
{: #dev_tools}

[前提条件の開発者ツール![外部リンク・アイコン](../icons/launch-glyph.svg "外部リンク・アイコン")](get_code.html#prereq-dev-tools "外部リンク・アイコン"){: new_window} を必ずインストールしてください。


## プロジェクトの作成方法の選択
{: #choose_how}

Web ベースの [{{site.data.keyword.dev_console}}](#create-devex) を使用するか、またはコマンド駆動型 [{{site.data.keyword.dev_cli_notm}}](#create-cli) を使用して、プロジェクトを作成することができます。プロジェクトが作成されたら、[プロジェクトを実行](#run)できます。


## {{site.data.keyword.dev_console}} を使用したプロジェクトの作成
{: #create-devex}

1. {{site.data.keyword.Bluemix}} {{site.data.keyword.dev_console}} でプロジェクトを作成します。

	1. {{site.data.keyword.dev_console}} 内の [**「開始」** ![外部リンク・アイコン](../icons/launch-glyph.svg "外部リンク・アイコン")](https://console.ng.bluemix.net/developer/getting-started/ "外部リンク・アイコン") ページから**「プロジェクトの作成」**をクリックします。

		代替方法として、**「プロジェクト」**ページから**「プロジェクトの作成」**をクリックすることもできます。

	2. **「Web アプリ (Web App)」**を選択し、**「次へ」**をクリックします。

	3. **「ベーシック Web (Basic Web)」**を選択し、**「次へ」**をクリックします。

	4. プロジェクト名を入力します。このチュートリアルでは、`WebBasicProject` を使用します。   

	5. 固有のホスト名を入力します (自分のイニシャルに `-devhost` を付加したものなど)。以下に例を示します。
	
	 ```
	 abc-devhost
	 ```

	6. 言語プラットフォームを選択します。このチュートリアルでは、`Swift` を使用します。
   
	7. **「作成」**をクリックします。

2. オプション: Data (データ) 機能を追加します。

	1. **「プロジェクト概要 (Project Overview)」**ページで、**「Data (データ)」**に対して**「表示」**をクリックします。

      代替方法として、**「機能 (Capabilities)」>「Data (データ)」**ページで**「作成」**または**「既存の追加 (Add Existing)」**を選択することもできます。

   2. サービス名を入力し、**「作成」**をクリックします。

3. プロジェクト・コードを生成します。

	1. **「プロジェクト概要 (Project Overview)」**ページで**「コードの取得 (Get the Code)」**をクリックして、言語を選択します。
   
		代替方法として、**「コード」**ページで以下をクリックすることもできます。
      
	2. **「コードの生成 (Generate Code)」**をクリックします。
   
	3. プロジェクト・コードの生成が完了したら、**「コードのダウンロード」**をクリックして、プロジェクトのアーカイブをダウンロードします。

4. ダウンロードされたプロジェクトの処理を開始します。

	1. アーカイブされたファイルを解凍します。
	
	2. 新規プロジェクト・ディレクトリーにナビゲートします。
	
	3. {{site.data.keyword.dev_cli_notm}} を使用して処理を続行します。

5. オプション: 新しい言語を生成するために[プロジェクトを更新します](project_overview_page.html#update_language)。


## {{site.data.keyword.dev_cli_notm}} を使用したプロジェクトの作成
{: #create-cli}

1. [{{site.data.keyword.dev_cli_short}}](dev_cli.html) を必ずインストールしてください。

2. 端末のプロンプトで、使用するローカル・ディレクトリーにナビゲートし、以下のコマンドを実行します。
  
	```
	bx dev create
	```
	{: codeblock}

3. プロンプトが出されたら、以下の値を入力します。

	* パターンの選択: 1 (Web)
	* スターターの選択: 1 (ベーシック Web)
	* 言語の選択: 2 (Swift)
	* プロジェクト名の入力: `WebBasicProjectCLI`
	* プロジェクトのホスト名の入力: `abc-devhost`
	  * 固有のホスト名を入力します (自分のイニシャルに `-devhost` を付加したものなど)。以下に例を示します。
	
	     ```
	     abc-devhost
	     ```

4. `WebBasicProjectCLI` プロジェクトが正常に保存されたら、`WebBasicProjectCLI` フォルダーにナビゲートします。

5. 独自のコードを追加、ビルドし、プロジェクトを実行します。
	
	1. 以下のコマンドを使用してプロジェクトをビルドします。
 
		```
		bx dev build
	```
		{: codeblock}
	 
	2. 以下のコマンドを使用してプロジェクトを実行します。
 
		```
		bx dev run
		```
		{: codeblock}


## Web プロジェクトの実行
{: #run}

必要なビルド・ツールをインストールした場合、あるいは {site.data.keyword.dev_cli_notm}} で使用可能なコンテナー・サポートを使用すると、アプリケーションをホスト・システム上でローカルに実行することができます。


### {{site.data.keyword.dev_cli_short}} の使用
{: #dev notoc}

1. ノードの依存関係をインストールします。

  ```
  npm install
  ```
  {: codeblock}

2. フロントエンド・コードをモジュールにバンドルします。

  ```
  gulp
  ```
  {: codeblock}

3. 現行プロジェクト・ディレクトリーでプロジェクトをビルドするには、以下のコマンドを入力します。

  ```
bx dev build
```
  {: codeblock}

4. 現行プロジェクト・ディレクトリーでプロジェクトを実行するには、以下のコマンドを入力します。

  ```
  bx dev run
  ```
  {: codeblock}

5. ブラウザーで `http://localhost:8080` を開きます。


## Xcode でのプロジェクトの実行
{: #Xcode}

1. Xcode プロジェクトを作成します。

	Xcode で開発するには、その前に、Swift パッケージ・マネージャーを使用して Xcode プロジェクトをビルドする必要があります。
	
	```
	swift project generate-xcodeproj
	```
	{: codeblock}

2. アクティブ・ターゲットを該当の実行可能ファイルに変更します。

	次に、Xcode でプロジェクトを開き、アクティブ・ターゲットが該当の実行可能ファイルであることを確認します。オプション・キーを押したままドロップダウン・メニューをクリックすることで、目的のアクティブ実行可能ファイルを選択できます。

3. **「実行 (run)」**を押します。

4. ブラウザーで `http://localhost:8080` を開きます。

