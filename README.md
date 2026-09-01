# Sistem de Administrare a Conținutului (CMS)

Aplicație web pentru administrarea conținutului (CMS), dezvoltată cu Laravel (PHP) și PostgreSQL, în cadrul modulului S.07.O.022 Asistență pentru programarea server-side a site-urilor Web.

## Descriere

InkBase permite publicarea și administrarea articolelor pe un site web, cu suport pentru categorii, comentarii, autentificare utilizatori și panou de administrare separat de partea publică a site-ului.

## Tehnologii utilizate

| Componentă      | Tehnologie                   |
|------------------|-------------------------------|
| Backend          | Laravel (PHP)                 |
| Bază de date     | PostgreSQL                    |
| Frontend         | Blade, HTML, CSS, JavaScript  |
| Manager pachete  | Composer, NPM                 |

## Etapa 1: Configurarea serverului local

Această etapă corespunde primei unități de învățare din curriculum: Limbaje de programare pentru server-side.

### Cerințe preliminare

- PHP >= 8.1
- Composer
- PostgreSQL >= 13
- Node.js și NPM
- Editor de cod (VS Code, PhpStorm etc.)

### Pași de instalare

1. Instalarea PHP, Composer și PostgreSQL pe calculator

2. Verificarea instalării
   ``` 
   php -v
   composer -V
   psql --version
   ```

3. Crearea proiectului Laravel
   ``` 
   composer create-project laravel/laravel inkbase
   cd inkbase
   ```

4. Configurarea fișierului de mediu
   ``` 
   cp .env.example .env
   php artisan key:generate
   ```

5. Configurarea conexiunii la baza de date PostgreSQL în fișierul `.env`
   ``` 
   DB_CONNECTION=pgsql
   DB_HOST=127.0.0.1
   DB_PORT=5432
   DB_DATABASE=inkbase
   DB_USERNAME=postgres
   DB_PASSWORD=parola_ta
   ```

6. Crearea bazei de date PostgreSQL
   ``` 
   psql -U postgres
   CREATE DATABASE inkbase;
   ```

7. Pornirea serverului local Laravel
   ``` 
   php artisan serve
   ```

Aplicația va fi disponibilă la `http://localhost:8000`.

## Autori

Proiect elaborat de elevul Colegiului Universității Tehnice a Moldovei, specialitatea Programarea și analiza produselor program, grupa PAPP-231 Bîtlan Alexandru în cadrul modulului S.07.O.022 Asistență pentru programarea server-side a site web,.
