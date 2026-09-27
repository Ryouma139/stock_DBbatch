# stock_DBbatch

Notion の株価レポートから株価DB / 参照DB へ追記する Claude Code スキル。

- スキル: `.claude/skills/stock_db.md`（`/stock_db` コマンド: `.claude/commands/stock_db.md`）
- 入力: `Claude Contens/stock_reports/YYYYMMDD/YYYYMMDD_{企業名}` ページの株価テーブル
- 出力:
  - 株価DB に同じ銘柄が無い → `Claude Contens/株価DB` に追記
  - 株価DB に同じ銘柄がある → 株価DB の `参照回数` を +1 してから `Claude Contens/参照DB` に追記

```sh
/stock_db 20260925
/stock_db 企業名
/stock_db 20260925 企業名
```

Notion MCP の接続と認証が必要です。
