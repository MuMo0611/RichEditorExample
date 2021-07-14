# TinyMCE

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 12.1.1.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change
any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also
use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via a platform of your choice. To use this command, you need to first add a
package that implements end-to-end testing capabilities.

## Further help

To get more help on the Angular CLI use `ng help` or go check out
the [Angular CLI Overview and Command Reference](https://angular.io/cli) page.

# How to use TinyMCE Editor

### Download the library `` $ npm install --save @tinymce/tinymce-angular``

### Insert ``EditorModule`` in app.module.ts

### User the selector ``<editor></editor>`` in html files to view the editor.

### How to configure TinyMcE:

#### TinyMCE can be configured through the attribute ```[init]``` inside the tag ``editor``

#### In example:

```
<editor
  [init]="{
     height: 500,
     menubar: false,
     valid_elements : 'a[href|target=_blank],table,tbody,tr,th,td,strong/b,div[align],br',
     toolbar:
       'bold italic  | \
       alignleft aligncenter alignright alignjustify | \
       bullist numlist outdent indent | removeformat | help'
   }"
></editor>
```

where ``valid_elements`` refers to the allowed text format i.e., from the code above we can tell that the html
tags ``a`` with attribute ``href`` and ``target=blank`` are allowed. Moreover, the tags ``table`` is also allowed & etc.
This is useful in case of pasting a content from other rich client editor i.e., word. Furthermore, the feature of the
editor can be restricted with the help of ``toolbar`` we can see for text we defined ``bold`` and ``italic`` styles, let
us assume we need also the underline styling, then adding the keyword ``underline`` in the toolbar will also add the underline style to the editor.

