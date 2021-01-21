# namespace structure

> This namespace structure describes the excellens convention.

## package

Autoload: `'src/'` to `'<vendor>\<package>\'`.

### Source folder

* `<vendor>`
  * `<package>`
    * `Model`
      * `<object-name>`
      * `...`
    * `Entity`
      * `<object-name>` `extend the model`
      * `...`
    * `Contract`
      * `Mapper`
        * `<object-name>MapperInterface`
        * `...`
      * `Factory`
        * `<object-name>FactoryInterface` `(optional)`
        * `...`
      * `Repository`
        * `<object-name>RepositoryInterface`
        * `...`
      * `...`
    * `Mapper`
      * `<object-name>Mapper` `implement the contract`
      * `...`
    * `Factory`
      * `<object-name>Factory` `implement the contract (optional)`
      * `...`
    * `Repository`
      * `<object-name>Repository` `if only one implementation`
      * `...`
    * `Proxy`
      * `Contract`
        * `Repository`
          * `<object-name>RepositoryInterface` `extend or use in implmentation`
          * `...`
        * `...`
      * `Repository`
        * `<type>`
          * `<object-name>Repository`
          * `...`
        * `...`
      * `Mapper`
        * `<type>`
          * `<object-name>Mapper`
          * `...`
        * `...`
      * `...`
    * `Implementation`
      * `<type>`
        * `Mapper`
          * `...`
        * `Factory`
          * `...`
        * `Repository`
          * `...`
        * `...`
      * `...`
    * `...`

### Root folder:

* `mapping/` `doctrine mapping xml`
* `metadata/` `jms-serializer metadata yml`
* `src/` `source code`
* `composer.json`
* `composer.lock`
* `LICENSE.txt`
* `README.md`

---

## symfony-bundle

Autoload: `'src/'` to `'<vendor>\<package>\Bundle\'`.

### Source folder

* `<vendor>`
  * `<package>`
    * `Bundle`
      * `DependencyInjection`
        * `Compiler`
          * `Implementation`
            * `<type>`
              * `Repository`
                * `<object-name>RepositoryPass`
                * `...`
              * `RepositoryPassAbstract`
              * `...`
            * `...`
          * `<topic>Pass`
          * `...`
        * `Factory`
          * `Implementation`
            * `<type>`
              * `Repository`
                * `<object-name>RepositoryFactory`
                * `...`
              * `RepositoryFactoryAbstract`
              * `...`
            * `...`
          * `...`
        * `<vendor><package>Configuration`
        * `<vendor><package>Extension`
      * `Resource`
        * `config`
          * `packages`
            * `<configuration-root>.yaml`
            * `...`
          * `services.yaml`
          * `...`
        * `...`
      * `<vendor><package>Bundle`

### Root folder:

* `src/` `source code`
* `.gitignore`
* `composer.json`
* `composer.lock`
* `LICENSE.txt`
* `README.md`

---

Version: `1.1`, `2021-01-21`
