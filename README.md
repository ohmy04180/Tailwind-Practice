# Tailwind-Practice

## 실행 방법

### 1. terminal 에서 설치

```bash
npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init
```

### 2. tailwind.config.js 에서 compile할 html 경로 지정

```bash
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: ["./src/**/*.{html,js}"],
  theme: {
    extend: {},
  },
  plugins: [],
}
```

### 3. css 파일에 사용할 tailwind 임포트

```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

### 4. terminal 에서 실행

```bash
npx tailwindcss -i ./src/input.css -o ./dist/output.css --watch
```

### 5. link요소로 css 임포트, html 작성

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link href="/dist/output.css" rel="stylesheet" />
  </head>
  <body>
    <h1 class="text-3xl font-bold underline">Hello world!</h1>
  </body>
</html>
```
