## BlazorTailwindPostCSS 
### Project link:
https://tailwindcss.com/docs/installation/using-postcss/
### 1. ���������� Tailwind CSS
���������� tailwindcss � ��� ������������ ����������� ����� npm � �������� ���� tailwind.config.js.
#### Terminal
    npm install -D tailwindcss postcss autoprefixer
    npx tailwindcss init
### 2. �������� Tailwind � ������������ PostCSS
�������� tailwindcss � autoprefixer � ���� ���� postcss.config.js ��� �����, ��� PostCSS �������� � ����� �������.
    
    module.exports = {
      plugins: {
        tailwindcss: {},
        autoprefixer: {},
      }
    }
    
### 3. ��������� ���� � ��������
�������� ���� �� ���� ����� ������ �������� � ���� tailwind.config.js.
#### tailwind.config.js
    /** @type {import('tailwindcss').Config} */
    module.exports = {
      content: ["./src/**/*.{html,js}"],
      theme: {
        extend: {},
      },
      plugins: [],
    }
### 4. �������� ��������� Tailwind � ���� CSS
�������� ��������� @tailwind ��� ������� ������ Tailwind � ���� �������� ���� CSS.
#### main.css
    @tailwind base;
    @tailwind components;
    @tailwind utilities;
### 4. �������  ������� ������ 
��������� ������� ������ � ������� ` npm run dev `  ��� ����� ������ �������, ����������� � ����� ����� package.json.
#### Terminal
    npm run dev
### 5. ������� ������������ Tailwind � ����� HTML
���������, ��� ��� ���������������� CSS ������� � <head> (��� ��������� ����� ���������� � ���� �� ���), ����� ������� ������������ ��������� ������ Tailwind ��� ���������� ������ ��������.
#### index.html
    <html>
    <head>
      <meta charset="UTF-8">
      <meta name="viewport" content="width=device-width, initial-scale=1.0">
      <link href="/dist/main.css" rel="stylesheet">
     </head>
    <body>
      <h1 class="text-3xl font-bold underline">
        ������ ���!
      </h1>
    </body>
    </html>

