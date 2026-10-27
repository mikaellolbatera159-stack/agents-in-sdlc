---
title: "レッスン 12 - GitHub Pages でサイトを公開する"
description: "GitHub Copilot アプリを使って Pages ワークフローを構成し、そのプル リクエストを確認して、公開された Space Quiz を検証します。"
authors:
  - jamesmontemagno
lastUpdated: 2026-10-12
---

GitHub Pages で Space Quiz をデプロイし、誰でもアクセスできるようにします。Copilot はワークフローを準備してデプロイを案内できますが、変更を確認し、サイトが公開されたことを自分で確かめてください。

このレッスンでは、次の内容を学習します。

- Copilot に GitHub Pages のデプロイを構成するよう依頼します。
- マージする前にワークフローとプル リクエストを確認します。
- デプロイの状況を追跡し、公開されたサイトを検証します。

## シナリオ

Space Quiz はすでに GitHub リポジトリにありますが、まだ簡単に試す方法がありません。1 つのファイルで構成されたサイトを GitHub Pages で公開すれば、サーバーやランタイム依存関係を追加せずに、公開 URL からアクセスできるようになります。

## Copilot にサイトのデプロイを依頼する

Copilot アプリで `space-quiz` のセッションを開き、次のプロンプトを送信します。

```plaintext
Enable GitHub Pages for this repository. Create a GitHub Actions workflow that builds the website if needed and deploys it to GitHub Pages. Add a README describing the app and how to run it locally if one does not already exist. Create a pull request with these changes and merge it after required checks pass. Monitor the deployment until it succeeds, then report the final URL of the live website. If you lack permission to enable Pages or merge, tell me exactly what I need to approve or do; do not report success until the site is live.
```

![3 段階の図: マージ済みの space-quiz プル リクエスト、Build website、Upload artifact、Deploy to Pages の各ステップを含む GitHub Actions の Deploy website 実行の成功、yourname.github.io/space-quiz/ で公開された Space Quiz。](../../../_images/first-steps-app-pages-deploy.svg)

> [!WARNING]
> このプロンプトは、エージェントにプル リクエストの作成とマージ、およびリポジトリの Pages 設定の変更を依頼します。続行する前に、差分、デプロイ権限、GitHub の承認要求を確認してください。

## ワークフローを確認してデプロイを検証する

1. README がまだない場合に限り、追加されていることを確認します。
2. ワークフローのビルドとデプロイの手順を含め、プル リクエストの変更を確認します。
3. 必須のプル リクエスト チェックに合格してからマージします。
4. GitHub Actions のデプロイ実行を追跡し、成功するまで確認します。
5. 報告された URL を開き、Space Quiz が表示されることを確認します。

エージェントが Pages を有効にできない場合やプル リクエストをマージできない場合は、提示された具体的な手順に従います。デプロイが成功し、公開サイトが読み込まれるまで、タスクを完了したと見なさないでください。

## まとめと次のステップ

Space Quiz が公開され、エージェントの報告だけに頼らずデプロイを確認できました。[レッスン 13: 振り返りと次のステップ][next-lesson]に進みます。

[next-lesson]: ../13-review/
