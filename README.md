# Fluxograma_Eventos

Descrição Narrativa
-------------------
1. Obter o evento 
2. Se a data do evento for maior que data atual, a inscrição poderá continuar
3. obter idade do inscrito
4. Se a idade do inscrito for menor que >= 18, inscrição poderá continuar. 
5. Verificar a quantidade de inscritos. 
6. Se a quantidade de inscritos for menor ou igual a 100, inscrição realizada.
7. Listar Palestrante do evento e os inscritos
--------------------------------------------------------------------------------

Algoritmo
---------
01. algoritmo "InscricaoEvento"
02. var
03. data_atual, data_evento, data_nascimento:data
04. var
05. indice, idade, total_inscritos: real
06. var
07. evento, participantes: arquivo_de_dados
08. evento <- arquivo_eventos_cadastrados
08. participantes <- arquivo_cadastro_paricipantes
09. data_evento = evento.data_inicio
10. data_atual <- data.sistemaOperacional
11. selecionar Evento
12. se data_evento > data_atual
13.    ler data_nascimento
14.    idade <- data_atual - data_nascimento
15. 		se idade >= 18
16.			   total_inscritos <-  participantes.total_de_registros
17.			   se total_inscritos <= 100
18.				  escrever("Parabéns. Inscrição foi concluida no Evento: " + evento.evento_nome)
19.				  escrever ("Palestrante será: " + evento.nome_palestrante)
20.				  escrever ("Inscritos: ")
21.				  indice <- 1;
22.				  enquanto indice <= total_inscritos faça
23.				        Escrever (participantes.nome[indice])
24.				        indice <- indice + 1
25.				  fimenquanto				
26.			   senao
27.			      escrever ("Evento lotado. Não será possivel fazer inscrição")
28.			   fimse
29.	         senão
30.			   escrever ("Participante precisa ter maior idade")
31.	         fimse
32. senão
33.    escrever (Evento já iniciado e não será possivel realizar a inscrição.")	
34. fimse
35. =================================================================================
36. fim
