# Code Review Overview

## コードレビューの目的

* 大前提として、以下の目的でコードレビューは行われる
  1. 実装者の他にマージされたコードをメンテナンスできる人が存在できるようにするため
  2. 実装内容について合意形成を取るため（合意する内容は、仕様と実装が一致していることの他に、既存のコードとの一貫性や保守性、可読性などすべて含まれる）

* 上記の大前提を踏まえたうえで、実際のレビューはプロジェクトあるいは各レビューごとに目的を設定する
* 設定される目的はプロジェクトやチーム規模、企業風土によっても異なる
* レビューの目的が何であるかは最低限レビュアーとレビューイの間でコンセンサスを取る（本当はプロジェクト全体でコンセンサスを取るのが望ましい）

## ガイドライン

* コードレビューを行う際は、「どのような点に着目してレビューを行うのか」というレビューの観点を予め定義しておく
* 各観点には優先順位を設定し、優先度の高い観点から順番にレビューを実施する
* 優先度の高い観点でレビューを行う際は、より低い優先度の観点については考えないようにする
* 大きな損失を生む問題・後から修正が困難な問題については、優先度を高く設定しておく
  * 例えば、要求仕様と実装の機能が一致しているかどうかの確認や、将来的に修正しづらくなると分かっているデザインや実装方針の指摘など
* コードの変更が大きい場合、レビューイに対してレビューの単位を細かく分割することを提案する
  * 目安としては、以下の条件を満たすなら分割を検討する
    * 5ファイル以上が大きく変更されている
    * レビューに20分以上かかると思われる

### レビュアー向けのTips

1. 細かいコーディングスタイルよりも設計を第一にレビューする
   * 設計に関する観点の優先度を高く設定しておく
   * スタイルについてはliterやformatterで自動的に修正できるのが理想
2. 「自分がこのコードをメンテナンスする」という観点でレビューする
   * 自分が理解でき、正しく保守や拡張ができると言えるコードであるかどうかを優先的に考える
3. 自分の考えを押しつけ過ぎない
   * レビュアーとレビューイとの間でイメージが食い違っていたとしても、書かれたコードのほうが劣る点を明確に指摘できない場合はレビューイの方針を尊重する
4. 人ではなくコードを批判する
   * 可能な限りコードを書いた個人への言及を避ける
   * 一般論としては、人ではなく物を主語にした文体を意識すると、個人への言及と取られるような文を避けやすい
5. 良い設計やスタイルを見つけたら褒める
   * レビューイはたまたま良いパターンを書いただけで、その真の価値に気づいてないかもしれない
   * レビュアーがそのパターンを良いと知っているのであれば、その知見を共有することで学習効率を上げることができる
6. レビューイからの質問には必ず答える
   * レビューイは知識量の差や単なる説明不足によってレビューコメントを理解できないことがありそのギャップを埋めるために質問をしているので、レビュアーは必ず答える義務がある

### レビューイ向けのTips

1. レビューはなるべく小さくする
   * レビュアーへの負担を軽減するため、コードレビューの大きさは小さいほうがよい
   * 可能な限り小さい変更で目的を達成できるようにする
2. コンテキストをPRやコミットログ、チケット等で可能な限り説明する
   * レビュアーが「なぜこの変更を行わなくてはならないのか」を知りたい場合もある
   * コード変更の内容や背景を端的に説明する
3. レビュアーの質問は攻撃ではない
   * レビュアーはそのコードを自分がメンテナンスしないといけないという気持ちでレビューする
   * レビュアーからの質問には必ず答える
4. コードへの指摘はレビュアー自身への攻撃を意図していない
   * レビュアーはレビューイを傷つけるために指摘しているわけではない
   * 批判的なコメントを受けることが多い場合、レビューイの能力が低いと糾弾されているように感じるかもしれない
   * レビューコメントが精神的な負担になっているのであれば、プロジェクトマネージャーや同等以上の立場の人に相談すること

## チェックリスト
* [コードレビューチェックリスト](/docs/checklist.md)

## 参考
* [コードレビューの目的と考え方](https://osak.hatenablog.jp/entry/code-review-objectives-and-howto)
* [Code Review Checklist](https://github.com/mgreiler/code-review-checklist)