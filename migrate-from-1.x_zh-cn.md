## �� 1.x ��������

[View English version](./migrate-from-1.x.md)

������ roadhog@2 �����鷳�����ǿ��Բο� [ant-design-pro ������ PR](https://github.com/ant-design/ant-design-pro/pull/542) ��������

---

���ڴ󲿷ֵ�Ӧ����˵��ֻҪ��

* ���� roadhog �汾Ϊ 2.x
* ���� .roadhogrc Ϊ .webpackrc
* ���� roadhog server Ϊ roadhog dev

Ȼ������������ `babel@7`��

* ��������� babel-polyfill������Ϊ `@babel/polyfill`
* ����� babel-runtime ��������ɾ������Ϊ�����ô���
* ���� babel@7 �޷�ʹ�� babel-plugin-add-module-exports�����е� `require('./file')` ���Ϊ `require('./file').default`
* ������� babel-plugin-dva-hmr���������� 0.4.x��

��Ȼ������� `src/index.ejs`����Ҫ�������� [html](https://github.com/sorrycc/roadhog#html) ���ԣ�

```
"html": { "template": "./src/index.ejs" }
```

����������ò���֧�֣��迼�����������ʹ�� webpack.config.js �������á�

* multipage (use commons instead)
* autoprefixer (use browserslist instead)
* dllPlugin (ѧϰ�ɱ�̫�ߣ����������������������� dev server �����ٶ�)
* svgSpriteLoaderDirs
* library
* libraryTarget
* cssModulesExclude
