PROF.(A):Tiago de Almeida Lopes
ALUNO(A): André Carnicelli Kushnir
DATA:09 /01 / 2019

Lista de Exercícios 01 – Introdução Java

1.	O que são variáveis locais?

Variáveis locais são definidas dentro de um método e elas incluem parâmetros de métodos. Devem ser inicializadas explicitamente antes de utiliza-las.

2.	Quais os tipos de dados primitivos da linguagem Java?

•	Inteiro (byte, short, int, long)
•	Ponto Flutuante (float, double)
•	Caractere (char)
•	Booleano (Boolean)

3.	O que são bytecodes?

Bytescodes é o código de um programa java que foi compilado e desta forma gerado um código que será interpretado pela JVM.

4.	O que é uma referência?

Quando valorizamos uma variável com o valor da criação de um objeto, estamos criando uma referencia para o objeto, aonde poderemos acessar os seus atributos e métodos a partir da referencia.

5.	O que é Garbage Collection?

O garbage collection é o responsável por gerenciar os objetos que não possuem mais referência, desta forma será realizado a desalocação da memoria não mais utilizada. 

6.	Qual a necessidade de adotar um padrão de codificação?

Com um padrão de codificação o código fica muito mais legível, limpo e esteticamente mais bonito, tornando assim mais fácil o entendimento por outra pessoa para futuras manutenções.

7. Ler dois valores para as variáveis A e B, efetuar a troca dos valores de forma
que a variável A passe a possuir o valor da variável B e que a variável B passe a possuir o valor da variável A. Apresentar os valores trocados.

/*
 * Ler dois valores para as variáveis A e B, efetuar a troca dos valores de forma
 * que a variável A passe a possuir o valor da variável B e que a variável B 
 * passe a possuir o valor da variável A. Apresentar os valores trocados.
*/
import java.util.Scanner;

public class Item7 {
	
    public static void main(String[] args) {
	int a=0;
	int b=0;
	int aux=0;
		
	Scanner dados = new Scanner(System.in);
		
        	// Solicitara a digitação da variavel a 
System.out.println("Digite Variavel a: ");
	a = dados.nextInt();		

        	// Solicitara a digitação da variavel b
System.out.println("Digite Variavel b: " + "\n");
	b = dados.nextInt();		

        	// Ira apresentar os valores das variaveis antes da troca
			
	System.out.println("Valores das variaveis antes da troca");        
        	System.out.println("Variavel a: " + a);
        	System.out.println("Variavel b: " + b + "\n");

	// Logica para realização da troca dos valores das variaveis
		
	aux = a;
	a = b;
	b = aux;
		
        	// Ira apresentar os valores das variaveis apos a troca
		
	 System.out.println("Valores das variaveis apos da troca");        
        	System.out.println("Variavel a: " + a);
        	System.out.println("Variavel b: " + b);
    }
}

8. Escreva uma classe que verifica se um dado número inteiro é par ou ímpar.


/*
 * Escreva uma classe que verifica se um dado número inteiro é par ou ímpar
 */
import java.util.Scanner;

public class Item8 {
	
    public static void main(String[] args) {
    	int a=0;
		
	Scanner dados = new Scanner(System.in);
		
        	// Solicita a digitação de um numero inteiro
        	System.out.println("Digite um numero inteiro: ");
a = dados.nextInt();		

	if ( a % 2 == 0){
		System.out.println("Numero digitado é Par" );
	}
	else{
		System.out.println("Numero digitado é Impar" );
	}
    }
}

9. Encontre o quadrado dos números de 0 até 10. Utilize o controle de fluxo for.

/*
 * Encontre o quadrado dos números de 0 até 10. Utilize o controle de fluxo for
 */

public class Item9 {
	
    public static void main(String[] args) {
		
	for (int i=0; i < 11; i++){
		System.out.println("O quadrado do numero " + i + "é: " + i * i);
        	}		
    }
}

10. Faça um programa com 3 variáveis do tipo inteiro (int) tal que a primeira tenha o valor de 6, a segunda o valor 4 e a terceira receba o valor da divisão da
primeira pela segunda. Exiba o valor da terceira variável. Faça uma análise do
resultado.
/*
 * Faça um programa com 3 variáveis do tipo inteiro (int) tal que a primeira tenha o      
 * valor de 6, a segunda o valor 4 e a terceira receba o valor da divisão da primeira pela  
 * segunda. Exiba o valor da terceira variável. Faça uma análise do resultado.
 */
