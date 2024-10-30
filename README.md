# Learn-app

Это простое приложение на Node.js с использованием Express, которое возвращает JSON-ответ и HTML-страницу.
1. Создаем новый репозиторий на GitHub.
2. Клонируем репозиторий на свой локальный компьютер:
   ```bash
   git clone https://github.com/ваш-логин/ваш-репозиторий.git
   cd ваш-репозиторий

4. Инициализируем проект и устанавливаем необходимые зависимости:
   ```bash
   npm init -y
   npm install express

6. Создаем файл app.js и добавляем следующий код:
```bash
   const express = require('express');
   const app = express();
   const port = 3000;

   app.get('/json', (req, res) => {
       res.json({ status: 'ok' });
   });

   app.get('/', (req, res) => {
       res.send('<h1>Hello World</h1>');
   });

   app.listen(port, () => {
       console.log(`Server is running at http://localhost:${port}`);
   });
```
8. Обновляем файл package.json, добавляем скрипт для запуска приложения:
```
    "scripts": {
       "start": "node app.js"
   }

   *Итоговый скрипт должен быть:
      {
     "name": "simple-express-app",
     "version": "1.0.0",
     "description": "A simple Express app that returns JSON and HTML.",
     "main": "app.js",
     "scripts": {
       "start": "node app.js"
     },
     "dependencies": {
       "express": "^4.17.1"
     },
     "author": "",
     "license": "ISC"
   }
   ```
10. Запускаем приложение:
 ```
   npm start
```
11. Проверяем работу приложения:
   Откройте в браузере http://localhost:3000/ — вы должны увидеть "Hello World".
   Откройте http://localhost:3000/json — вы должны увидеть JSON-ответ { "status": "ok" }.

