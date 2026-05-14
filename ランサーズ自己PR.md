# ランサーズ用自己PR

## はじめに
はじめまして、飯田剛通と申します。  
現在出前館にてFlutterを用いたモバイルアプリケーション開発に従事しており、エンジニア歴は7年になります。  
幅広い技術スタックと豊富な開発経験を活かし、クライアント様のプロジェクトに貢献させていただきたく思います。

## 💼 現在の職歴・スキル概要

### 現職：株式会社出前館（2025年4月〜現在）
**Flutter モバイルアプリケーション開発エンジニア**
- Bloc/Cubitパターンを用いた状態管理とビジネスロジック実装
- GraphQL (Ferry) を活用したサーバー連携
- TypeScript製BFFの保守・運用
- 新機能の企画〜リリースまでの一貫した開発経験

### 副業・個人案件（2026年1月〜現在）
**フルスタック Web エンジニア（Next.js / Supabase / WordPress）**
- クチコミ生成 SaaS「Rissun」を主担当として開発・運用（Next.js 16 + Supabase + Square 課金）
- デジタルスタンプラリー SaaS「StampPass」の要件定義〜DB/API/画面設計
- 三井化学・密科学 MAGSETH 連携の農業生産管理システム（Vercel + Supabase）の設計
- WordPress 案件（GrandPyramid / TourGator / Japan Documented）の Bedrock 化・運用
- Claude Agent SDK を用いた X 自動投稿 MVP「KaigaiMarkeStudio」の設計

## 🚀 得意な技術分野と実績

### 🌐 Webアプリ開発（Next.js / Supabase）**直近の主力スタック**
- **Frontend**: Next.js 16 (App Router) / React 19 / TypeScript / Tailwind CSS v4 / shadcn/ui
- **Backend**: Server Actions + Supabase (PostgreSQL / Auth / Storage / Edge Functions / RLS必須運用)
- **決済**: Square Subscriptions・割引コード・HMAC + 冪等性保証付き Webhook の実装
- **テスト/品質**: Jest, Playwright (E2E), Storybook v8 + MSW、GitHub Actions CI（lint・型・Jest・Storybook ビルド）
- **実績例**:
  - クチコミ生成 SaaS「Rissun（りっすん）」の主担当として、Square 課金システム・MSW モック駆動 Storybook・アナリティクス基盤（CSV Shift_JIS／期間指定／アンケート別 ZIP）・8言語対応・Google Business Profile API 連携を実装
  - デジタルスタンプラリー × プリペイドチケット「StampPass」の要件定義〜DB/API/画面設計
  - 農業生産管理システム（三井化学・密科学 MAGSETH 連携）を Vercel + Supabase 構成で設計

### 📱 モバイルアプリ開発（Android・Flutter）**3年の実務経験**
- **Android開発**: Kotlin, Jetpack Compose, MVVM + Clean Architecture
- **Flutter開発**: Bloc/Cubit, GraphQL (Ferry) 連携, マルチプラットフォーム対応
- **実績例**:
  - 出前館アプリ（Flutter）の継続的な機能改善・パフォーマンスチューニング
  - N予備校Androidアプリの新機能開発・Jetpack Compose 化リファクタリング主導
  - 決済サービス向けNFC決済機能の実装

### 🛠 WordPress（Bedrock 構成）**副業案件で運用中**
- **構成**: Bedrock + Composer 管理、`hello-elementor` 親テーマ・主要プラグイン（Elementor / ACF / The Events Calendar / WPML / CF7）の wpackagist 経由導入
- **コンテンツ設計**: ACF ローカル JSON、CPT 登録のコード化、Elementor テンプレートの JSON 管理
- **運用**: SSH / WP-CLI デプロイ、All-in-One WP Migration による移行、All in One SEO 等での SEO 対策
- **実績例**:
  - GrandPyramid / TourGator / Japan Documented の WordPress 改修・コード化・運用
  - 非エンジニアの誤操作を防ぐ管理画面ガードレール機能（月次リンク変更ボタン等）の実装

### 🤖 AI 駆動開発・運用（Claude Code × Gemini CLI × Claude Agent SDK）

本業・副業の両方で **AI を主力開発エージェント** として日常運用しており、単なる「コード補完ツール」ではなく **CLAUDE.md によるルールエンジン整備・Sub-Agent 分業・コスト最適化** までを含めた運用ノウハウを蓄積しています。

