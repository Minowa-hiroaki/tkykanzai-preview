# デプロイ(未確定・保留)

**公開先未確定。確定後に手順を追記する。**

**原則: 公開はユーザーが実行する。エージェントは差分提案までで、デプロイ・公開操作は一切しない。**

## 現時点で確認できた事実(2026-07-07)

- 実装には Apache 用 `.htaccess` が存在する(HTTPS強制リダイレクト、ErrorDocument 404、キャッシュ制御)。根拠: website/.htaccess
- Netlify 用の設定ファイル(netlify.toml / _redirects / _headers)は存在しない。
- `.htaccess` は Netlify では機能しないため、公開先が Netlify であれば同等設定の移植が必要になる。
- 公開ドメイン: https://www.tkykanzai.co.jp/ 根拠: robots.txt / sitemap.xml
- カスタム404: /404.html。根拠: .htaccess / 404.html

## 要確認

- ⚠️ 公開先が Netlify か Apache系ホスティングか。確定後、この節を手順に置き換える。
