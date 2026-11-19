Controle da Impressora Elgin em C

Programa em linguagem C que controla a impressora térmica Elgin (i8 / i9) usando a biblioteca da própria Elgin, `E1\\\_Impressora01.dll`.

O que o programa faz

Ao abrir, o programa pede um login. Depois de entrar, mostra um menu que permite configurar e abrir a conexão com a impressora e enviar comandos para ela: imprimir texto, QR Code, código de barras, cupom fiscal SAT (XML), cancelamento SAT, abrir a gaveta de dinheiro e emitir sinal sonoro.

Requisitos

* Windows
* Compilador C de **64 bits** (ex.: TDM-GCC do Dev-C++ ou MSYS2 mingw64)
* Impressora Elgin conectada via USB, com o driver instalado

Qual DLL usar

Este projeto usa a DLL de **64 bits (x64)**.

A DLL precisa ter a mesma arquitetura do compilador:

|Compilador|DLL|
|-|-|
|64 bits (Dev-C++ com TDM-GCC 64, MSYS2 mingw64)|pasta **x64**  (a usada neste projeto)|
|32 bits (ex.: MinGW do Code::Blocks)|pasta **x86**|

Arquivos necessários

Todos precisam estar na mesma pasta:



main.c
E1\_Impressora01.dll   (nome exato, sem "(2)" ou "\_2")
XMLSAT.xml
CANC\_SAT.xml



Como compilar e executar

abra o main.c e aperte (Compilar e Executar).

Pelo terminal:

gcc main.c -o impressora.exe
impressora.exe



Login de teste

Usuário: admin
Senha: 1234

São permitidas 3 tentativas. Depois disso, o programa é encerrado.

Opções do menu

|Opção|Ação|
|-|-|
|1|Configurar Conexão (tipo, modelo, porta e parâmetro)|
|2|Abrir Conexão|
|3|Fechar Conexão|
|4|Imprimir Texto|
|5|Imprimir QR Code|
|6|Imprimir Código de Barras|
|7|Imprimir XML SAT|
|8|Imprimir XML Cancelamento SAT|
|9|Abrir Gaveta (Elgin)|
|10|Abrir Gaveta|
|11|Emitir Sinal Sonoro|
|0|Sair|

A conexão padrão é **USB, modelo i9**. Para usar outro modelo (ex.: i8), use a opção 1 antes da opção 2.

Autores

* Layssa Gilo Pereira
* Samuel Moura de Jesus

