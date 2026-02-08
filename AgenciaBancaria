/*s
 * Click nbfs://nbhost/SystemFileSystem/Templates/Licenses/license-default.txt to change this license
 */

package com.mycompany.agenciabancaria;

import java.util.Scanner;
/**
 *
 * @author lucas
 * Desenvolvimento Sistema Bancário
 */

class Cliente {
    private String nome;
    private String sobrenome; 
    private String cpf;
    private double saldo;
    
    
    public Cliente(String nome, String sobrenome, String cpf){
        this.nome = nome;
        this.sobrenome = sobrenome;
        this.cpf = cpf;
        this.saldo = 0.0;
    }

    //Métodos da classe Cliente    
    public void ConsultarSaldo() {
        System.out.println("Seu saldo atual: R$" + saldo);
    }//fim método consultarSaldo
 
    public void depositar(double valor) {
        if (valor > 0) {
            saldo += valor;
            System.out.println("Deposito de R$" + valor + " realizado com sucesso.");
        } else {
            System.out.println("Valor de depósito invalido!");
        }
    }//fim método depositar
    
    public void sacar(double valor) {
        if (valor > 0 && valor <= saldo) {
            saldo -= valor;
            System.out.println("Saque de R$" + valor + " realizado com sucesso.");
        } else {
            System.out.println("Saldo insuficiente ou valor de saque invalido.");
        }
    }//fim método sacar
}//fim classe cliente



public class AgenciaBancaria {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.println("Informe seu nome por favor:");
        String nome = scanner.nextLine();
        System.out.println("Informe seu sobrenome por favor:");
        String sobrenome = scanner.nextLine();
        System.out.println("Informe seu CPF por favor:");
        String cpf = scanner.nextLine();
        //instanciando um objeto da classe cliente
        Cliente cliente = new Cliente(nome, sobrenome, cpf);
        
        boolean continuar = true;
        while(continuar) {
            System.out.println("\nO que deseja");
            System.out.println("1 - Consultar saldo");
            System.out.println("2 - Fazer deposito");
            System.out.println("3 - Fazer saque");
            System.out.println("4 - Encerrar aplicacao\n\n");
            
            int escolha = scanner.nextInt();
            switch (escolha) {
                case 1:
                    cliente.ConsultarSaldo();
                    break;
                case 2:
                    System.out.println("Informe o valor a ser depositado:");
                    double valorDeposito = scanner.nextDouble();
                    cliente.depositar(valorDeposito);
                    break;
                case 3:
                    System.out.println("Informe o valor a ser sacado:");
                    double ValorSaque = scanner.nextDouble();
                    cliente.sacar(ValorSaque);
                    break;
                case 4:
                    continuar = false;
                    System.out.println("Encerrando a aplicacao, ate breve.");
                    break;
                default:
                    System.out.println("Opcao invalida. Tente novamente.");
                    break;
            }
        }
        scanner.close();
    }
}
        
        
