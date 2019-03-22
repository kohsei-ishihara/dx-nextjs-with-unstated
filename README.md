# DX next.js example
DX フロントエンド開発用に調整した Next.js によるアプリケーションです。ボイラープレート的な。  
アクセシビリティ、ユーザビリティ、SEO対策、SNS対応、Docker環境の設定などが含まれています。


## Description
下記は、レポジトリに含まれるファイルとその説明となります。各プロジェクトに合わせて調整してください。  
特に画像は上書いてください。

```
.
├── actions
│   ├── actions.tsx                                  // Action ファイル
│   └── api.tsx                                      // API ファイル
├── components                                       // コンポーネント
│   ├── functions                                    // 関数群
│   │   ├── getPageContext.tsx                       // Material UI SSR用
│   │   └── CheckUndefined.tsx                       // Undefinedの判定
│   ├── index                                        // index ページ関連
│   │   └── IndexMain.tsx                            // index ページ main コンポーネント
│   ├── layouts                                      // レイアウト関連
│   │   ├── BreadCrumb.tsx                           // パンくずリスト
│   │   ├── CustomHead.tsx                           // カスタム head タグ
│   │   ├── Footer.tsx                               // フッター
│   │   ├── Header.tsx                               // ヘッダー
│   │   ├── JsonLd.tsx                               // json-ld タグ
│   │   └── SkipToContent.tsx                        // レイアウト関係のコンポーネント
│   ├── other                                        // other ページ関連
│   │   └── OtherMain.tsx                            // other ページ main コンポーネント
│   ├── LazyImg.tsx                                  // Lazyloading Img タグ
│   ├── StyledButton.tsx                             // MaterialUI Button タグカスタマイズサンプル
│   └── StyledButton2.tsx                            // Bootstrap Button タグカスタマイズサンプル
├── docker                                           // Dockerフォルダ
│   ├── development                                  // 開発用
│   │   ├── express
│   │   │   └── Dockerfile                           // アプリ用 Docker
│   │   └── nginx
│   │       └── Dockerfile                           // nginx用 Docker
│   └── production                                   // 本番用
│       ├── express
│       │   └── Dockerfile                           // アプリ用 Docker
│       └── nginx
│           └── Dockerfile                           // nginx用 Docker
├── keys                                             // SSL用のキー郡
│   ├── private.key
│   └── server.crt
├── nginx                                            // nginx用 Docker nginx設定
│   └── conf.d
│       ├── default.conf
│       ├── private.key
│       ├── private.pass
│       └── server.crt
├── pages                                            // ページファイル
│   ├── _app.tsx                                     // アプリケーション本体
│   ├── _document.tsx                                // head タグ拡張用
│   ├── index.tsx                                    // index ページ
│   └── other.tsx                                    // other ページ
├── reducers
│   └── reducer.tsx                                  // Reducer ファイル
├── sagas
│   └── saga.tsx                                     // Saga ファイル
├── scss                                             // Sass フォルダ
│   └── custom.scss                                  // サイト全体のカスタマイズ用
├── static                                           // 静的ファイル郡
│   ├── images                                       // 画像ファイル
│   │   ├── favicon.ico                              // デフォルトの favicon
│   │   ├── icon-1200×630.png                        // OGP
│   │   ├── icon-128x128.png                         // manifest
│   │   ├── icon-144x144.png                         // manifest, msapplication-TileImage
│   │   ├── icon-150x150.png                         // browserconfig
│   │   ├── icon-152x152.png                         // manifest
│   │   ├── icon-16x16.png                           // favicon
│   │   ├── icon-180x180.png                         // apple-touch-icon
│   │   ├── icon-192x192.png                         // manifest
│   │   ├── icon-310x150.png                         // browserconfig
│   │   ├── icon-310x310.png                         // browserconfig
│   │   ├── icon-32x32.png                           // favicon 大
│   │   ├── icon-512x512.png                         // manifest
│   │   ├── icon-70x70.png                           // browserconfig
│   │   ├── icon-96x96.png                           // favicon Google TV
│   │   └── shim.png                                 // 1x1 透過 png
│   ├── browserconfig.xml                            // win10 用タイル設定
│   ├── robots.txt                                   // クローリング除外設定
│   ├── site.webmanifest                             // pws 設定, Android Chrome 設定
│   └── sitemap.xml                                  // クローリング用、Google Search Consoleから更新
├── stores
│   └── store.tsx                                    // Store ファイル
├── .babelrc                                         // babel 設定
├── .env.sample                                      // 環境変数 .env にリネームで利用
├── .eslintrc                                        // eslint 設定
├── .gitignore                                       // git 除外設定
├── .npmrc                                           // fontawesome pro 用 npmライセンス設定
├── .prettierignore                                  // prettier 除外設定
├── .stylelintrc.json                                // stylelint 設定
├── README.md                                        // このファイル
├── docker-compose.development.sh                    // Docker compose 起動ファイル 開発用
├── docker-compose.development.yml                   // Docker compose 設定ファイル 開発用
├── docker-compose.sh                                // Docker compose 起動ファイル 本番用
├── docker-compose.yml                               // Docker compose 設定ファイル 本番用
├── jest.config.js                                   // jest 設定
├── jest.setup.js                                    // jest 用アダプタ
├── jest.tsconfig.json                               // jset 用 Typescript 設定
├── next.config.js                                   // next.js 設定
├── package-lock.json                                // アプリ設定バージョン管理
├── package.json                                     // アプリ設定
├── postcss.config.js                                // PostCSS 設定
├── server.js                                        // express サーバー
├── tsconfig.json                                    // Typescript 設定
└── yarn.lock                                        // yarn で入れた node モジュールのバージョン管理
```
## Todo
* [x] SEO対策
* [x] Accessibility対策
* [x] SNS対策
* [x] CSS組み込み
* [x] コンポーネント単位でのスタイル掛け
* [x] ユニットテストの整理
* [ ] インフラ、ディプロイ方法周りの整理
* [ ] データアクセス部分の整理
* [ ] ログイン処理の実装

### 既存サービスに実装の場合
* [ ] サービスのUIを移植
* [ ] サービスとのAPIつなぎ込み

## Demo

## Requirement

## Usage

## Install

## Contribution

## Licence
UNLICENSED

## Author
[Author](https://github.com/Author)
