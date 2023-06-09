# コードレビューチェックリスト

## 実装について

* [ ] 変更後のコードは想定している目的を達成していますか？
* [ ] コードをより単純化することはできますか？
* [ ] 不要な依存関係を追加していませんか？（コンパイル時、実行時ともに）
* [ ] 使用すべきでないフレームワーク、API、ライブラリ等が使用されていませんか？
* [ ] 追加されたフレームワーク、API、ライブラリはソリューションの改善に役立っていますか？
* [ ] コードは適切な抽象化レベルにありますか？
* [ ] コードは十分にモジュール化されていますか？
* [ ] 保守性、可読性、パフォーマンス、セキュリティの観点でより良いソリューションはありませんか？
* [ ] 似たような機能はすでにベースとなるコードに存在していませんか？もし存在しているならば、それらの機能は再利用することはできませんか？
* [ ] このコードはオブジェクト指向の分析・設計原則（SOLID原則など）に準拠していますか？これらの原則に準拠するためにより良いデザインパターンを適用されていますか？

## ロジックのエラーとバグについて

* [ ] コードが意図したとおりに動作しないユースケースを思い浮かべることができますか？
* [ ] コードが破壊されるような入力や外部イベントを思い浮かべることができますか？

## エラーハンドリングとログについて

* [ ] エラー処理は正しく行われていますか？
* [ ] ロギングやデバッグの情報を追加したり削除したりする必要はありますか？
* [ ] エラーメッセージはユーザフレンドリーになっていますか？
* [ ] ログは十分に出力されており、簡単にデバッグできるように設計されていますか？

## 整合性について

* [ ] コードの変更に伴い、設計資料やREADME等についても更新が行われましたか？
* [ ] システムの他の箇所や後方互換性に影響を与える可能性はありますか？

## セキュリティやデータプライバシーについて

* [ ] コードにセキュリティの脆弱性はないですか？
* [ ] 認可や認証は正しく処理されていますか？
* [ ] セキュリティ攻撃（クロスサイトスクリプティングやSQLインジェクションなど）を防ぐために、入力の検証は正しく処理されていますか？
* [ ] 機密情報（顧客情報やクレジットカード情報）などは安全に扱われ、適切に保管されていますか？
* [ ] 正しい暗号化が使用されていますか？
* [ ] コードの変更によって機密情報の漏洩は発生しないですか？
* [ ] 外部APIやライブラリから取得した情報は、セキュリティ上問題ないかチェックされていますか？

## パフォーマンスについて

* [ ] コードの変更によって、システムのパフォーマンスが低下することはありませんか？
* [ ] コードのパフォーマンスを大幅に向上させるソリューションは存在しないですか？

## テストについて

* [ ] 変更したコードはテスト可能ですか？
* [ ] コードの変更に伴い、テストコードあるいは関連するテストもコードの変更をカバーするように更新されましたか？
* [ ] 追加でテストすべきテストケース、入力、あるいはエッジケースなどはありませんか？

## 可読性について

* [ ] コードは理解しやすいですか？
* [ ] メソッドを小さくすることで、コードの読みやすさを向上させることはできませんか？
* [ ] 関数名、メソッド名、変数名を変えることで、コードの読みやすさを向上させることはできませんか？
* [ ] コードは正しいファイル/フォルダ/パッケージに配置されていますか？
* [ ] 冗長なコメントや古くなったコメントはありませんか？
* [ ] よりわかりやすく伝えるコメントはありませんか？
* [ ] コメントアウトされたコードはありませんか？また、それは削除することはできませんか？

## 参考

* [デザインパターンについて](https://refactoring.guru/ja/design-patterns)
* [「良いコード」を書くために意識している17のTips まとめ](https://zenn.dev/ishiyama/articles/a0c5a7504b856f)
* [モデルやメソッドに名前を付けるときは英語の品詞に気をつけよう](https://qiita.com/jnchito/items/459d58ba652bf4763820)
* [Naming -名前付け-](https://qiita.com/Koki_jp/items/f3d3e824f98d182d4100)
* [うまくメソッド名を付けるための参考情報](https://qiita.com/KeithYokoma/items/2193cf79ba76563e3db6)
* [うまくクラス名を付けるための参考情報](https://qiita.com/KeithYokoma/items/ee21fec6a3ebb5d1e9a8)
* [初心者プログラマーのための英語命名法](https://qiita.com/YutaManaka/items/62dda256bb7ba6c08399)