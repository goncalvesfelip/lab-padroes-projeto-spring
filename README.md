🧠 Objetivo do Projeto
Criar uma API REST usando Java e Spring Boot que aplica os padrões de projeto Strategy, Facade e Singleton, como parte do Bootcamp Bradesco na DIO.

🛠️ Padrões de Projeto Utilizados
1. Strategy
Aplicado na camada de serviço para abstrair operações de manipulação de clientes.
Permite trocar a lógica de como os dados dos clientes são salvos, sem alterar o código principal.
2. Facade
Usado para simplificar a integração com o ViaCEP, que é uma API pública para consulta de endereços por CEP.
Encapsula a lógica de chamada à API externa, deixando o código mais limpo e desacoplado.
3. Singleton
A classe de serviço de cliente é tratada como Singleton pelo próprio Spring (por padrão, os beans são Singleton).
Garante que haja uma única instância da classe de serviço durante o ciclo de vida da aplicação.
📦 Estrutura do Projeto
Modelos:

Cliente: contém nome e endereço.
Endereco: contém CEP, logradouro, bairro, etc.
Repositórios:

ClienteRepository: interface JPA para persistência de clientes.
EnderecoRepository: interface JPA para persistência de endereços.
Serviços:

ClienteServiceImpl: implementa a lógica de negócio, aplicando Strategy e Facade.
🌐 Endpoints da API REST
GET /clientes: lista todos os clientes.
GET /clientes/{id}: busca cliente por ID.
POST /clientes: cria um novo cliente.
PUT /clientes/{id}: atualiza cliente existente.
DELETE /clientes/{id}: remove cliente por ID.
🔧 Tecnologias Usadas
Java 11
Spring Boot
Spring Data JPA
API ViaCEP
Maven
