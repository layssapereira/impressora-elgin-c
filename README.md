# Controle da Impressora Elgin em C

Programa em linguagem C que controla a impressora térmica Elgin (`i8` / `i9`) utilizando a biblioteca oficial da Elgin, `E1_Impressora01.dll`.

## O que o programa faz

Ao abrir, o programa solicita um login. Após a autenticação, exibe um menu interativo que permite configurar e abrir a conexão com a impressora e enviar comandos para ela:

- Imprimir texto
- Imprimir QR Code
- Imprimir código de barras
- Imprimir cupom fiscal SAT (XML) e cancelamento SAT
- Abrir a gaveta de dinheiro
- Emitir sinal sonoro

## Requisitos

- **Sistema Operacional:** Windows
- **Compilador:** Compilador C de **64 bits** (ex.: TDM-GCC do Dev-C++ ou MSYS2 `mingw64`)
- **Hardware:** Impressora Elgin conectada via USB, com o driver devidamente instalado

## Qual DLL usar

Este projeto utiliza a DLL de **64 bits (x64)**. A arquitetura da DLL deve ser exatamente a mesma do compilador utilizado:

| Compilador | Pasta da DLL |
| :--- | :--- |
| **64 bits** (Dev-C++ com TDM-GCC 64, MSYS2 mingw64) | **`x64`** *(usada neste projeto)* |
| **32 bits** (ex.: MinGW do Code::Blocks) | **`x86`** |

## Arquivos necessários

Todos os arquivos abaixo devem estar localizados na **mesma pasta** do executável:

```text
├── main.c
├── E1_Impressora01.dll   # Nome exato, sem "(2)" ou "_2"
├── XMLSAT.xml
└── CANC_SAT.xml
