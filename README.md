Welcome to the SSO login Task

1. Installation Guide
Follow these steps to run the application

    # 1. Clone the repository
    git clone https://github.com/ini-kaisarmonir/ecommerce.git

    # 2. Install PHP dependencies
    composer install

    # 3. Folder Permissions
    (If you use linux or vps)
    chmod -R 775 storage/logs/
    chmod -R 775 storage/framework/
    chmod -R 775 bootstrap/cache/
    (If you use cpanel or other panel change it manually)

    # 4. Install and compile Frontend assets
    npm install
    npm run build

    # 5. Environment Setup
    Copy the example env file and name it (.env) by running `cp .env.example .env` command and then  `php artisan key:generate` (If you use cpanel or other panel copy it manually).

    # 6. Database Setup (Ensure your .env has correct DB credentials)(Currently using mysql, you can change it as per your need)
    run `php artisan migrate:fresh --seed`
    
2. Usage guide
    It's for auth server. I have used laravel passport package for this. After installation you need to run `php artisan passport:keys` to generate passport encryption key. Then `php artisan passport:client` to generate credentials for client (Food website) then use the generated client id and client secret to the food site's env. One default user is in the seeder, the credential is-
    admin@example.com / 123456
