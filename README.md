# Codigo-Banco-de-dados

create database atividade;
use atividade;

describe ator;
describe filme;
describe personagem;


create table ator (
	codAtor varchar(3) primary key,
    nomeArtistico varchar(40) not null,
    nomeReal varchar(40) not null,
    nacionalidade varchar(20) not null,
    sexo char(1) not null,
    idade int not null,
    indicacaoOscar int,
    oscar int
);

create table filme (
	codFilme varchar(3) primary key,
    nomeFilme varchar(40) not null,
    anoFilme int not null,
    orcamento int not null,
    tempo int not null
);

create table personagem (
	codFilme varchar(3) not null,
    codAtor varchar(3) not null,
    personagem varchar(40) not null,
    cache int not null,
    primary key (codFilme, codAtor, personagem, cache),
    foreign key (codFilme) references filme(codFilme),
    foreign key (codAtor) references ator(codAtor)
);

select * from filme;
select * from ator;

insert into filme values 
('f1', 'A Jurada', '1996', '1000000', '18'),
('f10', 'Cidade das Sombras', '1997', '10000000', '7'),
('f11', 'Irresistível Paixão', '1998', '10000000', '10'),
('f12', 'A Máscara do Zorro', '1998', '11000000', '11'),
('f13', 'Quem vai ficar com Marry?', '1997', '6000000', '8'),
('f14', 'O Resgate do Soldado Ryan', '1997', '10000000', '7'),
('f15', 'O Show de Truman', '1998', '10000000', '14'),
('f16', 'Batman, o Filme', '1995', '10000000', '9'),
('f17', 'Filadélfia', '1996', '10000000', '6'),
('f18', 'O Máscara', '1995', '6000000','7'),
('f19', 'O Beijo da Mulher Aranha', '1990', '8000000','24'),
('f2', 'A Letra Escarlate', '1995', '10000000','24'),
('f20', 'O Pacificador', '1997', '10000000','15'),
('f21', 'Ace Ventura', '1995', '7000000','12'),
('f22', 'Chaplin', '1993', '8000000','14'),
('f23', 'Batman e Robin', '1997', '10000000','20'),
('f24', 'Strip Tease', '1996', '7000000','12'),
('f25', 'Passageiro 57', '1993', '200000000','15'),
('f26', 'Forrest Gump', '1996', '90000000','15'),
('f3', 'Seven', '1995', '15000000','20'),
('f4', 'Tootsie', '1982', '5000000','16'),
('f5', 'Tieta', '1995', '2000000','18'),
('f6', 'Código de Violência', '1997', '10000000','15'),
('f7', 'Quando o Amor Acontece', '1998', '5000000','12'),
('f8', 'A vingança de Bette', '1998', '10000000','9'),
('f9', 'Blade, o Caçador de Vampiros', '1998', '100000000','18');

INSERT INTO ator VALUES
('a1', 'Demi Moore', 'Maria da Silva', 'USA', 'F', 32, NULL, NULL),
('a10', 'Willian Hurt', 'Willian Ernst Hurt', 'USA', 'M', 45, 2, 1),
('a11', 'George Clooney', 'George Costa Smith', 'USA', 'M', 37, 1, NULL),
('a12', 'Jennifer Lopez', 'Maria Conchita Lopez', 'México', 'F', 32, NULL, NULL),
('a13', 'Antony Hopkins', 'Antony Richard Hopcroft', 'USA', 'M', 65, 6, 3),
('a14', 'Antônio Banderas', 'Antônio Augusto Banderas', 'Espanha', 'M', 34, NULL, NULL),
('a15', 'Tom Hanks', 'Antony Hanks', 'USA', 'M', 45, 1, 1),
('a16', 'Matt Damon', 'Matthew Louis Damon', 'USA', 'M', 32, 1, NULL),
('a17', 'Jim Carrey', 'James Carrey', 'USA', 'M', 40, NULL, NULL),
('a18', 'Nicole Kidman', 'Susan West', 'Austrália', 'F', 33, NULL, NULL),
('a19', 'Val Kilmer', 'Valerio Soza Kilmer', 'Porto Rico', 'M', 40, NULL, NULL),
('a2', 'Brad Pitt', 'João Paulo', 'USA', 'M', 28, 1, NULL),
('a20', 'Cameron Diaz', 'Esperanza Diaz', 'Costa Rica', 'F', 29, NULL, NULL),
('a21', 'Holly Hunter', 'Susan Richards', 'USA', 'F', 33, 1, 1),
('a22', 'Richard Gere', 'Richard Gere', 'USA', 'M', 56, NULL, NULL),
('a3', 'Jessica Lange', 'Jessica Lange', 'USA', 'F', 42, 2, 2),
('a4', 'Dustin Hoffman', 'Dustin Hoffman', 'USA', 'M', 56, 2, NULL),
('a5', 'Sônia Braga', 'Sônia Braga', 'Brasil', 'F', 45, NULL, NULL),
('a6', 'Samuel Jackson', 'Samuel L. Jackson', 'USA', 'M', 60, NULL, NULL),
('a7', 'Sandra Bullock', 'Sandra Bullock', 'USA', 'F', 30, 2, NULL),
('a8', 'Harry Cornick Jr.', 'Harry Cornick Jr.', 'USA', 'M', 40, NULL, NULL),
('a9', 'Wesley Snipes', 'Wesley Snipes', 'USA', 'M', 31, 1, NULL);
