# angular-material
angular-material
官方Angular Material入门有问题，请按照以下方法解决：

1、安装Angular CLI

npm install -g @angular/cli
 2、创建并运行新项目

ng angular-material
cd angular-material
ng serve --open --port 4200
3、安装Angular Material，Angular CDK和Angular Animations

npm install --save @angular/material @angular/cdk @angular/animations
4、配置动画

安装动画包后，导入BrowserAnimationsModule到您的应用程序/angular-material/src/app/app.module.ts文件中以启用动画支持。

import {BrowserAnimationsModule} from '@angular/platform-browser/animations';
 
@NgModule({
  ...
  imports: [BrowserAnimationsModule],
  ...
})
export class AppModule{ }
5、导入组件模块

为要使用的每个组件导入NgModule：

import {MatButtonModule, MatCheckboxModule} from '@angular/material';
 
@NgModule({
  ...
  imports: [MatButtonModule, MatCheckboxModule],
  ...
})
export class AppModule{ }
6、包含主题

包含主题是将所有核心和主题样式应用于您的应用程序所必需的。

要开始使用预先构建的主题，请在应用程序中全局包含Angular Material的预构建主题之一。如果您使用的是Angular CLI，可以将其添加到styles.css：

@import "~@angular/material/prebuilt-themes/indigo-pink.css";
7、Gesture 支持

一些组件（mat-slide-toggle，mat-slider，matTooltip）依靠HammerJS的手势。为了获得这些组件的完整功能集，必须将HammerJS加载到应用程序中。

您可以通过npm，CDN（例如Google CDN）将HammerJS添加到您的应用程序，或直接从您的应用程序提供。

要通过npm安装，请使用以下命令：

npm install --save hammerjs
8、添加材料图标

如果要将mat-icon组件与官方Material Design Icons一起使用，请在您的index.html。中加载图标字体。

<link href="https://fonts.googleapis.com/icon?family=Material+Icons" rel="stylesheet">
有关使用“材质图标”的更多信息，请查看“ 材质图标指南”。

请注意，它mat-icon支持任何字体或svg图标; 使用材料图标是众多选项之一。
