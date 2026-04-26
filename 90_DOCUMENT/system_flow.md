# System Flow

> **注意**: このドキュメントはシステム間の時系列的な繋がりを mermaid 図で表記します。
> `system_architecture.md` と同列に扱い、実装・変更のたびに必ず更新すること。

最終更新: 2026-04-26

---

## アプリ起動フロー

> 実装が進むにつれて更新すること。

```mermaid
flowchart TD
    A([アプリ起動]) --> B[初期化処理]
    B --> C{認証状態確認}
    C -->|未認証| D[ログイン画面]
    C -->|認証済み| E[メイン画面]
    D --> F[認証処理]
    F --> E
```

---

## 画面遷移フロー

```mermaid
flowchart LR
    Login[ログイン画面] --> Main[メイン画面]
    Main --> Detail[詳細画面]
    Main --> Setting[設定画面]
```

> 画面が増えるたびに追記すること。

---

## データフロー

```mermaid
flowchart TD
    UI[UI Layer] --> VM[ViewModel / Controller]
    VM --> Repo[Repository]
    Repo --> Remote[Remote DataSource]
    Repo --> Local[Local DataSource]
    Remote --> API[外部 API]
    Local --> DB[ローカル DB / SharedPreferences]
```

> アーキテクチャが確定したら実際の構成に合わせて更新すること。

---

## 変更履歴

| 日付 | 変更内容 | 更新者 |
|------|---------|--------|
| 2026-04-26 | 初版作成（プレースホルダー） | Claude |
