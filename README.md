# 食品ECサイト Webアプリケーション (Java / Spring Boot)

チーム開発用の Spring Boot Webアプリケーション・プロジェクトです。
各自のPCに `git clone` して実行することで、すぐに開発を開始できます。

---

## 🛠️ 開発環境（動作前提）

- **Java**: JDK 17 以上
- **IDE**: Visual Studio Code (推奨)
- **ビルドツール**: Maven (プロジェクト同梱のWrapperを使用)
- **データベース**: H2 Database (メモリ内DB / 開発用)

---

## 🧩 推奨VSCode拡張機能

クローン後、VSCodeの拡張機能タブ（`Ctrl+Shift+X` / `Cmd+Shift+X`）から以下の拡張機能をインストールしてください。

1. **Extension Pack for Java** (Microsoft公式) 【必須】
   - Javaのビルド・実行・コード補完・デバッグ機能
2. **Spring Boot Extension Pack** (Microsoft公式) 【必須】
   - Spring Bootプロジェクトの認識・ワンクリック起動・設定ファイルの補完
3. **GitLens — Git supercharged** 【推奨】
   - コードの変更履歴や誰が書いたかが一目で判別できるツール

---

## 🚀 開発の始め方（初回セットアップ）

### 1. リポジトリの取得
ターミナルで以下のコマンドを実行し、プロジェクトをダウンロードします。

```bash
git clone https://github.com/RX80PR/Java.git
cd Java
```

### 2. VSCodeでプロジェクトを開く
VSCodeを起動し、ダウンロードした `Java` フォルダ（`pom.xml` がある階層）を開きます。

> **注意:** 初回起動時はVSCodeのJava拡張機能がライブラリを自動ダウンロードするため、画面左下のビルド完了まで数秒〜数十秒待ってください。

---

## ▷ アプリケーションの起動方法

1. `src/main/java/com/example/demo/DemoApplication.java` を開きます。
2. コード内の `main` メソッド上に出る **[▷ Run]** をクリック（または `F5` キー）して起動します。
3. ターミナルに `Started DemoApplication` と表示されたら起動成功です。

---

## 🌐 アクセス先（URL）

- **Webサイト（メイン画面）**: 
  [http://localhost:8080](http://localhost:8080)
- **H2 データベース管理画面 (H2 Console)**: 
  [http://localhost:8080/h2-console](http://localhost:8080/h2-console)

---

## 🗄️ データベース（H2 Console）の中身の確認方法

アプリ起動中、ブラウザからデータベース内のテーブル構造や保存されているデータ（レコード）を視覚的に確認・検索できます。

### 1. H2 Console にログインする
1. アプリ（`DemoApplication.java`）を起動した状態で、ブラウザで [http://localhost:8080/h2-console](http://localhost:8080/h2-console) にアクセスします。
2. ログイン画面が表示されたら、以下の通り入力・確認して **[Connect]** ボタンを押します：
   - **Saved Settings**: `Generic H2 (Embedded)`
   - **Driver Class**: `org.h2.Driver`
   - **JDBC URL**: `jdbc:h2:mem:testdb`  *(※ `testdb` の部分が正しく入力されているか確認してください)*
   - **User Name**: `sa`
   - **Password**: *(空欄のまま)*

### 2. テーブルとデータの中身を確認する
- **テーブル一覧の確認**:
  ログイン成功後、画面左側のサイドバーに `USERS`, `ITEMS`, `CATEGORIES` などのテーブル一覧が表示されます。
- **データ（中身）の表示**:
  左側のテーブル名（例: `ITEMS`）をクリックすると、中央のSQL入力エリアに `SELECT * FROM ITEMS;` と自動入力されます。
  上部の **[Run]** ボタンを押すと、画面下部にデータの一覧（商品名、価格、在庫数など）が表示されます。

---