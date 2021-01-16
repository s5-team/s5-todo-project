# nodeイメージをpull
FROM node:10.15.3-alpine

# nodeサーバーにおけるワーキングディレクトリの指定
WORKDIR /app

# VueCLIのインストール
RUN npm install -g @vue/cli

# npm run serve の実行（Vueサーバーの起動）もしかしたらこれもいらん？
CMD [ "npm", "run", "serve" ]
