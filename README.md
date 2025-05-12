# 🚀 SHIFTRY （※開発段階）
- SHIFTRY（シフトリー）**は、LINEとAIを活用した小規模店舗向けのシフト自動化SaaSです。
希望提出から調整・作成・通知まで、すべてLINE上で完結。
専用のLINE botをグループに招待するだけで、スタッフとのやり取りをスムーズにします。

「シフト管理はスマホで。」そんな新しい当たり前をつくるべく、日々開発を進めています。

![SHIFTRY pc image](assets/pc-image)

---

## 🧑🏻‍💻 開発状況
- 開発期間：二ヶ月半経過（5/12日時点）
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
| TypeScript | TypeScript | neonDB | LineOauth |
| Next.js | express | prisma | JWT |
| Redux |  |  | Bearer認証 |
| TailwindCSS |  |  | Helmet |
| daisyUI |  |  |  |

| インフラ | 外部API | テスト・フォーマット | その他 |
| --- | --- | --- | --- |
| Vercel (フロント) | line api | githubActions | turbo |
| AWS ECS（バックエンド） | stripe | jest | postman |
|  | openAI api | biome |  |


## 🗺️ 技術構成図
![SHIFTRY pc image](assets/SHIFTRY-技術構成図.png)

