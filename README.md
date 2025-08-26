# JCL – Japanese C Language（公式ポータル）

> **日本語で書ける、C言語学習のための教育向け言語エコシステム**  
> JCLは「日本語キーワード → C言語」への変換を通じて、初学者の学習曲線をなめらかにします。

[![Latest Release – Extension](https://img.shields.io/github/v/release/Konoa-1025/JCL-Extension?label=VSCode%20Extension)](https://github.com/Konoa-1025/JCL-Extension/releases)
[![Latest Release – Engine](https://img.shields.io/github/v/release/Konoa-1025/JCL-Engine?label=Engine)](https://github.com/Konoa-1025/JCL-Engine/releases)
[![Latest Pre-release – Cloud](https://img.shields.io/github/v/release/Konoa-1025/JCL-Cloud?include_prereleases&label=Cloud)](https://github.com/Konoa-1025/JCL-Cloud/releases)

---

## 💭 開発者の想い — なぜJCLを作ったのか

いまプログラマー人口が伸び悩む中で、「プログラムは思ったより簡単で、誰でもできる」という実感をもっと広げたい——その想いから、JCL（Japanese C Language）を開発しました。  
JCLは**日本語で書ける**けれど、**文法はC言語そのもの**。初心者が最初から「本物の構文」を使って学べるように設計し、あとでPythonやCに進むときの**ギャップを最小化**します。

- 📚 書き方（構文）を母語で理解する  
- 🎯 プログラムの**構造**（型・分岐・反復）に早く慣れる  
- 🔍 「ここが**これ**に当たるのか！」という**対応関係の発見**を得る

JCLで書いたコードをトランスパイルすると、対応する**Cコードが見える**ため、  
> ✨「この日本語の1行が、このCの1行になるのか！」  
> 💪「意外と理解できる！」  
> 🎉「苦手意識が薄れてきた！」

という“腹落ち体験”が起きます。**結びつける思考**（対応づけ・抽象化）は、プログラミングだけでなく、ものづくり全般の学びに不可欠。JCLはその思考を育て、**成長と工夫**を促す入り口を目指しています。

将来的には実際の教育現場に持ち込めるような言語を目指しています。

---

## 🔥 目玉の機能（Highlights）

1. **日本語 → C言語 トランスパイル（対訳が見える）**  
   - JCLで書いたコードが**どのC構文に対応するか**を可視化。  
   - 「対応づけ」の体験が学習の核心です。

2. **“本物の構文”準拠**  
   - if/else、for、型など**C言語の構造**をそのまま学べる。  
   - 後でPython/Cへ進む際の**学習転移がスムーズ**。

3. **自動コンパイル＆実行（ローカル/VSCode）**  
   - `.jc → .c → 実行` を自動化。VS Code拡張で**F5ワンクリック実行**。

4. **クラウド実行（Webエディタ）**  
   - ブラウザだけで試せる。**JCL↔Cの対応**をその場で確認。

5. **学習補助**  
   - 複数行の`表示`に対応（自動改行）。  
   - 未対応キーワードや構文の**警告表示**で学習をガイド。

---

## 🎓 想定する導入位置

- **初学者の最初の一歩**（中高〜大1、リテラシー教育）  
- **Python/Cに進む前の“ブリッジ”**  
- **授業・部活・自習**での短時間体験（45分×2コマで表示→分岐→繰り返し）

---

## 🗺️ 今後の展望（Roadmap 抜粋）

- エラー表示の詳細化（行・列、ヒント提案）  
- サンプル/課題バンドル（配列・関数・文字列・乱数…）  
- 教材モード（JCL↔Cの**チートシート連動**）  
- 実行サンドボックスの安全性・安定性強化


## 体験する
- **Webで今すぐ試す（JCL Cloud β）**  
  https://konoa-1025.github.io/JCL-Cloud/web-editor/
- **VS Code 拡張（JCL Extension）**  
  Marketplace: https://marketplace.visualstudio.com/items?itemName=Studio-Delta.japanese-c-language  
  Releases: https://github.com/Konoa-1025/JCL-Extension/releases

---

## プロジェクト構成
- **JCL-Engine**（ローカル実行用トランスパイラ）  
  https://github.com/Konoa-1025/JCL-Engine
- **JCL-Extension**（VS Code統合・ハイライト・F5実行）  
  https://github.com/Konoa-1025/JCL-Extension
- **JCL-Cloud**（ブラウザ実行・JCL↔C可視化）  
  https://github.com/Konoa-1025/JCL-Cloud

---

## 5分クイックスタート（VS Code 拡張）
1. VS Code 拡張「Japanese C Language (JCL)」をインストール  
2. 新規ファイル `hello.jc` を作成して次を貼り付け： `表示 "こんにちは、JCL！"`  
3. **F5** で実行 → 出力を確認

> ローカル実行派は JCL-Engine の `runner.py` でもOK。

---

## ローカル実行（JCL-Engine）
- リポジトリ取得: `git clone https://github.com/Konoa-1025/JCL-Engine.git` → `cd JCL-Engine`  
- サンプル作成: `echo '表示 "こんにちは、JCL！"' > samples/hello.jc`  
- 実行（JCL → C 生成 → コンパイル → 実行）: `python runner.py samples/hello.jc`

---

## 教育活用のヒント
- 45分×2コマで「表示 → 分岐 → 繰り返し」  
- 課題例（配列/関数/文字列/乱数）はサンプル集で段階的に提示

---

## リリース情報
- **Extension**: 安定版 `v1.x` を順次公開  
- **Engine**: 安定版 `v1.x`  
- **Cloud**: 現在 **β**（`v0.9.0-beta.*`）で公開中

---

## ライセンス・クレジット
- License: MIT（各リポジトリ参照）  
- © StudioDeltaLab / JCL Project
