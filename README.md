# goit-typescript-hw-01
Встанови source maps в tsconfig.json у проєкті TypeScript для налагодження коду у браузері (Модуль 1.5 “Debugging”).


 ми зробимо його компіляцію в консолі за допомогою команди:tsc test.ts

 стежити за зміною файлу в режимі реального часу, виконавши команду:
tsc test.ts -w

baseUrl: Якщо ваш проєкт має складну структуру, і ви не хочете прописувати повний шлях, як app/javascript/react/Component під час імпорту, ви можете використовувати baseUrl для спрощення імпорту, наприклад, react/Component. У цьому разі baseUrl буде app/javascript.



outDir: Каталог, де зберігаються скомпільовані файли.



rootDir: Коренева папка проєкту, у якій знаходиться основний файл.



target: Визначає версію ECMAScript, яка використовується для генерації вихідного коду. Наприклад, якщо вказати es5, компільований файл не матиме команд const і let та інших нових функцій, які були додані до es6, але код буде підтримуватися старими браузерами.

ESNext генерує код, який відповідає останній версії ECMAScript.
У сучасному світі можна починати з версії es2019 і вище.


module: Визначає систему модулів для використання. commonjs — стандартна система модулів для Node.js. Але ES2020 або ES2022 краще підходить для розробки на клієнтській стороні.



strict: Включає всі суворі перевірки типів у TypeScript. Це допомагає уникнути багатьох поширених помилок коду.



lib: Визначає, які бібліотеки слід використовувати. Якщо передати порожній масив у lib, у нашому коді буде недоступний навіть console.log. У lib потрібно вказати мінімально необхідну версію JavaScript, наприклад ["ES2021"].



﻿allowJs: Дозволяє компілятору TypeScript обробляти файли JavaScript. Це може бути корисно, якщо ви мігруєте проєкт, написаний на JavaScript і переписується на TypeScript. Після завершення міграції це налаштування зазвичай ставлять у false.



esModuleInterop: Дозволяє імпортувати модулі CommonJS так, ніби вони були б ES6-модулями. Це означає, що якщо у нас є якась бібліотека, яка використовує CommonJS, нам доведеться писати так:



import * as express from 'express';
