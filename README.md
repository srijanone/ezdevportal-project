# Getting Started

### Prerequisites

```
- PHP >= 8.0
- MariaDB 10.3.7+
- MySQL 5.7.8+
- Composer = 2.*
```

EzDevPortal utilizes composer to manage its dependencies.
So, before using EzDevPortal, make sure you have
composer installed on your machine.

### Installation from source
```
git clone git@github.com:srijanone/ezdevportal-project.git
cd ezdevportal-project
composer install
```

### Installation via composer

- Choose a name for your project, like “MY_PROJECT”
- Use the given command to create the project
- The command will download Drupal core along with necessary modules,
  EzDevPortal profile, and all other dependencies necessary for the project

```bash
composer create-project srijanone/ezdevportal-project
MY_PROJECT --no-interaction
```

In case you come across any memory issues, run this command -

```bash
php -d memory_limit=-1 /path/to/composer.phar create-project
srijanone/ezdevportal-project MY_PROJECT --no-interaction
```

**You can install the site either through drush or using GUI method.**

### Drush method

Navigate to the project root through terminal and execute the following command:

```bash
./vendor/bin/drush si ezdevportal
--db-url='mysql://{mysql_user}:{mysql_password}@{mysql_host}/{db_name}'
--site-name='EzDevPortal' --account-name='Srijan'
--account-pass='Admin@123'  --account-mail='admin@example.com' -y
```
### GUI Method

Setup a local environment using either docker(ddev, lando etc.) or LAMP stack.

Run the normal drupal GUI installation process.
You can choose to install the demo module during installion or you can install
it later from extend page or using drush.

Clear the drupal cache after installing the demo module.
