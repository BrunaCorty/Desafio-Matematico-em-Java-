# Desafio-Matematico-em-Java-

Ler 1 caractere Maiúsculo que indica uma operaçāo a ser realizada numa Matriz M[12][12]

Em seguida calcule e mostre a soma ou a média considerando somente elementos na direita da Matriz, conforme a imagem anexa.


import java.util.Scanner;

public class Desafio {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        double m[][] = new double[12][12];
        double sum = 0;
        int count = 0;
        String v = sc.next();
        for (int i = 0; i < m.length; i++) {
            for (int j = 0; j < m.length; j++) {
                double x = sc.nextDouble();
                m[i][j] = x;
                if (j > m.length - i - 1 && i < j) {
                    sum += x;
                    count++;
                }
            }
        }
        if (v.equals("S")) {
            System.out.printf("%.1f\n", sum);
        } else {
            System.out.printf("%.1f\n", (sum / count));
        }
    }
}



