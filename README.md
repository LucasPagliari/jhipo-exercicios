# JHIPO:
Desenvolvido por Peter Jandl Junior  
  * [Github](https://github.com/pjandl/jhipo/)  
  * [Twitter](https://twitter.com/pjandl/)  
  * [Blog](http://tecnopode.blogspot.com//)  
  
### Objetivo: 
Simplificado o conteúdo para os alunos de Tecnologia de Análise e Desenvolvimento de Sistemas.

###### Requisito: Java 1.8 +

### How to: 
1. No prompt de comando: Utilizando o comando: cd navegue até o diretório (use tecla TAB para autopreencher)
>  jhipo-vyyyyddmm.jar será o arquivo que foi dispinibilizado, no caso deste repositório jhipo-v20181018.jar

Assembly: `java -cp jhipo-vyyyyddmm.jar jhipovm +h` para obter as opções de parâmetros  

| on & off| Resultado|
| --------|--------- |
| +/-a | memory map|
| +/-e | execute program |
| +/-i | i/o map |
| +/-m | microinstructions|
| +/-o | opcode decode|
| +/-p | performance|
| +/-s | processpr status|

MacroAssembly: `java -cp jhipo-vyyyyddmm.jar masm +h`   

| on & off| Resultado|
| --------|--------- |
| +/-a | show assembly|
| +/-c | syntax check only |
| +/-d | debug mode|
| +/-e | execute in VM|
| +/-n | case sensitive|
| +/-s | symbol table|
| +/-v | verbose mode|

2. Executando arquivos em assembly:  
`java -cp jhipo-vyyyyddmm.jar jhipovm +a +e programs\arquivo.asm`  

3. Executando arquivos diretamente em macroassembly:
`java -cp jhipo-vyyyyddmm.jar masm +e programs\arquivo.masm`  
 
4. Gerando Arquivos Assembly pelo MacroAssembly:
`java -cp jhipo-vyyyyddmm.jar masm programs\arquivo.masm programs\arquivo.masm programs\arquivo.asm`  

## Comandos
| OpCode     | Instrução    | Ação da instrução |
| --------|---------|-------|
| 0x00 | NOP end | Nenhuma Operação |
| 0x10 | STA end | MEM(end) <- ACC  |
| 0x20 | LDA end | ACC <- MEM(end)  |
| 0x30 | ADD end | ACC <- ACC + MEM |
| 0x40 | SUB end | ACC <- ACC – MEM |
| 0x50 | OR end| ACC <- ACC OR MEM  |
| 0x60 | AND end | ACC <- AND MEM |
| 0x70 | NOT | ACC <- NOT (ACC) |
| 0x80 | JMP end | PC <- end  |
| 0x90 | JN end | IF N = 1 THEN PC <- end |
| 0xA0 | JZ end | IF Z = 1 THEN PC <- end |
| 0xB0 | CALL end | MEM(SP) <- PC; SP <- SP-1; PC <- end  |
| 0xC0 | RET | PC <- MEM(SP); SP <- SP+1  |
| 0xD0 | IN end | ACC <- I/O(end) |
| 0xE0 | OUT end | I/O(end) <- ACC  |
| 0xF0 | HTL | Término de execução  |

[Material](https://drive.google.com/open?id=1Nn5GXN-8dg1xKHN_lFzVGdWt1B6Fzaul/):
