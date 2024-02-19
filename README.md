# Сборка Gulp 
Целью этой сборки является упростить разработку веб-сайтов.

## Возможности

Эта сборка самостоятельно: 
- Конвертирует и подключает шрифты,
- Записывает подключение в файл стилей.
- Обновляет браузер.
- Собирает в один несколько HTML\PUG файлов.
- Работает с CSS препроцессорами, например SASS(SCSS) и оптимизирует их.
- Не только сжимает изображения но и конвертирует их в современный формат WEBP, а также самостоятельно подключает результат к HTML и CSS файлам.
- Собирает в один несколько JavaScript файлов с помощью WEBPACK,  оптимизирует и сжимает их.
- Умеет работать с TypeScript
- Есть возможность работать в синтаксисе ES6.
- Умеет создавать SVG спрайты, создавать ZIP архив с результатом.

## Установка

1. Для работы сборки вам понадобится скачать и установить node.js.
2. Также установите систему контроля версии Git.
3. Для установки (клонирования репозитория) в текущую папку из консоли введите команду: `git clone https://github.com/ArtiomKochkin/gulp-build-2.git`
4. Во избежании всевозможных ошибок вам необходимо установить gulp глобально, но это в том случае если вы этого еще не делали в других проектах. Эта процедура делается один раз и в следующий раз, когда будете разворачивать новый проект повторять эту команду не потребуется.
   `npm i gulp -g`
5. После того как все исходники будут скачаны из удаленного репозитория, введите в консоли команду `npm install` для установки проекта. Все зависимости установятся автоматически.
6. Когда все зависимости были установлены для запуска проекта достаточно в консоли написать команду `npm run start` или `gulp`. Если нет ошибок, то в браузере по умолчанию откроется домен http://localhost:3000 со стартовым шаблоном проекта.

## Дополнительные команды
В файле package.json в секции `scripts` вы найдете команды для запуска проекта:

- dev - для запуска проекта в режиме разработки (development).
- build - для запуска проекта в режиме построения (production).
- svgSprive - оптимизация и объединение SVG-файлов, создавая спрайт SVG.
- zip - создание архива с исходниками проекта + папка dist.

Для запуска команды в консоли пишем "npm run имя_команды", например
`npm run build`

## Структура файлов проекта

- **gulp-pack/**
  - **dist/**
  - **gulp/**
    - **config/**
      - *path.js*
      - *plugins.js*
    - **tasks/**
      - *copy.js*
      - *fonts.js*
      - *images.js*
      - *html.js*
      - *js.js*
      - *reset.js*
      - *scss.js*
      - *server.js*
      - *zip.js*
      - *svgSprive.js*
    - *version.json*
  - **src/**
    - **files/**
    - **fonts/**
    - **html/**
      - *footet.html*
      - *header.html*
      - *head.html*
    - **img/**
    - **js/**
    - **scss/**
      - **blocks/**
      - **vendor/**
        - *reset.scss*
      - *style.scss*
      - *_mixins.scss*
      - *_vars.scss*
    - **ts/**
      - **modules/**
        - *functions.ts*
      - *app.ts*
    - **svgicons/**
    - *index.html*
  - *.gitignore*
  - *gulpfile.js*
  - *package.json*
  - *tsconfig.json*

- dist - это директория, куда компилируются и минифицируются файлы для развертывания.
- src - это директория с исходными файлами. Содержит папки для различных файлов, например js, html, scss, fonts и т.д.
- gulp - это директория с задачами сборщика и отдельными файлами для более структурированной и оптимизированной сборки
- .gitignore — файл со списком исключений для Git
- gulpfile.js — файл настроек для сборщика Gulp
- package.json — файл с настройками проекта с указанием списка зависимостей для установки
- tsconfig.json - файл конфигурации для компиляции TypeScript
