# Springboot 3

## O que tem de novo?

### Java 17

Embora já houvesse suporte para Java 17 antes, esta versão LTS agora obtém a linha de base.
Ao migrar do LTS versão 11, os desenvolvedores Java se beneficiarão dos novos recursos da linguagem.

#### Registros

Os registros Java ( JEP 395 , veja Java 14 Record Keyword ) foram planejados para serem usados ​​como uma maneira rápida de criar classes portadoras de dados, ou seja, as classes cujo objetivo é simplesmente conter dados e transportá-los entre módulos, também conhecidas como POJOs (Plain Old Objetos Java) e DTOs (Objetos de Transferência de Dados).

Podemos facilmente criar DTOs imutáveis:

```
public record Person (String name, String address) {}
```

Atualmente, precisamos ter cuidado ao combiná-los com Bean Validation porque as restrições de validação não são suportadas em argumentos do construtor, como quando a instância é criada na desserialização JSON (Jackson) e colocada no método de um controlador como parâmetro.

### Blocos de texto

Com o JEP 378 , agora é possível criar blocos de texto multilinhas sem a necessidade de concatenar strings em quebras de linha:

```
String textBlock = """
Hello, this is a
multi-line
text block.
""";
```

## Como criar um projeto?

[Spring Initializr](https://start.spring.io/)
