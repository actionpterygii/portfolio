# いつまでも

## 雑記
- いままでの`package.json`もってきて`npm install`した(jsonにあるやつでインストールされる)のに
```
internal/modules/cjs/loader.js:584
    throw err;
    ^

Error: Cannot find module 'typescript'
```
とかでたので今使ってる`node-modules`フォルダのをそのままコピペでつかっています。
- `Adobe Illustrator 2019` でSVGを作成してCSSで操作(アニメーション)
    - HTMLに埋め込まれたSVGはCSSアニメーションのノリでいじれる
    - Monacoフォントで文字を書いてアウトライン化です
    - [ここ](https://matthewlein.com/tools/ceaser)でCSSアニメーションのためのいい感じを見つけれてとてもいいです。
    - ベクタグラフィックスってかっこいいよね
    - SVGのなんとなくがわかった
        - 謎の`<g></g>`タグがいっぱい生成されていたので(空、無駄囲み)けしました。そうしてよいよう。
        - 今回でいうと`<rect />`がなんか枠で`<path />`がひとつひとつの文字みたいな。
        - このでの、widthやheightは絶対的な扱われ方をするものではないってそりゃそうか
