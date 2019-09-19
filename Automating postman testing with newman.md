## Automatizando testes de API do Postman com Newman

Basicamente newman é um comando onde ele executa todos os testes de API na sua collection do Postman e gera um relatório como report/evidência.


### Instalação:

Para instalar o Newman é preciso primeiramente instalar o gerenciador de pacotes NPM:

```
$ npm install npm@latest -g
```

Em Seguida, vamos instalar o Newman:

```
$ npm install -g newman
```

Existe uma versão mais completa, onde os reports vem com cores mais indicativas, para instalar essa versão, esse é o comando:

```
$ npm install -g newman-reporter-htmlextra
```

Pronto, com tudo instalado já podemos executar nossos testes em cima da nossa collection de API do postman, o comando para execução é bem simples, e logo em seguida é gerado um report em **.HTML**:

```
$ newman run MyCollection.postman_collection.json -e MyEnvironment.json -r htmlextra
```

Os comandos apartados basicamente tem essas funções:

**newman run MyCollection.postman_collection.json:** Executa o Newman apontando para qual collection vamos utilizar.

**-e MyEnvironment.json:** -e aponta as variáveis que nossa collection vai consumir.

**-r htmlextra:** Informa qual o tipo de relatório queremos, nesse caso, o extra.
