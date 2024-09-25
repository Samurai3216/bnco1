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