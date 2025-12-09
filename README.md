<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400" alt="Laravel Logo"></a></p>

<p align="center">
<a href="https://github.com/laravel/framework/actions"><img src="https://github.com/laravel/framework/workflows/tests/badge.svg" alt="Build Status"></a>
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

Laravel has the most extensive and thorough [documentation](https://laravel.com/docs) and video tutorial library of all modern web application frameworks, making it a breeze to get started with the framework. You can also check out [Laravel Learn](https://laravel.com/learn), where you will be guided through building a modern Laravel application.

If you don't feel like reading, [Laracasts](https://laracasts.com) can help. Laracasts contains thousands of video tutorials on a range of topics including Laravel, modern PHP, unit testing, and JavaScript. Boost your skills by digging into our comprehensive video library.

## Laravel Sponsors

We would like to extend our thanks to the following sponsors for funding Laravel development. If you are interested in becoming a sponsor, please visit the [Laravel Partners program](https://partners.laravel.com).

### Premium Partners

- **[Vehikl](https://vehikl.com)**
- **[Tighten Co.](https://tighten.co)**
- **[Kirschbaum Development Group](https://kirschbaumdevelopment.com)**
- **[64 Robots](https://64robots.com)**
- **[Curotec](https://www.curotec.com/services/technologies/laravel)**
- **[DevSquad](https://devsquad.com/hire-laravel-developers)**
- **[Redberry](https://redberry.international/laravel-development)**
- **[Active Logic](https://activelogic.com)**

## Contributing

Thank you for considering contributing to the Laravel framework! The contribution guide can be found in the [Laravel documentation](https://laravel.com/docs/contributions).

## Code of Conduct

In order to ensure that the Laravel community is welcoming to all, please review and abide by the [Code of Conduct](https://laravel.com/docs/contributions#code-of-conduct).

## Security Vulnerabilities

If you discover a security vulnerability within Laravel, please send an e-mail to Taylor Otwell via [taylor@laravel.com](mailto:taylor@laravel.com). All security vulnerabilities will be promptly addressed.

## License

The Laravel framework is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).

# 📘 回答問題

## a. app1 專案定義了哪些命名空間 (name space)，命名空間的基底目錄各為何？

| Namespace                 | 基底目錄               |
|---------------------------|-------------------------|
| `App\\`                   | `app/`                  |
| `Database\\Factories\\`   | `database/factories/`   |
| `Database\\Seeders\\`     | `database/seeders/`     |
| `Tests\\`                 | `tests/`                |

---

## b. app1 專案預定安裝那些必需（require）的套件&版本，以及 app1 專案開發過程必需（require-dev）的套件&版本。

### require
```json
"require": {
    "php": "^8.2",
    "laravel/framework": "^11.0",
    "guzzlehttp/guzzle": "^7.8"
}
```
## 套件用途說明

| 套件名稱             | 版本  | 用途（補充解釋） |
|----------------------|--------|------------------|
| **php**              | ^8.2   | Laravel 11 的最低執行版本。此欄位指定 PHP 的語言版本，確保專案無法在過舊的 PHP 版本上執行。 |
| **laravel/framework** | ^11.0  | Laravel 的核心框架，提供 MVC、Routing、Middleware、Eloquent ORM、Queue、Mail、Validation 等核心功能，是整個專案的基礎。 |
| **guzzlehttp/guzzle** | ^7.8   | 最常用的 PHP HTTP client，用於發送 API 請求，例如串接外部服務（Line API、金融 API 或任何 REST API）。Laravel 內部部分功能也使用 Guzzle。 |

### require-dev
```json
"require-dev": {
    "laravel/pint": "^1.0",
    "phpunit/phpunit": "^10.0",
    "fakerphp/faker": "^1.9.1"
}
```
## 套件用途說明

| 套件名稱             | 版本    | 用途（補充解釋） |
|----------------------|---------|------------------|
| **laravel/pint**     | ^1.0    | Laravel 官方提供的 PHP 程式碼格式化工具，用於自動排版程式碼，維持團隊一致的 coding style。 |
| **phpunit/phpunit**  | ^10.0   | Laravel 內建的單元測試框架，用於撰寫並執行測試。因為部署到正式環境後不需要，所以是 dev 套件。 |
| **fakerphp/faker**   | ^1.9.1  | 用來產生假資料（如姓名、電話、地址），常用於 seeding 或測試環境。正式上線環境不會使用。 |

---

## c. 請試著找出 laravel/framework 及 guzzlehttp/guzzle 兩個套件在 app1 專案當中的位置。

| 套件                | 路徑                               |
|---------------------|-------------------------------------|
| `laravel/framework` | `vendor/laravel/framework/`          |
| `guzzlehttp/guzzle` | `vendor/guzzlehttp/guzzle/`          |

---

## d. 在 composer.lock 檔案當中 packages 區域，分別找出 laravel/framework 及 guzzlehttp/guzzle 兩個套件，請分別寫出上述兩個套件的真正安裝的版本、原始碼或網站的 URL、以及各自相依那些套件。（請自行與這兩個套件的 composer.json 的內容比較）

### ① laravel/framework

- **實際安裝版本：** `v10.49.1`
- **原始碼網址：** https://github.com/laravel/framework.git

```json
"require": {
    "brick/math": "^0.9.3|^0.10.2|^0.11|^0.12",
    "composer-runtime-api": "^2.2",
    "doctrine/inflector": "^2.0.5",
    "dragonmantank/cron-expression": "^3.3.2",
    "egulias/email-validator": "^3.2.1|^4.0",
    "ext-ctype": "*",
    "ext-filter": "*",
    "ext-hash": "*",
    "ext-mbstring": "*",
    "ext-openssl": "*",
    "ext-session": "*",
    "ext-tokenizer": "*",
    "fruitcake/php-cors": "^1.2",
    "guzzlehttp/uri-template": "^1.0",
    "laravel/prompts": "^0.1.9",
    "laravel/serializable-closure": "^1.3",
    "league/commonmark": "^2.2.1",
    "league/flysystem": "^3.8.0",
    "monolog/monolog": "^3.0",
    "nesbot/carbon": "^2.67",
    "nunomaduro/termwind": "^1.13",
    "php": "^8.1",
    "psr/container": "^1.1.1|^2.0.1",
    "psr/log": "^1.0|^2.0|^3.0",
    "psr/simple-cache": "^1.0|^2.0|^3.0",
    "ramsey/uuid": "^4.7",
    "symfony/console": "^6.2",
    "symfony/error-handler": "^6.2",
    "symfony/finder": "^6.2",
    "symfony/http-foundation": "^6.4",
    "symfony/http-kernel": "^6.2",
    "symfony/mailer": "^6.2",
    "symfony/mime": "^6.2",
    "symfony/process": "^6.2",
    "symfony/routing": "^6.2",
    "symfony/uid": "^6.2",
    "symfony/var-dumper": "^6.2",
    "tijsverkoyen/css-to-inline-styles": "^2.2.5",
    "vlucas/phpdotenv": "^5.4.1",
    "voku/portable-ascii": "^2.0"
}
```

---

### ② guzzlehttp/guzzle

- **實際安裝版本：** `7.10.0`
- **原始碼網址：** https://github.com/guzzle/guzzle.git

```json
"require": {
    "ext-json": "*",
    "guzzlehttp/promises": "^2.3",
    "guzzlehttp/psr7": "^2.8",
    "php": "^7.2.5 || ^8.0",
    "psr/http-client": "^1.0",
    "symfony/deprecation-contracts": "^2.2 || ^3.0"
}
```

---

## e. 請分別找出 laravel/framework 及 guzzlehttp/guzzle 兩個套件定義了哪些命名空間（name space），命名空間的基底目錄各為何？ 

### 查詢方式
可透過查看各套件的 `composer.json` 中 `autoload > psr-4` 區段取得 namespace 與基底目錄對應。

### 結果整理

| 套件                | Namespace（主要命名空間） | 基底目錄（PSR-4 對應）                               | 補充說明 |
|---------------------|----------------------------|--------------------------------------------------------|----------|
| laravel/framework   | `Illuminate\`              | `vendor/laravel/framework/src/Illuminate/`            | 在 composer.json 中透過 `"Illuminate\\": "src/Illuminate/"` 定義，Laravel 所有核心元件皆位於此命名空間下。 |
| guzzlehttp/guzzle   | `GuzzleHttp\`              | `vendor/guzzlehttp/guzzle/src/`                       | composer.json 透過 `"GuzzleHttp\\": "src/"` 指派，對應 HTTP client 相關類別。 |

---

## f. 請開啟 app1 專案當中的 AppServiceProvider 類別，位於 /app/HTTP/Providers/AppServiceProvider.php，請說出此類別在怎樣的 namespace 當中。

檔案位置：

```
app/Http/Providers/AppServiceProvider.php
```

命名空間：

```php
namespace App\Providers;
```

---

## g. 上述 Controller 類別使用（use）了哪些其他命名空間的類別，你可以找出這些類別在那個套件、以及套件當中的位置（找到後可開啟他們的程式碼欣賞一下）。（提示；滑鼠移動到那些類別，Phpstorm 會提示你）

```php
namespace App\Http\Controllers;

use Illuminate\Foundation\Auth\Access\AuthorizesRequests;
use Illuminate\Foundation\Validation\ValidatesRequests;
use Illuminate\Routing\Controller as BaseController;
```

| 類別名稱                     | 套件來源           | 路徑 |
|------------------------------|--------------------|------|
| `AuthorizesRequests`         | laravel/framework | `vendor/laravel/framework/src/Illuminate/Foundation/Auth/Access/` |
| `ValidatesRequests`          | laravel/framework | `vendor/laravel/framework/src/Illuminate/Foundation/Validation/` |
| `Illuminate\Routing\Controller` | laravel/framework | `vendor/laravel/framework/src/Illuminate/Routing/Controller.php` |