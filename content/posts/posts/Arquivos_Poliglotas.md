---
title: "Arquivos possuem RG?"
date: 2024-10-24T04:10:42Z
tags: ["Malware",".PDF","Engenheria_Reversa"]
draft: false
---

# Estenografia em arquivos digitais, uma introdução

Uma técnica perspicaz para esconder malwares


## Índice

- Como um determinado formato de arquivo é reconhecido
- Ah, então arquivos possuem RG? (Magic Bytes)
- Abrindo um pdf com ISO embutida
- Bibliográfia e sugestões de leitura
- Licença

## SAY MY NAME
<img source ="\\C:\Users\Gusta\Blog\images\waltu.jpg">

Certamente você já se perguntou o que faz de um DOCX um DOCX? É seu conteúdo? Certamente, mas não só isso. Um arquivo é um conjunto de informações organizadas de maneira específica para cada tipo de formato. Por exemplo, um TXT e um PDF terão estruturas hexadecimais distintas de organização a nível binário porque não têm a mesma forma de expor o conteúdo. O TXT é texto puro sem formatação, enquanto o PDF tem um corpo muito mais complexo com cabeçalhos, segmentação e objetos dentro de um único documento

## Arquivos possuem RG? Sobre Magic Bytes e Assinaturas de Arquivos


Da mesma forma que um macaco verifica o formato de um cubo para encaixar em uma caixa colorida cheia de formas geométricas, nossa máquina irá verificar qual a forma que o nosso arquivo tem. Todo arquivo possui uma assinatura no seu início que permite a execução deste formato pelo sistema operacional, verificando quais programas lidam com esse tipo de arquivo (nativo ou não) e também permite que os programas façam um check antes de inicializar o arquivo, verificando se o formato é reconhecido pelo seu código.


Exemplos de Magic Bytes
PDF: %PDF-

JPEG: FF D8 FF E0 (Cabeçalho) e FF D9 (Final)


[Explique como usar o projeto, com exemplos, comandos ou telas.]

## PoC
Ahhh, se a gente pudesse, se a gente pudesse ah...
E se a gente conseguisse alterar um magic byte em um disassembler? Ou melhor, chavinho, e se a gente conseguisse modificar o cabeçalho e dizer que o arquivo é uma coisa mas na verdade é outra? Bem-vindo à toca do coelho!

### PoCorgtfo02.pdf: um poliglota pdf com mbr





