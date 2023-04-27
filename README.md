# Steps to setup boilerplate for Vite with React and TailwindCSS + @tailwindcss/form

### 1. Setup Vite
```
yarn create vite
```
or
```
npm create vite
```
### 2. Setup SASS
install sass

```
yarn add sass
```
create scss file 
for example: 
```
src/scss/main.scss
```

then import main.scss in the App.tsx file


### 3. Setup Tailwindcss

install the packages
```
yarn add -D tailwindcss postcss autoprefixer @tailwindcss/form
```

create tailwind.config.js and postcss.config.js files
```
npx tailwindcss init -p
```

add content and plugin to tailwind.config.js file
```
import tailwindForm from "@tailwindcss/forms";
/** @type {import('tailwindcss').Config} */
export default {
  content: [
    "./index.html",
    "./src/**/*.{js,ts,jsx,tsx}",
  ],
  theme: {
    extend: {},
  },
  plugins: [tailwindForm],
}
```

Add the Tailwind directives the SCSS file (main.scss)

```
@tailwind base;
@tailwind components;
@tailwind utilities;
```

### 5. Run the app

```
yarn
```

and

```
yarn dev
```