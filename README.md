# Upgrading angular coreui admin dashboard v2 to v4 

1. upgrade/install
```@coreui/angular": "^4.4.1```,
 ```@coreui/coreui": "^4.2.6```,
```@coreui/icons": "^3.0.1```,
```@coreui/icons-angular": "^4.4.1```



2.
copy default-layout from coreui template and try to inster your old logic in there
```
https://github.com/coreui/coreui-free-angular-admin-template
```

3. These modules
``` AppAsideModule, AppFooterModule, AppHeaderModule, AppSidebarModule...``` no longer exist, use ``` FooterModule, HeaderModule, SidebarModule... ``` instead ```AppAsideModule doesnt exist```
 import icons (iconSetService or smthing like that), iconSubSet, add defaultHeaderComponent and defaultFooterComponent to APP_CONTAINERS


4. Copy _layout.scss
- there is a markdown for .wrapper class

5. change your primary color in _variables.scss
```
insert at the top of file

$primary: #0f7fc7;
@import "../node_modules/@coreui/coreui/scss/coreui";

```


6. change css to match bootstrap v5
```
regex in vscode replce all fe.: /(class=".*)(?<![\w\d-])(card)(?![-\w\d])(.*")/ replace /$1 card mb-4 $3/

form-group -> mb-3  )
card -> card mb-4
text-right/left -> text-end/start
pollish (offset-1) the new version is wider offset-1 -> offset-md-1


```
