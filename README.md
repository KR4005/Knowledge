# README

## イントロダクション

日々学んだことや作業の記録を残していく

## 特徴

- 効率的に管理
  - 緊急性と重要性に基づいてメモを分類し、優先順位を明確。その結果、重要なタスクに集中しやすくなり、必要な情報を迅速に見つけられるため、作業にも大きく効果をもたらす。
- メモをもっと活用
  - メモを単なる情報保管だけでなく、積極的に活用することに意義を持ち、メモを取る際には、その活用方法を考え、現状の行動にプラスになるか、関心や必要性があるかどうかを常に判断しそのことで、メモして終わりではなく、必要な動機として活用に繋がる
- メモツールに依存しない
  - PARAメソッドは方法論であり、特定のツールに縛られることはなく、(NotionやEvernoteなど)、普段使っているツールから容易に導入が可能。

## 運用

以下のルールに基づいてファイル及びディレクトリを管理する

### 00_Project

- 概要: 明確な目標と期限がある一時的な活動
  - 新しいLinuxサーバーのセットアップ手順の作成
  - Gitのベストプラクティスに関するガイドの作成
  - 特定のプロジェクトで使用するスクリプトの開発

### 01_Area

- 概要: 継続的に管理する必要がある責任領域
  - 継続的なLinuxの学習
  - Gitの操作に関するトレーニング
  - 定期的なツールやコマンドの更新とメンテナンス

### 02_Resource

- 概要: プロジェクトやエリアに直接関連しないが、将来的に役立つ可能性のある参考資料
  - Linuxコマンドリファレンス
  - Gitのチュートリアルやドキュメント
  - よく使うスクリプトや設定ファイルのサンプル

### 03_Archive

- 概要: 完了したプロジェクトや不要になったリソースの保管場所
  - 完了したLinuxのセットアップ手順
  - 古いGitプロジェクトのドキュメント
  - 使わなくなったスクリプトや設定ファイル

## 実際のフォルダ構造の例

```text
PARA/
├── Projects/
│   ├── Linux Setup Guide/
│   │   ├── README.md
│   │   └── setup_steps.md
│   ├── Git Best Practices/
│   │   ├── README.md
│   │   └── best_practices.md
│   └── Script Development/
│       ├── README.md
│       └── scripts/
├── Areas/
│   ├── Linux Learning/
│   │   ├── basics.md
│   │   └── advanced.md
│   ├── Git Training/
│   │   ├── basics.md
│   │   └── advanced.md
│   └── Tool Maintenance/
│       ├── updates.md
│       └── tools_list.md
├── Resources/
│   ├── Linux Reference/
│   │   ├── commands.md
│   │   └── tips.md
│   ├── Git Tutorials/
│   │   ├── beginner.md
│   │   └── advanced.md
│   └── Sample Scripts/
│       ├── script1.sh
│       └── script2.sh
└── Archives/
    ├── Completed Linux Guides/
    │   ├── setup_guide_v1.md
    │   └── setup_guide_v2.md
    ├── Old Git Documents/
    │   ├── best_practices_2019.md
    │   └── training_2020.md
    └── Deprecated Scripts/
        ├── old_script1.sh
        └── old_script2.sh

```

## 各フォルダの詳細

- Projects (プロジェクト)
  - 各プロジェクトごとにフォルダを作成し、その中に関連するドキュメントやファイルをまとめます。プロジェクトが完了したら、Archivesフォルダに移動
- Areas (エリア)
  - 継続的に学習や管理が必要な分野に関する情報を整理。例えば、LinuxやGitに関する学習資料やメンテナンス情報を保存
- Resources (リソース)
  - 直接的なプロジェクトやエリアには関連しないが、将来的に役立つ可能性のある資料やサンプルを保存。参考になるリファレンスやチュートリアル、サンプルスクリプトなどがここに含まれます。
- Archives (アーカイブ)
  - 完了したプロジェクトや不要になったリソースを保管。将来的に参照する可能性があるため、ここに保存
