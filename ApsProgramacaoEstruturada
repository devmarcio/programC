/*
*********** APS Programação Estruturada - Turma AAA ***********
* Aluna: Adr
* Aluna: Cin
* Aluno: MC
***************************************************************
*/
/*
      ************* Enunciado **************
1.
* Implementar um programa estruturado em C para imprimir
* quais dos N elementos de um vetor são primos.
* 
2.
* Implementar um programa estruturado em C para imprimir
* o maior elemento primo de cada linha de uma matriz 
* tridimensional M x N x P.
* 
3.
* Implementar um programa estruturado em C para imprimir
* o resultado da soma de duas matrizes tridimensionais 
* de ordem M por N por P.   
* 
4. 
* Implementar um programa estruturado em C para ler e 
* gravar dados de uma estrutura de pontos de um polígono
* de N pontos tridimensionais (alocados dinamicamente)
* em um arquivo texto.  
*/

/*****Bibliotecas*****/

#include <stdio.h>
#include <stdlib.h>
#include <time.h>

/*****Definições*****/
#ifdef WIN32
#define PAUSE 1
#else
#define PAUSE 0
#endif
/*****Mensagens*****/
#define INTRO0 "************ APS Programação Estruturada - Turma AAA ************\n"
#define INTRO1 "| Aluno: AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA - Matricula xxxxxxxxxx |\n"
#define INTRO2 "*****************************************************************\n"
#define MSGQ00 "Digite 0 para sair ou o número da questão: "
#define MSGQ01 "Questão 01"
#define MSGQ02 "Questão 02"
#define MSGQ03 "Questão 03"
#define MSGQ04 "Questão 04"
#define PAUSAR "\nDigite <enter> para continuar...\n"
#define ENUQ01 "Implementar um programa estruturado em C para imprimir quais dos N elementos\nde um vetor são primos."
#define ENUQ02 "Implementar um programa estruturado em C para imprimir o maior elemento\nprimo de cada linha de uma matriz tridimensional M x N x P."
#define ENUQ03 "Implementar um programa estruturado em C para imprimir o resultado da soma\nde duas matrizes tridimensionais de ordem M x N x P."
#define ENUQ04 "Implementar um programa estruturado em C para ler e gravar dados de uma\nestrutura de pontos de um polígono de N pontos tridimensionais\n(alocados dinamicamente) em um arquivo texto."
#define MSGALL "\n0-Para sair\n1-Questão 01\t2-Questão 02\t3-Questão 03\t4-Questão 04\n"
#define MSGINV "Opção inválida!!"
#define SAIR   "Saindo..."
#define VET_OK "\nVetor inicializado com sucesso...\n"
#define MOSTRAR_VET "\nVetor original:\n"
#define MOSTRAR_MAT "\nMatriz original:\n"
#define MOSTRAR_PRI "\nMostrar Primos:"
#define NUM_MAX 1000
#define TAM_VET 100
#define NUML 5
#define NUMC 4
#define NUMP 3

/*****Protótipos*****/
int menu();
int ehPrimo(int num);
void esperarTela();
void limparTela();
int geraNum();
void preencherVetor();
void mostrarVetor();
void preencherMatriz();
void mostrarMatriz();
void mostrarPrimo();
void selection_sort (int vetor[],int max);

/*****Variáveis Globais*****/
int vetor[TAM_VET];
int matriz[NUML][NUMC][NUMP]
int max,num,elem;

/***** Funções*****/
int main(){
	printf(INTRO0);
	printf(INTRO1);
	printf(INTRO2);
	menu();
	printf("\n%s",SAIR);
	return 0;
	}
