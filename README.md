# test_dependabot
dependabot を導入してみるテスト

[dependabotとは](https://docs.github.com/ja/code-security/supply-chain-security/managing-vulnerabilities-in-your-projects-dependencies/configuring-dependabot-security-updates)

## 確認手順

### マニフェストファイル（`Dockerfile`）を追加。  
今回は、Docker Imageのバージョン更新有無を確認して欲しいので、
マニフェストファイルとしてDockerfileを設定。

### github ディレクト配下に`dependabot.yml`を追加
dependabotを導入するのに必要なので、設定。

### デフォルトブランチにpush
デフォルトブランチにdependabot.ymlがないと、dependabotが動かないので、早速push。

### プルリクが作成されるか確認
https://github.com/kokiwaku/test_dependabot/pull/3

作成された！！！

### Github > リポジトリ（test_dependabot） > Insightsタブ > Dependency graph > Depandabot を確認

こんな感じで、dependabotが走った結果のログが吐かれている。
どうやら、手動でdependabotすることもできるみたい。