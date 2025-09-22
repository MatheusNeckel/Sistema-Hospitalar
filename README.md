# Sistema Hospitalar 🏥

Sistema desktop em **Java (Swing)** com **MySQL** para **cadastro e consulta de pacientes e convênios**.  
Projeto acadêmico com camadas **DAO/DTO/Serviços**, **JUnit** para testes e organização pronta para portfólio.

<p align="left">
  <img alt="Java" src="https://img.shields.io/badge/Java-8%2B-orange">
  <img alt="Build" src="https://img.shields.io/badge/build-Ant%20%7C%20Maven-blue">
  <img alt="License" src="https://img.shields.io/badge/license-MIT-success">
</p>

---

## ✨ Funcionalidades
- Cadastro de **pacientes**
- Cadastro de **convênios**
- Consultas e listagens com **JTable**
- Persistência **MySQL (JDBC)** via DAO
- **Testes unitários (JUnit)**

---

## 🧰 Tecnologias
- Java 8+ (POO, Swing)
- MySQL (JDBC)
- NetBeans/Ant (ou Maven, se aplicável)
- DAO, DTO e camada de Serviços

---

## ⚙️ Como executar

> **Dica:** publique quaisquer **.zip/.jar** em **Releases**; mantenha o **código-fonte descompactado** no repositório para melhor visualização.

### 1) Pré-requisitos
- **Java 8+**
- **MySQL** em execução (`localhost`)
- **NetBeans** (ou outra IDE compatível)

### 2) Banco de dados
- Execute o script SQL (ex.: `SCRIPT_BANCO_SISTEMA_HOSP.sql`) para criar as tabelas.

### 3) Configuração JDBC
Ajuste a conexão (ex.: `src/persistencia/ConexaoBanco.java`):
```java
String url = "jdbc:mysql://localhost:3306/sistema_hospitalar";
String user = "root";
String password = "sua_senha";
```

### 4) Executar
- **NetBeans/Ant**: abra o projeto e rode a classe principal (ex.: `visao/Menu.java`).  
- **Maven** (se houver `pom.xml`):
  ```bash
  mvn clean package
  java -jar target/<artefato>.jar
  ```

---

## 📁 Estrutura sugerida
```
/README.md
/LICENSE
/.gitignore
/.github/workflows/build.yml
/src/
  dao/...
  modelo/...
  servicos/...
  visao/...
  persistencia/ConexaoBanco.java
/sql/SCRIPT_BANCO_SISTEMA_HOSP.sql
/test/...
nbproject/            # se NetBeans/Ant
pom.xml               # se Maven
```
> Mantenha apenas **código-fonte e configs** no versionamento. Binários e zips devem ir nas **Releases**.

---

## 🧪 CI (GitHub Actions)
Workflow de exemplo para compilar com **Ant** (se `build.xml` existir) ou **Maven** (se `pom.xml` existir) e validar o build em **Java 8** e **17**.

---

## 📝 Licença
Distribuído sob a licença **MIT**. Veja `LICENSE` para detalhes.
