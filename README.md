package org.example;

import java.util.Scanner;

public class login {
    public static void main(String[] args) {
        Scanner ler = new Scanner(System.in);
        String  email, senha;
        boolean loginValido;

        do {

            System.out.println("Digite o seu email: ");
            email = ler.nextLine();

            System.out.println("Digite sua senha: ");
            senha = ler.nextLine();

            boolean resultadoSenha = senha.equals("123456789");
            boolean resultadoLogin = email.equals("freitasdarlan5@gmail.com");

            loginValido =  resultadoSenha && resultadoLogin;

            if (loginValido) {
                System.out.println("\nBem-vindo, usuário logado!");
            } else {
                System.out.println("\nLogin do usuário ou senha inválidos. Tente novamente.");
            }
        } while (!loginValido);

        ler.close();
    }
}
