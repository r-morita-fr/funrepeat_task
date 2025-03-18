# Simple CRM - 顧客管理システム

シンプルでユーザーフレンドリーな顧客管理システムのフロントエンド実装です。このアプリケーションは、ログイン機能と顧客情報の管理機能を提供します。

![アプリケーションのスクリーンショット](./screenshots/app-overview.png)

## 目次

- [機能概要](#機能概要)
- [セットアップ手順](#セットアップ手順)
- [使用した技術・ライブラリ](#使用した技術ライブラリ)
- [実装した機能の説明](#実装した機能の説明)
- [動作確認方法](#動作確認方法)
- [フォルダ構成](#フォルダ構成)
- [今後の改善点](#今後の改善点)

## 機能概要

このアプリケーションは以下の主要機能を提供します：

- シンプルなログイン画面
- 顧客情報の一覧表示
- 顧客情報の検索機能
- 顧客データの並び替え機能
- レスポンシブデザイン対応

## セットアップ手順

以下の手順でアプリケーションをローカル環境で実行できます。

### 前提条件

- Node.js (v14.0.0 以上)
- npm (v6.0.0 以上)

### インストール

1. リポジトリをクローンします

```bash
git clone https://github.com/yourusername/simple-crm.git
cd simple-crm
```

2. 依存パッケージをインストールします

```bash
npm install
```

3. アプリケーションを起動します

```bash
npm start
```

4. ブラウザで以下のURLにアクセスします

```
http://localhost:3000
```

## 使用した技術・ライブラリ

- **フレームワーク**: React (Create React App)
- **UI ライブラリ**: Material-UI
- **状態管理**: React Context API
- **スタイリング**: Styled Components
- **フォーム管理**: React Hook Form
- **データ処理**: Lodash
- **開発ツール**: ESLint, Prettier

## 実装した機能の説明

### 1. ログイン機能

- ユーザーID・パスワード入力フォーム
- 入力バリデーション（空欄チェック）
- エラーメッセージ表示
- ログイン状態の保持（Context APIで管理）

### 2. 顧客一覧画面

- 顧客情報の表形式での表示
  - 顧客名
  - メールアドレス
  - 電話番号
  - 登録日
  - ステータス
- **検索機能**
  - 顧客名による絞り込み検索
  - リアルタイム検索結果表示
- **並び替え機能**
  - 名前順（昇順・降順）
  - 登録日順（昇順・降順）
- **レスポンシブ対応**
  - スマートフォン向けの最適化表示
  - カード形式の顧客情報表示（モバイル）

### 3. デザイン

- Material-UIを使用した一貫性のあるデザイン
- ライトモード/ダークモード切替対応
- アクセシビリティに配慮したUI設計

## 動作確認方法

### ログイン画面

1. アプリケーションを起動すると、最初にログイン画面が表示されます
2. テスト用アカウントでログインできます：
   - ユーザーID: `admin`
   - パスワード: `password`
3. 入力欄を空にしてログインボタンを押すと、エラーメッセージが表示されます

### 顧客一覧画面

1. ログイン後、自動的に顧客一覧画面に遷移します
2. 画面上部の検索バーに顧客名を入力して、顧客を検索できます
3. カラムヘッダーをクリックすると、そのカラムでデータを並び替えることができます
4. 画面右上のアイコンからダークモードに切り替えることができます
5. ブラウザの幅を狭めると、レスポンシブ対応された表示に自動的に切り替わります

## フォルダ構成

```
src/
├── components/        # 再利用可能なUIコンポーネント
│   ├── Login/         # ログイン関連コンポーネント
│   ├── CustomerList/  # 顧客一覧関連コンポーネント
│   └── UI/            # 汎用UIコンポーネント
├── context/           # React Context定義
├── hooks/             # カスタムHooks
├── data/              # モックデータ
├── utils/             # ユーティリティ関数
├── pages/             # ページコンポーネント
├── styles/            # グローバルスタイル
└── App.js             # アプリケーションのルート
```

## 今後の改善点

- 顧客詳細画面の実装
- フィルタリング機能の拡張
- 顧客データの追加・編集・削除機能
- バックエンドとの連携（API実装）
- ユニットテストの追加
