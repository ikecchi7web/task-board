# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project

タスクの追加・完了切り替え・削除ができるシンプルなタスクボードアプリ。タスクは localStorage に永続化される。

## デプロイ先

https://ikecchi7web.github.io/task-board/

main ブランチへの push で GitHub Actions が自動デプロイする（`.github/workflows/deploy.yml`）。

## 技術スタック

- **React 18** + **Vite 6**
- スタイルはコンポーネントごとの CSS ファイル（CSS Modules 不使用）
- 状態管理: `useState` / `useEffect`（外部ライブラリなし）
- ストレージ: `localStorage`

## コンポーネント命名規約

- コンポーネントファイル: PascalCase（例: `TaskBoard.jsx`）
- CSS ファイル: コンポーネントと同名（例: `TaskBoard.css`）
- コンポーネント関数: PascalCase の default export
- イベントハンドラ: `handle` + 動詞（例: `handleKeyDown`、`addTask`、`deleteTask`）

## Git Workflow

After every code change, commit and push to GitHub:

```bash
git add <files>
git commit -m "commit message"
git push
```

Remote: https://github.com/ikecchi7web/task-board.git (branch: main)