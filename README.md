# Pontuacao-de-times-capionato-futebol-codigo-em-Java

Considere o seguinte problema:

Escreva um programa que leia a pontuação de 20 times de um campeonato de futebol. O programa deve mostrar, ao final, qual a pontuação dos campeões, bem como mostrar quantos times dividiram o título.

Complete o programa abaixo, arrastando e soltando os trechos de código nos espaços em branco, de forma que o problema acima seja corretamente implementado.



public class VerificaCampeoes {
	public static void main(String[] args) {
		[int[] pontos = new int[20];]
		
		// Leitura
		for(int cont = 0; cont < pontos.length; cont++) {
			System.out.printf("Pontuacao do time %d: ", cont+1);
			[pontos[cont] = Integer.parseInt(System.console().readLine());]
		}
		
		// Processamento
		[int maior = pontos[0];]
		for(int cont = 1; cont < pontos.length; cont++) {
			[if(maior < pontos[cont])]
				[maior = pontos[cont];]
		}
		
		int campeoes = 0;
		for(int cont = 0; cont < pontos.length; cont++) {
			[if(pontos[cont] == maior)]
				campeoes++;
		}
		
		// Saida
		System.out.printf("\nNUMERO DE CAMPEOES = %d\n", campeoes);
	}
}
