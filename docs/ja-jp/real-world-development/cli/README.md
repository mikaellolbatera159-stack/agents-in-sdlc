---
slug: ja-jp/real-world-development/cli
title: "GitHub Copilot CLI"
description: "Copilot CLI のモード、カスタマイズ、MCP ツール、プル リクエストの自動化を学びながら、Tailspin Toys の変更を 2 つ実装、検証、提供します。"
authors:
  - geektrainer
lastUpdated: 2026-09-18
---

**[GitHub Copilot CLI][about-copilot-cli]** は、ターミナルで GitHub Copilot をエージェント型のコーディング アシスタントとして利用できるようにします。コードベースを探索し、コードを生成し、コマンドを実行し、外部ツールに接続できます。すべてコマンド ラインから行えるため、グラフィカル エディターに切り替えずに作業の流れを保てます。

このワークショップでは、Tailspin Toys の一連の作業に取り組みます。

1. GitHub Codespaces でプロジェクトを準備し、Copilot CLI をインストールして、基本を確認します。
2. 星評価の変更を実装し、ブラウザーで確認して、最初のプル リクエスト (PR) を手動でマージします。
3. 絞り込みの issue から始め、Plan モードでアプローチを決め、Autopilot モードで実装し、Interactive モードでレビューします。
4. リポジトリの指示を更新し、絞り込みの作業に適用します。
5. 既存の `quality-checks` スキルをカスタマイズして、プロジェクトのチェックを実行します。
6. Playwright Model Context Protocol (MCP) サーバーを追加し、ブラウザーで絞り込みの動作を確認します。
7. 品質保証 (QA) カスタム エージェントを作成し、要件、カバレッジ、検証の証拠を確認します。
8. 絞り込みの変更全体を確認し、絞り込み PR に Agent Merge を使用します。
9. コンテキスト、モデル、共有、クラウド エージェントへの任意の委任に役立つスラッシュ コマンドを確認します。

ワークショップに集中できるよう、PR は 2 つ作成します。最初は星評価、次は指示、スキル、QA プロファイル、テストの更新を含む絞り込みです。絞り込みと品質の作業は 1 つの会話とブランチで進めるため、各ツールを学びながら作業を積み重ねられます。

## レッスン

| レッスン | トピック | 説明 |
| ------ | ----- | ----------- |
| [0. 前提条件][ex0] | セットアップ | リポジトリと Codespace を作成します |
| [1. Copilot CLI のインストール][ex1] | インストール | Copilot CLI をインストールして認証し、基本を確認します |
| [2. 星評価を追加する: 手早く成果を出す][ex2] | 最初の変更 | 既存の評価と null の場合の代替表示を確認し、最初の PR をマージします |
| [3. エージェント モード: Plan と Autopilot][ex3] | エージェント モード | issue から機能を計画し、Autopilot で実装して Interactive モードでレビューします |
| [4. カスタム指示で Copilot をガイドする][ex4] | コンテキスト | 指示を確認して更新し、絞り込みの作業に適用します |
| [5. quality-checks スキルをカスタマイズして使用する][ex5] | 繰り返し実行できるチェック | 既存のスキルを確認し、レポート形式を変更して実行します |
| [6. Playwright MCP で機能を検証する][ex6] | ブラウザーでの確認 | CLI で MCP を構成し、絞り込みの動作を調べます |
| [7. QA エージェントを作成して使用する][ex7] | 要件とカバレッジ | 専門プロファイルを作成して選択し、最終検証の証拠を集めます |
| [8. 機能 PR を作成してマージする][ex8] | レビューとマージ | 変更全体を確認して PR を作成し、Agent Merge を使用します |
| [9. GitHub Copilot CLI のスラッシュ コマンド][ex9] | CLI の機能 | コンテキスト、モデル、共有、クラウド エージェントへの任意の委任を確認します |
| [10. まとめと次のステップ][ex10] | まとめ | 作業の流れ、再利用できるカスタマイズ、その他のリソースを確認します |
| [オプション: Foundry を組み込む][foundry] | ホスト型エージェント | モデルを準備し、カタログに基づくエージェントをデプロイして Web サイトに接続します |

## 前提条件

このワークショップに参加する前に、次を準備してください。

- [ ] **Copilot Student、Pro、Pro+、Business、Enterprise** のいずれかの有効なプランがある GitHub アカウント
- [ ] リポジトリと Codespace を作成する権限
- [ ] ターミナルまたはコマンド ライン操作の基本的な知識

> [!TIP]
> 有料プランがありませんか。認証済みの学生は [GitHub Education][student-plan] を通じて GitHub Copilot を無料で利用できます。**Copilot Student** プランには、このワークショップで使用するエージェント、MCP、コード レビュー、Copilot CLI の機能が含まれています。

> [!NOTE]
> Copilot Business または Copilot Enterprise を使用している場合は、管理者が Copilot CLI を有効にしていることを確認してください。

## はじめる

**[前提条件から始める →][ex0]**

[about-copilot-cli]: https://docs.github.com/copilot/concepts/agents/about-copilot-cli
[student-plan]: https://github.com/education/students
[ex0]: 0-prerequisites/
[ex1]: 1-install-copilot-cli/
[ex2]: 2-add-star-rating/
[ex3]: 3-agent-modes/
[ex4]: 4-custom-instructions/
[ex5]: 5-agent-skills/
[ex6]: 6-mcp-playwright/
[ex7]: 7-qa-agent/
[ex8]: 8-create-pull-request/
[ex9]: 9-cli-power-tools/
[ex10]: 10-review/
[foundry]: 8-foundry-agent/
