# Exercicio de Polimorfismo

Este projeto demonstra conceitos basicos de Spring Boot com uso de JPA e polimorfismo.
Ele possui uma estrutura dividida em camadas e algumas entidades que representam produtos.

## Estrutura do projeto

- `src/main/java/com/roniceyangelo/demo/domain` – entidades JPA. A classe base `Produto` eh estendida por
  `Livro`, `Mouse` e `Teclado`, que sobrepoem o metodo `getDescricao`.
- `src/main/java/com/roniceyangelo/demo/repository` – contem `ProdutoRepository` com operacoes CRUD via `JpaRepository`.
- `src/main/java/com/roniceyangelo/demo/service` – classe `ProdutoService`, atualmente vazia.
- `src/main/java/com/roniceyangelo/demo/controller` – `ProdutoController` (sem metodos implementados).
- `src/test/java/com/roniceyangelo/demo` – teste basico para verificar se o contexto Spring carrega.

O ponto de entrada `DemoApplication` cria diferentes produtos, adiciona-os em uma lista e imprime suas descricoes antes de iniciar a aplicacao Spring.

## Configuracao de banco

O arquivo `src/main/resources/application.properties` esta configurado para usar MariaDB na porta `3307`.
Ha exemplos comentados de configuracao para H2, caso prefira um banco em memoria.

## Como executar

Para compilar e iniciar o projeto utilize o wrapper do Maven:

```bash
./mvnw spring-boot:run
```

## Como testar

Os testes podem ser executados com:

```bash
./mvnw test
```

## Dicas

- Experimente criar novas subclasses de `Produto` para praticar polimorfismo.
- Implemente metodos REST no `ProdutoController` para expor operacoes via API.
- Utilize H2 se nao tiver um banco MariaDB instalado.

