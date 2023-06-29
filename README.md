# CURSOJAVA

Copy code
import java.util.Scanner;

public class IMCCalculator {
    private double peso;
    private double altura;

    public void calcular() {
        double imc = peso / (altura * altura);
        mostrarResultado(imc);
    }

    public void mostrarPeso() {
        System.out.println("Peso: " + peso + " kg");
    }

    public void setPeso(double peso) {
        this.peso = peso;
    }

    public void setAltura(double altura) {
        this.altura = altura;
    }

    private void mostrarResultado(double imc) {
        System.out.println("Seu IMC é: " + imc);
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        IMCCalculator calculadora = new IMCCalculator();

        System.out.print("Digite o peso em quilogramas: ");
        double peso = scanner.nextDouble();
        calculadora.setPeso(peso);

        System.out.print("Digite a altura em metros: ");
        double altura = scanner.nextDouble();
        calculadora.setAltura(altura);

        calculadora.mostrarPeso();
        calculadora.calcular();
    }
}
