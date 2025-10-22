# Simulador-de-emprestimo
##Simulador de Empréstimo, pequeno projeto desenvolvido para a faculdade.
import java.util.Scanner;

public class SimuladorEmprestimo {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Digite o salário do cliente: ");
        double salario = scanner.nextDouble();

        System.out.print("Digite a quantidade de pendências: ");
        int pendencias = scanner.nextInt();
        System.out.print("Digite o valor do empréstimo: ");
        double valorEmprestimo = scanner.nextDouble();

        System.out.print("Digite a quantidade de parcelas: ");
        int numParcelas = scanner.nextInt();

        double taxaJuros = 0.009;

        double juros = valorEmprestimo * taxaJuros * numParcelas;
        double valorTotal = valorEmprestimo + juros;

        double valorParcela = valorTotal / numParcelas;

        System.out.println("\n--- Resumo do Empréstimo ---");
        System.out.printf("Valor do Empréstimo: R$ %.2f\n", valorEmprestimo);
        System.out.printf("Número de Parcelas: %d\n", numParcelas);
        System.out.printf("Taxa de Juros: %.1f%% ao mês\n", taxaJuros * 100);
        System.out.printf("Valor Total a Pagar: R$ %.2f\n", valorTotal);
        System.out.printf("Valor de Cada Parcela: R$ %.2f\n", valorParcela);

        scanner.close();
    }
}
