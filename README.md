# tool-catalog（ツール一覧カタログ）

作成済みツールの索引です。**新しいツールを作る前に、まずここを検索してください。**
キーワード（例：シート書き込み、送信、見守り）で既存ツールがヒットしたら、0から作らず既存ツールを流用・拡張します。
新しいツールを作ったら、この表に1行追加してください。

## 共通ツール（他プロジェクトで流用できるもの）

| ツール名 | 何ができる | 検索キーワード | リポジトリ | 状態 |
|---|---|---|---|---|
| sheet-writer | Google Sheetsへの書き込みで見切れ防止書式（列幅・折り返し・行高）を機械的に担保する書き込みtool＋違反検出の検査役 | シート, スプレッドシート, 書き込み, 書式, 見切れ | [sheet-writer](https://github.com/Charee-Villapong/sheet-writer) | 利用可 |
| bookkeep | 応募候補リストの後処理（応募済み記録＋行グレー化／終了記録）を1コマンド化し読み戻し検証まで行う | 候補リスト, 応募, グレー, 後処理, シート | [job-candidate-list](https://github.com/Charee-Villapong/job-candidate-list) | 利用可 |
| inventory-harness | 棚卸し・リファクタリング点検の管理（観点×対象マトリクス、未消化が残ると完了にできない） | 棚卸し, リファクタリング, 点検, マトリクス | [inventory-harness](https://github.com/Charee-Villapong/inventory-harness) | 利用可 |
| mac-connection | Mac画面操作ツール集。中の gui_flow がLINE／DiscordのGUI送信（前面化→空確認→入力→読み戻し照合）を担う。ScreenCheck（窓キャプチャ）等の補助ツールも含む | Mac, GUI, 送信, LINE, Discord, 画面操作, スクリーンショット | [mac-connection](https://github.com/Charee-Villapong/mac-connection) | 利用可 |
| win_ops | Macの窓・メニュー操作CLI（窓一覧・窓撮影・AXスナップショット取得と項目press・窓閉じ）。GUIエージェントキュー経由で実行し結果をJSONで返す。送信系の gui_flow とは分離（mac-connection内 tools/win_ops） | Mac, 窓, メニュー, AX, スクリーンショット, 画面操作 | [mac-connection](https://github.com/Charee-Villapong/mac-connection) | 利用可 |
| cron-watchdog | 定期実行（cron）の稼働見守り。最終成功時刻を台帳化し、期限超過を検出する | cron, 見守り, 死活監視, 台帳 | [cron-watchdog](https://github.com/Charee-Villapong/cron-watchdog) | シャドー運用中 |
| pre-push-scan | GitHub push前の検閲スクリプト（個人情報・接続情報・認証情報の混入チェック）。現在は mac-connection/scripts と job-candidate-list/scripts に同等品が別々に存在する | 検閲, push前, 個人情報, スキャン | mac-connection / job-candidate-list の各 scripts | 要共通化（重複あり） |

## 専用プロジェクト（部品は流用できる場合あり）

| ツール名 | 何ができる | 検索キーワード | リポジトリ | 状態 |
|---|---|---|---|---|
| interview-notes | 面談の録音→転送→文字起こし→要約md保存のパイプラインと面談ノート管理 | 面談, 録音, 文字起こし, 要約 | [interview-notes](https://github.com/Charee-Villapong/interview-notes) | 開発中 |
| job-candidate-list | 求人情報から応募候補を収集し、適合判定してシートに記録する | 求人, 転職, 候補リスト, 収集 | [job-candidate-list](https://github.com/Charee-Villapong/job-candidate-list) | 第2段階進行中 |
| fortune | 毎朝の「今日の占い」PDF生成（複数占術の組み合わせ） | 占い, PDF生成 | [fortune](https://github.com/Charee-Villapong/fortune) | 稼働中 |
| kids-mac-notify | 子供のMacへ通知を送るエージェント（ダイアログ表示＋音声読み上げ） | 子供, Mac, 通知, リマインド | [kids-mac-notify](https://github.com/Charee-Villapong/kids-mac-notify) | 作成済み・未設置 |
| skills | AIエージェント向けカスタムスキル集（SKILL.mdの手順書集） | スキル, 手順書, SKILL.md | [skills](https://github.com/Charee-Villapong/skills) | 稼働中 |
| entropy-reduction | 仕組みの総量（リポジトリ・cron・ルール・台帳行など）を計測し、重複・死蔵・符号化の候補を検出→判定→仕分け提示→削減実行までを疎結合なユニット群で担う。削減の担保は保存率テスト（意味の保存が絶対の制約、削減量は記録のみ） | エントロピー, 削減, 計測, 重複, 死蔵, 保存率, 埋め込み, PCA | [entropy-reduction](https://github.com/Charee-Villapong/entropy-reduction) | 開発中 |
| codify-taskforce | mdで運用されるルールのうちコード化できる部分を週次で抽出・判定し、開発Issueとして起票する（相反点検とわかりにくい記述の書き換え候補も対象）。判定はチェックリスト方式の2軸で、コード化可の候補は週上限の範囲で起票する | コード化, 抽出, 判定, 起票, 相反, 書き換え, 週次, ハーネス | [codify-taskforce](https://github.com/Charee-Villapong/codify-taskforce) | 稼働中（毎週火曜10:08） |

| ledger-morning-harness | タスク台帳の毎朝メンテナンス（新規収集→現況更新→確認・前進）を3エージェント直列で実行するワークフロー（ハーネス） | 台帳, ハーネス, ワークフロー, 直列 | [ledger-morning-harness](https://github.com/Charee-Villapong/ledger-morning-harness) | 稼働中 |
## 管理用

| 名前 | 役割 | リポジトリ |
|---|---|---|
| ai-organization | AI組織の企画管理本部（企画はIssueで管理） | [ai-organization](https://github.com/Charee-Villapong/ai-organization) |

## 運用ルール

1. 新規ツール作成前に、このカタログをキーワード検索する
2. 既存ツールで足りる場合は流用し、足りない分だけ拡張する（コピーを作らない）
3. 新規ツールを作ったら、push前に検閲を通し、この表に行を追加する
4. 汎用化は「共通部分を1本にまとめ、違う部分だけ設定・引数で渡す」形にする
