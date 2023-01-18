A repo for reproducing the Drupal bug at https://www.drupal.org/project/drupal/issues/3241439

Usage
=====
```shell
# Clone this repo
git clone https://github.com/weitzman/drupal-twice.git
cd drupal-twice
composer install
# Get DDEV from ddev.readthedocs.io/ if needed.
ddev start
ddev snapshot restore --latest
# Make sure you see Drupal bootstrap : Successful
ddev drush status
```

At this point, you can continue per the issue. What I did:
```shell
drush config:import
# The below command shows a diff, even though we just imported.
drush config:export
```

