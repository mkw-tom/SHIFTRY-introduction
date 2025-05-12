# 🚀 SHIFTRY 

現在、LINEグループを活用したシフト管理SaaS **「SHIFTRY」** を開発中です（※開発段階）。

- SHIFTRY（シフトリー）**は、LINEとAIを活用した小規模店舗向けのシフト自動化SaaSです。
希望提出から調整・作成・通知まで、すべてLINE上で完結。
専用のLINE botをグループに招待するだけで、スタッフとのやり取りをスムーズにします。

「シフト管理はスマホで。」そんな新しい当たり前をつくるべく、日々開発を進めています。

![SHIFTRY pc image](assets/pc-image)

---

## 🧑🏻‍💻 開発状況
- 開発期間：現在で約1ヶ月半
- 人数：1人

## ⚒️ リポジトリ
- [バックエンドはこちら](https://github.com/mkw-tom/SHIFTRY-backend/tree/develop)
- [フロントエンドはこちら](https://github.com/mkw-tom/SHIFTRY-frontend/tree/develop)

## ✨ 導入までのステップ

1.  **オーナーがLINE BOT「SHIFTRY」を追加**
2.  **line認証＆オーナー・店舗登録**
3.  **Botを店舗のlineグループに招待**
4.  **完了**

- スタッフは、lineグループ内に「シフト提出依頼通知」の際に送信されたリンクから登録・ログインして、利用します。
  

## 🧩 使用技術
| フロント | バックエンド | DB | 認証 |
| --- | --- | --- | --- |
| TypeScript | TypeScript | neon | LineOauth |
| Next.js | express | prisma | LIFF |
| Redux |  |  | Bearer認証 |
| TailwindCSS |  |  | JWT |
| daisyUI |  |  |  |

| インフラ | 外部API | テスト・フォーマット | その他 |
| --- | --- | --- | --- |
| Vercel (フロント) | line api | githubActions | Figma |
| AWS ECS（バックエンド） | stripe | jest | Notion |
|  | openAI api | biome | miro |
|  |  |  | postman |


## 🗺️ 技術構成図
![SHIFTRY pc image](assets/SHIFTRY-技術構成図)


## ディレクトリ構成
- Turboを使用したモノレポ構成を採用しており、frontendとbackendで型とバリデーションを共有し、保守性や変更容易性を考慮した設計にしています。
shiftry/
├── apps/ # アプリケーション群
│ ├── frontend/ # Next.js + React フロントエンド
│ │ ├── public/
│ │ ├── app/ # App Router構成
│ │ └── ...
│ └── backend/ # Express.js バックエンドAPI
│ ├── src/
│ └── ...
│
├── packages/ # パッケージ群（共有ロジック・型など）
│ ├── shared/src/ # Type  / z.infer型 / Prisma型 / Zodスキーマ
│
├── .github/ # GitHub Actions 用設定
│ └── workflows/
│
├── .turbo/ # Turboのキャッシュ設定
├── .env # 共通環境変数
├── turbo.json # TurboRepo 設定
├── package.json
├── tsconfig.base.json
└── README.md
