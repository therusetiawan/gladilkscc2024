# Gladi LKS Cloud Computing 2024

Repository ini merupakan aplikasi berbasis web yang digunakan untuk seleksi gladi LKS 2024 bidang Cloud Computing.

```
   ...    *    .   _  .
*  .  *     .   * (_)   *
  .      |*  ..   *   ..
   .  * \|  *  ___  . . *
*   \/   |/ \/{o,o}     .
  _\_\   |  / /)  )* _/_ *
      \ \| /,--"-"---  ..
_-----`  |(,__,__/__/_ .
       \ ||      ..
        ||| .            *
        |||
lkscc   |||
  , -=-~' .-^- _
```

## Requirements
 - [v8.1+](https://www.php.net/)
 - [Composer v2](https://yarnpkg.com/en/docs/install)

## Getting started
### Clone the repo:
```bash
git clone --depth 1 https://github.com/therusetiawan/gladilkscc2024
cd gladilkscc2024
rm -rf .git
```

### Set environment variables:
```bash
cp .env.example .env
```

### Set key:
```bash
php artisan key:generate
```

### Set database on .env (fill your AWS database config):
```bash
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=
DB_USERNAME=
DB_PASSWORD=
```

### Set S3 on .env (fill your AWS S3 config):
```bash
AWS_ACCESS_KEY_ID=
AWS_SECRET_ACCESS_KEY=
AWS_DEFAULT_REGION=ap-southeast-1
AWS_BUCKET=
AWS_USE_PATH_STYLE_ENDPOINT=false
```

### Set SQS on .env (fill your AWS SQS config):
```bash
QUEUE_DRIVER=sqs
QUEUE_CONNECTION=sqs
SQS_KEY=<aws_access_key_id>
SQS_SECRET=<aws_secret_access_key>
SQS_QUEUE=<queue_name>
SQS_REGION=ap-southeast-1
SQS_PREFIX=https://sqs.ap-southeast-1.amazonaws.com/<aws_account_id>
```

### Install dependencies:
```bash
composer install
```

### Database migration and seed:
```bash
php artisan migrate
```

### Running locally (in personal computer):
```bash
php artisan serve --host=0.0.0.0
```

## License and Copyright

The Laravel framework is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).
