# Paginação com Spring Data JPA

Paginação é a divisão dos resultados de uma consulta em partes menores (páginas), melhorando desempenho e usabilidade em aplicações com muitos dados.

## Por que usar?
- 🔄 Evita carregar todos os dados de uma vez
- ⚡ Melhora performance e tempo de resposta
- 🧠 Reduz uso de memória

## Como funciona?
Use as interfaces `Pageable`, `Page` e `Sort` para controlar a paginação e ordenação dos resultados.

### Exemplo:
```java
Page<User> users = userRepository.findAll(
    PageRequest.of(0, 10, Sort.by("name").ascending())
);
```
## Teste
Utilize o Swagger para testar
http://localhost:8080/swagger-ui/index.html