#### Claude Code（Anthropic）の活用
- **役割**: ターミナル統合の `claude` CLI を主力エージェントとして、アーキテクチャ設計・複数ファイル横断のリファクタリング・セキュリティレビュー・CI/CD ワークフロー生成・コミット／PR 作成までを担当させる運用
- **CLAUDE.md 設計**: 各プロジェクトのルートに `CLAUDE.md` を配置し、以下を明文化して AI を「そのプロジェクト専属エンジニア」化:
  - セキュリティ必須ルール（`esc_html()` / `$wpdb->prepare()` / nonce / Capability check 等）
  - コーディング規約（インデント・プレフィックス・`declare(strict_types=1)` 等）
  - 環境前提（Docker Compose / WP-CLI エイリアス / Next.js Server Actions 等）
  - 禁止事項（コアファイル直接編集・`eval()`・`wp-config.php` への書き込み 等）
- **プラン運用**: Claude Pro → **Claude Max** へアップグレードし、トークン消費量・チームでの利用権共有を含めた契約最適化までを担当

#### Gemini CLI（Google）の活用
- **役割**: 最大 100 万トークンのコンテキストウィンドウを活かし、コードベース全域の一括スキャン・ドキュメント初稿生成・依存関係マッピングに活用
- **Search grounding**: WordPress / Next.js / 各種 API の最新仕様取得に Google Search grounding を利用し、AI の知識カットオフ問題を回避
- **Google API 連携**: Search Console API / Analytics API / Google Business Profile API 等、Google エコシステム連携コードの初稿生成

#### Sub-Agent 運用ルール（案件レベルで標準化）
- **分業ルール**: トークン消費を抑える観点から **広域調査・ドキュメント初稿・全域スキャン → Gemini CLI**、**実装・コミット・PR → Claude Code** に分担。Gemini の出力は必ず Claude がレビューしてから適用するフローを Rissun 等の案件で運用ルール化
- **使い分けチートシート**:

| タスク | 担当 | 理由 |
|--------|------|------|
| アーキテクチャ設計・複雑なリファクタリング指示 | Claude | 推論品質・指示忠実度 |
| コードベース全体の一括解析・初稿ドキュメント生成 | Gemini | 大規模コンテキスト |
| 最新仕様の取得（WordPress / Next.js / Google API） | Gemini | Search grounding |
| セキュリティレビュー（XSS / SQLi / CSRF） | Claude | セキュリティ判断の精度 |
| Google API 連携コード生成 | Gemini | Google エコシステム理解 |
| 実装・コミット・PR 作成 | Claude Code | 直接ファイル操作・Git 操作 |

#### Claude Agent SDK によるエージェント設計
- **構成**: Next.js 15 + Claude Agent SDK (TypeScript) + Supabase + 既存 n8n
- **モデル運用**: Sonnet 4.6 を主軸に、`fallbackModel` で深掘り時のみ Opus 4.7 に切替える二段構成
- **Prompt Caching**: System Prompt と過去高評価データセットをキャッシュ対象化し、Claude API コストを **30〜50% 圧縮**
- **エージェント協調**: Research（情報収集）→ Writer（文章生成 3 案）→ Critic（事実誤認・炎上・CTA・ハッシュタグの投稿前チェック）の **3 エージェント協調パイプライン** を設計
- **コスト管理**: Anthropic コンソールでの月予算アラート設定、月額 $5〜10（約 750〜1,500 円）に収めるコスト設計

#### WordPress × AI-CLI 連携の開発フロー整備
- **Docker Compose 環境**: ローカル開発を Docker Compose 化し、`d-wp = docker compose exec -u www-data wordpress wp` のエイリアス経由で WP-CLI を AI から叩かせる構成を整備
- **AI 主導の運用**: 「`d-wp theme list` でテーマを確認 → 該当 PHP の WPCS 違反を修正」「`d-wp post list --format=json` から取得して特定 ACF を一括更新」など、AI が WP-CLI を組み合わせて自律実行するワークフローを構築
- **GitHub Actions × AI レビュー**: PR に対して AI がセキュリティチェックを実行する CI を設計

#### 実績例
- クチコミ生成 SaaS「Rissun」: Gemini API（2.0 Flash / 2.5 Flash Lite）でアンケート→クチコミ文生成。Sub-Agent 運用ルールを案件レベルで標準化
- 海外マーケ X 自動投稿 MVP「KaigaiMarkeStudio」: Claude Agent SDK で 3 エージェント協調パイプラインを設計（Reddit / RSS 収集 → Research → Writer → Critic → n8n 連携予約投稿）
- WordPress 案件群（GrandPyramid / TourGator / Japan Documented）: CLAUDE.md による WPCS 準拠の自律開発フロー、Docker × AI-CLI 連携の整備

