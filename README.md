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

<br> <br> 
#### 4.2 QUAIS PERGUNTAS PODEM SER RESPONDIDAS COM O SISTEMA PROPOSTO?
> O Stock&Shop fornece, inicialmente, os seguintes relatórios:
* Relatório de vendas por período  -  apresenta informações sobre os pedidos realizados em um determinado período, incluindo o valor total das vendas, a quantidade de produtos vendidos e as informações dos clientes.
* Relatório de estoque  -  fornece uma visão geral do estoque atual, incluindo a quantidade disponível de cada produto, a data de compra e de vencimentos, o valor de compra e informações dos fornecedores.
* Relatório de clientes ativos  -  lista os clientes que realizaram pedidos recentemente, mostrando seus dados pessoais, quantidade de compras no período e valor total gasto.
* Relatório de produtos mais vendidos  -  lista os produtos que tiveram maior volume de vendas em um determinado período, fornecendo informações sobre o produto, a quantidade vendida, o valor total arrecadado.
* Relatório de retorno de produtos  -  fornece informações sobre os produtos devolvidos, o motivo da devolução, o número de devoluções por período, o valor total dos produtos devolvidos.

<br> <br> 
#### 4.3 TABELA DE DADOS DO SISTEMA:
    a) Esta tabela deve conter todos os atributos do sistema e um mínimo de 10 linhas/registros de dados.
![Tabela de dados do sistema Stock&Shop](https://github.com/discipbd1/trab01/blob/master/arquivos/TabelaEmpresaDevCom_sample.xlsx?raw=true "Tabela - Empresa Devcom")

<br><br>
### 5. MODELO CONCEITUAL:
![Alt text](https://github.com/gavazzantonio/Trabalho-de-BD1/blob/master/conceitual%20v1752.png "Modelo Conceitual")
    
<br><br> 
#### 5.1 Validação do Modelo Conceitual
    [Grupo01]: [Nomes dos que participaram na avaliação]
    [Grupo02]: [Nomes dos que participaram na avaliação]

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
### 7	MODELO FÍSICO
        a) inclusão das instruções de criacão das estruturas em SQL/DDL 
        (criação de tabelas, alterações, etc..) 
        
       
### 8	INSERT APLICADO NAS TABELAS DO BANCO DE DADOS<br>
        a) inclusão das instruções de inserção dos dados nas tabelas criadas pelo script de modelo físico
        (Drop para exclusão de tabelas + create definição de para tabelas e estruturas de dados + insert para dados a serem inseridos)
        b) Criar um novo banco de dados para testar a restauracao 
        (em caso de falha na restauração o grupo não pontuará neste quesito)
        c) formato .SQL


### 9	TABELAS E PRINCIPAIS CONSULTAS<br>
    OBS: Incluir para cada tópico as instruções SQL + imagens (print da tela) mostrando os resultados.<br>
#### 9.1	CONSULTAS DAS TABELAS COM TODOS OS DADOS INSERIDOS (Todas) <br>

># Marco de Entrega 01: Do item 1 até o item 9.1<br>

#### 9.2	CONSULTAS DAS TABELAS COM FILTROS WHERE (Mínimo 4)<br>
#### 9.3	CONSULTAS QUE USAM OPERADORES LÓGICOS, ARITMÉTICOS E TABELAS OU CAMPOS RENOMEADOS (Mínimo 11)
    a) Criar 5 consultas que envolvam os operadores lógicos AND, OR e Not
    b) Criar no mínimo 3 consultas com operadores aritméticos 
    c) Criar no mínimo 3 consultas com operação de renomear nomes de campos ou tabelas

#### 9.4	CONSULTAS QUE USAM OPERADORES LIKE E DATAS (Mínimo 12) <br>
    a) Criar outras 5 consultas que envolvam like ou ilike
    b) Criar uma consulta para cada tipo de função data apresentada.

#### 9.5	INSTRUÇÕES APLICANDO ATUALIZAÇÃO E EXCLUSÃO DE DADOS (Mínimo 6)<br>
    a) Criar minimo 3 de exclusão
    b) Criar minimo 3 de atualização

#### 9.6	CONSULTAS COM INNER JOIN E ORDER BY (Mínimo 6)<br>
    a) Uma junção que envolva todas as tabelas possuindo no mínimo 2 registros no resultado
    b) Outras junções que o grupo considere como sendo as de principal importância para o trabalho

#### 9.7	CONSULTAS COM GROUP BY E FUNÇÕES DE AGRUPAMENTO (Mínimo 6)<br>
    a) Criar minimo 2 envolvendo algum tipo de junção

#### 9.8	CONSULTAS COM LEFT, RIGHT E FULL JOIN (Mínimo 4)<br>
    a) Criar minimo 1 de cada tipo

#### 9.9	CONSULTAS COM SELF JOIN E VIEW (Mínimo 6)<br>
        a) Uma junção que envolva Self Join (caso não ocorra na base justificar e substituir por uma view)
        b) Outras junções com views que o grupo considere como sendo de relevante importância para o trabalho

#### 9.10	SUBCONSULTAS (Mínimo 4)<br>
     a) Criar minimo 1 envolvendo GROUP BY
     b) Criar minimo 1 envolvendo algum tipo de junção

># Marco de Entrega 02: Do item 9.2 até o ítem 9.10<br>

### 10 RELATÓRIOS E GRÁFICOS

#### a) análises e resultados provenientes do banco de dados desenvolvido (usar modelo disponível)
#### b) link com exemplo de relatórios será disponiblizado pelo professor no AVA
#### OBS: Esta é uma atividade de grande relevância no contexto do trabalho. Mantenha o foco nos 5 principais relatórios/resultados visando obter o melhor resultado possível.

    

### 11	AJUSTES DA DOCUMENTAÇÃO, CRIAÇÃO DOS SLIDES E VÍDEO PARA APRESENTAÇAO FINAL <br>

#### a) Modelo (pecha kucha)<br>
#### b) Tempo de apresentação 6:40 

># Marco de Entrega 03: Itens 10 e 11   <br><br>      <br><br>   




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

    
### OBSERVAÇÕES IMPORTANTES

#### Todos os arquivos que fazem parte do projeto (Imagens, pdfs, arquivos fonte, etc..), devem estar presentes no GIT. Os arquivos do projeto vigente não devem ser armazenados em quaisquer outras plataformas.
1. <strong>Caso existam arquivos com conteúdos sigilosos<strong>, comunicar o professor que definirá em conjunto com o grupo a melhor forma de armazenamento do arquivo.

#### Todos os grupos deverão fazer Fork deste repositório e dar permissões administrativas ao usuário do git "profmoisesomena", para acompanhamento do trabalho.

#### Os usuários criados no GIT devem possuir o nome de identificação do aluno (não serão aceitos nomes como Eu123, meuprojeto, pro456, etc). Em caso de dúvida comunicar o professor.


Link para BrModelo:<br>
http://www.sis4.com/brModelo/download.html   <br><br>   

Link para curso de GIT<br>
![https://www.youtube.com/curso_git](https://www.youtube.com/playlist?list=PLo7sFyCeiGUdIyEmHdfbuD2eR4XPDqnN2?raw=true "Title")


