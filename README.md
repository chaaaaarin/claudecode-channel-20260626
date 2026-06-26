# No.68【公式発表】Codex long-running 撮影ノート

## 動画タイトル案
- 【OpenAI公式】Codexを「仕事の置き場所」に変える新機能まとめ——Durable Threads・ループ・メモリを一気に解説
- Codexが「チャット」から「仕事の拠点」へ——long-running work完全解説

---

## ✅ 確定情報（公式確認済み）

### Codex-maxxing とは
- OpenAI公式PDF「Codex-maxxing for long-running work」（2026年公開）
- 著者：OpenAI Codex開発者 Jason Liu
- 単発プロンプトではなく「長く続く仕事の置き場所」としてのCodex利用を提唱
- 全27ページ、10章構成

### 主要機能10章
1. **Durable threads（永続スレッド）** — 仕事専用の継続スレッド。コンテキストを失わずに再開できる
2. **Voice input（音声入力）** — 整理されていない思考をそのまま渡せる。スピードではなく「質の変化」
3. **Steering（ステアリング）** — 作業中に次の指示・修正を追加できる
4. **Memory（メモリ）** — 会話の外に記憶を置く。`vault/` ディレクトリ構造を推奨
5. **Computer & Browser use** — $browser（ローカル）/ @chrome（認証済み）/ @computer（GUI）の使い分け
6. **Remote control（リモートコントロール）** — 別デバイスから確認・承認・方向修正
7. **Thread automations（スレッド自動化）** — ハートビート型の定期実行。例：30分ごとにSlack/Gmailチェック
8. **Three loops（3つのループ例）** — Chief of Staff / フィードバック監視 / 返金対応
9. **Goals（ゴール設定）** — 弱いゴール vs 強いゴール。完了条件・制約・検証基準まで指定
10. **Side panel（サイドパネル）** — Markdown・CSV・スプレッドシート・スライドをスレッド内でレビュー

### 公式が示す役割分担
- **Codexがやること**：探す、読む、整理する、下書きする、選択肢を作る
- **人間がやること**：判断する、承認する、送信する、公開する、責任を持つ

---

## 🔶 一次情報あり（要確認）

- Codex週間アクティブユーザー数：**400万人超**（2026年5月時点）
- コーディング以外のユースケースが**50%超**に（Codex公式ブログより）
- Boris Cherny（Claude Code責任者）の発言：「直近30日、Claude Codeへの自分の貢献の100%がClaude Codeによって書かれた。259本のPRをマージした」
- Uberがエンジニア1人あたりAI利用に月**1,500ドル**上限を設定（コスト管理のため）

---

## ⚠️ 未確認・補足情報

### ループエンジニアリングの文脈（@taiyo_ai_gakuse より）
- 「エージェントにプロンプトを打つな。ループを設計しろ」（Peter Steinberger、220万ビュー超）
- ralphループ（2025年）→ /goalコマンド（2026年）→ オーケストレーションループという進化の系譜
- ループの4条件：①タスクが繰り返す ②検証が自動化されている ③トークン予算に余裕 ④エージェントがシニア相当の道具を持つ
- 注意：「新規性は少し盛られている」——Anthropicが2024年12月に文書化済みのevaluator-optimizerパターンの延長線

### @kawai_design の整理（記事「Codex公式ガイド完全解説〜長時間タスクを任せる10の型〜」）
- 最初に考えるべきは「どんなプロンプトを書くか」ではなく「この仕事の文脈をどこへ置くか」
- 最初に作る3ファイル：`workstream.md` / `memory/project-state.md` / `done-definition.md`
- 長期スレッド向き：毎週続くプロジェクト、顧客対応、OSSのissue確認、リリースノート作成

### @AnatoliKopadze の投稿（182万ビュー）
- 「Anthropicのエンジニアが3エージェント（計画・構築・判定）でゼロからフルアプリを40分で構築」
- 「勝者は最も賢いモデルを持っている人ではなく、最良のループを持っている人」

---

## 台本構成メモ

### 導入（1〜2分）
- 「Codexをチャットとして使うと、毎回同じ説明を繰り返す羽目になる」
- 「OpenAIが公式PDFで"仕事の置き場所"という概念を提唱した」

### 本編（10〜12分）
1. Durable threads の仕組みと活用例
2. Memory / vault の設計思想
3. Thread automations のデモイメージ（30分ごとのSlack監視）
4. 3つのループ例（Chief of Staff / フィードバック監視 / 返金）
5. 人間の役割：承認と不可逆判断だけ

### まとめ（1〜2分）
- 続く仕事は専用スレッドへ
- 記憶は会話外に
- Codexは準備、人間は承認

---

## 出典

| 確度 | ソース | URL |
|---|---|---|
| ✅ | OpenAI公式 Codex-maxxing PDF | https://cdn.openai.com/pdf/8a9f00cf-d379-4e20-b06f-dd7ba5196a11/OAI_WhitePaper_Codex-maxxing26.pdf |
| ✅ | OpenAI公式ページ | https://openai.com/index/codex-maxxing-long-running-work/ |
| ✅ | YouTube解説（まさおAIじっくり解説ch） | https://youtu.be/EJ-NSOLKUkw?si=iOpB6g26A7IFf_Tq |
| 🔶 | @kawai_design X記事 | https://x.com/kawai_design/status/2069933062276948232 |
| 🔶 | @taiyo_ai_gakuse Xスレッド | https://x.com/taiyo_ai_gakuse/status/2064329757328830627 |
| 🔶 | @AnatoliKopadze ポスト | https://x.com/AnatoliKopadze/status/2068690663919530207 |

---

⚠️ 本資料は非公式まとめです。最新の仕様は公式サイトでご確認ください。
