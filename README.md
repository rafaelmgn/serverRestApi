# Teste de API ServerRest 
Criação de testes de API ServerRest utilizando postman, newman e newman-htmlextra.

## Versões Utilizadas
- Postman versão web
- Node.js v20.11.1
- Newman v10.2.4
- Newman-reporter-html

## Documentação

- Documentação da API [consulte Swagger](https://serverest.dev).

## Instalação

- Baixar e instalar o **Node.js**: [clique aqui](https://nodejs.org/en/download);
- Para garantir que o Node.js foi instalado corretamente em seu sistema, você pode usar o seguinte comando para verificar a versão instalada:
```
node -v
```
- Com node instalado, abra o terminal e use o comando para instalar o **newman** de forma global:
```
npm install -g newman
```
- Caso deseja utilizar o *report html* do **newman**, instale o **newman-reporter-html** pelo terminal com o comando:
```
npm install -g newman-reporter-html
```

## Rodar os testes

### Pelo Postman web ou desktop

-  Importe a collection e o enviroment;
-  Execute os testes de forma manual ou automatizado.

### Pelo newman
- Para rodar os testes, execute o comando no terminal:
```
newman run ServeRest.postman_collection.json -e ServeRest.postman_environment.json -r cli
```
- Para rodar os testes e gerar o relatório, execute o comando no terminal:
```
newman run ServeRest.postman_collection.json -e ServeRest.postman_environment.json -r cli,htmlextra
```
#### Informaçoes adicionais
- `newman run`: Este é o comando principal do Newman para executar coleções de testes.
- `ServeRest.postman_collection.json`: Este é o arquivo da coleção do Postman que contém todas as solicitações de teste.
- `-e ServeRest.postman_environment.json`: Este é o arquivo do ambiente do Postman que contém as variáveis de ambiente necessárias para a execução dos testes.
- `-r cli`: Este parâmetro define o tipo de relatório que será gerado após a execução dos testes. Neste caso, "cli" indica que o relatório será exibido no terminal de linha de comando.
- `-r htmlextra`: Este parâmetro define o tipo de relatório que será gerado após a execução dos testes. Neste caso, "htmlextra" indica que o relatório será gerado no formato HTML com recursos extras, como gráficos e estatísticas adicionais, para uma visualização mais abrangente dos resultados. Após a execução dos testes, o relatório HTML será gerado e salvo em um diretório chamado "newman" dentro do diretório atual, onde você pode abrir o arquivo HTML em um navegador da web para visualizar os resultados.

### Report HTML

- Ao executar os testes com o parâmetro `-r htmlextra`, um relatório detalhado em formato HTML será gerado. Este relatório fornece uma visão abrangente dos resultados dos testes, incluindo estatísticas, gráficos e detalhes específicos sobre cada solicitação testada.
- O relatório HTML é útil para revisar de forma clara e visual os resultados dos testes de API. Ele permite identificar facilmente quaisquer falhas ou problemas encontrados durante a execução dos testes, além de fornecer insights sobre a performance e a qualidade da API testada.
- Além disso, o relatório HTML pode ser compartilhado com membros da equipe ou partes interessadas, facilitando a comunicação e o acompanhamento do progresso do teste. Ele também pode ser armazenado como documentação dos testes realizados, ajudando na auditoria e revisão futura.
- Para visualizar o relatório HTML, basta abrir o arquivo gerado em um navegador da web após a conclusão dos testes.
