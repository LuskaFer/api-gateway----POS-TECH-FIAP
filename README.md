# API Gateway - POS-TECH

Este projeto é o **API Gateway** da aplicação POS-TECH, responsável por rotear as requisições HTTP para os respectivos microsserviços da aplicação. Ele foi construído utilizando **Spring Cloud Gateway** com padrão **Clean Architecture**, e está configurado para rodar em **Java 17**.

---

## ✅ Funcionalidades

- Roteamento inteligente de requisições entre microsserviços
- Estrutura modular seguindo Clean Architecture
- Dockerfile pronto para build e deploy
- Suporte para variáveis de ambiente
- Centralização de pontos de entrada da aplicação

---

## 🔀 Rotas configuradas

| Serviço            | Path Base       | Porta  |
|--------------------|------------------|--------|
| **Gateway**        | -                | `8080` |
| Cliente            | `/clientes/**`   | `8081` |
| Produto            | `/produtos/**`   | `8082` |
| Pedido             | `/pedidos/**`    | `8083` |
| Pedido Receiver    | `/receiver/**`   | `8084` |
| Pagamento          | `/pagamentos/**` | `8085` |
| Estoque            | `/estoque/**`    | `8086` |

---

## ⚙️ Pré-requisitos

- Java 17
- Maven 3.9+
- Docker

---

## 🚀 Executando localmente

### Build com Maven

```bash
./mvnw clean package
```

### Executar com Java

```bash
java -jar target/api-gateway-0.0.1-SNAPSHOT.jar
```

---

## 🐳 Docker

### Build da imagem

```bash
docker build -t seu-usuario/api-gateway-pos-tech .
```

### Executar o container

```bash
docker run -p 8080:8080 seu-usuario/api-gateway-pos-tech
```

---

## 📁 Estrutura esperada

```plaintext
api-gateway/
│
├── src/
│   └── main/
│       ├── java/
│       └── resources/
│           └── application.yml   <-- arquivo principal de configuração
│
├── Dockerfile
├── pom.xml
└── README.md
```


## 👨‍💻 Autor

Desenvolvido por **Lucas** durante o desafio da POS-TECH FIAP 2025.

---
