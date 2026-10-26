# 生成サマリと要確認リスト(2026-07-07 docs整備タスク)

過去タスクの指摘(#1a2940→#1a3a8f ほか)は各タスク記録を参照。

## 生成ファイル

- website/CLAUDE.md(Folder instructions。brand/facts は shared/ 参照)
- website/facts.md(確定事実+更新ルール。**後で shared/ へ移動**)
- website/docs/voice.md / copy_decisions.md(ADR 7件)/ changelog.md
- website/deploy.md(公開先未確定のため手順は保留)
- 既存 html は未変更。

## 実装の要修正・要確認箇所

### 1. 年数直書き(「75年」等)— facts.md の計算派生ルール適用対象

⚠️ 第1段階では本文4箇所と報告したが、meta タグ等を含め再集計の結果 **17箇所**。

| file | 行 |
|---|---|
| index.html | 15, 24, 34(meta)、1101, 1113, 1264, 1434 |
| company.html | 24, 34(meta)、631, 710 |
| careers.html | 646, 724 |
| tklab.html | 568, 1245, 1246, 1274 |

### 2. CEO年齢の直書き

| file | 行 | 内容 |
|---|---|---|
| company.html | 856 | 「1978年生まれ(47歳)」— 年齢は計算派生へ。47歳の基準時点も未確認 |

### 3. 緑 #22c55e 残存(正: #2d8a5f、shared/brand.md)

| file | 行 |
|---|---|
| tklab.html | 65(--green定義)、270, 342, 703, 714, 715, 721 |

### 4. デプロイ手段未確定

- 指定は「Netlify公開」だが、実装は Apache 用 .htaccess のみで netlify.toml / _redirects / _headers 無し。公開先の確定待ち(詳細: deploy.md)。

## facts.md に「未確認」として残した点

二代目・三代目社長、五代目就任年、代表者の誕生日(月日)、沿革1951〜2007年の空白、金属素形材への事業拡大時期。
