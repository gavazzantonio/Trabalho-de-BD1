# TRABALHO 01:  Stock&Shop
Trabalho desenvolvido durante a disciplina de BD1

# Sumário
### 1. COMPONENTES<br>
Antonio Felipe Gavazza: gavazzantonio@gmail.com 

<br><br>
### 2. INTRODUÇÃO E MOTIVAÇÃO<br>
> A motivação por trás do Stock&Shop é proporcionar uma solução abrangente para empresas que buscam gerenciar seu estoque de forma eficiente, ao mesmo tempo em que integram suas operações de venda física e online. Esse tipo de integração se tornou fundamental para atender às expectativas dos clientes, oferecer uma experiência de compra consistente e maximizar as oportunidades de vendas.
> <br><br>
> Com a expansão do comércio eletrônico, as empresas enfrentam o desafio de sincronizar seus estoques entre suas lojas físicas e suas plataformas online. A falta de integração pode levar a problemas como vendas duplicadas, falta de produtos em estoque, erros de inventário e insatisfação do cliente. Portanto, a criação desse sistema visa superar essas dificuldades, permitindo que as empresas gerenciem seu estoque centralizado, atualizem os níveis de inventário em tempo real e sincronizem automaticamente as informações de venda tanto para as lojas físicas quanto para as vendas online.
> <br><br> 
> Além disso, o Stock&Shop oferece recursos para monitorar o desempenho de vendas, rastrear pedidos, gerar relatórios e análises de estoque e vendas, facilitando a tomada de decisões estratégicas. Com uma visão integrada de seu estoque, vendas e clientes, as empresas podem identificar tendências, ajustar seus inventários de acordo com a demanda, otimizar seus processos logísticos e desenvolver campanhas melhor direcionadas.

<br><br>
### 3. MINI-MUNDO
> O sistema Stock&Shop, gerencia diferentes estruturas da empresa e suas respectivas características. Temos os funcionários da loja, que são identificados por um ID único, assim como todos os elementos dentro do sistema, e do funcionário, são armazenados também o nome, email, telefone e a sua ocupação. Também temos os clientes, que têm um ID, e precisamos armazenar o CPF, nome, email, telefone e data de nascimento.
> <br><br>
> Os pedidos são uma importante parte do sistema, cada pedido é identificado com um ID, e são registrados a data de realização, o valor total da compra (que é a soma da multiplicação do valor de cada produto pela quantidade do mesmo, já que um pedido precisa ter pelo menos uma unidade de pelo menos um produto, mas um pedido aceita multiplos produtos e quantidades também), informações do cartão de crédito (número, titular, validade e código), além de informações de endereço, como tipo (rua, avenida, etc.), logradouro, número, bairro, cidade, estado, CEP e complemento. Um cliente, após o seu cadastro, pode realizar nenhum ou vários pedidos com cada pedido sendo atrelado a um único cliente.
> <br><br>
> Todos os produtos vendidos estão identificados no sistema com um ID e seu nome, valor de venda e a quantidade mínima que deve ter em estoque deste produto. Cada produto tem uma marca específica, que também possui um ID e nome e estas marcas podem ter nenhum ou vários produtos cadastrados no sistema. Além disso, os produtos também estão associados a categorias, e uma categoria pode conter nenhum ou vários produtos, cada categoria possui um ID e nome e uma categoria pode conter outras categorias, formando uma estrutura hierárquica onde cada subcategoria possui uma categoria-mãe.
> <br><br>
> Para controlar o estoque, cada item armazenado representa um único produto, mas pode haver produtos fora de estoque, cada item possui um ID próprio e é registrado com a sua a data de entrada, data de vencimento (se houver), o valor de aquisição e a informação de se o item está disponível no estoque e se foi devolvido (neste caso também é armazenado o motivo da devolução). O estoque é suprido pelos fornecedores, e cada um tem um ID no sistema, junto de seu CNPJ, nome, email, telefone e frequência de fornecimento em dias. Cada item do estoque é fornecido por um único fornecedor, e um fornecedor pode fornecer nenhum ou vários itens do estoque.
> <br><br>
> E temos, para utilização do sistema, o registro de usuários que podem estar atrelado a um cliente ou funcionário. Cada usuário tem um ID, nome de usuário, senha e pode ter diferentes papéis no sistema, como comprador, operador ou gerente. Um cliente ou funcionário só pode ser vinculado a um único usuário.

