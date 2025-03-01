<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400"></a></p>

<p align="center">
<a href="https://travis-ci.org/laravel/framework"><img src="https://travis-ci.org/laravel/framework.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/dt/laravel/framework" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/v/laravel/framework" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/l/laravel/framework" alt="License"></a>
</p>

## About Laravel

Laravel is a web application framework with expressive, elegant syntax. We believe development must be an enjoyable and creative experience to be truly fulfilling. Laravel takes the pain out of development by easing common tasks used in many web projects, such as:

- [Simple, fast routing engine](https://laravel.com/docs/routing).
- [Powerful dependency injection container](https://laravel.com/docs/container).
- Multiple back-ends for [session](https://laravel.com/docs/session) and [cache](https://laravel.com/docs/cache) storage.
- Expressive, intuitive [database ORM](https://laravel.com/docs/eloquent).
- Database agnostic [schema migrations](https://laravel.com/docs/migrations).
- [Robust background job processing](https://laravel.com/docs/queues).
- [Real-time event broadcasting](https://laravel.com/docs/broadcasting).

Laravel is accessible, powerful, and provides tools required for large, robust applications.

## Learning Laravel

Laravel has the most extensive and thorough [documentation](https://laravel.com/docs) and video tutorial library of all modern web application frameworks, making it a breeze to get started with the framework.

If you don't feel like reading, [Laracasts](https://laracasts.com) can help. Laracasts contains over 1500 video tutorials on a range of topics including Laravel, modern PHP, unit testing, and JavaScript. Boost your skills by digging into our comprehensive video library.

## Laravel Sponsors

We would like to extend our thanks to the following sponsors for funding Laravel development. If you are interested in becoming a sponsor, please visit the Laravel [Patreon page](https://patreon.com/taylorotwell).

### Premium Partners

- **[Vehikl](https://vehikl.com/)**
- **[Tighten Co.](https://tighten.co)**
- **[Kirschbaum Development Group](https://kirschbaumdevelopment.com)**
- **[64 Robots](https://64robots.com)**
- **[Cubet Techno Labs](https://cubettech.com)**
- **[Cyber-Duck](https://cyber-duck.co.uk)**
- **[Many](https://www.many.co.uk)**
- **[Webdock, Fast VPS Hosting](https://www.webdock.io/en)**
- **[DevSquad](https://devsquad.com)**
- **[OP.GG](https://op.gg)**

## Contributing

Thank you for considering contributing to the Laravel framework! The contribution guide can be found in the [Laravel documentation](https://laravel.com/docs/contributions).

## Code of Conduct

In order to ensure that the Laravel community is welcoming to all, please review and abide by the [Code of Conduct](https://laravel.com/docs/contributions#code-of-conduct).

## Security Vulnerabilities

If you discover a security vulnerability within Laravel, please send an e-mail to Taylor Otwell via [taylor@laravel.com](mailto:taylor@laravel.com). All security vulnerabilities will be promptly addressed.

## License

The Laravel framework is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).

# アプリケーション内容

## アプリケーション名

Code Wiki

## アプリケーション概要

・ユーザー登録

・プログラムのコードの掲載またそのコードの使用方法やその詳細を投稿表ができる

・ボタンを押す事でそこに乗っているコードをコピーする事ができる

## URL

## テスト用アカウント

## 利用方法

・投稿されたコードの使用方法を確認しそのコードをワンクリックでコピーし使用できる

## 目指した課題解決

・独学で学習をしようとした際コードの一覧が纏められていたりその説明がされている辞典のようなサイト存在せずどこを確認すれば良いか分からなかった為ある程度分かり易く簡潔に纏められているサイトが欲しいと感じた為

## 洗い出した要件

| 優先順位（高：3、中：2、低：1） | 機能                | 目的                                                       | 詳細                                                     | ストーリー(ユースケース)                            | 見積もり（所要時間） |
| -------------------------- | ------------------- | --------------------------------------------------------- | ------------------------------------------------------ | ----------------------------------------------- | ----------------- |
| ユーザー登録機能              | ユーザー情報の登録     | 投稿されたコードは誰が投稿したかを確認できるようにする為           | 氏名,メールアドレス,パスワードを登録してもらう                              | ユーザー登録画面のフォームに記述してもらう              | ２日               |
| コード等の投稿機能            | コード等の投稿         | ユーザーにコードとその説明を投稿してもらう為                     | コード,使い方,詳細説明を記入してもらう                                    | 専用の投稿画面からログインしているユーザーに記述してもらう | ３日               |
| 投稿内容の一覧機能            | 投稿内容を一覧で表示する | 投稿された内容を一覧で表示し確認できるようにする為                | 投稿内容を一覧で表示し確認する為                                         | 言語別に一覧画面を作成する                           | １日                |
| 投稿コードのコピー            | 投稿コードのコーピー機能 | 投稿されたコードをボタンクリックのみで簡単にコピーできるようにする為 | 表示されたコードの隣にボタンを配置しそれをクリックする事でコピーできるようにする | クリックする事でコピーが可能                          | 1日                |

## 実装した機能についてのGIFと説明

・ユーザー登録機能

・商品投稿機能

・商品一覧機能

・商品コピー機能

## ローカルでの動作方法

PHP     ver 7.3.11
laravel ver 8.15.0

% git clone https://github.com/ryu20010202/codewiki

% cd codewiki

% mysql -u root

CREATE DATABASE `laravel-project`;

% php artisan migrate

# データベース設計

## items

|  Column             | Type       | Options     |
| ------------------- | ---------- | ----------- |
| code                | string     | null: false |
| how                 | string     | null: false |
| explanation         | text       | null: false |
| user                | references | null: false |

### Association

- belongs_to :user

## user

| Column             | Type   | Options     |
| ------------------ | ------ | ----------- |
| email              | string | null: false |
| encrypted_password | string | null: false |
| name               | string | null: false |