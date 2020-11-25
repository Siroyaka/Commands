# 初期化テンプレ
```powershell
npx create-next-app my-app
cd my-app
ni tsconfig.json
ni .env.local
npm i -d typescript @types/react @types/node
ni -ItemType directory src
move-item .\pages\ .\src\
move-item .\styles\ .\src\
Get-ChildItem src -Recurse -include *.js -exclude api | Rename-item -NewName {​​​​​​​​​​​​​​​​​ $_.FullName -replace "\.js$", ".tsx" }​​​​​​​​​​​​​​​​​
```