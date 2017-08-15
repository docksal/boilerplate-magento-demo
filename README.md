# Docksal powered Magento CE Installation

This is a sample Magento CE installation with default content pre-configured for use with Docksal.

Features:

- Magento CE with predefined content
- `fin init` example

## Setup instructions

### Step #1: Docksal environment setup

**This is a one time setup - skip this if you already have a working Docksal environment.**  

Follow [Docksal environment setup instructions](https://github.com/docksal/docksal/blob/develop/docs/env-setup.md)

### Step #2: Project setup

1. Clone this repo into your Projects directory

    ```
    git clone https://github.com/docksal/magento.git
    cd magento
    ```

2. Initialize the site

    This will create administrator and install the site with `php ./magento setup:install` 

    ```
    fin init
    ```

3. Point your browser to

    ```
    http://magento.docksal
    ```

## PHPStorm settings

Exclude next folders from index to improve performance of IDE:
```
docroot/pub/media
docroot/var

```


## More automation with 'fin init'

Site provisioning can be automated using `fin init`, which calls the shell script in [.docksal/commands/init](.docksal/commands/init).  
This script is meant to be modified per project. The one in this repo will give you a good example of advanced init script.

Some common tasks that can be handled by the init script:

- initialize local settings files for Docker Compose, Magento, etc.
- import DB or perform a site install
