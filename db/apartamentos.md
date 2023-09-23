# Apartamentos

No esquema de banco de dados demonstrado a seguir, conside as seguintes suposições:
- Cada apartamento pode ter vários inquilinos e cada inquilino pode ter vários apartamentos. 
- Cada apartamento pertence a um único prédio e cada prédio pertencente a um único condomínio.

## Apartamentos

###  Esquema
|Nome da coluna  |  Tipo dos dados|
|--|--|
| IdApt | int  |
| Unidade | varchar(10)  |
| IdPredio | int  |

### Exemplo de dados
| IdApt |  Unidade | Id Predio |
|--|--|--|
| 1 | 101A  | 1 |
| 2 | 101A  |2 |
| 3 | 201B  |1 |
| 4 | 201A | 1|
| 5 | 401A | 3|

## Predios
### Esquema
|Nome da coluna  |  Tipo dos dados|
|--|--|
| IdPredio | int  |
| IdCondominio | int  |
| NomePredio | varchar(10)  |

### Exemplo de dados
| IdPredio |  IdCondominio | NomePredio |
|--|--|--|
| 1 | 1  | Torre 01 |
| 2 | 1  | Torre 02 |
| 3 | 2  | Bloco A |
| 4 | 2 |  Bloco B |
| 5 | 2 |  Bloco C |

## Contratos
### Esquema
|Nome da coluna  |  Tipo dos dados|
|--|--|
| IdContrato | int  |
| Status | varchar(100)  |
| IdApt | int  |
| Descricao | varchar(500)  |

### Exemplo de dados
| IdContrato |  Status | IdApt | Descricao |
|--|--|--|--|
| 1 | Em Análise  | 1 |
| 2 | Aprovado  | 2|
| 3 | Rejeitado  | 3 |
| 4 | Aprovado |  3 |
| 5 | Aprovado |  4 |

## Condominios
### Esquema
|Nome da coluna  |  Tipo dos dados|
|--|--|
| IdCondominio | int  |
| NomeCondominio | varchar(100)  |
### Exemplo de dados
| IdCondominio |  NomeCondominio  |
|--|--|
| 1 | Portal da Cidade |
| 2 | Mundi  |
| 3 | Condominio Laranjeiras  |

## AptInquilinos
### Esquema
|Nome da coluna  |  Tipo dos dados|
|--|--|
| IdInquilino | int  |
| IdApt | int  |
### Exemplo de dados
| IdInquilino |  IdApt  |
|--|--|
| 1 | 1|
| 1| 2  |
| 2| 3 |
| 3| 4 |

## Inquilinos
### Esquema
|Nome da coluna  |  Tipo dos dados|
|--|--|
| IdInquilino | int  |
| Nome | varchar(100)|
### Exemplo de dados
| IdInquilino |  Nome  |
|--|--|
| 1 | Joao Silva |
| 2| Maria Pessoa  |
| 3| Joana Costa |
|4 | Felipe Paiva |