int menu()
{
	int opt;
	do{
	
	printf("\n\nMENU\n");
	printf(MSGALL);
	printf("\n%s",MSGQ00);
	scanf("%d",&opt);
	switch(opt){
		case 0:
			limparTela();
			return 0;
			break;
			
		case 1:
			printf("\n%s\n%s",MSGQ01,ENUQ01);
			preencherVetor();
			esperarTela();
			limparTela();
			mostrarVetor();
			esperarTela();
			printf("%s\n",MOSTRAR_PRI);
			mostrarPrimo();
			esperarTela();
			selection_sort(vetor,TAM_VET);
			esperarTela();
			break;
			
		case 2:
			printf("\n%s\n%s",MSGQ02,ENUQ02);
			esperarTela();
			break;
			
		case 3:
			printf("\n%s\n%s",MSGQ03,ENUQ03);
			esperarTela();
			break;
			
		case 4:
			printf("\n%s\n%s",MSGQ04,ENUQ04);
			esperarTela();
			break;
			
		default: printf("\n%s\n",MSGINV);
		esperarTela();	
	}
}while(opt);

	return 0;
}

/*****Função Primo*****/
int ehPrimo(int num)
{
  int i, metade;
  
  if(num<2)
     return 0;
     
  metade=(int)num/2;	

  for(i=metade;i>=2;i--)
  {
	if((num%i)==0)/*teste para primo resultou falso*/
  	  return 0;
  }
  return 1;/*teste para primo resultou verdadeiro*/
}

/*****Esperar Tela*****/
void esperarTela()
{
   printf(PAUSAR);
   if(PAUSE==1)
   system("pause");
else
   system("read -p \"-->  \" Saindo");
   
}
/*****Limpar Tela*****/
void limparTela()
{
   if(PAUSE==1)
   system("cls");
else
   system("clear");
}
/*****Gerar Numero*****/
int geraNum(){
	num= rand() % NUM_MAX;
	return num;
}
/*****Gerar Vetor****/
void preencherVetor(){
	int i=0;
	srand(time(NULL));
	do{
		num=geraNum();
		vetor[i]=num;
		i++;		
	}while(i<TAM_VET);
		printf(VET_OK);
		return;
	}
void mostrarVetor(){
	int i=0,j=0;
	printf(MOSTRAR_VET);
	do{
		printf("%4d",vetor[i]);
		i++;j++;
		if (j==10) {j=0;printf("\n");}
		} while(i<TAM_VET);
		return;
	}
/*****Gerar Matriz****/
void preencherMatriz(){
	int m=0,n=0,p=0;
	srand(time(NULL));
	do{
		elem=geraNum();
		vetor[m][n][p]=elem;
		i++;		
	}while(i<TAM_VET);
		printf(VET_OK);
		return;
	}
void mostrarMatriz(){
	int i=0,j=0,k=0;
	printf(MOSTRAR_MAT);
	
		for(m=0;m<numL;m++){
		for(n=0;n<numC;n++){
			for(p=0;p<numP;p++){
		printf("%4d",matriz[m][n][p]);}
	}}
		//if (j==10) {j=0;printf("\n");}
		return;
	}

void mostrarPrimo(){
	int i=0,j=0;
	int num1;
	do{
		num1=vetor[i];
		if(ehPrimo(num1)){j++;
		printf("%4d",num1);if (j==10) {j=0;printf("\n");}}
		i++;
		
		} while(i<TAM_VET);
		return;
	}

void selection_sort (int vetor[],int max) {
  int i, j, min, aux;
  
  for (i = 0; i < (max - 1); i++) {
    /* O minimo é o primeiro número não ordenado ainda */
    min = i;
    for (j = i+1; j < max; j++) {
      /* Caso tenha algum numero menor ele faz a troca do minimo*/
      if (vetor[j] < vetor[min]) {
   min = j;
      }
    }
    /* Se o minimo for diferente do primeiro numero não ordenado ele faz a troca para ordena-los*/
    if (i != min) {
      aux = vetor[i];
      vetor[i] = vetor[min];
      vetor[min] = aux;
    }
  }
  /* Imprime o vetor ordenado */
  printf("\nVetor ordenado:\n");
  for (i = 0; i < max; i++) {
	
    printf ("%4d ",vetor[i]);
  }
  printf ("\n");
}
