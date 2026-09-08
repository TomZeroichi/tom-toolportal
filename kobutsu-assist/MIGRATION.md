# TOM 古物商申請アシスト — GitHub移行

現在の基準版: **v0.17.2**

## 現行構成
- スマホ入力: GitHub Pages + Supabase同期
- PCヘルパー: PowerShell + ローカルWeb UI
- PDF生成: 岐阜県警の正式PDFを台紙として固定し、入力レイヤーのみ重ねる
- 完成PDF: PCの `output` フォルダへ保存

## GitHub運用方針
- 開発は `dev` 相当ブランチで実施
- 実機確認後のみ `main` へ反映
- 正式PDFの罫線・太枠・細枠・印字文字・余白・A4サイズは変更しない
- Word / Excelで申請書自体を再構築しない
- スマホ入力データはSupabaseで同期し、秘密情報や利用者データはGitHubへ保存しない

## 専用リポジトリ移行予定
最終移行先: `TomZeroichi/kobutsu-assist`

専用リポジトリ作成後、v0.17.2のPCヘルパー・Web UI・モバイル画面・PDF座標設定をソース単位で移管する。
