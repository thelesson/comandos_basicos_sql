# comandos_basicos_sql
comandos básicos sql mais utilizados



/**Criando um banco de dados**/
CREATE DATABASE nome_tabela;

/**Selecionando todos os registro de uma tabela**/
SELECT * FROM nome_tabela;

/**Selecionando registro de uma tabela utilizando a condição where **/
SELECT * FROM nome_tabela WHERE nome_Campo = '1';

/**Selecionando registro pelo intervalo entre duas datas**/
SELECT * FROM nome_tabela WHERE nome_campo BETWEEN '01-01-2015' and '31-12-2017';
SELECT valor, data, observacoes, recebido FROM compras WHERE data BETWEEN '2008-02-19' AND '2009-03-21';

/**Criando um registro do tipo enum**/
create type enum_satisfacao as enum('muito_satisfeito', 'satisfeito','insatisfeito');
alter table compras add column satisfacao enum_satisfacao;

/** Adicionando uma coluna nova na tabela**/
alter table nome_tabela add column nome_coluna tipo_dados(11);

/**Alterando uma coluna na tabela**/

/**Deletando um registro**/
delete * from nome_tabela where nome_campo = valor;

/**Contando registros**/
select count(*) as quantidade_registros from nome_tabela;

/**Calculando a média de valores**/
select avg(campo_valor) as media from nome_tabela;

/**Somando valores**/
select sum(campo_valor) as total_soma from nome_tabela;

/**Recuperando o meno valor**/
select min(campo_Valor) from nome_tabela;

/**Recuperando o maior valor**/
select max(campo_valor) from nome_tabela;

/**Ordenar registro pro ordem crescente**/
select * from nome_tabela order by nome_campo asc;

/**Ordenar registro por ordem descrecente**/
select * from compras order by id desc;

/**Utilizando a clausula JOIN para juntar informações de 2 tabelas**/
select * from tabela_A a JOIN tabela_B b on a.id_loja = b.id;
select * JOIN tabela1 on tabela1.id_loja = tabela2.id;

/** **/
/** **/
/** **/
/** **/
/** **/
/** **/
