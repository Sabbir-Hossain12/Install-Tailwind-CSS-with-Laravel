## Install Tailwind CSS with Laravel using Vite
#### Setting up Tailwind CSS in a Laravel project.

---
### Create your project 

```bash
composer create-project laravel/laravel my-project

cd my-project
```
---
### Install Tailwind CSS

```bash
 npm install -D tailwindcss postcss autoprefixer
 
 npx tailwindcss init -p
```
---
### Configure your template paths
Add the paths to all of your template files in your tailwind.config.js file.
```javascript
/** @type {import('tailwindcss').Config} */
export default {
  content: [
    "./resources/**/*.blade.php",
    "./resources/**/*.js",
    "./resources/**/*.vue",
  ],
  theme: {
    extend: {},
  },
  plugins: [],
}
```
---
### Add the Tailwind directives to your CSS
Add the @tailwind directives for each of Tailwind’s layers to your ./resources/css/app.css file.

```bash
@tailwind base;
@tailwind components;
@tailwind utilities;
```
---
### Start using Tailwind in your project
Make sure your compiled CSS is included in the `<head>` then start using Tailwind’s utility classes to style your content.
```html
<!doctype html>
<html>
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  @vite('resources/css/app.css')
</head>
<body>
  <h1 class="text-3xl font-bold underline">
    Hello world!
  </h1>
</body>
</html>
```
---
### Start your build process
Run your build process on development mode with npm run dev.
```bash
npm run dev
```
---
### Publish your build 
Finally, after your work, you can apply Tree shaking  and publish the project
```bash
npm run build
```
---
