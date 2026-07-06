# study-planner

日次学習ToDoビュワー。GitHub Pagesでホストし、Supabase RESTからその日のToDoをライブ取得・チェックで実績を書き戻す。

- データ: Supabase `study.study_todo`（`public.study_todo_view` 経由・security_invoker）
- アクセス制御: RLSで `x-family-key` ヘッダーを検証（鍵はURLフラグメント `#k=...` で受け渡し・リポジトリには含めない）
- ToDoの生成・週次更新は管理側リポジトリ（Claude Code）から実施。このリポジトリはビュワーのみ
