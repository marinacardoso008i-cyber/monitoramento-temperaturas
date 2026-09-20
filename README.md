# Monitoramento de Temperaturas

## Identificação

**Nome do aluno:** Marina Alves
**Disciplina:** Algoritmos e Pensamento Computacional
**Professora:** Profa. Karla Sartin
**Título do projeto:** Monitoramento de Temperaturas

## Descrição do projeto

Este projeto foi desenvolvido em linguagem C com o objetivo de criar um sistema simples para monitoramento de temperaturas.

O programa recebe temperaturas informadas pelo usuário e continua realizando o monitoramento até que a temperatura atinja ou ultrapasse o limite de 80 °C, o usuário escolha encerrar o programa ou ocorram três erros consecutivos.

Ao final, o programa apresenta um relatório com a média das temperaturas, a maior temperatura, a menor temperatura e todas as temperaturas válidas que foram informadas.

## Funcionalidades

O programa possui as seguintes funcionalidades:

* Entrada de temperaturas em graus Celsius;
* Alerta quando a temperatura chega a 80 °C ou mais;
* Cálculo da média das temperaturas;
* Identificação da maior temperatura;
* Identificação da menor temperatura;
* Listagem de todas as temperaturas informadas;
* Verificação do zero absoluto;
* Tratamento de entradas que não sejam números;
* Encerramento após três erros consecutivos;
* Opção de encerramento voluntário utilizando `Q` ou `q`.

## Tratamento de erros

O programa verifica se a temperatura informada é válida.

Temperaturas abaixo de **-273,15 °C**, que corresponde ao zero absoluto, são consideradas inválidas.

Também são rejeitadas entradas que não sejam números, como letras ou outros caracteres.

Quando ocorre um erro, o programa informa ao usuário e contabiliza o erro. Após três erros consecutivos, o programa é encerrado automaticamente.

Quando o usuário informa uma temperatura válida, a contagem de erros consecutivos volta para zero.

## Relatório final

Ao finalizar, o programa apresenta:

* Quantidade de temperaturas registradas;
* Média das temperaturas;
* Maior temperatura registrada;
* Menor temperatura registrada;
* Lista de todas as temperaturas válidas informadas.

## Tecnologias utilizadas

* Linguagem C
* Biblioteca `stdio.h`
* Biblioteca `stdlib.h`
* Biblioteca `string.h`
* Biblioteca `math.h`

## Estrutura do projeto

```text
desafio-monitoramento/
│
├── README.md
├── monitoramento.c
│
└── evidencias/
    ├── teste01.png
    ├── teste02.png
    └── teste03.png
```

## Exemplo de execução

```text
========================================
     MONITORAMENTO DE TEMPERATURA
========================================

Digite uma temperatura (°C): 25
Temperatura registrada: 25.0 °C

Digite uma temperatura (°C): 30
Temperatura registrada: 30.0 °C

Digite uma temperatura (°C): 80
Temperatura registrada: 80.0 °C
ALERTA: temperatura acima ou igual ao limite de 80 °C!

========================================
          RELATORIO FINAL
========================================

Quantidade de temperaturas: 3
Media das temperaturas: 45.00 °C
Maior temperatura: 80.00 °C
Menor temperatura: 25.00 °C

Temperaturas informadas:
1 - 25.00 °C
2 - 30.00 °C
3 - 80.00 °C
```

## Objetivo

O objetivo deste projeto é aplicar conceitos básicos de programação em linguagem C, como variáveis, estruturas de repetição, estruturas condicionais, vetores, entrada de dados, tratamento de erros e cálculos matemáticos.

## Justificativa da Estrutura de Repetição

Escolhi utilizar a estrutura `while` porque o programa precisa continuar recebendo temperaturas enquanto elas forem válidas e estiverem abaixo do limite de 80 °C. O `while` testa a condição antes de executar o bloco, permitindo verificar se o monitoramento deve continuar.

Essa escolha também foi importante porque o usuário pode encerrar o programa voluntariamente ou o programa pode ser encerrado após três erros consecutivos. Nesse caso, a repetição pode ser interrompida antes de uma nova leitura.

Não utilizei `do...while` porque não era necessário garantir uma execução obrigatória do bloco antes de testar a condição. A estrutura `while` se adequou melhor à lógica do monitoramento.
