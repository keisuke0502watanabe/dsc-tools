# dsc-tools

DSC パネルグリッド（`dsc-panel-grid.html`）を GitHub Pages で公開するリポジトリ。

## 構成

| 置き場所 | 内容 |
| --- | --- |
| `index.html` | `dsc-panel-grid.html` をリネームしたもの（Pages のトップ） |
| `.claude/skills/dsc-panel-grid/SKILL.md` | Claude Code 用スキル |
| `docs/overview.md` | 概要ドキュメント |
| `.github/workflows/pages.yml` | `main` への push で Pages にデプロイ |

## 元ファイルの取り込み（Mac 側で実行）

```sh
cd /path/to/dsc-tools
SRC=/Users/keisukemac/katsumoto_lab/sumitani/ToSumitani_from
cp "$SRC/dsc-panel-grid.html" index.html
cp "$SRC/SKILL.md" .claude/skills/dsc-panel-grid/SKILL.md
cp "$SRC/overview.md" docs/overview.md
rm .claude/skills/dsc-panel-grid/README.md docs/README.md
git add -A && git commit -m "Add dsc-panel-grid, skill, and overview" && git push
```

## GitHub Pages の有効化（初回のみ、Web UI で）

1. リポジトリの **Settings → Pages** を開く（設定済み）
2. **Build and deployment → Source** を **GitHub Actions** にする
3. `main` に push する（または Actions タブから `Deploy to GitHub Pages` を手動実行）

公開 URL: https://keisuke0502watanabe.github.io/dsc-tools/
