
Serverless plugin for migrate
==============================
[![serverless](http://public.serverless.com/badges/v3.svg)](http://www.serverless.com)
[![npm version](https://badge.fury.io/js/serverless-migrate-plugin.svg)](https://badge.fury.io/js/serverless-migrate-plugin)

This is a plugin for the [Serverless][serverless-web] framework that allows you to manage and run database-agnostic migrations. To do so, it works on top of [migrate][migrate-npm].

## Features

With this plugin you can

* Make the commands of `migrate` available via the `serverless` CLI.
* Be aware of the environment variables configured in your _serverless.yml_.
* Add the env variable `SERVERLESS_ROOT_PATH` which points to the root directory of your project.
* Configure aspects of your migration using your _serverless.yml_: no need to specify them as options with the CLI.
* Set values to env variables just for the migration context.
* Specify an custom character indicator of the last run migration.

Basically, these migrations can do anything that involves applying I/O changes and undo them.
Watch the [CHANGELOG](./CHANGELOG.md) to see what has been added to the date.

## Quick start

Check out the project located in the folder [example](example) of this repository. It contains a 
README with all the explanation you need to start creating your migrations. For starters, this is what you must do to 
start working with migrations:

1. Install `serverless-migrate-plugin` in your project:
```bash
npm i serverless-migrate-plugin
```

1. Add it to your _serverless.yml_ to the `plugins` section:
```yaml
plugins: 
  - serverless-migrate-plugin
```

1. Create your first migration:
```bash
sls migrate create <your-migration-name>
```

Now you are ready to implement your migrations. Once you have finished, you can test them using `sls migrate up` and 
`sls migrate down`.

It is highly recommended you to read about how to 
[create migrations for migrate](https://github.com/tj/node-migrate#creating-migrations).

## Built With

* [Serverless framework](https://serverless.com/): A powerful, unified experience to develop, deploy, 
test, secure, and monitor your Serverless applications.
* [Migrate](https://github.com/tj/node-migrate): Abstract migration framework for node.
* [NodeJS](https://nodejs.org/): As runtime for Javascript 8+.


## Author

* **Eliecer Hernandez** - [eliecerhdz@gmail.com](mailto:eliecerhdz@gmail.com). 
For more information, please visit my [website](http://eliux.github.io).

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.

[migrate-npm]: https://www.npmjs.com/package/migrate
[serverless-web]: https://www.serverless.com/