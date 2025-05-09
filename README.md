# Microservices and Web Engineering - CP2
- Sistema de agenda de consultas

## 📌 Estrutura do Projeto   

### 📂 **Model**  
Contém as entidades do sistema, que representam as tabelas do banco de dados.  

### 📂 **DTO (Data Transfer Object)**  
Utilizado para transferir dados entre camadas sem expor diretamente as entidades do banco.  

### 📂 **Service**  
Responsável pela lógica de negócio do sistema, incluindo validações e regras antes de acessar o banco de dados.  

### 📂 **Controller**  
Gerencia as requisições HTTP, direcionando as chamadas para a camada de serviço e retornando as respostas adequadas.  

* ### **Endpoints**
* ```POST/pacientes``` - Criar Paciente;
* ```PUT/pacientes/{id}``` - Atualizar Paciente;
* ```DELETE/pacientes/{id}``` - Deletar Paciente;
* ```GET/pacientes/{id}``` - Buscar Paciente por Id;
* ```GET/pacientes``` - Buscar todos os Pacientes;
* ```POST/profissionais``` - Criar Profissional;
* ```PUT/profissionais/{id}``` - Atualizar Profissional;
* ```DELETE/profissionais/{id}``` - Deletar Profissional;
* ```GET/profissionais/{id}``` - Buscar Profissional por Id;
* ```GET/profissionais``` - Buscar todos os Profissionais;

## 🛠️ Instalação

* Limpar e criar a pasta */target*

```
mvn clean package
```

* Configuração do Swagger

    - https://springdoc.org/properties.html

- application.properties

```
springdoc.swagger-ui.path=/
springdoc.swagger-ui.disable-swagger-default-url=true
```

## Docker 
* Conexão com o banco de dados 

```
 docker run -d \
 	--name mysql \
 	--rm \
 	-e MYSQL_ROOT_PASSWORD=root_pwd \
 	-e MYSQL_USER=new_user \
 	-e MYSQL_PASSWORD=my_pwd \
 	-p 3306:3306 \
 	mysql
```

## 🌐 Navegação

### Executar a API

-  *Executando* **Maven**

```
mvn spring-boot:run
```

### Documentação da API (Swagger)
- http://localhost:8080/


## Referencias

- https://springdoc.org/
