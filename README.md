# Compilador em Python 3.6

Luis carlos Santos Melo de Jesus RA: 1272122545

Este projeto faz parte de uma tarefa acadêmica cujo principal propósito era criar um compilador em uma linguagem para produzir código C.

## Descrição do Projeto

Python é uma linguagem simples e intuitiva, razão pela qual foi selecionada para a criação deste compilador.

O projeto se estrutura da seguinte maneira: ao receber um arquivo txt que representa uma linguagem conhecida como Mgol, o programa deve ser capaz de compilá-lo e produzir um arquivo escrito em C.

Para isso, o projeto foi divido em 3 etapas bem definidas:

- desenvolvimento do analisador léxico
- desenvolvimento do analisador sintático
- desenvolvimento do analisador semântico

O desenvolvimento do analisador semântico contém as partes desenvolvidas no analizador léxico e sintático, portanto é a parte final de todo este projeto.

## Informações extras sobre o Projeto

Como é de conhecimento geral, o formalismo utilizado pelo analisador léxico é o das Expressões Regulares. Com isso em mente, um DFA (Autômato Fino Determístico) foi incorporado ao analisador léxico, representado por uma tabela de transição sobre os símbolos lidos, de acordo com a condição atual do DFA. Em última análise, o objetivo do analisador léxico é apresentar uma estrutura composta por três campos: token, lexema e tipo.

No que se refere ao analisador sintático, a abordagem formal adotada é a GLC (Gramática Livre de Contexto). Portanto, o funcionamento deste segmento do projeto envolve a recepção da estrutura retornada pelo analisador léxico e, através da estratégia de análise sintática Bottom-up, uma tabela sintática foi criada para representar o autômato LR(0). Com base nessa tabela sintática, o analisador sintático aplica as análises sintáticas apropriadas ao arquivo txt Mgol.

E por fim, o analisador semântico foi desenvolvido de maneira que ele é gerenciado pelo analisador sintático, isto é, análise semântica dirigida pelo sintático. Logos as regras semanticas são aplicadas sempre que uma operação de redução ocorre no analisador sintático.

Este projeto final, conforme mencionado anteriormente, recebe um arquivo escrito em uma linguagem hipotética (conhecida como linguagem Mgol) e o compila para produzir um código simples em linguagem C.