<br><br>
### 4.PROTOTIPAÇÃO, PERGUNTAS A SEREM RESPONDIDAS E TABELA DE DADOS:
#### 4.1 RASCUNHOS BÁSICOS DA INTERFACE (MOCKUPS):
![Alt text](https://github.com/gavazzantonio/Trabalho-de-BD1/blob/master/images/balsamiq.png?raw=true "Title")
![Arquivo PDF do Protótipo Balsamiq feito para Smart Shop](https://github.com/gavazzantonio/Trabalho-de-BD1/blob/master/arquivos/smartshop.pdf?raw=true "Smart Shop")

 <br><br>
#### 4.2 QUAIS PERGUNTAS PODEM SER RESPONDIDAS COM O SISTEMA PROPOSTO?
> O Stock&Shop fornece, inicialmente, os seguintes relatórios:
* Relatório de vendas por período  -  apresenta informações sobre os pedidos realizados em um determinado período, incluindo o valor total das vendas, a quantidade de produtos vendidos e as informações dos clientes.
* Relatório de estoque  -  fornece uma visão geral do estoque atual, incluindo a quantidade disponível de cada produto, a data de compra e de vencimentos, o valor de compra e informações dos fornecedores.
* Relatório de clientes ativos  -  lista os clientes que realizaram pedidos recentemente, mostrando seus dados pessoais, quantidade de compras no período e valor total gasto.
* Relatório de produtos mais vendidos  -  lista os produtos que tiveram maior volume de vendas em um determinado período, fornecendo informações sobre o produto, a quantidade vendida, o valor total arrecadado.
* Relatório de retorno de produtos  -  fornece informações sobre os produtos devolvidos, o motivo da devolução, o número de devoluções por período, o valor total dos produtos devolvidos.

<br><br>
#### 4.3 TABELA DE DADOS DO SISTEMA:
    a) Esta tabela deve conter todos os atributos do sistema e um mínimo de 10 linhas/registros de dados.
![Tabela de dados do sistema Stock&Shop](https://github.com/discipbd1/trab01/blob/master/arquivos/TabelaEmpresaDevCom_sample.xlsx?raw=true "Tabela - Empresa Devcom")

<br><br>
### 5. MODELO CONCEITUAL:
#### 5.1 Diagrama
![Alt text](https://github.com/gavazzantonio/Trabalho-de-BD1/blob/master/conceitual%20v1752.png "Modelo Conceitual")

<br><br>
#### 5.2 Descrição dos dados 
    FUNCIONARIO: Tabela que armazena as informações relativas aos funcionários da empresa.
    id: campo que armazena o ID único do funcionário.
    nome: campo que armazena o nome do funcionário.
    email: campo que armazena o endereço de email do funcionário.
    telefone: campo que armazena o número de telefone do funcionário.
    ocupacao: campo que armazena a ocupação ou cargo do funcionário na empresa.
    
    CLIENTE: Tabela que armazena as informações relativas aos clientes da empresa.
    id: campo que armazena o ID único do cliente.
    cpf: campo que armazena o número do Cadastro de Pessoa Física (CPF) do cliente.
    nome: campo que armazena o nome do cliente.
    email: campo que armazena o endereço de email do cliente.
    telefone: campo que armazena o número de telefone do cliente.
    nascimento: campo que armazena a data de nascimento do cliente.
    
    PEDIDO: Tabela que armazena as informações relativas aos pedidos realizados pelos clientes.
    id: campo que armazena o ID único do pedido.
    data: campo que armazena a data de realização do pedido.
    valor: campo que armazena o valor total do pedido.
    cartao_numero: campo que armazena o número do cartão de crédito utilizado no pedido.
    cartao_titular: campo que armazena o nome do titular do cartão de crédito.
    cartao_validade: campo que armazena a data de validade do cartão de crédito.
    cartao_codigo: campo que armazena o código de segurança do cartão de crédito.
    endereco_tipo: campo que armazena o tipo de logradouro (rua, avenida, etc.).
    endereco_logradouro: campo que armazena o nome do logradouro do endereço.
    endereco_numero: campo que armazena o número do endereço.
    endereco_bairro: campo que armazena o nome do bairro do endereço.
    endereco_cidade: campo que armazena o nome da cidade do endereço.
    endereco_estado: campo que armazena o nome do estado do endereço.
    endereco_cep: campo que armazena o CEP (Código de Endereçamento Postal) do endereço.
    endereco_complemento: campo que armazena informações adicionais sobre o endereço.
    
    ITEM: Tabela que armazena as informações relativas aos itens presentes em um pedido.
    id: campo que armazena o ID único do item.
    valor: campo que armazena o valor unitário do item.
    quantidade: campo que armazena a quantidade do item.
    
    PRODUTO: Tabela que armazena as informações relativas aos produtos cadastrados no sistema.
    id: campo que armazena o ID único do produto.
    nome: campo que armazena o nome do produto.
    valor: campo que armazena o valor unitário do produto.
    quantidade_minima: campo que armazena a quantidade mínima em estoque para a manutenção da disponibilidade do produto.
    
    MARCA: Tabela que armazena as informações relativas às marcas dos produtos.
    id: campo que armazena o ID único da marca.
    nome: campo que armazena o nome da marca.
    
    CATEGORIA: Tabela que armazena as informações relativas às categorias dos produtos.
    id: campo que armazena o ID único da categoria.
    nome: campo que armazena o nome da categoria.
    
    ESTOQUE: Tabela que armazena as informações relativas ao estoque dos produtos.
    id: campo que armazena o ID único do item do estoque.
    data_entrada: campo que armazena a data de entrada do produto no estoque.
    data_vencimento: campo que armazena a data de vencimento do produto.
    valor: campo que armazena o valor de compra do produto.
    disponivel: campo que indica se o produto está disponível (verdadeiro ou falso).
    devolvido: campo que indica se o produto foi devolvido (verdadeiro ou falso).
    devolvido_motivo: campo que armazena o motivo da devolução do produto, caso tenha sido devolvido.
    
    FORNECEDOR: Tabela que armazena as informações relativas aos fornecedores dos produtos.
    id: campo que armazena o ID único do fornecedor.
    cnpj: campo que armazena o número do Cadastro Nacional da Pessoa Jurídica (CNPJ) do fornecedor.
    nome: campo que armazena o nome do fornecedor.
    email: campo que armazena o endereço de email do fornecedor.
    telefone: campo que armazena o número de telefone do fornecedor.
    frequencia_dias: campo que armazena a frequência de fornecimento em dias.
    
    USUARIO: Tabela que armazena as informações relativas aos usuários do sistema.
    id: campo que armazena o ID único do usuário.
    usuario: campo que armazena o nome de usuário do usuário.
    senha: campo que armazena a senha do usuário.
    comprador: campo que indica se o usuário possui o papel de comprador (verdadeiro ou falso).
    operador: campo que indica se o usuário possui o papel de operador (verdadeiro ou falso).
    gerente: campo que indica se o usuário possui o papel de gerente (verdadeiro ou falso).

<br><br>
### 6	MODELO LÓGICO
![Alt text](https://github.com/gavazzantonio/Trabalho-de-BD1/blob/master/images/logico%20v1803.png "Modelo Lógico")

<br><br>
##    OBSERVAÇÃO DO PROFESSOR
* Por sugestão do professor, foi adotado um modelo lógico/físico menor do que apresentado anteriormente, que será identifciado abaixo. Também foi insruido pelo professor, uma vez que este trabalho está sendo executado de forma individual, a adoção de metade das instruções solicitadas nos tópicos.

<br><br>
### 5. MODELO CONCEITUAL:
#### 5.1 Diagrama
![Alt text](https://github.com/gavazzantonio/Trabalho-de-BD1/blob/master/images/conceitual%20v6263.png "Modelo Conceitual")

<br><br>
#### 5.2 Descrição dos dados 
    CLIENTE: Tabela que armazena as informações relativas aos clientes da empresa.
    id: ID único do cliente.
    cpf: Número de CPF do cliente.
    nome: Nome do cliente.
    email: Endereço de email do cliente.
    telefone: Número de telefone do cliente.
    nascimento: Data de nascimento do cliente.
    endereco_cep: CEP do endereço do cliente.
    endereco_logradouro: Logradouro do endereço do cliente.
    endereco_numero: Número do endereço do cliente.
    endereco_bairro: Bairro do endereço do cliente.
    endereco_cidade: Cidade do endereço do cliente.
    endereco_estado: Estado do endereço do cliente.
    
    COMPRA: Tabela que armazena as informações relativas aos pedidos realizados pelos clientes.
    id: ID único da compra.
    data_compra: Data da compra.
    
    MARCA: Tabela que armazena as informações relativas aos pedidos realizados pelos clientes.
    id: ID único da marca.
    nome: Nome da marca.
    
    CATEGORIA: Tabela que armazena as informações relativas aos pedidos realizados pelos clientes.
    id: ID único da categoria.
    nome: Nome da categoria.
    
    PRODUTO:
    id: ID único do produto.
    nome: Nome do produto.
    valor: Valor do produto.
    quantidade: Quantidade disponível do produto.
    
    ITEM:
    valor: Valor do item praticado no dia da compra.
    quantidade: Quantidade do item.

<br><br>
### 6	MODELO LÓGICO
![Alt text](https://github.com/gavazzantonio/Trabalho-de-BD1/blob/master/images/logico%20v6263.png "Modelo Lógico")

<br><br>
### 7	MODELO FÍSICO
```sql
create table CLIENTE(
	id integer primary key,
	cpf varchar(14),
	nome varchar(100),
	email varchar(100),
	telefone varchar(15),
	nascimento date,
	endereco_cep varchar(9),
	endereco_logradouro varchar(100),
	endereco_numero integer,
	endereco_bairro varchar(100),
	endereco_cidade varchar(100),
	endereco_estado varchar(2)
);

create table COMPRA(
	id integer primary key,
	data_compra date,
	id_CLIENTE integer,
	foreign key (id_CLIENTE) references CLIENTE(id)
	  on update cascade
);

create table MARCA(
	id integer primary key,
	nome varchar(100)
);

create table CATEGORIA(
	id integer primary key,
	nome varchar(100),
	id_CATEGORIA integer,
	foreign key(id_CATEGORIA) references CATEGORIA(id)
	  match full on delete set null on update cascade
);

create table PRODUTO(
	id integer primary key,
	nome varchar(100),
	valor real,
	quantidade integer,
	id_MARCA integer,
	id_CATEGORIA integer,
	foreign key(id_MARCA) references MARCA(id)
	  on update cascade,
	foreign key(id_CATEGORIA) references CATEGORIA(id)
	  match full on delete set null on update cascade
);

create table ITEM(
	id_PRODUTO integer,
	id_COMPRA integer,
	valor real,
	quantidade integer,
	primary key(id_PRODUTO, id_COMPRA),
	foreign key(id_PRODUTO) references PRODUTO(id)
	  on update cascade,
	foreign key(id_COMPRA) references COMPRA(id)
	  on update cascade
);
```

<br><br>
### 8	INSERT APLICADO NAS TABELAS DO BANCO DE DADOS<br>
```sql
insert into CLIENTE (id, cpf, nome, email, telefone, nascimento, endereco_cep, endereco_logradouro, endereco_numero, endereco_bairro, endereco_cidade, endereco_estado)
values
(1, '123.456.789-00', 'João Silva', 'joao@gmail.com', '(11) 98765-4321', '1990-05-15', '12345-678', 'Rua A', 10, 'Centro', 'São Paulo', 'SP'),
(2, '987.654.321-00', 'Maria Santos', 'maria@gmail.com', '(11) 98765-4322', '1985-09-20', '54321-098', 'Rua B', 20, 'Vila Nova', 'Rio de Janeiro', 'RJ'),
(3, '111.222.333-00', 'Pedro Oliveira', 'pedro@gmail.com', '(11) 98765-4323', '1992-12-10', '67890-543', 'Rua C', 30, 'Jardins', 'São Paulo', 'SP'),
(4, '444.555.666-00', 'Ana Costa', 'ana@gmail.com', '(11) 98765-4324', '1998-02-28', '34567-890', 'Rua D', 40, 'Copacabana', 'Rio de Janeiro', 'RJ'),
(5, '777.888.999-00', 'Carlos Pereira', 'carlos@gmail.com', '(11) 98765-4325', '1995-07-05', '98765-432', 'Rua E', 50, 'Barra Funda', 'São Paulo', 'SP'),
(6, '000.111.222-33', 'Fernanda Sousa', 'fernanda@gmail.com', '(11) 98765-4326', '1993-11-12', '67890-123', 'Rua F', 60, 'Lapa', 'Rio de Janeiro', 'RJ'),
(7, '444.333.222-11', 'Mariana Rocha', 'mariana@gmail.com', '(11) 98765-4327', '1991-04-02', '54321-678', 'Rua G', 70, 'Moema', 'São Paulo', 'SP'),
(8, '555.666.777-00', 'Ricardo Almeida', 'ricardo@gmail.com', '(11) 98765-4328', '1997-08-18', '23456-789', 'Rua H', 80, 'Botafogo', 'Rio de Janeiro', 'RJ'),
(9, '888.999.000-11', 'Camila Santos', 'camila@gmail.com', '(11) 98765-4329', '1994-01-25', '98765-321', 'Rua I', 90, 'Pinheiros', 'São Paulo', 'SP'),
(10, '222.333.444-00', 'Lucas Lima', 'lucas@gmail.com', '(11) 98765-4330', '1996-06-08', '43210-987', 'Rua J', 100, 'Ipanema', 'Rio de Janeiro', 'RJ');

insert into COMPRA (id, data_compra, id_CLIENTE)
values
(1, '2023-06-01', 1),
(2, '2023-06-02', 2),
(3, '2023-06-10', 3),
(4, '2023-06-10', 4),
(5, '2023-06-11', 5),
(6, '2023-06-15', 3),
(7, '2023-06-17', 1),
(8, '2023-06-17', 8),
(9, '2023-06-20', 2),
(10, '2023-06-30', 10);

insert into MARCA (id, nome)
values
(1, 'Nike'),
(2, 'Adidas'),
(3, 'Dell'),
(4, 'Apple'),
(5, 'Under Armour'),
(6, 'Hering'),
(7, 'Reebok'),
(8, 'Samsung'),
(9, 'LG'),
(10, 'Havaianas');

insert into CATEGORIA (id, nome, id_CATEGORIA)
values
(1, 'Eletrônicos', NULL),
(2, 'Smartphones', 1),
(3, 'TVs', 1),
(4, 'Computadores', 1),
(5, 'Roupas', NULL),
(6, 'Masculino', 5),
(7, 'Feminino', 5),
(8, 'Calçados', 5),
(9, 'Esportes', NULL),
(10, 'Futebol', 9);

insert into PRODUTO (id, nome, valor, quantidade, id_MARCA, id_CATEGORIA)
values
(1, 'iPhone 12', 3499, 10, 4, 2),
(2, 'Galaxy S21', 2199.99, 15, 8, 2),
(3, 'OLED TV', 3099.99, 5, 9, 3),
(4, 'XPS 15', 4000, 8, 3, 4),
(5, 'Air Max', 400, 20, 1, 8),
(6, 'Superstar', 375, 15, 2, 8),
(7, 'Brasil Light', 30, 12, 10, 8),
(8, 'Classic', 379.99, 18, 7, 8),
(9, 'HeatGear', 220, 25, 5, 6),
(10, 'World', 60, 10, 6, 6);

insert into ITEM (id_PRODUTO, id_COMPRA, valor, quantidade)
values
(1, 1, 3499, 2),
(2, 2, 2199.99, 1),
(3, 2, 3099.99, 1),
(4, 3, 4000, 1),
(5, 4, 400, 3),
(6, 5, 375, 2),
(7, 6, 30, 1),
(8, 6, 379.99, 1),
(9, 7, 220, 2),
(10, 8, 60, 1),
(10, 9, 60, 1),
(7, 9, 30, 1),
(2, 10, 2599.99, 2);
```


<br><br>
### 9	TABELAS E PRINCIPAIS CONSULTAS<br>
#### 9.1	CONSULTAS DAS TABELAS COM TODOS OS DADOS INSERIDOS (Todas) <br>
Tabela CLIENTE
```sql
select * from CLIENTE order by id
```
![image](https://github.com/gavazzantonio/Trabalho-de-BD1/assets/94766580/d18ffd64-105e-47df-a49d-b554c5ac3ed4)

Tabela COMPRA
```sql
select * from COMPRA order by id
```
![image](https://github.com/gavazzantonio/Trabalho-de-BD1/assets/94766580/e6c02d56-aeed-4c0c-9da0-35691fba835c)

Tabela ITEM
```sql
select * from ITEM order by id_compra
```
![image](https://github.com/gavazzantonio/Trabalho-de-BD1/assets/94766580/55b78fff-bf85-4904-af07-df9df4be2e1e)

Tabela PRODUTO
```sql
select * from PRODUTO order by id
```
![image](https://github.com/gavazzantonio/Trabalho-de-BD1/assets/94766580/1fcb91bf-d4cd-43db-a3b0-dc2f09e6f3c7)

Tabela MARCA
```sql
select * from MARCA order by id
```
![image](https://github.com/gavazzantonio/Trabalho-de-BD1/assets/94766580/7c814503-440a-4a2a-8eae-cddff7a99b23)

Tabela CATEGORIA
```sql
select * from CATEGORIA order by id
```
![image](https://github.com/gavazzantonio/Trabalho-de-BD1/assets/94766580/012acaac-abad-423c-b34c-2e25fb0ae11a)

># Marco de Entrega 01: Do item 1 até o item 9.1<br>

<br><br>
#### 9.2	CONSULTAS DAS TABELAS COM FILTROS WHERE (Mínimo ~4~(2))<br>
##### Leads de clientes do estado de São Paulo
```sql
select nome, email, telefone
from cliente
where endereco_estado = 'SP'
```
![image](https://github.com/gavazzantonio/Trabalho-de-BD1/assets/94766580/ea232530-4d6f-424f-94e0-eeaba74d09bc)

##### Lista das categorias principais
```sql
select nome
from categoria
where id_categoria is null
```
![image](https://github.com/gavazzantonio/Trabalho-de-BD1/assets/94766580/cfc14166-dd3a-473e-ad14-e31d43e879cd)

<br><br>
#### 9.3	CONSULTAS QUE USAM OPERADORES LÓGICOS, ARITMÉTICOS E TABELAS OU CAMPOS RENOMEADOS (Mínimo ~11~(6))
    a) Criar 3 consultas que envolvam os operadores lógicos AND, OR e Not
##### Leads de clientes que moram na cidade de Rio de Janeiro, no estado de RJ
```sql
select nome, email, telefone
from cliente
where endereco_estado= 'RJ' and endereco_cidade = 'Rio de Janeiro'
```
![image](https://github.com/gavazzantonio/Trabalho-de-BD1/assets/94766580/cf24e8a3-bc6f-4b6a-9ee6-55a535edc219)

##### Produtos que custam menos de R$100 ou mais de R$1000
```sql
select nome, to_char(valor, 'FM999999999.00') as valor
from produto
where valor < 100 or valor > 1000 
```
![image](https://github.com/gavazzantonio/Trabalho-de-BD1/assets/94766580/5722e9d0-7b47-442b-b805-5d6b6352eee0)

##### Lista de subcategorias
```sql
select nome
from categoria
where id_categoria is not null
```
![image](https://github.com/gavazzantonio/Trabalho-de-BD1/assets/94766580/d0c06cc1-fbe0-4006-9d61-de5b95cb5602)

    b) Criar no mínimo 1 consultas com operadores aritméticos 
##### Itens vendido, com valor unitário, quantidade e total por item
```sql
select id_compra, id_produto, quantidade as qtd, 
    to_char(valor,'FM999999999.00') as valor, 
    to_char(quantidade*valor,'FM999999999.00') as total
from item
```
![image](https://github.com/gavazzantonio/Trabalho-de-BD1/assets/94766580/4e193fd2-3372-4631-8dd4-0776c339cf1c)

    c) Criar no mínimo 2 consultas com operação de renomear nomes de campos ou tabelas
##### Informações de endereço do cliente reunido em um único campo
```sql
select nome, endereco_logradouro||', '||endereco_numero||', '||endereco_bairro||', '||endereco_cidade||'/'||endereco_estado||', '||endereco_cep as endereco_completo
from cliente
```
![image](https://github.com/gavazzantonio/Trabalho-de-BD1/assets/94766580/f10fde7c-9264-420a-b400-3e08b1bde1b1)

##### Relação de categorias
```sql
select categoria_mae.nome as categoria_principal, categoria.nome as categoria
from categoria inner join categoria as categoria_mae on categoria.id_categoria = categoria_mae.id 
```
![image](https://github.com/gavazzantonio/Trabalho-de-BD1/assets/94766580/b93b5533-344c-4ff4-b8a0-a61c3453199b)

<br><br>
#### 9.4	CONSULTAS QUE USAM OPERADORES LIKE E DATAS (Mínimo ~12~(6)) <br>
    a) Criar outras 2 consultas que envolvam like ou ilike
##### Leads dos clientes que possuem o nome/sobrenome Santos
```sql
select nome, email, telefone
from cliente
where nome like '%Santos%'
```
![image](https://github.com/gavazzantonio/Trabalho-de-BD1/assets/94766580/621447fe-843d-4625-af64-61179a0aeee9)

##### Valor dos produtos que tenham que podem ter sido nomeadods como iphone/iPhone
```sql
select nome, to_char(valor,'FM999999999.00') as valor
    from produto
    where nome ilike '%iphone%'
```
![image](https://github.com/gavazzantonio/Trabalho-de-BD1/assets/94766580/892f0dc4-a793-4b70-b87a-d9a1dc018346)

    b) Criar 4 consultas com funções data apresentada.
#### Lista de clientes que realizaram compras na 2ª quinzena de julho/2023
```sql
select compra.id, nome, to_char(data_compra,'DD/MM/YYYY') as data
from compra inner join cliente on id_cliente = cliente.id
where data_compra >= '2023-06-15'
```
![image](https://github.com/gavazzantonio/Trabalho-de-BD1/assets/94766580/4600d713-fb1a-4c3e-8a42-51d82b9dd87e)
 
#### Leads de clientes ordenado pela idade
```sql
select nome, date_part('year',age(current_date, nascimento)) as idade, email, telefone
from CLIENTE
order by nascimento desc
```
![image](https://github.com/gavazzantonio/Trabalho-de-BD1/assets/94766580/719be6bd-86aa-4f86-afec-02cd9816c4e8)

#### Lista de compras realizadas com indicação do cliente, compra anterior e dias entre compras do mesmo cliente
```sql
select nome, data_compra, 
	(
		select sub_compra.data_compra
		from compra as sub_compra
		where sub_compra.id_cliente = compra.id_cliente and sub_compra.data_compra < compra.data_compra
		limit 1
	) as ultima_compra,
	date_part('day',age(data_compra,
	(
		select sub_compra.data_compra
		from compra as sub_compra
		where sub_compra.id_cliente = compra.id_cliente and sub_compra.data_compra < compra.data_compra
		limit 1
	))) as dias_entre_compras
from compra inner join cliente on id_cliente = cliente.id
order by data_compra
```
 ![image](https://github.com/gavazzantonio/Trabalho-de-BD1/assets/94766580/c4212346-0d90-482f-be9d-0a1eff87bbc2)

##### Quantidade de clientes aniversariantes por mês (atualização 9.5.b.3 realizada anterior a esta consulta)
```sql
select extract(month from nascimento) as mês, count(*) as qtd
from cliente
group by extract(month from nascimento)
```
 ![image](https://github.com/gavazzantonio/Trabalho-de-BD1/assets/94766580/92e3703e-53b9-44c9-afe3-fe0608e76bc3)

<br><br>
#### 9.5	INSTRUÇÕES APLICANDO ATUALIZAÇÃO E EXCLUSÃO DE DADOS (Mínimo ~6~(3))<br>
    a) Criar minimo 2 de exclusão
##### Exclusão dos dados de um cliente cujo id = 9 (consulta na tabela CLIENTE após atualização)
```sql
delete from cliente where id = 9;
select * from CLIENTE order by id
```
![image](https://github.com/gavazzantonio/Trabalho-de-BD1/assets/94766580/d1ce804d-fa30-41b3-baa7-549472d442ff)

##### Exclusão da subcategoria 'Futebol' (consulta na tabela CATEGORIA após atualização)
```sql
delete from CATEGORIA where nome = 'Futebol';
select * from CATEGORIA order by id
```
![image](https://github.com/gavazzantonio/Trabalho-de-BD1/assets/94766580/b713539c-b86e-450f-abf0-a6b579f1e10d)

    b) Criar minimo 2 de atualização
##### Atualização de valores de alguns produtos (consulta na tabela PRODUTO após atualização)
```sql
update produto set valor = 3999 where id = 1;
update produto set valor = 2599.99 where id = 2;
update produto set valor = 3499.99 where id = 3;
update produto set valor = 4700 where id = 4;
update produto set valor = 449.99 where id = 5;
update produto set valor = 475 where id = 6;
select * from PRODUTO order by id
```
![image](https://github.com/gavazzantonio/Trabalho-de-BD1/assets/94766580/21da729e-f1d9-42b0-997e-54c0d29c7f01)

##### Atualização da categoria principal 'Esportes' para uma subcategoria da categoria 'Roupas'
```sql
update CATEGORIA set id_categoria = 5 where id = 9;
select * from CATEGORIA order by id
```
 ![image](https://github.com/gavazzantonio/Trabalho-de-BD1/assets/94766580/994d1174-7bfd-4b04-8030-51fe773e19bd)

 ##### Atualização de data de aniversário de cliente (consulta na tabela CLIENTE após atualização)
```sql
update cliente set nascimento = '1995-08-05' where id = 5;
select * from CLIENTE order by id
```
 ![image](https://github.com/gavazzantonio/Trabalho-de-BD1/assets/94766580/368f5a02-e70b-4434-aa5a-9a73533a0511)

<br><br>
#### 9.6	CONSULTAS COM INNER JOIN E ORDER BY (Mínimo ~6~(3))<br>
    a) Uma junção que envolva todas as tabelas possuindo no mínimo 2 registros no resultado
##### Lista de todas as compras/itens
```sql
select cpf, cliente.nome as nome_cliente, compra.id as compra, to_char(compra.data_compra,'DD/MM/YYYY') as data_compra, categoria_mae.nome as categoria,
	categoria.nome as subcategoria, item.quantidade as qtd, marca.nome as marca, produto.nome as produto,
	to_char(item.valor,'FM999999999.00') as valor, to_char(item.valor*item.quantidade,'FM999999999.00') as total_item
from compra 
	inner join cliente on compra.id_cliente = cliente.id
	inner join item on item.id_compra = compra.id 
	inner join produto on item.id_produto = produto.id 
	inner join marca on produto.id_marca = marca.id
	inner join categoria on produto.id_categoria = categoria.id
	inner join categoria as categoria_mae on categoria.id_categoria = categoria_mae.id
order by compra.id
```
![image](https://github.com/gavazzantonio/Trabalho-de-BD1/assets/94766580/99e5a6df-4f52-45b9-ae67-d67100200249)


    b) Outras 2 junções que o grupo considere como sendo as de principal importância para o trabalho
##### Lista com o resumo de todas as compras
```sql
select cpf, nome as nome_cliente, compra.id as compra, to_char(compra.data_compra,'DD/MM/YYYY') as data_compra,
	sum(quantidade) as qtd_itens, to_char(sum(valor),'FM999999999.00') as valor_compra
from compra 
	inner join cliente on compra.id_cliente = cliente.id
	inner join item on item.id_compra = compra.id
group by cpf, nome, compra.id
order by compra.id
```
![image](https://github.com/gavazzantonio/Trabalho-de-BD1/assets/94766580/8a3488bc-a21b-47b8-820d-083ce3b13865)

##### Lista com informações dos produtos por categoria e quantidade em estoque
```sql
select categoria_mae.nome as categoria, categoria.nome as subcategoria, marca.nome as marca, produto.nome as produto, to_char(valor,'FM999999999.00') as valor, 
	quantidade-(select sum(quantidade) from item where item.id_produto = produto.id) as qtd_estoque
from categoria 
	inner join categoria as categoria_mae on categoria.id_categoria = categoria_mae.id
	inner join produto on produto.id_categoria = categoria.id 
	inner join marca on produto.id_marca = marca.id
order by categoria_mae.nome, categoria.nome, marca.nome, produto.nome
```
![image](https://github.com/gavazzantonio/Trabalho-de-BD1/assets/94766580/49142ed2-7a39-4b6f-955d-cb2dc01eeac8)

<br><br>
#### 9.7	CONSULTAS COM GROUP BY E FUNÇÕES DE AGRUPAMENTO (Mínimo ~6~(3))<br>
    a) Criar minimo 2 envolvendo algum tipo de junção
##### Quantidade de itens comprados e valor total gasto por cliente
```sql
select nome, sum(quantidade) as itens_comprado, 
	to_char(sum(valor),'999999999.00') as total_gasto
from cliente
	inner join compra on compra.id_cliente = cliente.id 
	inner join item on item.id_compra = compra.id 
group by nome
```
 ![image](https://github.com/gavazzantonio/Trabalho-de-BD1/assets/94766580/b6a00f2c-35c4-48c2-8155-f03b6d1f0fac)

##### Quantidade de clientes por cidade
```sql
select endereco_cidade as cidade, endereco_estado as UF, count(*)
from cliente
group by endereco_cidade, endereco_estado
```
![image](https://github.com/gavazzantonio/Trabalho-de-BD1/assets/94766580/809e58ce-f7ab-4750-a205-87a0d75f38c3)

##### Quantidades de produtos por categoria
```sql
select categoria_mae.nome as categoria, categoria.nome as subcategoria, count(*) as qtd
from categoria 
	inner join produto on produto.id_categoria = categoria.id 
	inner join categoria as categoria_mae on categoria.id_categoria = categoria_mae.id
group by categoria_mae.nome, categoria.nome
order by categoria_mae.nome
 ```
![image](https://github.com/gavazzantonio/Trabalho-de-BD1/assets/94766580/c7cc6d3e-a230-4196-9755-106f612eb63f)

<br><br>
#### 9.8	CONSULTAS COM LEFT, RIGHT E FULL JOIN (Mínimo ~4~(2))<br>
	a) Criar minimo 1 de cada tipo
##### Relação de clientes e compras
```sql
select nome, compra.id, data_compra
from cliente left join compra on compra.id_cliente = cliente.id
order by nome, compra.id
```
![image](https://github.com/gavazzantonio/Trabalho-de-BD1/assets/94766580/b4236fa7-78e6-445a-a212-7abf622b6edc)

##### Todos os registros de categorias com a existência ou não de categoria mãe
```sql
select categoria.nome as categoria, subcategoria.nome as subcategoria
from categoria right join categoria as subcategoria on categoria.id = subcategoria.id_categoria
order by categoria.nome desc
```
 ![image](https://github.com/gavazzantonio/Trabalho-de-BD1/assets/94766580/feb50356-ab72-4e88-a5c9-02b3bd49c788)

<br><br>
#### 9.9	CONSULTAS COM SELF JOIN E VIEW (Mínimo ~6~(3))<br>
        a) Uma junção que envolva Self Join (caso não ocorra na base justificar e substituir por uma view)
##### Categorias e subcategorias
```sql
select categoria.nome as categoria, subcategoria.nome as subcategoria
from categoria inner join categoria as subcategoria on categoria.id = subcategoria.id_categoria
order by categoria.nome
```
 ![image](https://github.com/gavazzantonio/Trabalho-de-BD1/assets/94766580/4c38d597-0ec5-4c0c-9e8d-fe851d5dccf1)

  
        b) Uma junções com views que o grupo considere como sendo de relevante importância para o trabalho
##### View que trás os detalhes das compras realizadas
```sql
create view compra_detalhe as (
		select cpf, cliente.nome as nome_cliente, compra.id as compra, to_char(compra.data_compra,'DD/MM/YYYY') as data_compra, categoria_mae.nome as categoria,
			categoria.nome as subcategoria, item.quantidade as qtd, marca.nome as marca, produto.nome as produto,
			to_char(item.valor,'FM999999999.00') as valor, to_char(item.valor*item.quantidade,'FM999999999.00') as total_item
		from compra 
			inner join cliente on compra.id_cliente = cliente.id
			inner join item on item.id_compra = compra.id 
			inner join produto on item.id_produto = produto.id 
			inner join marca on produto.id_marca = marca.id
			inner join categoria on produto.id_categoria = categoria.id
			inner join categoria as categoria_mae on categoria.id_categoria = categoria_mae.id
		order by compra.id
	);

select * from compra_detalhe where nome_cliente like '%Maria%'
 ```
![image](https://github.com/gavazzantonio/Trabalho-de-BD1/assets/94766580/9ec90102-2d6b-4958-be4a-db966c9cfc4d)


 ##### View que trás um resumo das compras realizadas
```sql
create view compra_resumo as (
		select cpf, nome as nome_cliente, compra.id as compra, to_char(compra.data_compra,'DD/MM/YYYY') as data_compra,
			sum(quantidade) as qtd_itens, to_char(sum(valor),'FM999999999.00') as valor_compra
		from compra 
			inner join cliente on compra.id_cliente = cliente.id
			inner join item on item.id_compra = compra.id
		group by cpf, nome, compra.id
		order by compra.id
	);

select * from compra_resumo where nome_cliente like '%Maria%'
```
![image](https://github.com/gavazzantonio/Trabalho-de-BD1/assets/94766580/66c38ad2-a904-4eb9-9684-9c29bb169fe0)

<br><br>
#### 9.10	SUBCONSULTAS (Mínimo ~4~(2))<br>
     a) Criar 1 envolvendo GROUP BY
##### Lista de produtos vendidos com quantidade vendida, a inflação entre valores praticados em vendas anteriores e o valor atual e a quantidade em estoque
```sql
select categoria_mae.nome as categoria, categoria.nome as subcategoria, marca.nome as marca, produto.nome as produto,
	(select sum(quantidade) from item as sub_item where sub_item.id_produto = produto.id) as qtd_vendido, 
	to_char(produto.valor,'FM999999999.00') as valor_atual,
	round((produto.valor / (select min(valor) from item as sub_item where sub_item.id_produto = produto.id)-1)*100)||'%' as inflação, 
	produto.quantidade - (select sum(quantidade) from item as sub_item where sub_item.id_produto = produto.id) as qtd_estoque
from compra 
	inner join item on item.id_compra = compra.id 
	inner join produto on item.id_produto = produto.id
	inner join marca on produto.id_marca = marca.id 
	inner join categoria on produto.id_categoria = categoria.id 
	inner join categoria as categoria_mae on categoria.id_categoria = categoria_mae.id
group by categoria_mae.nome, categoria.nome, marca.nome, produto.nome, produto.valor,
	(select sum(quantidade) from item as sub_item where sub_item.id_produto = produto.id),
	round((produto.valor / (select min(valor) from item as sub_item where sub_item.id_produto = produto.id)-1)*100)||'%',
	produto.quantidade - (select sum(quantidade) from item as sub_item where sub_item.id_produto = produto.id)
order by categoria_mae.nome, categoria.nome, marca.nome
```
![image](https://github.com/gavazzantonio/Trabalho-de-BD1/assets/94766580/cc785a17-da8d-410c-9af3-7293ea339b9d)

     b) Criar 1 envolvendo algum tipo de junção
##### Lista as categorias e, para cada uma, a quantidade de itens vendidos e o valor de faturamento
```sql
 select categoria.nome as categoria, 
		(	select sum(sub_item.quantidade) 
			from item as sub_item inner join produto as sub_produto on sub_item.id_produto = sub_produto.id 
			where sub_produto.id_categoria = categoria.id
		) as qtd_vendido,
		to_char(
			(	select sum(sub_item.valor) 
				from item as sub_item inner join produto as sub_produto on sub_item.id_produto = sub_produto.id 
				where sub_produto.id_categoria = categoria.id
			), 'FM999999999.00'
		) as faturamento
	from categoria
	where id_categoria is not null
```
![image](https://github.com/gavazzantonio/Trabalho-de-BD1/assets/94766580/7c32d565-0924-4260-8f29-5c8e3f5e8e8f)

># Marco de Entrega 02: Do item 9.2 até o ítem 9.10<br>

<br><br>
### 10 RELATÓRIOS E GRÁFICOS
[Relatórios no Google Colab](https://colab.research.google.com/drive/1HDbq9VZhicx5eGRgxcLQ9tj3wVxBK0BL?usp=sharing)
   
<br><br>
### 11	AJUSTES DA DOCUMENTAÇÃO, CRIAÇÃO DOS SLIDES E VÍDEO PARA APRESENTAÇAO FINAL <br>

#### a) Modelo (pecha kucha)<br>
#### b) Tempo de apresentação 6:40 

># Marco de Entrega 03: Itens 10 e 11   <br><br>      <br><br>   

<br><br>
### 12 FORMATACAO NO GIT:<br> 
https://help.github.com/articles/basic-writing-and-formatting-syntax/
<comentario no git>
    
##### About Formatting
    https://help.github.com/articles/about-writing-and-formatting-on-github/
    
##### Basic Formatting in Git
    
    https://help.github.com/articles/basic-writing-and-formatting-syntax/#referencing-issues-and-pull-requests
    
    
##### Working with advanced formatting
    https://help.github.com/articles/working-with-advanced-formatting/
#### Mastering Markdown
    https://guides.github.com/features/mastering-markdown/

<br><br>    
### OBSERVAÇÕES IMPORTANTES

#### Todos os arquivos que fazem parte do projeto (Imagens, pdfs, arquivos fonte, etc..), devem estar presentes no GIT. Os arquivos do projeto vigente não devem ser armazenados em quaisquer outras plataformas.
1. <strong>Caso existam arquivos com conteúdos sigilosos<strong>, comunicar o professor que definirá em conjunto com o grupo a melhor forma de armazenamento do arquivo.

#### Todos os grupos deverão fazer Fork deste repositório e dar permissões administrativas ao usuário do git "profmoisesomena", para acompanhamento do trabalho.

#### Os usuários criados no GIT devem possuir o nome de identificação do aluno (não serão aceitos nomes como Eu123, meuprojeto, pro456, etc). Em caso de dúvida comunicar o professor.


Link para BrModelo:<br>
http://www.sis4.com/brModelo/download.html   <br><br>   

Link para curso de GIT<br>
![https://www.youtube.com/curso_git](https://www.youtube.com/playlist?list=PLo7sFyCeiGUdIyEmHdfbuD2eR4XPDqnN2?raw=true "Title")


