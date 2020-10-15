# EasyPHP4 For Japanese


<p align="center">
   <img src="https://raw.githubusercontent.com/Tokyo-Lei/EasyPHP4/master/Public/Home/img/logo.png">
</p>
<p align="center">
  すみません、日本のPHPです!
</p>

<p align="center">
<img src="https://img.shields.io/badge/version-4.0.0-green.svg">
<img src="https://img.shields.io/badge/php-7+-brightgreen.svg">
<img src="https://img.shields.io/badge/mysql-5+-orange.svg">
<img src="https://img.shields.io/badge/license-MIT-blue.svg">
</p>



## 概要

EasyPHP Fraamewark 4は、快速開発のためのフレームワークであり、compserに基づいて開発された第4世代PHP MVCフレームです。

このフレームは中国で有名なThinkPHPフレームの思想で開発されました。

フレームはMVCのデザインを採用しています。初心者には難しいです。

将来はそれぞれの応用シーンに対して抱生します。例えば、日本語ブログ、文章CMSなどのプログラムです。



## 設置環境


-PHP：7.0以上
-Compser：2.0 RC-1
-PSR標準：PSR-4
-バックグラウンドスタイルは、boots watch liter aに基づいています。

  

## 協議の説明

-本コードのオープンソースはMITプロトコルに従う。
-一部コードCOMPOSERとクラスソースの第三者。

```
Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE
```


## ディレクトリ構造
```php
App
   |- admin          //バックグラウンドディレクトリ
        |-controller //コントローラ
             |-conn  //コントローラフォルダの設定
             |-index //バックグラウンドトップコントローラフォルダ
             |-user  //ユーザコントローラフォルダ
         |- model    //モデル
             |-UserModel.php //ユーザーモデル
         |- view     //表示
             |- article //記事ビューフォルダ
             |- conn    //ビューフォルダの設定
             |- include //ページの端、フッター、ナビゲーションなどのビューフォルダ
             |- index   //后バックグラウンドトップビューフォルダ
             |- user    //ユーザ登録等のビューフォルダ
   |-	home              //フロントディレクトリ
         |-controller     //フロントコントローラ
             |-HomeController.php    //フロントコントローラ
         |- model        //フロントモデル
         |- templates    //フロントテンプレート
         |- member       //フロントユーザーセンター
   |- config  //フォルダの設定
   |- file    //キャッシュフォルダ
   |- library //クラス
   |-	Bootstrap.php  //主体コアファイル
   |- Router.php     //ルート
Public
   | - index.php     //PPHP起動ファイル
vendor               //composerサードパーティのフォルダ

```



## 使用安装


- 直接ソースcompserをダウンロードして、第三者倉庫をインストールします。

```php
composer install
```

- データベースの設定

データベーステーブル

ユーザー名とパスワードはそれぞれ`admin`です。

- 直接compserインストール

```php
composer require tokyo-lei/easyphp4
```



## 开发手册

すべてのPHPファイル名は、ラクダピーク法（イニシャル大文字）で、ファイルディレクトリは小文字です。

#### 1.0简単なハローワールドを创建します！

第一歩：appディレクトリの下でhomeファイルはフロントモジュールで、app/home/controller/フォルダを開けて作成します。IndexController.phpファイル

コードは以下の通りです：

```
<?php
namespace App\home\controller;
class IndexController {
    public function index() {
       echo 'Hello World ';
    }
}
```

第二ステップ：ルートを設定し、ap/Router.phpファイル

コードは以下の通りです：

```
Route::get('/', 'App\Home\Controller\IndexController@index');
```

最後にブラウザを入力すればいいです。



## コンポーネントを導入

- Twig      テンプレートエンジン
- medoo     データベースフレーム
- macaw     ルート
- validate  Thinkphp検証
- whoops    エラーメッセージ
- monolog   ログ
- qr-code   QR生成
- upload    アップロード
- Tinymce   エディタ



## バージョンの更新

- 令和9月15日に新たな枠組みを開発する予定です。
- 令和9月21日に本体アーキテクチャを完成する
- 令和9月22日にwhouss、qr-codeを追加します。
- 令和9月23日にバックグラウンドを追加し、ThinkPHP-authを削除し、Authライブラリを追加し、コアを修正する。
- 令和9月24日にユーザーグループ管理、ajax提出、validate検証ルールを追加する。
- 令和10月09日に検証コードを修正し、バックグラウンドの簡単なsession検証、アップロードクラス、Tinymce 5エディタを追加します。
- 令和10月10日にバックグラウンドデータの設定を追加し、キャッシュを削除し、快速に作成する
- 令和10月11日フレーム主体完成
- 令和10月12日4.0.1最適化部分コード
