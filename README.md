# mvc-web-alunos

Aplicação web de cadastro de alunos desenvolvida com Spring Boot e Thymeleaf, 
seguindo o padrão de arquitetura MVC.

## Como o projeto está organizado

O projeto segue a separação em três camadas do padrão MVC:

**Model** — a classe `Aluno.java` representa os dados da aplicação. 
Ela não sabe nada sobre HTTP ou HTML, só cuida das regras da entidade, 
como garantir que o nome não seja vazio.

**Controller** — a classe `AlunoController.java` recebe as requisições do 
navegador, usa o Model para criar os alunos e decide qual View mostrar. 
Ele não renderiza HTML nem contém regra de negócio.

**View** — os arquivos `alunos-form.html` e `alunos-lista.html` só exibem 
os dados. Todo o conteúdo que aparece na tela veio do Controller, 
a View não busca nada por conta própria.

## Pré-requisitos

- Java JDK 17+
- Maven 3.8+
- VS Code com as extensões:
  - Extension Pack for Java
  - Spring Boot Extension Pack

## Como rodar

```bash
mvn spring-boot:run
```

Acesse no navegador: http://localhost:8080/alunos

## Como subir no GitHub

```bash
git init
git add .
git commit -m "Projeto MVC Web - Cadastro de Alunos"
git branch -M main
git remote add origin https://github.com/Matheus-Giampa/mvc-web-alunos.git
git push -u origin main
```