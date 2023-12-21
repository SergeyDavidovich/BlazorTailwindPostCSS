## BlazorTailwindPostCSS 
### Project link:
https://tailwindcss.com/docs/installation/using-postcss/
### 1. Установите Tailwind CSS
Установите tailwindcss и его одноранговые зависимости через npm и создайте файл tailwind.config.js.
#### Terminal
    npm install -D tailwindcss postcss autoprefixer
    npx tailwindcss init
### 2. Добавьте Tailwind в конфигурацию PostCSS
Добавьте tailwindcss и autoprefixer в свой файл postcss.config.js или везде, где PostCSS настроен в вашем проекте.
    
    module.exports = {
      plugins: {
        tailwindcss: {},
        autoprefixer: {},
      }
    }
    
### 3. Настройте пути к шаблонам
Добавьте пути ко всем вашим файлам шаблонов в файл tailwind.config.js.
#### tailwind.config.js
    /** @type {import('tailwindcss').Config} */
    module.exports = {
      content: ["./src/**/*.{html,js}"],
      theme: {
        extend: {},
      },
      plugins: [],
    }
### 4. Добавьте директивы Tailwind в свой CSS
Добавьте директивы @tailwind для каждого макета Tailwind в свой основной файл CSS.
#### main.css
    @tailwind base;
    @tailwind components;
    @tailwind utilities;
### 4. Начните  процесс сборки 
Запустите процесс сборки с помощью ` npm run dev `  или любой другой команды, настроенной в вашем файле package.json.
#### Terminal
    npm run dev
### 5. Начните использовать Tailwind в своем HTML
Убедитесь, что ваш скомпилированный CSS включен в <head> (ваш фреймворк может справиться с этим за вас), затем начните использовать служебные классы Tailwind для стилизации вашего контента.
#### index.html
    <html>
    <head>
      <meta charset="UTF-8">
      <meta name="viewport" content="width=device-width, initial-scale=1.0">
      <link href="/dist/main.css" rel="stylesheet">
     </head>
    <body>
      <h1 class="text-3xl font-bold underline">
        Привет мир!
      </h1>
    </body>
    </html>

