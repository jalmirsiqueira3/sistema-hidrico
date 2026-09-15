# Relatório do Projeto: Sistema de Monitoramento e Gestão Hídrica

## 1. Visão geral

O Sistema de Monitoramento e Gestão Hídrica foi desenvolvido como uma solução full stack para facilitar o acompanhamento e o controle do abastecimento de água em uma unidade. O projeto integra diferentes camadas tecnológicas, incluindo hardware embarcado, comunicação em tempo real, backend web, frontend interativo e banco de dados persistente.

A proposta principal do sistema é permitir que clientes acompanhem o consumo e o status do abastecimento, enquanto funcionários tenham acesso a ferramentas para monitorar infraestrutura, gerenciar usuários e controlar comportas de forma remota.

---

## 2. Objetivos do projeto

### Objetivo geral

Desenvolver uma solução prática e funcional para monitoramento e gestão do abastecimento hídrico, combinando processamento em tempo real, interface web e automação de operações.

### Objetivos específicos

- disponibilizar uma interface para consulta de consumo e status de abastecimento;
- permitir que clientes registrem relatos sobre problemas no sistema;
- centralizar o monitoramento do nível do reservatório;
- possibilitar o controle remoto das comportas;
- fornecer uma API segura para gestão de usuários e dados;
- demonstrar integração entre hardware, software e banco de dados.

---

## 3. Arquitetura proposta

A solução foi organizada em quatro principais camadas:

### 3.1 Camada de hardware

A camada embarcada é responsável pela coleta de dados de sensores e pela execução de ações físicas, como acionamento de válvulas e leitura de variáveis do ambiente.

### 3.2 Camada de comunicação

A aplicação utiliza MQTT como protocolo de comunicação entre o sistema embarcado e o backend. Esse padrão foi escolhido por ser leve e eficiente para troca de mensagens em tempo real.

### 3.3 Camada de aplicação

O backend foi implementado com Node.js e Express, com suporte a autenticação JWT, validação de dados, integração com MongoDB e documentação da API via Swagger.

### 3.4 Camada de interface

O frontend foi desenvolvido em React e oferece acesso com foco em experiência do usuário para clientes e funcionários.

### 3.5 Registro do protótipo físico

<p align="center">
	<img src="prototipo.jpeg" alt="Protótipo físico inicial do sistema hídrico" width="700"/>
</p>

> **Observação:** a imagem registra o protótipo físico desenvolvido e utilizado durante a apresentação inicial do projeto. Ele foi usado para demonstrar a integração entre o ESP32, sensores, bomba e circuito de acionamento. Essa montagem é uma representação inicial e não corresponde à versão final do sistema, pois houveram alterações.

---

## 4. Funcionalidades implementadas

### 4.1 Funcionalidades para clientes

- consulta do status atual da unidade;
- acompanhamento do consumo em tempo real;
- consulta do cronograma de abastecimento;
- verificação do status de racionamento;
- registro de relatos sobre falhas ou problemas;
- atualização de senha;
- consulta da situação das comportas associadas ao cliente.

### 4.2 Funcionalidades para funcionários

- cadastro e atualização de clientes e funcionários;
- consulta e gerenciamento de usuários;
- monitoramento do nível do reservatório;
- visualização do estado das comportas;
- acionamento remoto das comportas;
- consulta dos relatos registrados pelos clientes;
- reset e atualização de senhas;
- listagem de registros e históricos vinculados ao sistema.

---

## 5. Tecnologias utilizadas

### Backend

- Node.js
- Express
- MongoDB + Mongoose
- MQTT.js
- JWT
- Zod
- Swagger UI

### Frontend

- React
- Vite
- React Router
- MUI Joy

### Firmware

- ESP32
- MQTT para troca de mensagens
- sensores e atuadores do protótipo

---

## 6. Fluxo de funcionamento

O fluxo geral da aplicação pode ser resumido em etapas:

1. O sistema embarcado coleta dados de consumo e nível.
2. Esses dados são publicados em tópicos MQTT.
3. O backend recebe as mensagens, trata os dados e os persiste no banco de dados.
4. O frontend consulta a API para apresentar informações ao usuário.
5. Funcionários podem disparar ações de controle, como abrir ou fechar comportas.
6. Clientes podem consultar o estado do sistema e registrar ocorrências quando necessário.

Esse fluxo demonstra a integração entre hardware, comunicação, backend e experiência do usuário.

---

## 7. Arquitetura de dados

O sistema trabalha com entidades como:

- Usuário
- Cliente
- Funcionário
- Consumo
- Relato
- Nível
- Comporta
- Abastecimento

Esses dados são modelados no backend e armazenados em MongoDB. A estrutura possibilita consulta, atualização e rastreio de informações relacionadas ao abastecimento e à operação da infraestrutura.

---

## 8. Pontos fortes do projeto

### 8.1 Escopo técnico

O projeto vai além de um CRUD comum, pois integra:

- comunicação com hardware;
- protocolos de mensagens em tempo real;
- autenticação e autorização;
- banco de dados persistente;
- interface para diferentes tipos de usuário.

### 8.2 Valor para portfólio

Para quem está buscando a primeira oportunidade, este projeto funciona como uma demonstração concreta de capacidade de desenvolver soluções completas e de pensar em arquitetura de software em múltiplas camadas.

### 8.3 Relevância profissional

O sistema demonstra domínio de temas importantes para o mercado, como:

- desenvolvimento web;
- integração entre sistemas;
- arquitetura orientada a serviços;
- IoT e automação;
- gestão de dados e usuários.

---

## 9. Desafios e aprendizados

Durante o desenvolvimento do projeto, foram enfrentados alguns desafios importantes:

- integração entre backend, frontend e hardware;
- entendimento do fluxo MQTT e do tratamento de mensagens;
- organização de rotas, autenticação e permissões;
- modelagem dos dados para o domínio de gestão hídrica;
- implementação de um sistema funcional com múltiplos perfis de usuário.

Esses desafios contribuíram para o aprendizado prático sobre desenvolvimento de software em contextos reais e integrados.

---

## 10. Possíveis evoluções futuras

Algumas melhorias que podem ser feitas no projeto incluem:

- dashboard com gráficos de consumo e histórico;
- notificações automáticas para problemas detectados;
- autenticação e autorização mais refinadas por perfil;
- testes automatizados para backend e frontend;
- deploy em ambiente cloud;
- integração com painel operacional para gestão visual das comportas.

---

## 11. Conclusão

O Sistema de Monitoramento e Gestão Hídrica é um projeto de grande valor para portfólio, principalmente para quem busca iniciar na área de tecnologia. Ele reúne conceitos fundamentais de desenvolvimento de software, arquitetura, integração de sistemas e comunicação em tempo real, além de demonstrar capacidade de construir uma solução completa com impacto prático.

A combinação de backend, frontend, banco de dados, autenticação e hardware torna o projeto uma excelente referência para apresentação em entrevistas, avaliações acadêmicas e portfólios pessoais.

---

## 12. Equipe

- Joelmir Siqueira
- Jalmir Siqueira
- Daniel Ferreira
