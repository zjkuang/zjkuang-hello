(1) Create a new empty repository `hello` on GitHub

(2) mkdir @zjkuang && cd @zjkuang && mkdir hello && cd hello

(3) Follow the setup sequence provided by GitHub
```
echo "# hello" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/zjkuang/hello.git
git push -u origin main
```

(4) (From `hello` root folder,) `yarn init`  
For question `name`, input `@zjkuang/hello`  
For question `private`, input `no`

(5) Open `hello` with Visual Studio Code

(6) Create index.js in `hello` root folder
```
console.log('index.js > Hello, world!');
```

(7) Create bin.js in `hello` root folder
```
#!/usr/bin/env node

console.log('bin.js > Hello, world!');
```

(8) In `hello`'s `package.json` add "bin" entry
```
{
  "name": "@zjkuang/hello",
  "version": "0.0.1",
  "main": "index.js",
  "bin": "bin.js",
  "repository": "https://github.com/zjkuang/hello.git",
  "author": "Zhengqian Kuang <dev.kuang@gmail.com>",
  "license": "MIT",
  "private": false
}
```

(9) Test locally  
(From `hello` root folder)  
`node .`  
`npx .`

(10) Publish the package  
(From `hello` root folder)  
`yarn publish --access public`
