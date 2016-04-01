# eslint-config-prodest
>Configurações [ESLint](http://eslint.org/) para projetos AngularJS do [PRODEST](http://www.prodest.es.gov.br)

Garante que o código adere ao *coding style* para aplicações AngularJS do [PRODEST](http://www.prodest.es.gov.br), realizando o *linting*
do código usando [ESLint](http://eslint.org/). 

## Coding Style: [eslint-plugin-angular](https://github.com/Gillespie59/eslint-plugin-angular) + customizações
`eslint-config-prodest-angular` é um arquivo de configuração reaproveitável para as regras definidas em [eslint-plugin-angular](https://github.com/Gillespie59/eslint-plugin-angular), criando
assim um estilo de codificação para aplicações AngularJS no [PRODEST](http://www.prodest.es.gov.br).

## Dependências
Depende de [eslint-plugin-angular](https://github.com/Gillespie59/eslint-plugin-angular)


## Instalação
```
npm i --save-dev eslint-config-prodest-angular
```

**Também é preciso instalar [eslint-plugin-angular](https://github.com/Gillespie59/eslint-plugin-angular).**

## Uso
Em seu arquivo `.eslintrc`:
```json
{
  "extends": "prodest-angular"
}
```

Pode ser usado em conjunção com [eslint-config-prodest](https://github.com/prodest/eslint-config-prodest/blob/master/README.md) da seguinte maneira:
```json
{
  "extends": ['prodest','prodest-angular']
}
```

Esse arquivo de configuração faz 2 coisas:

 - habilita [eslint-plugin-angular](https://github.com/Gillespie59/eslint-plugin-angular).
 - adiciona `angular` como uma variável global.

### Regras
Customiza as [regras](https://github.com/Gillespie59/eslint-plugin-angular#user-content-rules) que o [eslint-plugin-angular](https://github.com/Gillespie59/eslint-plugin-angular) provêm, da seguinte maneira:
```json
rules: {
        'angular/angularelement': 1,
        'angular/controller-as': 2,
        'angular/controller-as-route': 2,
        'angular/controller-as-vm': [2, 'vm'],
        'angular/controller-name': [2, '/[a-z].*Controller$/'],
        'angular/deferred': 2, 
        'angular/definedundefined': 2,
        'angular/di': [2,"$inject"],
        'angular/di-order': [0, true],
        'angular/directive-name': 0,
        'angular/component-limit': [1, 1],
        'angular/document-service': 2,
        'angular/empty-controller': 0,
        'angular/file-name': 0,
        'angular/filter-name': 0,
        'angular/foreach': 0,
        'angular/function-type': [2, "named"],
        'angular/interval-service': 2,
        'angular/json-functions': 2,
        'angular/log': 2,
        'angular/module-getter': 2,
        'angular/module-name': 0,
        'angular/module-setter': 2,
        'angular/no-angular-mock': 0,
        'angular/no-controller': 0,
        'angular/no-cookiestore': 2,
        'angular/no-jquery-angularelement': 2,
        'angular/no-private-call': 2,
        'angular/no-service-method': 1,
        'angular/no-services': [2, ['$http', '$resource', 'Restangular']],
        'angular/on-watch': 2,
        'angular/rest-service': 0,
        'angular/service-name': 2,
        'angular/timeout-service': 2,
        'angular/typecheck-array': 2,
        'angular/typecheck-date': 2,
        'angular/typecheck-function': 2,
        'angular/typecheck-number': 2,
        'angular/typecheck-object': 2,
        'angular/typecheck-string': 2,
        'angular/watchers-execution': [0, '$digest'],
        'angular/window-service': 2,
        'no-use-before-define': 0
    }
```


### *Overrides*
Você pode facilmente sobrescrever regras de `eslint-config-prodest-angular` em seu próprio arquivo `.eslintrc`. Por exemplo, para nomes dos controllers
começando com letra maiúscula, use:
```json
rules: {
   'angular/controller-name': [2, '/[A-Z].*Controller$/'],
}
```


