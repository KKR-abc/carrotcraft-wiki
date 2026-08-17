# CarrotCraft Wiki

Minecraft サーバー **[CarrotCraft](https://carrotcraft.net)** の公式Wikiの本文です。

サイト本体 → **https://carrotcraft.net/ja/docs**

このリポジトリには**文章（.mdx）だけ**が入っています。サイトの実装コードは含まれません。

---

## 間違いを見つけたら / 直したいとき

**Pull Request を送ってください。** 運営が確認して取り込むと、**自動で本番サイトに反映**されます。

いちばん簡単なやり方:

1. 直したいページのファイルを開く（例: `docs/towny.mdx`）
2. 右上の **鉛筆アイコン（Edit this file）** を押す
3. 直して、下の **Propose changes** を押す
4. **Create pull request** を押す

これだけです。GitHubの操作に慣れていなくても、この手順だけで提案できます。

---

## ファイルの場所

```
docs/
  towny.mdx          日本語版
  towny.en.mdx       英語版
  meta.json          サイドバーの並び順（日本語）
  meta.en.json       サイドバーの並び順（英語）
  minigames/         ミニゲーム関連
```

- **`.en.mdx` が英語版**です。日本語を直したら、できれば英語版も直してください（片方だけでも歓迎です）
- `meta.json` はページの並び順です。ページを増やすときはここにも名前を足してください

---

## 書き方

普通の Markdown に加えて、いくつか部品が使えます。

### 注意書き

```mdx
<Callout type="info">補足です</Callout>
<Callout type="warn">気をつけること</Callout>
<Callout type="error">やってはいけないこと</Callout>
```

### カード・タブ・折りたたみ

```mdx
<Cards>
  <Card title="見出し" description="説明" />
</Cards>

<Tabs items={['Java版', '統合版']}>
  <Tab value="Java版">…</Tab>
  <Tab value="統合版">…</Tab>
</Tabs>

<Accordions>
  <Accordion title="よくある質問">答え</Accordion>
</Accordions>
```

`import` 文は書かなくて大丈夫です（サイト側で用意しています）。

### 色

`&6` のような色コードと `<#FF8C00>` のようなRGB指定が本文に出てきますが、これは
**ゲーム内の表示をそのまま載せている**箇所です。文章の装飾には使いません。

### 画像

画像は `/images/...` から始まる絶対パスで書きます。実体はサイト側にあるので、
このリポジトリ上では表示されませんが、**本番サイトでは正しく出ます**。

```mdx
<img src="/images/recruit/hero.png" alt="説明" />
```

### 他のページへのリンク

```mdx
[町の作り方](/ja/docs/towny)      日本語ページから
[How to make a town](/en/docs/towny)  英語ページから
```

**英語ページからのリンクは `/en/docs/...` にしてください。** `/docs/...` と書くと日本語ページに飛んでしまいます。

見出しへのリンク（`#見出し名`）は、**絵文字つきの見出しだとIDの先頭にハイフンが付きます**
（例: `## 📘 チュートリアル` → `#-チュートリアル`）。うまく飛ばないときはここを疑ってください。

---

## お願い

- **ゲームの仕様と違うことは書かないでください。** 分からないときは「〜のようです」と書かず、
  PRの説明欄に「未確認」と書いていただければ運営が確認します
- 大きな変更（ページの新設・構成の変更）は、先に [Discord](https://discord.gg/EKUPDxXaqb) で相談していただけると助かります
- 誤字脱字の修正だけでも歓迎です

---

## ライセンス / 取り扱い

このリポジトリの文章は CarrotCraft の運営が管理しています。
サーバー外での二次利用については [Discord](https://discord.gg/EKUPDxXaqb) までご相談ください。
