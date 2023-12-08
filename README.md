#  如何用 Vite 搭建 Tailwind & React 的项目（Set Up）

记录我在开发项目前，用 `Vite` 设置 `Tailwind` 和 `React` 环境的命令。

## Prerequisite

1. 安装了 [Node.js](https://nodejs.org/en)

## 创建 Vite 项目 &  选择 React 框架

1.  在当前目录中创建一个 Vite 项目
    ```bash
    npm create vite@latest
    ```
2. 根据 Vite 提示命名项目文件夹 `Project Name`，
3. 根据 Vite 提示选择框架，选择 `React`。
4. 根据 Vite 提示选择 `JavaScript` 或 `TypeScript`。
5. 进入项目文件夹 `Project Name`
    ```bash
    cd <project-name>
    ```
6. 在项目文件夹中安装 Node 项目依赖和指定包
    ```bash
    npm i
    ```

## 安装 Tailwind CSS

1. 在项目文件夹中安装 Tailwind CSS 和相关依赖
    ```bash
    npm install -D tailwindcss postcss autoprefixer
    ```
2. 生成 Tailwind 配置文件 `talwind.config` 和 `postcss.config.js`
   ```bash
   npx tailwindcss init -p
   ```

## 配置 Tailwind 配置文件
1. 用代码编辑器打开项目文件夹，找到 `tailwind.config.js` 文件，修改 `content: [],`内容：
    ```javascript
    content: [
    "./index.html",
    "./src/**/*.{js,ts,jsx,tsx}",
    ],
    ```
2. 找到`src/index.css`，全选并删除里面原有的内容，输入 Tailwind directives：
    ```css
    @tailwind base;
    @tailwind components;
    @tailwind utilities;
    ```
3. 运行 `npm run dev` 实时预览网页效果，可以开始开发了。

## Reference
1. [Tailwind Docs - Install Tailwind CSS with Vite](https://tailwindcss.com/docs/guides/vite)
2. [Tailwind CSS Tutorial for Beginners (2023) – What YOU need to know](https://youtu.be/DenUCuq4G04?si=Ot92NfPIe3gWQSw9)
