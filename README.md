# tool-catalog（ツール一覧カタログ）

作成済みツールの索引です。**新しいツールを作る前に、まずここを検索してください。**
キーワード（例：シート書き込み、送信、見守り）で既存ツールがヒットしたら、0から作らず既存ツールを流用・拡張します。
新しいツールを作ったら、この表に1行追加してください。

## 共通ツール（他プロジェクトで流用できるもの）

| ツール名 | 何ができる | 検索キーワード | リポジトリ | 状態 |
|---|---|---|---|---|
| sheet-writer | Google Sheetsへの書き込みで見切れ防止書式（列幅・折り返し・行高）を機械的に担保する書き込みtool＋違反検出の検査役 | シート, スプレッドシート, 書き込み, 書式, 見切れ | [sheet-writer](https://github.com/Charee-Villapong/sheet-writer) | 利用可 |
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

## 管理用

| 名前 | 役割 | リポジトリ |
|---|---|---|
| ai-organization | AI組織の企画管理本部（企画はIssueで管理） | [ai-organization](https://github.com/Charee-Villapong/ai-organization) |

## 対象外

- deadline-ledger：廃止済みのため対象外
- 旧ML系（for_practice / forest-type-classification 等）：ツールカタログの対象外

## 運用ルール

1. 新規ツール作成前に、このカタログをキーワード検索する
2. 既存ツールで足りる場合は流用し、足りない分だけ拡張する（コピーを作らない）
3. 新規ツールを作ったら、push前に検閲を通し、この表に行を追加する
4. 汎用化は「共通部分を1本にまとめ、違う部分だけ設定・引数で渡す」形にする
