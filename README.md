# Extending Admin UI

This bundle helps to extend admin ui

Requirements
------------

* eZ Platform 2.5+ 

## Install instructions

1. Add the project repository:
    
    In the main `composer.json`, add:
    ```
    "repositories": [
        // ...
        {
            "type": "vcs",
            "url": "https://github.com/rhidja/ExtendingTutorialBundle"
        }
    ],
    ```

2. Install the bundle via Composer (initial installation):

    ```
    $ composer require rhidja/extending-tutorial-bundle
    ```
    2.1 Update the bundle via Composer if needed
    ```
    $ composer update rhidja/extending-tutorial-bundle
    ```

3. Activate the bundle in your `app/AppKernel.php`:

    ```php
    $bundles = [
        ...
        new EzSystems\ExtendingTutorialBundle\EzSystemsExtendingTutorialBundle(),
        ...
    ];
    ```

4. Update app/config/routing.yml

    ```
    ez_systems_udw_tab_tutorial:
        resource: "@EzSystemsExtendingTutorialBundle/Resources/config/routing.yml"
        prefix:   /
