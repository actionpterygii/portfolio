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
### SVGをCSSアニメーション
- `Adobe Illustrator 2019` でSVGを作成してCSSで操作(アニメーション)
- HTMLに埋め込まれたSVGはCSSアニメーションのノリでいじれる
- Monacoフォントで文字を書いてアウトライン化です
- [ここ](https://matthewlein.com/tools/ceaser)でCSSアニメーションのためのいい感じを見つけれてとてもいいです。
- ベクタグラフィックスってかっこいいよね
- SVGのなんとなくがわかった
    - 謎の`<g></g>`タグがいっぱい生成されていたので(空、無駄囲み)けしました。そうしてよいよう。
    - 今回でいうと`<rect />`がなんか枠で`<path />`がひとつひとつの文字みたいな。
    - このでの、widthやheightは絶対的な扱われ方をするものではないってそりゃそうか
- 気持ちいいアニメーションを作ってしまうと何回もみてしまいます。
- なんかiPhone(iOS)からみるとCSSアニメーションの黄色がスッてでるのがいかんくなってきっしょい
    - Safari以外にGoogleChrome,Sleipnirからでもだめでした
    - パソコンからは思ったとおりのアニメーションができているのにでした
    - ディレイ実行で実行前を0%色なしwidth0、100%色ありwidth130にしてたけどそういうのはよくない
    - width0なら色ついてても見えないんで`animation-fill-mode: both;`で対応いたしました。よろしくお願いいたします。
        - アニメーション実行前は0%,実行後は100%の`@keyframes`になります >both
    
