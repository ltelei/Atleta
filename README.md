# Atleta
Atleta
Algoritmo "COB"
//
//
// Descrição   : Aqui você descreve o que o programa faz! (função)
// Autor(a)    : Nome do(a) aluno(a)
// Data atual  : 27/04/2023
tipo
   participante = registro
      nome, nome_atleta, pace : caractere
      numero ,km, idade, tempo_prova :inteiro

   fimregistro


Var
   // Seção de Declarações das variáveis
   atleta : vetor [1..100] de participante
   km, pace, op, qtd_atleta : inteiro
   dados_prova,tempo_prova : real







procedimento Menu()

inicio

   enquanto op <> 9 faca
      escreval("========== MENU ===================")
      escreval(" 1 - cadastrar atleta ============ ")
      escreval(" 2 - informar dados de prova====== ")
      escreval(" 3 - imprimir diário dados de prova")
      escreval("===================================")
      escreva("op > ")
      leia(op)
      escolha op
      caso 1
         cadastrar_atleta()
      caso 2
         dados_prova()
      caso 3
         impressao()
      outrocaso
         escreval("saindo ...")
      outrocaso
         escreval("opçao invalida")
      fimescolha
   fimenquanto
fimprocedimento



procedimento cadastrar_atleta()      // cadastrando atletas
var
   op1: caractere
inicio
   qtd_atleta<-qtd_atleta+1
   Escreval ("Digite o nome do atleta ")
   leia (atleta[qtd_atleta].nome)
   Escreval ("Digite a idade do Atleta")
   leia (atleta[qtd_atleta].idade)
   Escreval ("Digite o numero do atleta")
   leia (atleta[qtd_atleta].numero)
   Escreval (" Atleta cadastrado com sucesso, deseja cadastrar outro atleta? S / N?")
   leia (op1)
   se (op1 = "N") entao
      menu()

   fimse

fimprocedimento


procedimento dados_prova
var
   op1:caractere
inicio
   qtd_atleta<-qtd_atleta+1
   escreval("Digite o numero do atleta ")
   leia (atleta[qtd_atleta].numero)
   escreval("Quanto tempo o atleta levou para finalizar a prova?")
   leia(atleta[qtd_atleta].tempo_prova)
   Escreval("Quantos quilometros o atleta correu? ")
   leia (atleta[qtd_atleta].km)
   Escreval("Dados da prova cadastrados com sucesso, deseja inserir mais algum atleta? S/N")
   leia (op1)
   se (op1 = "N") entao
      menu()
   fimse
fimprocedimento

procedimento impressao()

inicio
   qtd_atleta<-qtd_atleta+1
   Escreval("Digite o numero do atleta que deseja saber ")
   leia (atleta[qtd_atleta].numero)
   escreval ("O atleta ",atleta[qtd_atlteta].nome," percorreu ",atleta[qtd_atlteta].km, " em ", atleta[qtd_atlteta].tempo_prova)

fimprocedimento









Inicio
   Menu()


Fimalgoritmo
