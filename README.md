# Adonis Database Encryption

<br>

[![gh-workflow-image]][gh-workflow-url] [![npm-image]][npm-url] [![npm-downloads]][npm-downloads] ![][typescript-image] [![license-image]][license-url]

Database Encryption is a feature that allows developers to store data with encrypted and consume again with data decrypted. This feature provides a structured and organized approach to managing application database, making it easier to query.

## Installation

```sh
node ace add @adityadarma/adonis-database-cryptable
```

## Usage

### Configuration

You can configuration encryption data from file config. for now only support `mysql or mariadb` database.

```ts
import { defineConfig } from '@adityadarma/adonis-database-cryptable/define_config'
import env from '#start/env'

const cryptableConfig = defineConfig({
  key: env.get('APP_KEY'),
  default: 'mysql',
  drivers: [
    'mysql'
  ]
})
export default cryptableConfig

```

### Adding to Model

You can choise what column will you encrypt with decorator `@columnCryptable()`.


```ts
@columnCryptable()
declare name: string

@columnCryptable()
declare email: string

@column()
declare emailVerifiedAt: DateTime
```

[gh-workflow-image]: https://img.shields.io/github/actions/workflow/status/adityadarma/adonis-database-cryptable/release.yml?style=for-the-badge
[gh-workflow-url]: https://github.com/adityadarma/adonis-database-cryptable/actions/workflows/release.yml 'Github action'
[npm-image]: https://img.shields.io/npm/v/@adityadarma/adonis-database-cryptable/latest.svg?style=for-the-badge&logo=npm
[npm-url]: https://www.npmjs.com/package/@adityadarma/adonis-database-cryptable/v/latest 'npm'
[typescript-image]: https://img.shields.io/badge/Typescript-294E80.svg?style=for-the-badge&logo=typescript
[license-url]: LICENSE.md
[license-image]: https://img.shields.io/github/license/adityadarma/adonis-database-cryptable?style=for-the-badge
[npm-downloads]: https://img.shields.io/npm/dm/@adityadarma/adonis-database-cryptable.svg?style=for-the-badge
[count-downloads]: https://npmcharts.com/compare/@adityadarma/adonis-database-cryptable?minimal=true
