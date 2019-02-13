# Building Web applications with Knockout.js and ASP.NET Core

[Building Web applications with Knockout.js and ASP.NET Core](https://www.dotnetcurry.com/aspnet/1394/aspnet-core-knockout)


�t�@�ӰѦ�: [Razor Pages, TypeScript and Knockout](https://www.mikesdotnetting.com/article/321/razor-pages-typescript-and-knockout)

## �w�˽d��
Nuget��[Microsoft.AspNetCore.SpaTemplates](https://www.nuget.org/packages/Microsoft.AspNetCore.SpaTemplates/)���ѤF�Ҧ�SPAhjju dm 
.

�w�˩Ҧ��d��
```
dotnet -v
## �w�˽d��
Nuget��[Microsoft.AspNetCore.SpaTemplates](https://www.nuget.org/packages/Microsoft.AspNetCore.SpaTemplates/)���ѤF�Ҧ�SPAhjju dm 
.

�w�˩Ҧ��d��
```
dotnet -v

//�w�˩Ҧ��d��
dotnet new --install Microsoft.AspNetCore.SpaTemplates::*

//�d�ݦ����ǽd���i�ϥ�
dotnet new --help
```

�b`KnockoutDemo`�ؿ��U�إ�knockout spa�d��
```
dotnet new knockout
```

�٭�package
```
npm install
npm audit fix
npm audit fix --force
```

�w��`typescript`
```
npm i -g typescript@2.8.3
```

**VS2017��`Web Package`�]�w**
�b`�u��/�ﶵ/�M�שM���/Web Package Management`��, �N`$PATH`�����1��, �j��VS2017�ϥ�npm�˪�
tsc
//�w�˩Ҧ��d��
dotnet new --install Microsoft.AspNetCore.SpaTemplates::*

//�d�ݦ����ǽd���i�ϥ�
dotnet new --help
```

�b`KnockoutDemo`�ؿ��U�إ�knockout spa�d��
```
dotnet new knockout
```

�٭�package
```
npm install
npm audit fix
npm audit fix --force
```

�w��`typescript`
```
npm i -g typescript@2.8.3
```

**VS2017��`Web Package`�]�w**
�b`�u��/�ﶵ/�M�שM���/Web Package Management`��, �N`$PATH`�����1��, �j��VS2017�ϥ�npm�˪�
tsc

## �e�ݤ��R

### �������J���R
������`HomeController`��`Index`��View���J. ���|�M��`Shared/_Layout.cshtml`, ���J`vendor.css, vendor.js`��, �A���J`main.js`.

��`site.css`�u���b`production`�ɤ~�|�����J.

�o�ǳ]�w���O��`webpack`�ӳB�z��.

### hot module replacement
webpack����HMR�\��, �D�n�b`Startup.cs/Configure`���h�]�w.

### lazy load
�Ҧ�page���O�H`lazy load`�覡���J, ���Τ@�}�l�������J. �]���ϥΤF[custom knockout.js component loader](http://knockoutjs.com/documentation/component-loaders.html),
�b`webpack-component-loader.ts`������@�H����lazy-load�\��.

## ��controller���J���
�t�Ψϥ�`isomorphic-fetch`�Vcontroller�����.

## Several Razor Views with Knockout.js components
�ϥγ�@Razor view + knockout spa����������, �Y�Ǫ��p�U�i�H�ϥ�`�V�X��SPA`.

> Hybrid SPA/Razor pages that mix both server side and SPA techniques offer great flexibility in practical applications because applications based entirely on SPA techniques offer a better interaction with the user but cost more, are more difficult to maintain and have a shorter life since client side techniques evolve very quickly.

