#include <stdio.h>
#include <stdlib.h>
#include <conio.h>


/* run this program using the console pauser or add your own getch, system("pause") or input loop */

int main(int argc, char *argv[]) {
	
		FILE *file;
		float motor = 100, suspensao = 200, freio = 300, Motor = 100, Suspensao = 200, Freio = 300;
		float horas, valorHora;
		int code = 1;
		char nome[20], modelo[20], nomeser[20], servico[10];
		int opcao;
		char sair;
		
		
		while (sair = "sim"){
		
		printf ("=========================================================================\n");
		printf ("                             AUTOS E AUTOMACAO\n");
		printf ("=========================================================================\n");
		printf ("       [1] SOLICITACAO DE SERVICO [2] FINAIZAR SERVICO] [3] SAIR\n");
		scanf ("%d", &opcao);
		
		switch (opcao) {
			case 1:
				printf ("Digite o nome do solicitante\n");
				scanf ("%s", &nome);
				printf ("Digite o modelo do veiculo\n");
				scanf ("%s", &modelo);
				printf ("Digite o servico\n");
				scanf ("%s", &servico);
				code++;
				printf ("Dados da OS\n Solicitante %s\n Modelo %s\n Servico %s\n \n", nome, modelo, servico);
				//gets(nome);
				file = fopen (nome, "w+t");
				fprintf (file, "%s\n %s\n %s\n", nome, modelo, servico);
				fclose (file);
				
				break;
			case 2:
				printf ("Digite o nome do cliente\n\n\n");
				scanf  ("%s", &nome);
				system ("cls");
				file = fopen (nome, "r+");
				fscanf (file, "%s\n %s\n %s\n", nome, modelo, servico);
				printf ("Nome do Cliente      = %s\n Modelo do Carro     = %s\n Servico requisitado = %s\n", nome, modelo, servico);
				if (servico == "Suspensao") {
					suspensao;
						printf ("Digite o numero de horas do serviço");
						scanf  ("%f", &horas);
						valorHora = horas * suspensao;
						printf ("O valor do serviço sem desconto é:%f", valorHora);
										    }
										 
										 
										 
										 
										 
				//printf ("Digite o numero de horas do serviço");
				//scanf  ("%f", &horas);
				//valorHora = horas * servico;
				//printf ("O valor do serviço fica em:%2.f", valorHora);
				
				break;
			case 3:
				printf ("Aperte qualquer tecla pra sair");
				exit(0);
				
		default :("Digite uma opcao valida");
			   }
		
	
	
	
	}
	return 0;
}
