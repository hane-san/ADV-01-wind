# 共通の開発手順（ADV-01-wind）

共通契約は [AGENTS.md](../AGENTS.md)、Claude Codeの入口は [CLAUDE.md](../CLAUDE.md)。

## 現在地（2026-10-20）

- 初期コミットのみ。ゲームの企画・仕様・素材・コードは**未採用**。
- 他ゲームと同じ流れ：人間の採用 → Issue → 作業ブランチ → PR → CI → リスク別レビュー → 人間の試遊・マージ。
- 企画が決まったら、最初のIssueに「目的・体験・対象外・受入条件・端末（iPhone縦持ちなど）」を書く。Claude Codeはそれまでゲーム内容を作らない。

## 最初のコードPRで決めること（人間の承認が必要）

1. 実行形態（他ゲームと同じ静的ES module + GitHub Pagesか）と公開URL。
2. `npm run check`（構文と決定論テスト）と `rules` / `browser` のCI。
3. 保存キーの名前空間（他ゲームと共有しない）。
4. このゲーム固有の不変条件を AGENTS.md に追記。

## Claude Codeによる監督・明け方の巡回

GPT/Codex等のPRをClaude Codeが受け取る手順は `.claude/skills/steward/SKILL.md`。明け方の巡回：毎日4:12（日本時間）に、専用セッション「明け方の監督巡回（独立監査担当）」が5つのリポジトリのPRを、このスキルの手順で見回る（2026-10-20 採用）。
