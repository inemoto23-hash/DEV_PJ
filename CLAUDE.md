# SeasonPlay - Android App Development

## プロジェクト概要
Flutter および Android Studio を使用した Android アプリ開発プロジェクト。

## 必須読み込みドキュメント
実装・更新作業の開始前に必ず以下を読み込むこと：
- [90_DOCUMENT/system_architecture.md](90_DOCUMENT/system_architecture.md) — システム全体構成の中核ドキュメント
- [90_DOCUMENT/system_flow.md](90_DOCUMENT/system_flow.md) — システム間の時系列フロー（mermaid図）

実装完了後は必ず両ドキュメントを更新し、鮮度を維持すること。
更新の際は [.claude/rules/document_hierarchy.md](.claude/rules/document_hierarchy.md) に定義された階層ルール（L1鳥瞰 / L2詳細 / L3定義）に従うこと。

---

## フォルダ構成

```
SeasonPlay/
├── CLAUDE.md                          # 本ファイル
├── .claude/
│   └── plans/                         # 実装計画書
├── 90_DOCUMENT/
│   ├── system_architecture.md         # システム構成中核ドキュメント（必読）
│   ├── system_flow.md                 # システムフロー mermaid 図（必読）
│   ├── 01_開発ドキュメント/           # ソースコード 1 ファイルにつき 1 つの .md
│   ├── 10_DB/
│   │   ├── SQL/                       # SQL ファイル
│   │   ├── クエリ/                    # クエリ定義
│   │   ├── テーブル/                  # テーブル定義
│   │   └── SP/                        # ストアドプロシージャ
│   └── 40_実行手順/                   # ユーザー向け手動実行手順書
└── 91_UPDATE/
    ├── update/                        # アップデート予定内容
    └── update_fix/                    # 完了済みアップデート内容
```

---

## 技術スタック
- **フレームワーク**: Flutter
- **IDE**: Android Studio
- **ターゲット**: Android

## コーディング規約
- Flutter の公式スタイルガイドに準拠
- ファイル名はスネークケース（`my_widget.dart`）
- クラス名はパスカルケース（`MyWidget`）
- コメントは WHY が非自明な場合のみ記述し、WHAT の説明は不要
