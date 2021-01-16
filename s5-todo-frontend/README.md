# s5-todo-frontend Vue CLIをdocker上で動作させる方法

## 1. Dockerfileからdockerイメージをビルド
`docker-compose build vue-app`

## 2. docker-composeをデタッチモードで実行
`docker-compose up -d`

## 3. 全コンテナのプロセスを確認。`vuecli3`コンテナが起動していることを確認。
1. `docker ps -a`を実行
2. `NAMES`が`vuecli3`であるコンテナの`STATUS`が`UP`になっていること

## 4. `vuecli3`コンテナにアタッチ
`docker exec -it vuecli3 sh`

## 5. Vueサーバーの起動
`npm run serve`

## 6. 動作確認
`http://localhost:8080`へアクセス。(localhostの部分は環境によって変化する）

### 参考資料
https://qiita.com/rh_taro/items/ca08b930f704275286a4#docker-composeyml%E3%82%92%E7%94%A8%E6%84%8F%E3%81%99%E3%82%8B
