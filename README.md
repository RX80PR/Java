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
git clone [https://github.com/RX80PR/Java.git](https://github.com/RX80PR/Java.git)
cd Java