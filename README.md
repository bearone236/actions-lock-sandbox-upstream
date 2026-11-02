# actions-lock-sandbox-upstream

[actions-lock-sandbox](https://github.com/bearone236/actions-lock-sandbox) で使う「上流の action」役のリポジトリです。
タグを force push で書き換えて、タグ改ざん型のサプライチェーン攻撃を再現するために使います。
ここで "COMPROMISED" と表示するコードは文字列を出力するだけで、secret の読み出しや外部送信はしません。

- `setup-tool/`: ツールをインストールする action の役（内側の依存）
- `scanner/`: 内部で `setup-tool@v1.0.0` を使う action の役（外側。trivy-action と setup-trivy の関係を模したもの）
