# dsc-tools

DSC 測定ファイル(島津 .tad / .txt、PerkinElmer Pyris .txt)をブラウザ上でパネル図と CSV にするツール「DSC Panel Grid」を GitHub Pages で公開するリポジトリ。

公開 URL: https://keisuke0502watanabe.github.io/dsc-tools/

## 構成

| 置き場所 | 内容 |
| --- | --- |
| `index.html` | DSC Panel Grid 本体(単一 HTML) |
| `docs/overview.md` | ツールの概要、入力形式、処理の流れ、出力、注意点 |
| `.claude/skills/dsc-panel-grid/SKILL.md` | Claude Code 用スキル。使い方の案内と CSV 集計の手順 |
| `.github/workflows/pages.yml` | push で GitHub Pages に自動デプロイ |

## 更新のしかた

`index.html` を書き換えて push すれば、GitHub Actions が 1 分ほどで公開ページを更新する。

```sh
git pull
cp /path/to/dsc-panel-grid.html index.html
git add -A && git commit -m "Update dsc-panel-grid" && git push
```

## Pages の設定

Settings → Pages → Build and deployment → Source を「GitHub Actions」にしてある。ブランチを `main` にリネームした場合は、`.github/workflows/pages.yml` のトリガーから旧ブランチ名の行を削除してよい。
