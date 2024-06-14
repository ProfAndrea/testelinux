# testelinux

# https://getcomposer.org/download/

php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
php -r "if (hash_file('sha384', 'composer-setup.php') === 'dac665fdc30fdd8ec78b38b9800061b4150413ff2e3b6f88543c636f7cd84f6db9189d43a81e5503cda447da73c7e5b6') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
php composer-setup.php
php -r "unlink('composer-setup.php');"

Composer (version 2.7.7) successfully installed to: /tmp/guest-5ovg4t/Documentos/laravel/testelinux/testelinux/composer.phar
Use it: php composer.phar


# > ls
composer.phar  README.md
# Help do composer
>php composer.phar <br>
   ______
  / ____/___  ____ ___  ____  ____  ________  _____
 / /   / __ \/ __ `__ \/ __ \/ __ \/ ___/ _ \/ ___/
/ /___/ /_/ / / / / / / /_/ / /_/ (__  )  __/ /
\____/\____/_/ /_/ /_/ .___/\____/____/\___/_/
                    /_/
Composer version 2.7.7 2024-06-10 22:11:12<br>

Usage:
  command [options] [arguments]<br>

Options:
  -h, --help                     Display help for the given command. When no command is given display help for the list command
  -q, --quiet                    Do not output any message
  -V, --version                  Display this application version
      --ansi|--no-ansi           Force (or disable --no-ansi) ANSI output
  -n, --no-interaction           Do not ask any interactive question
      --profile                  Display timing and memory usage information
      --no-plugins               Whether to disable plugins.
      --no-scripts               Skips the execution of all scripts defined in composer.json file.
  -d, --working-dir=WORKING-DIR  If specified, use the given directory as working directory.
      --no-cache                 Prevent use of the cache
  -v|vv|vvv, --verbose           Increase the verbosity of messages: 1 for normal output, 2 for more verbose output and 3 for debug
<br>
Available commands:
  about                Shows a short information about Composer
  archive              Creates an archive of this composer package
  audit                Checks for security vulnerability advisories for installed packages
  browse               [home] Opens the package's repository URL or homepage in your browser
  bump                 Increases the lower limit of your composer.json requirements to the currently installed versions
  check-platform-reqs  Check that platform requirements are satisfied
  clear-cache          [clearcache|cc] Clears composer's internal package cache
  completion           Dump the shell completion script
  config               Sets config options
  create-project       Creates new project from a package into given directory
  depends              [why] Shows which packages cause the given package to be installed
  diagnose             Diagnoses the system to identify common errors
  dump-autoload        [dumpautoload] Dumps the autoloader
  exec                 Executes a vendored binary/script
  fund                 Discover how to help fund the maintenance of your dependencies
  global               Allows running commands in the global composer dir ($COMPOSER_HOME)
  help                 Display help for a command
  init                 Creates a basic composer.json file in current directory
  install              [i] Installs the project dependencies from the composer.lock file if present, or falls back on the composer.json
  licenses             Shows information about licenses of dependencies
  list                 List commands
  outdated             Shows a list of installed packages that have updates available, including their latest version
  prohibits            [why-not] Shows which packages prevent the given package from being installed
  reinstall            Uninstalls and reinstalls the given package names
  remove               [rm|uninstall] Removes a package from the require or require-dev
  require              [r] Adds required packages to your composer.json and installs them
  run-script           [run] Runs the scripts defined in composer.json
  search               Searches for packages
  self-update          [selfupdate] Updates composer.phar to the latest version
  show                 [info] Shows information about packages
  status               Shows a list of locally modified packages
  suggests             Shows package suggestions
  update               [u|upgrade] Updates your dependencies to the latest version according to composer.json, and updates the composer.lock file
  validate             Validates a composer.json and composer.lock

# Ver a versão do composer instalado 
> php composer.phar -V<br><br>
Composer version 2.7.7 2024-06-10 22:11:12<br>
PHP version 7.4.3-4ubuntu2.20 (/usr/bin/php7.4)<br>
Run the "diagnose" command to get more detailed diagnostics output.<br>

# Criar um projeto laravel
>php composer.phar create-project laravel/laravel nomeProjeto<br>
Creating a "laravel/laravel" project at "./teste"
Cannot use laravel/laravel's latest version v11.1.1 as it requires php ^8.2 which is not satisfied by your platform.<br>
Installing laravel/laravel (v8.6.12)
  - Downloading laravel/laravel (v8.6.12)
  - Installing laravel/laravel (v8.6.12): Extracting archive
Created project in /tmp/guest-5ovg4t/Documentos/laravel/testelinux/testelinux/teste
> @php -r "file_exists('.env') || copy('.env.example', '.env');"
Loading composer repositories with package information<br>

# habilitar o servidor

>cd teste<br>
>php artisan serve<br>
Starting Laravel development server: http://127.0.0.1:8000
[Thu Jun 13 19:37:19 2024] PHP 7.4.3-4ubuntu2.20 Development Server (http://127.0.0.1:8000) started
[Thu Jun 13 19:37:58 2024] 127.0.0.1:35964 Accepted
[Thu Jun 13 19:37:58 2024] 127.0.0.1:35964 Closing
[Thu Jun 13 19:37:59 2024] 127.0.0.1:35976 Accepted
[Thu Jun 13 19:37:59 2024] 127.0.0.1:35976 [200]: GET /favicon.ico
[Thu Jun 13 19:37:59 2024] 127.0.0.1:35976 Closing

