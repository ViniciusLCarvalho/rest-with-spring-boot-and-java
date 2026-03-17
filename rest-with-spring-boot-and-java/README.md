# REST with Spring Boot and Java

Projeto de exemplo usando Spring Boot para expor um endpoint REST simples.

**Descrição**
- Aplicação Spring Boot que expõe um endpoint `/greeting` que retorna uma saudação em JSON.

**Requisitos**
- Java 11+ instalado (ou versão compatível com o projeto).
- Maven (opcional) — o repositório já inclui o Maven Wrapper (`mvnw`).

**Compilar e executar**
No diretório do projeto (onde está o `pom.xml`), execute:

```bash
./mvnw clean package
./mvnw spring-boot:run
```

No Windows (PowerShell/CMD):

```powershell
mvnw.cmd clean package
mvnw.cmd spring-boot:run
```

Após iniciar, a aplicação escuta em `http://localhost:8080` por padrão.

**Endpoints**
- GET `/greeting` — retorna um objeto JSON com id e mensagem.

Exemplo:

```bash
curl "http://localhost:8080/greeting?name=Alura"
```

Resposta esperada:

```json
{
  "id": 1,
  "content": "Hello, Alura!"
}
```

**Executar testes**

```bash
./mvnw test
```

**Estrutura do projeto**
- `pom.xml` — configurações do Maven e dependências.
- `src/main/java/br/com/quiet/Startup.java` — classe de inicialização da aplicação.
- `src/main/java/br/com/quiet/GreetingController.java` — controlador que expõe `/greeting`.
- `src/main/java/br/com/quiet/Greeting.java` — modelo de resposta.
