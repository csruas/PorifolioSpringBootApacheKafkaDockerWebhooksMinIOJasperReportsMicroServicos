# 🚀 iCompras — Arquitetura de Microservices com Spring Boot e Apache Kafka

Este projeto representa a construção de uma arquitetura distribuída baseada em **microservices**, desenvolvida com **Java e Spring Boot**, com foco em boas práticas de engenharia de software, comunicação assíncrona e arquitetura orientada a eventos.

O objetivo é simular um ambiente próximo de aplicações corporativas reais, onde cada serviço possui responsabilidades bem definidas, banco de dados independente e integração com outros serviços através de APIs REST e eventos utilizando **Apache Kafka**.

Ao longo do desenvolvimento, estão sendo implementados microservices responsáveis por diferentes áreas do domínio, como **clientes, produtos, pedidos, faturamento e logística**, permitindo explorar na prática os principais desafios de sistemas distribuídos.

## 🏗️ Arquitetura

A aplicação segue princípios de **Microservices Architecture** e **Event-Driven Architecture**, buscando reduzir o acoplamento entre os serviços e permitir maior independência, escalabilidade e evolução de cada componente.

Cada microservice possui sua própria responsabilidade e pode se comunicar com outros serviços através de:

- APIs REST;
- comunicação síncrona entre serviços;
- eventos assíncronos com Apache Kafka;
- Webhooks para integrações externas.

Essa abordagem permite trabalhar conceitos importantes como isolamento de responsabilidades, consistência entre serviços, processamento assíncrono e integração entre sistemas distribuídos.

## ⚙️ Tecnologias e ferramentas

O projeto utiliza tecnologias amplamente adotadas no desenvolvimento de aplicações backend modernas:

- **Java**
- **Spring Boot**
- **Spring Data JPA**
- **Spring Web**
- **OpenFeign**
- **Apache Kafka**
- **PostgreSQL**
- **Docker**
- **Docker Compose**
- **MinIO / S3 Compatible Storage**
- **JasperReports**
- **REST APIs**
- **Webhooks**
- **Maven**
- **Git e GitHub**

## 📦 Microservices

A arquitetura é composta por serviços independentes responsáveis por diferentes contextos do sistema:

### 👤 Clientes
Responsável pelo cadastro, consulta e gerenciamento dos clientes da aplicação.

### 📦 Produtos
Responsável pelo catálogo de produtos, informações comerciais e disponibilidade.

### 🛒 Pedidos
Responsável pela criação e gerenciamento dos pedidos, validação de clientes e produtos e início do fluxo de pagamento.

### 💳 Pagamentos
Responsável pelo processamento das solicitações relacionadas ao pagamento dos pedidos.

### 🧾 Faturamento
Responsável pelo processamento dos pedidos pagos e geração das informações relacionadas ao faturamento.

### 🚚 Logística
Responsável pelo fluxo de envio e acompanhamento dos pedidos.

## 📨 Apache Kafka

O Apache Kafka é utilizado como principal mecanismo de comunicação assíncrona da arquitetura.

Os microservices publicam e consomem eventos relacionados ao ciclo de vida de um pedido, permitindo que diferentes partes do sistema processem informações de maneira independente.

Exemplos de eventos trabalhados no projeto:

```text
Pedido criado
      ↓
Pagamento processado
      ↓
Pedido pago
      ↓
Faturamento
      ↓
Pedido faturado
      ↓
Logística
      ↓
Pedido enviado

Essa arquitetura permite aplicar conceitos importantes de sistemas distribuídos, como:
- producers e consumers;
- tópicos Kafka;
- particionamento;
- consumer groups;
- processamento assíncrono;
- desacoplamento entre serviços;
- arquitetura orientada a eventos.
🗄️ Banco de dados por microservice
O projeto também aplica o conceito de Database per Service, onde cada microservice possui seu próprio banco de dados.
Essa estratégia permite maior independência entre os serviços e evita que diferentes aplicações tenham acesso direto às tabelas umas das outras.
A comunicação de dados acontece através de APIs ou eventos.
🐳 Docker
O Docker é utilizado para disponibilizar a infraestrutura necessária para execução do ambiente de desenvolvimento.
Entre os serviços executados através de containers estão:
- PostgreSQL;
- Apache Kafka;
- serviços auxiliares da arquitetura;
- MinIO.
O Docker Compose permite subir toda a infraestrutura necessária de forma padronizada e reproduzível.
☁️ Armazenamento de arquivos
O projeto utiliza MinIO, uma solução compatível com a API do Amazon S3, para trabalhar com armazenamento de objetos.
Esse recurso permite explorar conceitos utilizados em ambientes Cloud para armazenamento de documentos, relatórios e outros arquivos gerados pela aplicação.
📊 Relatórios
A aplicação também explora a geração de relatórios utilizando JasperReports, permitindo criar documentos e relatórios dinâmicos a partir dos dados processados pelos microservices.
🔗 Webhooks
Webhooks são utilizados para explorar integrações entre sistemas externos e os microservices, permitindo que eventos sejam enviados automaticamente através de requisições HTTP.
🎯 Principais conhecimentos desenvolvidos
Durante o desenvolvimento deste projeto estão sendo aplicados e aprofundados conceitos como:
- arquitetura de microservices;
- arquitetura orientada a eventos;
- comunicação síncrona e assíncrona;
- desenvolvimento de APIs REST;
- integração entre microservices;
- Apache Kafka;
- bancos de dados independentes;
- persistência com Spring Data JPA;
- comunicação entre serviços com OpenFeign;
- containers com Docker;
- Docker Compose;
- armazenamento de objetos com MinIO;
- geração de relatórios;
- Webhooks;
- tratamento de erros;
- validação de regras de negócio;
- organização de aplicações Spring Boot;
- versionamento de código com Git.
🎓 Objetivo profissional
Este projeto faz parte do meu processo contínuo de evolução como desenvolvedor Java Backend, com foco no desenvolvimento de aplicações distribuídas utilizando Java, Spring Boot, Microservices, Apache Kafka e Docker.
Mais do que implementar funcionalidades, o objetivo deste repositório é consolidar conhecimentos sobre arquitetura de software, integração entre sistemas, mensageria, persistência de dados e desenvolvimento de soluções escaláveis e desacopladas.
O repositório também funciona como parte do meu portfólio técnico, documentando minha evolução prática no desenvolvimento de aplicações backend modernas.
