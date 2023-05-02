# Upgrading angular coreui admin dashboard v2 to v4 
This was is pain

1. upgrade  
```@coreui/angular": "^4.4.1```,
 ```@coreui/coreui": "^4.2.6```,
```@coreui/icons": "^3.0.1```,
```@coreui/icons-angular": "^4.4.1```

2. These modules
``` AppAsideModule, AppFooterModule, AppHeaderModule, AppSidebarModule...``` no longer exist, use ``` FooterModule, HeaderModule, SidebarModule... ``` instead
 import icons (iconSetService or smthing like that), iconSubSet, add defaultHeaderComponent and defaultFooterComponent to APP_CONTAINERS

3. copy default layout from coreui template  
```
$https://github.com/coreui/coreui-free-angular-admin-template
```

3.1.
``` ```

4. Copy _layout.scss
- there is a markdown for .wrapper class


5. change css to match bootstrap v5
```
regex in vscode replce all fe.: /(class=".*)(?<![\w\d-])(card)(?![-\w\d])(.*")/ replace /$1 card mb-4 $3/

form-group -> mb-3  )
card -> card mb-4
text-right -> text-end
```