public class Item10 {
	
    public static void main(String[] args) {
	int a=6;
	int b=4;
	int c=a/b;
		
        System.out.println("Valor da divisão, variavel a: " + a + " por variavel b: " + b + 
		                   " resultado: " + c + " resto: " + a % b);
    }
}
 

Analise: Como resultado da divisão de a por b, temos como resultado 1 inteiro e o resto igual a 2.

11. Utilize a estrutura if para fazer um programa que retorne o nome de um
produto a partir do código do mesmo. Considere os seguintes códigos:

001 ? Parafuso;
002 ? Porca;
003 ? Prego;

Para qualquer outro código: XXX ? Diversos.

/*
 * Utilize a estrutura if para fazer um programa que retorne o nome de um 
 * produto a partir do código do mesmo. Considere os seguintes códigos:
 *
 *	001 ? Parafuso;
 *	002 ? Porca;
 *         003 ? Prego;
 * 
 *         Para qualquer outro código: XXX ? Diversos.
 */

public class Item11 {
	
    public static void main(String[] args) {
		
	int codigoProduto = 1;

	if ( codigoProduto == 1){
		System.out.println("Parafuso" );
			
	}else if (codigoProduto == 2) {
		System.out.println("Porca" );
			
	}else if (codigoProduto == 3) {
		System.out.println("Prego" );
			
	}else {
		System.out.println("Diversos" );
	}	
    }
}

12. Imprima o resultado da divisão por 2 de todos os múltiplos de 3, entre 1 e 100, usando os tipos de dados int e double .

/*
 * Imprima o resultado da divisão por 2 de todos os múltiplos de 3, entre 1 e 100, 
 * usando os tipos de dados int e double .
 */

public class Item12 {
	
    public static void main(String[] args) {
		
	double resultado = 0;
		
	for (int i = 1; i < 101; i++){
		    
		if (i % 3 == 0){
			resultado = i;
			System.out.println("numero: " + i + 
" Resultado da divisao por 2: " + resultado / 2 );
		}	
        	}		
    }
}

13. Escreva uma classe que imprima todas as possibilidades de que no lançamento de dois dados tenhamos o valor 7 como resultado da soma dos valores de cada dado.

/*
 * Escreva uma classe que imprima todas as possibilidades de que no lançamento de  
* dois dados tenhamos o valor 7 como resultado da soma dos valores de cada dado.
*/

public class Item13 {
	
    public static void main(String[] args) {
		
	for (int i = 1; i < 7; i++){
		for (int j = 1; j < 7; j++){
			if (i + j == 7){	
				System.out.println("Dados 1 valor: " + i + 
                                                                                " X Dado 2 valor 2: " + j);
			}
		}	
            }		
    }
}

14. Faça um programa que utilize a estrutura while para ler 50 números e calcule e exiba a média aritmética deles. (Pesquise sobre como realizar entrada de dados)

/*
 * Faça um programa que utilize a estrutura while para ler 50 números e 
 * calcule e exiba a média aritmética deles. 
 * (Pesquise sobre como realizar entrada de dados)
 */
import java.util.Scanner;

public class Item14 {
	
    public static void main(String[] args) {
		
		int i = 1;
		int valor = 0;		
		Scanner dados = new Scanner(System.in);

		while (i < 51){
			System.out.println("Entre com o valor " + i + " : ");
			valor = valor + dados.nextInt();		
			i ++;
		}
	
		System.out.println("Media aritmética: " + valor / (i - 1));
	}
}	

15. Refaça o programa anterior utilizando a estrutura do while.
/*
 * Faça um programa que utilize a estrutura do while para ler 50 números e 
 * calcule e exiba a média aritmética deles. 
 * (Pesquise sobre como realizar entrada de dados)
 */
import java.util.Scanner;

public class Item15 {
	
    public static void main(String[] args) {
		
	int i = 1;
	int valor = 0;		
	Scanner dados = new Scanner(System.in);
       
	 do {
		System.out.println("Entre com o valor " + i + " : ");
		valor = valor + dados.nextInt();		
		i ++;
	} while (i < 51);
	
	System.out.println("Media aritmética: " + valor / (i - 1));
     }
}	


OBS: A entrega deve ser feita na sala de aula dia 15/05/2015 de forma
digital. 
