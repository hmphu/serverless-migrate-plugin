# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/)
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## Before release 2.0.2 - 2020-02-10
### Fixed
- Serverless config variables are now interpolated into env variables.
## Before release 2.0.1 - 2020-02-07
### Fixed
- When `store` or `state-file` are not specified it will not fail.
## Before release 2.0.0 - 2020-02-07
### Added
- Allows to override environment variables
### Changed
- Changes the param `store` and adds `state-file`:
    * `store`: Path where to get the class in charge of managing the migration data. If it is not
    specified it will use the default implementation which stores it in a file, i.e. `.migrate`.
    * `state-file`: Set the path of the state file. This path is also passed to the constructor of 
    the class specified by `store`.

## Before release 1.0.1 - 2019-09-06
### Added
- Allows the user to customize certain options throw custom.migrate:
    * `fileExtension`: Indicates the file extension for the migrations. By default `.js`.

## Before release 1.0.0 - 2019-09-01
### Added
Basic features:
- list: displays the migrations and its states
- create: Creates a migration file. You can specify the template to use with the option `template-file`.
- migrate up: Migrates forward. Optionally you can define name of a migration.
- migrate down: Migrates backwards. Optionally you can define name of a migration.
- Allows the user to customize certain options throw custom.migrate:
    * `store`: The migration states store file you want to use
    * `lastRunIndicator`: The text to append to the last migration that is applied
    * `noDescriptionText`: Text to show when a migration has no description
    * `ignoreMissing`: Ignores missing migration files if they are not found. 
    * `dateFormat`: The date format to use on the reports. By default it uses `yyyy-mm-dd`.
    * `templateFile`: The template to use to create your migrations.
    By default it is `false`, which makes the program throw an error if a migration is absent.
- Allows to specify the migration store file via the cli option `store`
- CHANGELOG.md added
- The example project was created.
- Injects content defined in the `environment` section of the serverless.yml into the 
`process.env` of the migrations.
- Injects the environment variable called `SERVERLESS_ROOT_PATH` which points to the absolute path of the project.

 
