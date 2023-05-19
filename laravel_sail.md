## 実行
```
npm run dev
```
## Laravel sail Install　方法 & Docker

https://biz.addisteria.com/01laravel_sail/

```
wsl --install
```

インストールできたかチェック

```
wsl --list --verbose
```


## Ubuntu Delete　方法


https://xtech.nikkei.com/atcl/nxt/column/18/01863/112600004/

```
wsl --unragister Ubuntu
```


## Laravelプロジェクトの作成

```
sudo curl -s https://laravel.build/test-app | bash
cd test-app && ./vendor/bin/sail up -d
```


## Sailをやめるとき

```
./vendor/bin/sail stop
```

## ポートが使用中の時

Docker-compose.ylmファイルの
mysqlのポート番号を変更する


## Reactで使用するとき


LaravelでReactを使用するには、 `laravel-mix` と呼ばれるnpmパッケージをインストールする必要があります。これは、フロントエンド開発用のビルドツールです。

1.まず、新しいLaravelアプリケーションを作成します：

```
laravel new my-app
```

2.`cd` コマンドを使って、新しいLaravelアプリケーションのディレクトリに移動します。

```
cd my-app
```

3.`laravel-mix` をインストールします。

```
npm install laravel-mix react react-dom babel-preset-react --save-dev
```

4.`webpack.mix.js` ファイルを作成し、次のように記述します。

```javascript
let mix = require('laravel-mix');
mix.react('resources/js/app.js', 'public/js');
```

5.`resources/js` ディレクトリに、 `app.js` ファイルを作成します。

6.`app.js` ファイルに、必要なReactコードを記述してください。

7.`npm run dev` コマンドを実行し、Laravel Mixを使用してReactアプリケーションをビルドします。

8.Laravelサーバーを起動し、 `http://localhost:8000` にアクセスすると、Reactアプリケーションが表示されます。

以上の手順で、LaravelアプリケーションにReactを統合して、Reactコンポーネントをビルドおよびレンダリングすることができます。

