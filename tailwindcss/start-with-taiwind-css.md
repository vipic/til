# 简单使用 tailwind css

这个是一个很酷很简单的东西，提供了基本的原子样式，自己通过组合就能很快的写出 button card 等各个组件。

最基础的使用方法


1. 安装并初始化，根据需求修改配置文件 `tailwind.config.js`

```shell
npm install -D tailwindcss
npx tailwindcss init
```

2. 将 tailwind css 引用到自己的项目内

```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```
3. 将工程文件编译成输出文件
```shell
npx tailwindcss -i ./src/input.css -o ./dist/output.css --watch
```
4. 引用输出文件，并在 html 或者 jsx 中使用

