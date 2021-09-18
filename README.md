# Desafio-Matematico-em-Java-

Ler 1 caractere Maiúsculo que indica uma operaçāo a ser realizada numa Matriz M[12][12]

Em seguida calcule e mostre a soma ou a média considerando somente elementos na direita da Matriz, conforme a imagem

import java.io.IOException;
import java.util.Scanner;

public class Desafio Matriz {

    public static void main(String[] args) throws IOException {
        Scanner leitor = new Scanner(System.in);
        double soma = 0;
        char O = leitor.next().toUpperCase().charAt(0);
        double[][] M = new double[12][12];
        for (int i = 0; i < M.length; i++) {
        	for (int j = 0; j < M[i].length; j++) {
        		M[i][j] = leitor.nextDouble();
        	}
        }
        
        for (int i = 0; i < M.length; i++) {
        	for (int j = 0; j < M[i].length; j++) {
        		if (j < i && j > M.length-i-1) soma += M[i][j];
        	}
        }

        if (O == 'M') soma /= 30;
    	System.out.println(String.format("%.1f", soma));
    }
	
}
