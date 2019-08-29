# maven-repository

社内向けのmaven artifactをホスティングする。

## resolverの設定

以下を `build.sbt` の冒頭に追記する。

- スナップショットの場合

```scala
resolvers += "Opt-Technologies Snapshots" at "https://raw.githubusercontent.com/opt-tech/maven-repository/master/snapshots"
```

- リリースの場合

```scala
resolvers += "Opt-Technologies Releases" at "https://raw.githubusercontent.com/opt-tech/maven-repository/master/releases"

## ディレクトリレイアウト

```
- README.md このファイル
- releases リリース版artifactを置く場所
  - 通常のmaven repositoryの規約に従ってディレクトリを掘ってartifactを置く
- snapshots スナップショット版artifactを置く場所
  - 通常のmaven repositoryの規約に従ってディレクトリを掘ってartifactを置く
```
