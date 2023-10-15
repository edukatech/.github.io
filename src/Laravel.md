# Laravel

## Crear proyecto
composer create-project laravel/laravel nombre-app

## Iniciar servidor
php artisan serve

## crear migracion la BD
php artisan make:migration Tabla  *crea la tabla individual laravel*

*Luego se ingresan los campos respectivos se usan estos códigos*
Schema-table
@table
    engine para actualizar en cascada
    bigIncrements clave principal
    string
    bigInteger('fk_catg')->unsigned(); *clave foránea*

Foreign *crear la relación de la clave foránea*

php artisan migrate *Crea la migración de las tablas a las DB*

php artisan migrate:fresh *para refrescar la migración*

Nota: Cuando se vaya a crear un combobox primero se crea la tabla principal y luego la que contiene la clave foránea

## Crear interfaces

### Login
composer require laravel/ui  *Autenticación Login integrar*

php artisan ui bootstrap --auth *crear elementos de autenticación*

npm install *se usa para compilar identificar elementos para la interfaz*
npm run dev

### Instrucciones para integrar los Crud 
composer require ibex/crud-generator --dev *herramienta para crear el crud para hacer la integración*

php artisan vendor:publish --tag=crud *instrucción para registrar y publicar*

### Instrucciones para crear los Crud de las tablas 
php artisan make:crud tablas

## Integrar interfaces
Para  integración de las interfaces se usa

El comando Route para determinar hacia donde se tiene que ir para dar la respuesta

Route::resource('libros', App\Http\Controllers\LibroController::class)->middleware('auth'); // middleware hacer solo cuando está autenticado
