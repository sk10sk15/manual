# Project Context & Rules: 作業書作成支援ツール (動画版)

## 👤 User Profile
- **Role**: 開発リーダー（元フロントエンドエンジニア）。社長の息子。
- **Background**: 技術的な議論が可能。UXの摩擦（0.1秒のストレス）を極端に嫌う。
- **Voice Preference**: 視覚的なフィードバックと、自律的な問題解決を重視。

## 🛠 Tech Stack
- **Frontend**: React, Tailwind CSS, JavaScript
- **Tools**: Warp (Terminal), Cursor (Editor)
- **Environment**: Windows

## 🎨 UI/UX Guidelines
- **Layout**: 
    - 動画プレイヤーとヘッダーは固定。右側の「作業項目リスト（Steps）」のみスクロールすること。
    - 印刷プレビュー（A4）の右マージンを確保し、文字サイズ拡大時の見切れを厳禁とする。
- **Navigation**:
    - 操作パネル（複数選択・上下移動ボタン）は「左サイドバー」の編集ツールセクション下に配置し、常に追従（Sticky）させること。
    - コンテンツ（Step）の上下移動時は、スクロール位置を自動調整して対象が常に画面内に留まるようにすること。
- **Visuals**:
    - フォント: 字幕や特定のテキストには「MS Gothic」を優先的に使用。
    - テキストラベルは赤文字に変更できる機能を持たせる。
- **Interaction**:
    - 削除時は確認ダイアログ「本当に消しますか？」を表示し、デフォルトは「いいえ」にフォーカスすること。

## 💾 Data Handling
- **JSON**: データの保存・読み込み時にテキストエリアの内容が完全に同期されることを保証すること。
- **Git Rules**:
    - ブランチ運用: `test` ブランチを本流とし、作業は機能別ブランチで行う。
    - マージ: 履歴の証跡を残すため、原則 `--no-ff` (No Fast-Forward) でマージすること。
    - 除外設定: `.claude/` フォルダはローカル設定を含むため、Git管理から除外（.gitignore）すること。

## 🤖 AI Interaction Prefs
- **Commit Messages**: 具体的かつ簡潔に。
- **Style**: 「〜してほしい」という指示に対し、ファイル編集からテスト実行、コミットまでを自律的に（Agent的に）完結させることを期待。