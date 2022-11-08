Url: https://laravel.com/docs/9.x/passport

Video: https://www.youtube.com/watch?v=aVynhiqeft4&ab_channel=ImproveProgrammingLogic

Git: https://github.com/silvicardo/laravel-passport-react
https://github.com/codeimprove0/laravel-8

Command:
php artisan key:generate

//cache clear
php artisan optimize

//cache clear
php artisan optimize:clear

//create server
php artisan serve

//cache clear
php artisan route:clear

//creat controller
php artisan make:controller PostController

//create table
php artisan make:migration create_patients_table

//drop table
php artisan migrate:rollback --path=/database/migrations/2022_09_22_113520_create_tests_table.php

//add new field to table
php artisan make:migration add_marital_status_to_patients_table --table=patients

public function up()
{
    Schema::table('users', function($table) {
        $table->integer('paid');
    });
}

public function down()
{
    Schema::table('users', function($table) {
        $table->dropColumn('paid');
    });
}

php artisan migrate

//git
git add .
git commit -m "Patient Form Added"
git push

Client ID: 1
Client secret: Axmwl60GlGL5ub2zIkiOlp5Xww1TYLZdxFGUDp8M
Password grant client created successfully.
Client ID: 2
Client secret: cUrqnBIjg84Nd1YIIuWx70RLd631L0zHFidOmLgc
