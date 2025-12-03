# Sunaneko Marp Theme

sunanekoのスライドデザインを参考に作成したMarpテーマです。

## 特徴

1. 📝 マークダウンでsunanekoのスライドデザインのスライドが作成可能
2. 🤗 テーブル、目次、簡単な図解など、マークダウン要素に対応
3. 🤖 Cursorにスライド化したい内容, marp-prompt.mdを入力して爆速でスライド作成可能

## 利用方法

### 初期設定

#### 1. Marpのインストール
[Marp for VS Code](https://marketplace.visualstudio.com/items?itemName=marp-team.marp-vscode) 拡張機能をインストールしてください。

#### 2. 必要なファイルのダウンロード
以下のファイルをGitHubからダウンロードしてください：

- **`marp-prompt.md`** - プロンプトファイル（必須）
  - 生成AIを使用してスライドを作成する際のプロンプトです
- **`template-slide.md`** - テンプレートファイル（推奨）
  - スライド作成の参考となるテンプレートです
  - 各種レイアウトの使用例が含まれています

#### 3. CSSファイルの設定

CSSの読み込み方法は2通りあります。状況に合わせて選択してください。

##### A. GitHub上のCSSを使用する場合

インターネット接続が必要です。常に最新版が適用されます。

1. **Cursor/VS Codeの設定を開く**
   - `Cmd+,`（Mac）または `Ctrl+,`（Windows/Linux）で設定を開きます

2. **Marpテーマの設定を開く**
   - 検索ボックスで「Markdown › Marp: Themes」を検索します

3. **テーマURLを追加**
   - 「項目の追加」をクリックします
   - 以下のURLを入力します：
     ```
     https://raw.githubusercontent.com/suh-sunaneko/sunaneko-marp-slide/main/sunaneko-theme.css
     ```

4. **動作確認**
   - ダウンロードした`template-slide.md`を開いてプレビューし、同じデザインになればOKです！

##### B. ローカルのCSSを使用する場合

オフラインでも動作します。CSSをカスタマイズしたい場合に便利です。

1. **CSSファイルを配置**
   - `sunaneko-theme.css` をプロジェクトのルートなど、任意の場所に配置します

2. **Cursor/VS Codeの設定を開く**
   - `Cmd+,`（Mac）または `Ctrl+,`（Windows/Linux）で設定を開きます

3. **Marpテーマの設定を開く**
   - 検索ボックスで「Markdown › Marp: Themes」を検索します

4. **テーマパスを追加**
   - 「項目の追加」をクリックします
   - CSSファイルのパスを入力します（**プロジェクトルートからの相対パスを推奨**）：
     ```
     ./sunaneko-theme.css
     ```
     ⚠️ **注意**: 絶対パスでは反映されない場合があります。必ず相対パス（`./`で始まるパス）を使用してください

5. **動作確認**
   - ダウンロードした`template-slide.md`を開いてプレビューし、同じデザインになればOKです！

#### 4. オリジナルのCSSを作る場合（応用編）

自分用のCSSを作りたい場合は、以下の方法があります：

##### 組織で使う場合

1. **CSSファイルをカスタマイズ**
   - `sunaneko-theme.css` をダウンロードして、必要に応じて編集します

2. **CSSファイルをGitHubで公開**
   - カスタマイズしたCSSファイルをGitHubリポジトリにアップロードして公開します

3. **Marpテーマの設定**
   - 上記「3. CSSファイルの設定」の手順に従って、カスタマイズしたCSSファイルのGitHub URLを設定します
   - 例：
     ```
     https://raw.githubusercontent.com/[組織名]/[リポジトリ名]/main/custom-theme.css
     ```

4. **動作確認**
   - `template-slide.md`を開いてプレビューし、カスタマイズしたデザインが反映されているか確認します

##### 個人だけで使う場合

1. **CSSファイルをカスタマイズ**
   - `sunaneko-theme.css` をダウンロードして、必要に応じて編集します

2. **Marpテーマの設定**
   
   以下の2つの方法から選択できます：
   
   **方法A: UI設定から追加（推奨）**
   
   1. **Cursor/VS Codeの設定を開く**
      - `Cmd+,`（Mac）または `Ctrl+,`（Windows/Linux）で設定を開きます
   
   2. **Marpテーマの設定を開く**
      - 検索ボックスで「Markdown › Marp: Themes」を検索します
   
   3. **テーマパスを追加**
      - 「項目の追加」をクリックします
      - CSSファイルのパスを入力します（**相対パスを推奨**、例：`./custom-theme.css`）
        ⚠️ **注意**: 絶対パスでは反映されない場合があります
   
   **方法B: settings.jsonを編集**
   
   1. **settings.jsonを開く**
      - ワークスペースまたはユーザー設定の`settings.json`を開きます
   
   2. **設定を追加**
      - 以下の設定を追加します：
        ```json
        {
          "markdown.marp.themes": [
            "./custom-theme.css"
          ]
        }
        ```
      - `./custom-theme.css` の部分を、実際のCSSファイルのパス（**相対パスを推奨**）に置き換えてください
        ⚠️ **注意**: 絶対パスでは反映されない場合があります

3. **動作確認**
   - `template-slide.md`を開いてプレビューし、カスタマイズしたデザインが反映されているか確認します

### 使い方

1. **スライドにしたい内容を準備**
   - テキストファイルやMarkdownファイルなど、スライドにしたい内容を用意します

2. **Cursorでプロンプトを実行**
   - 以下のような指示文でCursorに実行を依頼します：
   
   ```
   @元ファイルを @marp-prompt.md に従ってMarpスライド作成して
   ```
   
   - `@元ファイル` はスライドにしたい内容のファイルを指定
   - `@marp-prompt.md` はダウンロードしたプロンプトファイルを指定

3. **生成されたスライドを確認**
   - Cursorが生成したMarpスライドファイル（`.md`）を確認・編集します
   - Marp拡張機能でプレビューできます

### ロゴ画像のリンクを取得する方法

スライドでロゴ画像を使用する場合、GitHubのrawファイルURLを使用できます。

1. **画像ファイルをGitHubリポジトリにアップロード**
   - ロゴ画像ファイル（PNG、JPGなど）をGitHubリポジトリにアップロードします
   - 例：`images/logo.png` というパスに配置

2. **rawファイルURLを取得**
   - GitHubで画像ファイルを開きます
   - 「Raw」ボタンをクリックします
   - ブラウザのアドレスバーに表示されるURLがrawファイルURLです
   - URLの形式：
     ```
     https://raw.githubusercontent.com/[ユーザー名]/[リポジトリ名]/[ブランチ名]/[ファイルパス]
     ```
   - 例：
     ```
     https://raw.githubusercontent.com/[ユーザー名]/sunaneko-marp-slide/main/images/logo.png
     ```

3. **スライドで使用**
   - 取得したURLをMarkdownの画像記法で使用します：
     ```markdown
     ![ロゴ w:400px](https://raw.githubusercontent.com/[ユーザー名]/[リポジトリ名]/main/images/logo.png)
     ```

## 参考サイト

- [【AIスライド作成】クラスメソッド社内用のMarpテーマを作ってみた！](https://dev.classmethod.jp/articles/classmethod-marp-theme/)

