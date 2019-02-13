# Building Web applications with Knockout.js and ASP.NET Core

[Building Web applications with Knockout.js and ASP.NET Core](https://www.dotnetcurry.com/aspnet/1394/aspnet-core-knockout)


另一個參考: [Razor Pages, TypeScript and Knockout](https://www.mikesdotnetting.com/article/321/razor-pages-typescript-and-knockout)

## 安裝範本
Nuget的[Microsoft.AspNetCore.SpaTemplates](https://www.nuget.org/packages/Microsoft.AspNetCore.SpaTemplates/)提供了所有SPAhjju dm 
.

安裝所有範本
```
dotnet -v
## 安裝範本
Nuget的[Microsoft.AspNetCore.SpaTemplates](https://www.nuget.org/packages/Microsoft.AspNetCore.SpaTemplates/)提供了所有SPAhjju dm 
.

安裝所有範本
```
dotnet -v

//安裝所有範本
dotnet new --install Microsoft.AspNetCore.SpaTemplates::*

//查看有哪些範本可使用
dotnet new --help
```

在`KnockoutDemo`目錄下建立knockout spa範本
```
dotnet new knockout
```

還原package
```
npm install
npm audit fix
npm audit fix --force
```

安裝`typescript`
```
npm i -g typescript@2.8.3
```

**VS2017的`Web Package`設定**
在`工具/選項/專案和方案/Web Package Management`中, 將`$PATH`移到第1個, 強迫VS2017使用npm裝的
tsc
//安裝所有範本
dotnet new --install Microsoft.AspNetCore.SpaTemplates::*

//查看有哪些範本可使用
dotnet new --help
```

在`KnockoutDemo`目錄下建立knockout spa範本
```
dotnet new knockout
```

還原package
```
npm install
npm audit fix
npm audit fix --force
```

安裝`typescript`
```
npm i -g typescript@2.8.3
```

**VS2017的`Web Package`設定**
在`工具/選項/專案和方案/Web Package Management`中, 將`$PATH`移到第1個, 強迫VS2017使用npm裝的
tsc

## 前端分析

### 頁面載入分析
網站由`HomeController`的`Index`的View載入. 它會套用`Shared/_Layout.cshtml`, 載入`vendor.css, vendor.js`等, 再載入`main.js`.

而`site.css`只有在`production`時才會做載入.

這些設定都是由`webpack`來處理的.

### hot module replacement
webpack提供HMR功能, 主要在`Startup.cs/Configure`中去設定.

### lazy load
所有page都是以`lazy load`方式載入, 不用一開始全部載入. 因此使用了[custom knockout.js component loader](http://knockoutjs.com/documentation/component-loaders.html),
在`webpack-component-loader.ts`中有實作以完成lazy-load功能.

## 由controller載入資料
系統使用`isomorphic-fetch`向controller取資料.

## Several Razor Views with Knockout.js components
使用單一Razor view + knockout spa的成本較高, 某些狀況下可以使用`混合型SPA`.

> Hybrid SPA/Razor pages that mix both server side and SPA techniques offer great flexibility in practical applications because applications based entirely on SPA techniques offer a better interaction with the user but cost more, are more difficult to maintain and have a shorter life since client side techniques evolve very quickly.

