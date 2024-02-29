# Logger tools by Bout de code

![https://boutdecode.fr](https://boutdecode.fr/img/logo.png)

[Bout de code](https://boutdecode.fr) - Développement de site internet et blog avec de vrais morceaux de codes, simples, élégants, utiles (parfois) et surtout sans fioriture.

## Installation

```shell
$ npm install @boutdecode/logger
```

## Yion plugin

For yion : 

```javascript
const { createApp, createServer } = require('@boutdecode/yion')
const logger = require('@boutdecode/logger')

const app = createApp()
const server = createServer(app)

app.use(logger())

app.get('/', ({ logger }) => {
  logger.info('Info message')
  logger.error('Error message')
  logger.warn('Warning message')
  logger.debug('Debug message')
})

server.listen(8080)
```

And every request will be logged with the following format :

```
Thu Feb 29 2024 20:02:02 GMT+0100 (heure normale d’Europe centrale) - ::ffff:127.0.0.1 - GET / => 200 : OK 3.19ms
```

## Tests

```shell
$ npm run test
```