### 🌐 バックエンド開発 **4年の実務経験**
- **Go**: Echo, PostgreSQL, Redis, RabbitMQ使用のマイクロサービス開発
- **Ruby on Rails**: Webアプリケーション開発・保守
- **Python/Django**: データ分析Webアプリケーション開発
- **実績例**:
  - フィンテック決済システムのAPI開発
  - チェーン店向け業務システムの保守・運用

### ☁️ インフラ・DevOps
- **コンテナ技術**: Docker, Kubernetes
- **CI/CD**: Bitrise, GitHub Actions, Jenkins, Vercel 自動デプロイ
- **クラウド**: Vercel, Supabase, Firebase, Heroku, Google Play Console
- **データベース**: PostgreSQL, MySQL, Oracle, Redis

### 🔧 その他の技術経験
- **ブロックチェーン**: Ethereum, Solidity, IPFS（1年）
- **データ分析**: VBA, Oracle Database
- **.NET**: VB.NET業務システム開発

## 🎯 対応可能な案件・サービス

### モバイルアプリ開発
- ✅ Android・Flutterアプリの新規開発
- ✅ 既存アプリの機能追加・改修
- ✅ UI/UX改善・パフォーマンス最適化
- ✅ ストア申請・リリース管理
- ✅ 技術的負債の解消・リファクタリング

### バックエンド・API開発
- ✅ REST API・GraphQL APIの設計・開発
- ✅ マイクロサービスアーキテクチャの構築
- ✅ データベース設計・最適化
- ✅ CI/CD環境の構築・改善

### 技術コンサルティング・レビュー
- ✅ アーキテクチャ設計の相談・レビュー
- ✅ コードレビュー・品質改善提案
- ✅ 技術選定のアドバイス
- ✅ チーム開発体制の構築支援

### AI 駆動開発の導入支援
- ✅ Claude Code / Gemini CLI を用いた開発フローの導入・運用設計
- ✅ プロジェクト固有 **CLAUDE.md**（セキュリティ制約・規約・環境前提）の設計と運用定着
- ✅ Sub-Agent 分業ルール（広域調査=Gemini ／ 実装=Claude）の整備
- ✅ Claude Agent SDK を用いたマルチエージェント・アプリケーションの設計・実装
- ✅ Prompt Caching・モデル使い分け（Sonnet / Opus / Gemini Flash）による API コスト最適化
- ✅ WordPress × AI-CLI（Docker + WP-CLI）連携環境の構築

## 💡 強み・特徴

### 🔄 フルスタック対応力
モバイルからバックエンドまで一貫した開発が可能で、プロジェクト全体を俯瞰した最適な提案ができます。

### 📈 ビジネス視点での開発
出前館やN予備校など、実際のユーザーを持つサービスでの開発経験により、ビジネス価値を意識した開発アプローチが得意です。

### 🎓 指導・育成経験
インターン生の指導やTECH::CAMPでのメンター経験があり、技術的な説明や提案を分かりやすく伝えることができます。

### ⚡ 迅速な学習・適応力
新しい技術やフレームワークへの習得が早く、プロジェクトの要求に応じて柔軟に対応できます。

### 🤖 AI を「現場で運用」できる実践力
Claude Code・Gemini CLI・Claude Agent SDK を本業／副業の両方で日常的に運用しています。単なる利用者ではなく、**CLAUDE.md によるルールエンジン整備・Sub-Agent 分業ルール策定・Prompt Caching でのコスト圧縮**まで含めて運用設計しており、AI を「現場のエンジニアリングパートナー」として安全に組み込むノウハウを提供できます。

## 📞 お仕事のご相談について

### 対応可能時間
- **平日夜間**: 19:00〜22:00
- **土日祝日**: 9:00〜18:00
- ※ 急ぎの案件の場合は調整可能です

### 希望単価・期間
- **時間単価**: 3,000円〜5,000円（案件内容により調整）
- **月額**: 10万円〜30万円（稼働時間により調整）
- **短期集中**: 1週間〜の短期案件も対応可能

### コミュニケーション
- Slack、Chatwork、Teams等のツール対応
- 週1〜2回の定期MTG参加可能
- リモート開発・チーム開発に慣れています

## 🎯 理想的な案件

1. **技術的チャレンジのあるプロジェクト**
2. **ユーザー価値を重視するサービス開発**
3. **長期的な関係性を築けるクライアント様**
4. **チーム開発でのスキル向上機会**

## 📱 お気軽にご相談ください

技術的な課題解決から新規開発まで、幅広くサポートいたします。  
まずはお気軽にメッセージをお送りください。

**連絡先**: [Twitter DM](https://twitter.com/gorillaz815)

---

*最後までお読みいただき、ありがとうございました。  
クライアント様のプロジェクト成功に向けて、全力でサポートさせていただきます！*
