# Drupal Gin
__Module name:__ `gt/gt_gin`
For customizations to the Gin admin theme.
Will be called into the `drupal-admin` recipe.

# Development
@TODO: Work in progress!

## Via local repo
Modules can be loaded locally in a couple ways, to make it easy to make changes and commit those changes back to the remote repo.

### Save directly to modules directory
If a module is added directly to the `web/modules/contrib` (or `web/modules/custom`) directory, it will be loaded.
1. Navigate to the modules directory:
```bash
cd web/modules/contrib
```
2. Clone the module to the directory, with the module machine name:
```bash
git clone https://github.com/gatech-arcs/drupal-gin.git gt_gin
```
3. Create a new working branch or swap to an existing one:
```bash
cd gt_gin
git checkout -b $newBranch
```

### Using Composer with local path

added directly to the `web/modules/contrib`/`web/modules/custom` directory.
1. Clone the `drupal_gin` repo to your project directory

## Via remote repo
1. Add an SSO-authorized Personal Access Token to your `git` config
2. Add the repo to your project's `composer.json` repositories list:
```bash
composer config repositories.gt_gin vcs https://github.com/gatech-arcs/drupal-gin.git
```
3. Add the module to the Drupal project:
```bash
# Dev version of module from master branch
composer require gt/gt_gin @dev

# Version of module from other branch
composer require gt/gt_gin:dev-$branchName
```

This will place the module in `web/modules/contrib/gt_gin`.