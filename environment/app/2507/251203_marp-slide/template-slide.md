---
marp: true
theme: sunaneko
paginate: true
html: true
title: サンプルスライド
description: サンプルスライドです。
---

<!--
利用用途に合わせてスライドをコピーする形で利用するといいと思います
特にスライド上部にある"_class: "は大切な要素なので間違えないようにしてください
 -->

<!-- _class: title　-->
<!-- _paginate: false -->

# タイトルページ（title）
## XX株式会社御中
### サブタイトル

![sunaneko-logo w:400px](https://raw.githubusercontent.com/suh-sunaneko/sunaneko-marp-slide/main/images/logo_white.png)

---

<!-- _class: align-center agenda -->
<!-- _paginate: false -->

# 目次（align-center agenda）

|  |  |
|---|---|
| 01 | アジェンダ名 |
| 02 | アジェンダ名 |

---

<!-- _class: align-center agenda column-layout -->
<!-- _paginate: false -->

# 目次（8つ以上の場合）（align-center agenda column-layout）

<div class="column">

|  |  |
|---|---|
| 01 | アジェンダ名 |
| 02 | アジェンダ名 |
| 03 | アジェンダ名 |
| 04 | アジェンダ名 |

</div>

<div class="column">

|  |  |
|---|---|
| 05 | アジェンダ名 |
| 06 | アジェンダ名 |
| 07 | アジェンダ名 |
| 08 | アジェンダ名 |

</div>

---

<!-- _class: section -->
<!-- _paginate: false -->

## レイアウト | 中扉・セクション
テキストは左寄せの中央に配置、背景色はグレーになります

---

# 基本のレイアウト

基本のレイアウトを使用する際は必ずスライドタイトルに h1 を利用してください

# 最初のh1以外でもh1を使うことができます

スライドタイトルの下に一本の線が引かれるのでタイトルと内容がハッキリと区別できます

---

# 通常のマークダウン記法

通常のマークダウン記法はそのまま利用することができます。

# 見出し

**太字**, *斜体*, ***太字斜体***, ~~取り消し線~~, `インライン`, [リンク](https://example.com)


- リスト
1. 番号付きリスト


> 引用


```ts
// コードブロック
console.log("Hello, World!");
```

| テーブル | 列2 | 列3 |
| -------- | --- | --- |
| A        | B   | C   |

---

# 通常のMarp記法（よく使うものを抜粋）

## 見出し内の**太字**は赤色になる

見出し内で`**`で囲んだ部分は赤色のアクセントカラーになります

```md
## 見出しの一部を**赤色のアクセントカラー**にする
見出し内で**に囲まれた部分は赤色のアクセントカラーになります
```

---

<!-- _class: no-header -->

# ヘッダーなしレイアウト（no-header）

このスライドではヘッダー部分が非表示になります
フルスクリーンでコンテンツを表示したい場合に便利です

---

<!-- _class: column-layout -->

# 横並びレイアウト（column-layout）

<div class="column">

## 左カラム
- ポイント1
- ポイント2
- ポイント3
</div>

<div class="column">

## 中央カラム
1. 手順1
2. 手順2
3. 手順3
</div>

<div class="column">

## 右カラム
1. 方法1
2. 方法2
3. 方法3
</div>

---

<!-- _class: all-text-center -->

<!-- ↑ここをtext-center, h1-text-center, h2-text-center, h3-text-center, h4-text-center, h5-text-center, h6-text-centerに変更すると、それぞれの見出しレベルごとに中央揃えになります -->

<!-- all-text-centerに変更すると、スライド内のすべてのテキストが中央揃えになります -->

# テキストの中央揃え（all-text-center）
<!-- タイトルは影響を受けません -->

# 見出しレベル1のテキスト h1-text-center
## 見出しレベル2のテキスト h2-text-center
### 見出しレベル3のテキスト h3-text-center
#### 見出しレベル4のテキスト h4-text-center
##### 見出しレベル5のテキスト h5-text-center
###### 見出しレベル6のテキスト h6-text-center
通常のテキスト text-center

---

<!-- _class: align-center -->

# スライド全体のテキストの縦方向中央揃え（align-center）
<!-- タイトルは影響を受けません -->

# 見出しレベル1のテキスト
## 見出しレベル2のテキスト
### 見出しレベル3のテキスト

---

# コードブロック

```ts
type User = {
  id: number;
  name: string;
  email: string;
  isActive: boolean;
};

const users: User[] = [
  { id: 1, name: "山田太郎", email: "taro@example.com", isActive: true },
  { id: 2, name: "鈴木花子", email: "hanako@example.com", isActive: false },
  { id: 3, name: "佐藤次郎", email: "jiro@example.com", isActive: true },
];

function printActiveUsers(userList: User[]) {
  console.log("アクティブなユーザー一覧:");
  userList
    .filter(user => user.isActive)
    .forEach(user => {
      console.log(`ID: ${user.id}, 名前: ${user.name}, メール: ${user.email}`);
    });
}

function activateUser(userList: User[], id: number) {
  const user = userList.find(u => u.id === id);
  if (user) {
    user.isActive = true;
    console.log(`${user.name} をアクティブにしました。`);
  } else {
    console.log("該当ユーザーが見つかりません。");
  }
}

printActiveUsers(users);
activateUser(users, 2);
printActiveUsers(users);
```

コードの大きさに合わせて自動でコードブロック内のテキストが小さくなります

---

<!-- _class: table-custom -->

# 表形式レイアウト（table-custom）

カスタムテーブルスタイルを使用した表形式のサンプルです。

| 項目名 | 説明 | ステータス | 備考 |
|--------|------|------------|------|
| プロジェクトA | 新規システム開発 | 進行中 | 2024年Q1完了予定 |
| プロジェクトB | 既存システム改修 | 完了 | 2024年Q2完了 |
| プロジェクトC | インフラ構築 | 計画中 | 2024年Q3開始予定 |
| プロジェクトD | セキュリティ強化 | 進行中 | 2024年Q2完了予定 |

---

# マイルストーン（Ganttチャート）（Mermaid使用）

<div class="mermaid-script" style="display:none;position:absolute;left:-9999px;width:0;height:0;overflow:hidden;">
<script src="https://cdn.jsdelivr.net/npm/mermaid@10/dist/mermaid.min.js"></script>
<script>
  mermaid.initialize({
    startOnLoad: true,
    gantt: {
      useWidth: 1920,
      useMaxWidth: false,
      leftPadding: 50,
      gridLineStartPadding: 25,
      fontSize: 10,
      sectionFontSize: 20,
      numberSectionStyles: 4,
      axisFormat: '%y/%m',
      tickInterval: '1month',
      topPadding: 20,
      bottomPadding: 15,
      rightPadding: 10
    }
  });
</script>
</div>

<div class="mermaid">
gantt
    title プロジェクトマイルストーン
    dateFormat YYYY-MM-DD
    axisFormat %y/%m
    tickInterval 1month
    section 計画
    要件定義: 2024-01-01, 30d
    基本設計: 2024-02-01, 28d
    section 実行
    詳細設計: 2024-03-01, 31d
    開発: 2024-04-01, 30d
    section 監視制御
    テスト: 2024-05-01, 31d
</div>

---

# マイルストーン詳細

## 計画フェーズ（1-2月）
- **要件定義**: 2024年1月（30日間）
- **基本設計**: 2024年2月（28日間）

## 実行フェーズ（3-4月）
- **詳細設計**: 2024年3月（31日間）
- **開発**: 2024年4月（30日間）

## 監視制御フェーズ（5月）
- **テスト**: 2024年5月（31日間）

---

<!-- _class: column-layout -->

# ステップ・フロー説明用レイアウト（column-layout）

<div class="column">

## STEP1
### 要件定義を行います
- ユーザー要件のヒアリング
- 機能要件の整理
- 非機能要件の確認

</div>

<div class="column">

## STEP2
### 設計・開発を実施します
- システム設計
- コーディング
- 単体テスト

</div>

---

<!-- _class: column-layout -->

# 開発フロー例（column-layout）

<div class="column">

## 計画フェーズ
### プロジェクトの全体像を設計
- スコープ定義
- リソース計画
- スケジュール策定

</div>

<div class="column">

## 実行フェーズ
### 実際の開発作業を実施
- アーキテクチャ設計
- 実装
- コードレビュー

</div>

<div class="column">

## 検証フェーズ
### 品質を確認・改善
- テスト実施
- バグ修正
- リリース準備

</div>

---

<!-- _class: all-text-center align-center -->

![w:450px](https://raw.githubusercontent.com/suh-sunaneko/sunaneko-marp-slide/main/images/logo.png)
