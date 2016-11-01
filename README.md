# google-chrome-ui-element-samples-side-nav
https://soarflat-prototype.github.io/google-chrome-ui-element-samples-side-nav/

## 概要
https://github.com/GoogleChrome/ui-element-samples/blob/gh-pages/side-nav/index.html

https://www.youtube.com/watch?v=thNyy5eYfbc&app=desktop

で紹介されていた、パフォーマンスを考慮したサイドバー。

## 特徴
- 要素の移動にはtransformを利用する。
- will-changeを常に適用していると、電池消費が増加したりパフォーマンスに影響を及ぼすため、アニメーション中の時のみ適用する。
- 描画イベントは常に1/60秒ごとに発生するため、スワイプ等のイベントとタイミングを合わせることはできない。そのため、スワイプにより発生するイベントでは、変数に位置情報だけ記録し、描画イベント発生時に記録された位置情報を元に描画位置を更新する。