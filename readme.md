# TypeWeaver

**音と実用が融合する、適応型タッチタイピング・スタジオ**

`TypeWeaver` は、インストール不要・単一HTMLファイルで動作するブラウザ向けタッチタイピング練習アプリです。無意味な文字列の反復ではなく、自分が読みたい記事やコードを題材（BYOT）にしながら、Web Audio APIによるリアルタイム音響と「指の迷いレーダー」で毎日の練習を楽しく継続できます。

## Live Demo（GitHub Pages）

`https://jkj7vv2nd7-lang.github.io/type-weaver/`

*(※GitHub Pagesを有効化した後、上記URLをご自身の環境に書き換えてください)*

## 主な特徴

* **BYOT（Bring Your Own Text）ステージ生成**

  任意の日本語テキスト、英単語、プログラムコード（TypeScript / Pythonなど）を貼り付けるだけで、即座に練習ステージへ変換します。

* **日本語ローマ字入力の「動的揺れ判定エンジン」**

  `si` / `shi`、`ti` / `chi`、`tu` / `tsu`、促音「っ」の子音重ね先読み、撥音「ん」の文脈判定および余剰 `n` 吸収まで、状態遷移モデルでリアルタイムに許容します。

* **Web Audio API シンクロ音響エンジン（ゼロ遅延）**

  打鍵ごとにペンタトニックスケールの音色をリアルタイム合成。`Lo-fi Synth` / `Mechanical + Piano` / `Zen Marimba` / `Chiptune 8-bit` の4音色と、Lo-fi伴奏ビート（`BGM: ON/OFF`）を備えています。

* **Flow Score & 迷いレーダー（Bigram Latency解析）**

  速度（WPM）と正確率だけでなく、打鍵間隔の均一性を示す `Flow Score` とキー間の遷移遅延（ms）を計測。完走後に苦手運指の特化ドリルをワンクリックで生成できます。

* **立体キートップ配列 & 3テーマ切替**

  物理キーボードと連動して光るQWERTY運指ガイド（F/Jホームポジション突起付き）を搭載。右上のボタンから `Studio` / `Paper` / `Amber` の3テーマを切り替えられます。

## ファイル構成

```
.
├── index.html   # アプリ本体（HTML / CSS / JS 単一ファイル完結）
└── README.md    # 本ドキュメント

```

## GitHub Pages での公開方法

1. GitHub上で新しい公開リポジトリ（例：`typeweaver`）を作成します。

2. `index.html` と `README.md` をリポジトリのルートにアップロード（または `git push`）します。

3. リポジトリの **Settings → Pages** を開きます。

4. **Build and deployment** の Source を `Deploy from a branch`、Branch を `main` / `/ (root)` に設定して **Save** をクリックします。

5. 数分後に発行される `https://<ユーザー名>.github.io/<リポジトリ名>/` へアクセスして利用できます。

## 使い方・推奨環境

* **推奨ブラウザ**: Google Chrome / Microsoft Edge / Safari / Firefox（最新版・PC推奨）

* **入力モード**: 日本語ステージを練習する際は、PCのIMEを **半角英数（直接入力）モード** に切り替えて打鍵してください。入力欄をクリックせず、画面を開いたままそのまま打ち始められます。

* **モバイル環境**: 画面内のタップ入力欄または画面下部のオンスクリーンキーボードから試用できます。