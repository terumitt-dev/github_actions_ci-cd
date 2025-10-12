# GitHub Actions CI/CD

このリポジトリは、GitHub Actionsを使用したCI/CDワークフローの設定例を提供します。

## 概要

このプロジェクトには以下のGitHub Actionsワークフローが含まれています：

- **Bot Approve PR**: コメントベースでのPR自動承認機能
- **Reusable CI**: Qodo Mergeを使用した再利用可能なCIワークフロー

## ワークフロー詳細

### 1. Bot Approve PR (`bot-approve.yml`)

プルリクエストにコメント `/bot-approve` を投稿することで、Botが自動的にPRを承認します。

- **トリガー**: プルリクエストへの新しいコメント
- **実行条件**: コメント内容が `/bot-approve` の場合のみ
- **動作**: GitHub CLIを使用してPRを自動承認

### 2. Reusable CI (`reusable-ci.yml`)

Qodo Merge（旧PR-Agent）を使用したAI駆動のコードレビューワークフローです。

- **トリガー**: 他のワークフローから呼び出し、または手動実行
- **入力**: PR番号、実行コマンド、対象リポジトリ
- **動作**: AIを使用したコードレビューや改善提案

## 使用例

### Bot承認の使用例
プルリクエストのコメント欄に以下を投稿：
```
/bot-approve
```

### Qodo Mergeコマンド例
プルリクエストのコメント欄に以下を投稿：
- コードレビューの実行
```
/review
```
- コードの改善提案
```
/improve
```
