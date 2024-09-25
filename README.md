# banco1
-- criando banco de dados
create database bdteste;

-- usar banco de dados

use bdteste;

-- criar tabelas
create table clientes (
codigo int primary key,
 nome varchar (100),
 email varchar (200),
 datanaci date
);

-- alter table clientes
 alter table clientes add cpf varchar(11);
 
 -- CRIAR TABELA produtos
 create table produtos (
codigo int primary key,
nome varchar(100),
preco decimal(10,2)
);
-- criar tabelas 
create table faturas (
codigo int primary key,
 dataCriacao date,
 valorFatura decimal (10,2)
);


-- auterar nome de coluna
alter table produtos rename column nome to nomeProdutos;




__________________________________________________________________________________




EXERCICIOS COMPLEMENTARES

-- 1. cria a tabela funcionarios
create table funcionarios (
    id int primary key,
    nome varchar(100),
    sobrenome varchar(100),
    salario decimal(10, 2)
);

-- 2. adiciona a coluna datanascimento à tabela funcionarios
alter table funcionarios
add datanascimento date;

-- 3. cria a tabela departamentos
create table departamentos (
    id int primary key,
    nome varchar(100)
);

-- 4. adiciona a coluna iddepartamento à tabela funcionarios
alter table funcionarios
add iddepartamento int;

-- 5. cria a tabela projetos
create table projetos (
    id int primary key,
    nomeprojeto varchar(100)
);


-- 6. cria a tabelalocacoes
create table alocacoes (
    id int primary key,
    idfuncionario int,
    idprojeto int
);

-- 7. renomeia a coluna sobrenome para apelido na tabela funcionarios
alter table funcionarios
rename column sobrenome to apelido;

-- 8. cria a tabela clientes
create table clientes (
    id int primary key,
    nomecliente varchar(100)
);

-- 9. adiciona a coluna idcliente à tabela projetos
alter table projetos
add idcliente int;

-- 10. cria a tabela enderecos
create table enderecos (
    id int primary key,
    rua varchar(255),
    cidade varchar(100),
    cep varchar(10)
);

-- 11. adiciona a coluna ideendereco à tabela funcionarios
alter table funcionarios
add ideendereco int;

-- 12. renomeia a coluna nomecliente para nomeempresa na tabela clientes
alter table clientes
rename column nomecliente to nomeempresa;

-- 13. cria a tabela pedidos
create table pedidos (
    id int primary key,
    datapedido date,
    idcliente int
);

-- 14. adiciona a coluna idcliente à tabela pedidos
alter table pedidos
add idcliente int;

-- 15cria a tabela itenspedido
create table itenspedido (
    id int primary key,
    idpedido int,
    idproduto int
);

-- 16. renomeia a coluna nomeproduto para descricaoproduto na tabela produtos
alter table produtos
rename column nomeproduto to descricaoproduto;

-- 17. cria a tabela estoques
create table estoques (
    id int primary key,
    quantidade int
);

-- 18 adiciona a coluna idproduto à tabela estoques
alter table estoques
add idproduto int;

-- 19. cria a tabela vendas
create table vendas (
    id int primary key,
    datavenda date,
    idcliente int
);

-- 20adiciona a coluna idcliente à tabela vendas
alter table vendas
add idcliente int;

