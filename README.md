# くさのねっと
懐かしの90年代ホームページを作成するためのリポジトリです．
レンタルサーバーを見つけるまでの間はdocker上の仮想環境で動作確認予定です．

# ページ構成
```
|-nginx: リバースプロキシサーバ
| |-Dockerfile: nginxコンテナ構成用ファイル
| |_conf.d
|   |_default.conf: どこのポート開けるとか記述したファイル
|
|-www
| |-iamge: imageフォルダ
| |_index.html: アクセスページ
|
|-docker-compose.yml: docker起動用yamlファイル
|_README.md: こ れ
```

# 起動方法
macOS(unix系OSなら同じだと思う)を使用している前提で書きます．
1. コンテナをビルドする
```
cd kusano_net
docker-compose build
```
2. コンテナをうpーします
```
docker-compose up -d
# コンテナが立ち上がっているか確認
docker ps
```
3. デフォのままだとブラウザで```localhost```にアクセスすると背景の色が気色悪いページにアクセスできるとおもいます．

# 動作環境
- docker v20.10.6, build 370c289
- docker-compose v1.29.1, build c34c88b2
- Firefox Developper Edition

# ありがちなエラー
- CORS error: たぶんクロスドメインとか，あとで対処します
- frame要素を使うなエラー: iframeを使うとページがなんか新しくなる気がするので絶対に使わない予定

# たすけて？
デカ男にdiscordあてにメッセージをおくってください．
