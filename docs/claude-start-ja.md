# Claudeなど別のAIへ渡す手順

2026年10月18日更新。ユーザーの依頼で、現行ファイルだけを入れた公開用リポジトリを作成しました。開発元のリポジトリと過去の履歴は非公開のままです。**閲覧に認証は不要ですが、公開するだけで別のAIにシェル・ネットワーク・GitHubへの書き込み機能が備わるわけではありません。**

## 渡すもの

- [現在の実装があるブランチ](https://github.com/montainternoadorihistorion/thought-physics-analogies-public/tree/feat/research-prototype)
- [引き継ぎ文書](handoff-ja.md)／[直接取得するテキスト](https://raw.githubusercontent.com/montainternoadorihistorion/thought-physics-analogies-public/refs/heads/feat/research-prototype/docs/handoff-ja.md)
- [ソース一式のZIP](https://github.com/montainternoadorihistorion/thought-physics-analogies-public/archive/refs/heads/feat/research-prototype.zip)
- [編集元の直接リンク](https://raw.githubusercontent.com/montainternoadorihistorion/thought-physics-analogies-public/refs/heads/feat/research-prototype/simulator/source.html)

実装は `feat/research-prototype` にあります。公開用リポジトリではこれが既定ブランチです。非公開の開発元を利用する権限がある場合も、このブランチを指定してください。開発元の `main` には現行の実装が揃いません。ZIPにはGit履歴や認証情報は含まれません。ZIPを展開したら `simulator/index.html` をブラウザーで開けます。ビルドや追加のパッケージは不要です。

## URLを取得できないAIの場合

ユーザーのPCでZIPを取得・展開し、相手のAIのファイル添付機能で渡してください。ZIPを受け付けない場合は、次のファイルを添付できます。

1. `docs/handoff-ja.md`
2. `docs/model-notes-ja.md`
3. `simulator/source.html`（編集元）
4. `simulator/index.html`（単独で開ける完成版）

研究本文を検討する場合は `docs/research-draft-ja.md` も渡してください。添付の数や形式に制限があれば、担当する変更に必要なファイルから渡します。

## 書き込み機能がないAIの場合

GitHubへのpushやPR更新を担当させる必要はありません。修正ファイル、または変更対象のパスが分かるunified diffを返してもらい、ユーザーまたは元の開発環境で反映します。その際は、読んだ版・変更点・実施した確認・実行できなかった確認も併せて受け取ってください。

反映担当は、元になった版と現在の変更を確認して差分を適用し、単独HTMLと会話内表示の同期、変更に応じた検証を行います。確認後に作業ブランチへコミットし、非公開の開発元にある[下書きPR #1](https://github.com/montainternoadorihistorion/thought-physics-analogies/pull/1)へ反映し、確認したファイルを公開用リポジトリにも同期します。公開用コピーの更新だけでは開発元へ自動反映されません。認証情報を相手のチャットへ貼る必要はありません。

## そのまま渡せる依頼文

> このプロジェクトの公開ソースは https://github.com/montainternoadorihistorion/thought-physics-analogies-public の `feat/research-prototype` ブランチにあります。URLまたは添付ファイルから `docs/handoff-ja.md` と `docs/model-notes-ja.md` を読んでください。担当してほしい変更は、続けて私が指定します。既存の四つの場面とユーザーの方針を守り、研究初稿の本文は変更しないでください。取得・実行・GitHubへの書き込みができない場合でも、提供したソースをもとに検討し、修正ファイルまたはunified diffを返してください。実際に確認できたことと、環境上できなかった確認を区別して報告してください。
