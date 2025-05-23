# SistemaUniversidade
<<<<<<< HEAD

create database sistema_universidade;

CREATE TABLE aluno (
id_aluno int not null primary key auto_increment,
cpf VARCHAR(20),
rg VARCHAR(15),
Nome VARCHAR(30),
email VARCHAR(30),
genero VARCHAR(15),
data_nascimento VARCHAR(15)
);

CREATE TABLE telefone_aluno (
id_telefone_aluno int not null primary key auto_increment,
telefone_aluno VARCHAR(20),
id_aluno int,
FOREIGN KEY(id_aluno) REFERENCES Aluno (id_aluno)
);

CREATE TABLE Professor (
id_professor int not null primary key auto_increment,
email VARCHAR(20),
rg VARCHAR(15),
genero VARCHAR(20),
nome VARCHAR(30),
cpf VARCHAR(20)
);

alter table professor add id_aluno int;
alter table professor add constraint fk_aluno_professor foreign KEY (id_aluno) REFERENCES aluno (id_aluno);


CREATE TABLE telefone_professor (
id_telefone_professor int not null primary key auto_increment,
telefone_professor VARCHAR(20),
id_professor int,
FOREIGN KEY (id_professor) REFERENCES professor (id_professor)
);

CREATE TABLE endereco (
id_endereco int not null primary key auto_increment,
lougradouro VARCHAR(40),
bairro VARCHAR(20),
estado VARCHAR(20),
cep VARCHAR(10),
cidade VARCHAR(20),
pais VARCHAR(20),
id_aluno int,
id_professor int,

constraint fk_aluno_endereco
     foreign key (id_aluno)
     references aluno (id_aluno),
=======
>>>>>>> d8b0352d3729280b6d88529015b4301e87eea958
     
