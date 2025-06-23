# Interactive 3D Glassmorphism Card

[![Deploy on GitHub Pages](https://img.shields.io/badge/Live%20Demo-nanaism.github.io-cyan?style=for-the-badge&logo=github)](https://nanaism.github.io/glass-card/)

マウスの動きに合わせて立体的に傾き、光沢が走るインタラクティブな「グラスモーフィズム」カードです。
モダンなCSSとJavaScriptだけで、どれだけリッチな表現が可能かを探求したフロントエンドの実験的プロジェクトです。

**👇 今すぐサイトで体験！**
### [https://nanaism.github.io/glass-card/](https://nanaism.github.io/glass-card/)

<img width="1894" alt="グラスモーフィズムカードのインタラクション" src="https://github.com/user-attachments/assets/a749e732-30b8-48fe-80ab-a64602edc05d" />

---

## 🌟 プロジェクトの特徴 (Features)

このプロジェクトは、フレームワークに頼らず、Webの基本技術だけで実装されています。

-   **💧 グラスモーフィズム (Glassmorphism)**
    -   CSSの `backdrop-filter` プロパティを駆使し、すりガラスのような半透明で美しい質感を実現しています。

-   **👀 3Dティルトエフェクト**
    -   JavaScriptでマウスカーソルの位置を監視し、その座標に応じてCSSの `transform` プロパティ（`rotateX`, `rotateY`）を動的に変更。
    -   親要素に `perspective` を設定することで、カードがまるで宙に浮いているかのようなリアルな3D表現を生み出します。

-   **✨ 動的な光沢ハイライト**
    -   マウスの位置に応じて、カードの表面を流れるような光のハイライトを生成。ガラスやプラスチックの質感をより一層高めます。

-   **🪶 軽量＆ピュア**
    -   **Vanilla JS, CSS, HTML5** のみで構築。外部ライブラリやフレームワークは一切使用しておらず、コードは軽量で学習にも最適です。

## 💡 技術的なハイライト： どうやって動いているか

このインタラクションは、いくつかのCSSとJavaScriptのテクニックの組み合わせで実現されています。

1.  **CSSによる舞台設定**:
    -   カードの親要素に `perspective` を設定し、3D空間を作り出します。
    -   カード自体には `transform-style: preserve-3d;` を適用し、子要素も3D空間内に配置されるようにします。

2.  **JavaScriptによるマウス追跡**:
    -   `mousemove` イベントリスナーで、マウスがカードの上に乗った時の座標を取得します。
    -   カードの中心を原点(0,0)として、そこからのマウスの相対距離を計算します。

3.  **CSSカスタムプロパティへの動的反映**:
    -   計算した相対距離を、CSSカスタムプロパティ（例: `--rotateX`, `--rotateY`）にリアルタイムでセットします。
    -   CSS側では、これらのカスタムプロパティを `transform: rotateX(var(--rotateX)) rotateY(var(--rotateY));` のように参照します。
    -   この手法により、JavaScript（ロジック）とCSS（スタイリング）の関心をきれいに分離できます。

## 🛠️ 使用技術 (Tech Stack)

-   **HTML5**
-   **CSS3**
-   **JavaScript (Vanilla JS)**

## 🚀 ローカルでの実行方法 (Getting Started)

このプロジェクトは非常にシンプルです。

1.  **リポジトリをダウンロードまたはクローンします。**
    ```sh
    git clone https://github.com/nanaism/glass-card.git
    ```
2.  **`index.html` ファイルをブラウザで直接開くだけで動作します。**
