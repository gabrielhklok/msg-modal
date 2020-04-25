# msg-modal

Fun��o para mostrar uma modal desenvolvida na linguagem TL++ (Linguagem propriet�ria da TOTVS).

<br />

1. [Defini��o](#Defini��o)
1. [Parametros](#Parametros)
1. [Compila��o](#Compila��o)
    - [Sem include](#Sem\ include)
    - [Com include](#Com\ include)
1. [Exemplos](#Exemplos)

<br />

## Defini��o
Fun��o destinada a substituir fun��es padr�es TOTVS Protheus como 'msginfo', 'msgstop', 'msgalert', 'msgyesno', 'msgnoyes', al�m de implementar um modal com �cone de sucesso. � de conhecimento que j� existem fun��es padr�es que executam as fun��es acima citadas, entre tanto s�o fun��es separadas e n�o possuem o �cone de sucesso, atrav�s da fun��o aqui desenvolvida podemos centralizar as mensagem modal e manter a aparencia do sistema padr�o.

<br />

## Parametros
Confira abaixo as valores poss�veis assim como as regras de obrigatoriedade.
Par�metro | Tipo | Valores poss�veis | Valor default | Obrigat�rio
:-------------:|:-------------:|:-------------:|:-------------:|:-------------:
cMessage | caracter | Texto | | x
cTitle | caracter | Texto | " " |
nTypeIcon | num�rico |1 = Sucesso<br>2 = Alerta<br>3 = Erro<br>4 = Informa��o | 4 |
nTypeButton | num�rico |1 = Fechar<br>2 = Sim/N�o<br>3 = N�o/Sim | 1 |

<br />

## Compila��o
### Sem include
Para fazer uso da fun��o como fun��o de usu�rio padr�o, ou seja, utilizando 'U_' antes da chamada, basta compilar o fonte 'msgmodal.tlpp' e usar conforme o exemplo 1.

Ex.:  
```tlpp
U_msgmodal("message", "title", 1)
```


### Com include
Para utilizar a fun��o de forma personalizada sem o uso do 'U_' ou em forma de COMANDOS basta colocar o include 'msgmodal.ch' presente na pasta 'includes/' na sua pasta de includes e usar conforme o exemplo 2.

Ex. fun��o: 
```tlpp
msgmodal("message", "title", 1, 1)
```

Ex. comando:
```tlpp
MSG "message" TITLE "title" ICON 1 BUTTON 1
```
<br />

## Exemplos

Modal com �cone de sucesso.
![msgmodal-sucess](assets/msgmodal-sucess.png)
<br />

Modal com �cone de alerta.
![msgmodal-alert](assets/msgmodal-alert.png)
<br />

Modal com �cone de erro.
![msgmodal-error](assets/msgmodal-error.png)
<br />

Modal com �cone de informa��o.
![msgmodal-info](assets/msgmodal-info.png)
<br />

Modal com bot�es SIM/N�o com foco no SIM.
![msgmodal-yesno](assets/msgmodal-yesno.png)
<br />

Modal com bot�es N�O/SIM com foco no N�O.
![msgmodal-noyes](assets/msgmodal-noyes.png)