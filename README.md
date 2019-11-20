package vekHunter;

import java.util.Scanner;

public class projetoVekExecutavel {

	public static void main(String[] args) {

		Scanner teclado = new Scanner(System.in);

		double[] descAvista = new double[5];
		double[] descCredito = new double[5];
		int aumentoDescVekAvista;
		int aumentoDescVekCredito;

		String[] nomeConcorrente = new String[5];

		aumentoDescVekAvista = 5;
		aumentoDescVekCredito = 4;

		nomeConcorrente[0] = "Panificadora Conceição";
		nomeConcorrente[1] = "Panificadora Lagoa";
		nomeConcorrente[2] = "Panificadora Saco Grande";
		nomeConcorrente[3] = "Panificadora Matadeiro";
		nomeConcorrente[4] = "Panificadora Itacorubi";

		descAvista[0] = 10;
		descAvista[1] = 11;
		descAvista[2] = 12;
		descAvista[3] = 15;
		descAvista[4] = 9;

		descCredito[0] = 2;
		descCredito[1] = 3;
		descCredito[2] = 2;
		descCredito[3] = 1;
		descCredito[4] = 5;

		System.out
				.println("Olá! Me chamo VekHunter e vou te ajudar a fazer a melhor compra comparada aos concorrentes!");

		System.out.println(
				"Por favor, digite de 1 à  5 para selecionar o estabelecimento concorrente, ou 0 para encerrar: "
						+ "\n1 - " + nomeConcorrente[0] + "; \n2 - " + nomeConcorrente[1] + "; \n3 - "
						+ nomeConcorrente[2] + "; \n4 - " + nomeConcorrente[3] + "; \n5 - " + nomeConcorrente[4]
						+ "; \n0 - Sair.");
		int concorrente = teclado.nextInt();

		while (concorrente < 6) {

			System.out.println("---------- Em relação ao Cliente, responda! ----------");

			System.out.print("Por favor, informe o CPF ou CNPJ: ");
			String cpf = teclado.next();
			System.out.print("Por favor, informe o Telefone: ");
			String telefone = teclado.next();
			System.out.print("Por favor, informe o E-mail: ");
			String email = teclado.next();
			System.out.println(" ");
			System.out.println("Por favor, indique nessa lista, em qual ramo de atividade você se enquadra: "
					+ "\n1 - Professor(a); \n2 - Desenvolvedor(a); \n3 - Funcionário(a) Público; \n4 - Enfermeiro(a); \n5 - Gerente; \n6 - Autônomo(a);"
					+ "\n7 - Educador(a) Físico; \n8 - Arquiteto(a); \n9 - Desempregado(a); \n0 - Outros.");
			int ramo = teclado.nextInt();
			if (ramo == 9) {
				System.out.println();

				System.out.println("Informamos que a partir deste ano, não estamos disponibilizando"
						+ " descontos para pessoas desempregadas");
				System.exit(0);
			} else {

				System.out.println(" ");
				System.out.println("---------- Em relação ao Produto, responda! ----------");
				while (ramo != 9 && cpf != null && telefone != null) {
					switch (concorrente) {

					case 1: {
						System.out.print(
								"Digite o preço (sem desconto) do produto desejado na " + nomeConcorrente[0] + ": ");
						int precoProdutoX = teclado.nextInt();
						System.out.println(" ");
						System.out.println("Analisando as taxas de descontos do concorrente, concluímos: \n"
								+ "O produto desejado custará na " + nomeConcorrente[0] + ": R$"
								+ (precoProdutoX - (precoProdutoX * descAvista[0]) / 100) + " à vista e R$"
								+ (precoProdutoX - (precoProdutoX * descCredito[0]) / 100) + " no crédito.");
						System.out.println(" ");
						System.out.println(
								"Notamos que você é uma pessoa legal. Portanto, verificaremos o seu desconto \nem "
										+ "nossa loja para esse produto... ");
						System.out.println(" ");
						System.out.println("Pronto! Segue abaixo os nossos super descontos:");
						System.out.println("Desconto de " + (descAvista[0] + aumentoDescVekAvista)
								+ "% para compras à vista;\n" + "Desconto de "
								+ (descCredito[0] + aumentoDescVekCredito) + "% para compras no crédito;");
						System.out.println(" ");
						System.out.println("Sendo assim, o produto desejado irá custar em nossa loja: \n" + "R$"
								+ (precoProdutoX - (precoProdutoX * (descAvista[0] + aumentoDescVekAvista)) / 100)
								+ " à vista; \nR$"
								+ (precoProdutoX - (precoProdutoX * (descCredito[0] + aumentoDescVekCredito)) / 100)
								+ " no crédito!");
						System.out.println(" ");
						System.out.println("Para confirmar a compra e garantir a reserva"
								+ "do produto digite 1, caso contrário, digite 0: ");
						int confirma = teclado.nextInt();
						if (confirma != 0) {
							System.out.println("Muito bem! Seu produto está esperando por você!\nPara retirá-lo,"
									+ " basta apresentar o documento do CPF " + cpf + ".");
							System.out.println("- O comprovante de reserva será encaminhado para o email " + email
									+ ".\n- Um SMS" + " foi enviado para o telefone " + telefone + ".");
							System.out.println(" ");
							System.out.println("Agradecemos a confiança!");
							System.out.println(" ");
							System.out.println("VEK!");
							System.exit(0);
						} else {
							System.out.println("Muito bem! Aguardamos seu retorno!");
							System.exit(0);
						}

						break;
					}
					case 2: {
						System.out.print(
								"Digite o preço (sem desconto) do produto desejado na " + nomeConcorrente[1] + " : ");
						int precoProdutoX = teclado.nextInt();
						System.out.println(" ");
						System.out.println("Analisando as taxas de descontos do concorrente, concluímos: \n"
								+ "O produto desejado custará na " + nomeConcorrente[1] + ": R$"
								+ (precoProdutoX - (precoProdutoX * descAvista[1]) / 100) + " à vista e R$"
								+ (precoProdutoX - (precoProdutoX * descCredito[1]) / 100) + " no crédito.");
						System.out.println(" ");
						System.out.println(
								"Notamos que você é uma pessoa legal. Portanto, verificaremos o seu desconto \nem "
										+ "nossa loja para esse produto... ");
						System.out.println(" ");
						System.out.println("Pronto! Segue abaixo os nossos super descontos:");
						System.out.println("Desconto de " + (descAvista[1] + aumentoDescVekAvista)
								+ "% para compras à vista;\n" + "Desconto de "
								+ (descCredito[1] + aumentoDescVekCredito) + "% para compras no crédito;");
						System.out.println(" ");
						System.out.println("Sendo assim, o produto desejado irá custar em nossa loja: \n" + "R$"
								+ (precoProdutoX - (precoProdutoX * (descAvista[1] + aumentoDescVekAvista)) / 100)
								+ " à vista; \nR$"
								+ (precoProdutoX - (precoProdutoX * (descCredito[1] + aumentoDescVekCredito)) / 100)
								+ " no crédito!");
						System.out.println(" ");
						System.out.println("Para confirmar a compra e garantir a reserva"
								+ "do produto digite 1, caso contrário, digite 0: ");
						int confirma = teclado.nextInt();
						if (confirma != 0) {
							System.out.println("Muito bem! Seu produto está esperando por você!\nPara retirá-lo,"
									+ " basta apresentar documento do CPF " + cpf + ".");
							System.out.println("- O comprovante de reserva será encaminhado para o email " + email
									+ ".\n- Um SMS" + " foi enviado para o telefone " + telefone + ".");
							System.out.println(" ");
							System.out.println("Agradecemos a confiança!");
							System.out.println(" ");
							System.out.println("VEK!");
							System.exit(0);
						} else {
							System.out.println("Muito bem! Aguardamos seu retorno!");
							System.exit(0);
						}

						break;
					}
					case 3: {
						System.out.print(
								"Digite o preço (sem desconto) do produto desejado na " + nomeConcorrente[2] + " : ");
						int precoProdutoX = teclado.nextInt();
						System.out.println(" ");
						System.out.println("Analisando as taxas de descontos do concorrente, concluímos: \n"
								+ "O produto desejado custará na " + nomeConcorrente[2] + ": R$"
								+ (precoProdutoX - (precoProdutoX * descAvista[2]) / 100) + " à vista e R$"
								+ (precoProdutoX - (precoProdutoX * descCredito[2]) / 100) + " no crédito.");
						System.out.println(" ");
						System.out.println(
								"Notamos que você é uma pessoa legal. Portanto, verificaremos o seu desconto \nem "
										+ "nossa loja para esse produto... ");
						System.out.println(" ");
						System.out.println("Pronto! Segue abaixo os nossos super descontos:");
						System.out.println("Desconto de " + (descAvista[2] + aumentoDescVekAvista)
								+ "% para compras à vista;\n" + "Desconto de "
								+ (descCredito[2] + aumentoDescVekCredito) + "% para compras no crédito;");
						System.out.println(" ");
						System.out.println("Sendo assim, o produto desejado irá custar em nossa loja: \n" + "R$"
								+ (precoProdutoX - (precoProdutoX * (descAvista[2] + aumentoDescVekAvista)) / 100)
								+ " à vista; \nR$"
								+ (precoProdutoX - (precoProdutoX * (descCredito[2] + aumentoDescVekCredito)) / 100)
								+ " no crédito!");
						System.out.println(" ");
						System.out.println("Para confirmar a compra e garantir a reserva"
								+ "do produto digite 1, caso contrário, digite 0: ");
						int confirma = teclado.nextInt();
						if (confirma != 0) {
							System.out.println("Muito bem! Seu produto está esperando por você!\nPara retirá-lo,"
									+ " basta apresentar documento do CPF " + cpf + ".");
							System.out.println("- O comprovante de reserva será encaminhado para o email " + email
									+ ".\n- Um SMS" + " foi enviado para o telefone " + telefone + ".");
							System.out.println(" ");
							System.out.println("Agradecemos a confiança!");
							System.out.println(" ");
							System.out.println("VEK!");
							System.exit(0);
						} else {
							System.out.println("Muito bem! Aguardamos seu retorno!");
							System.exit(0);
						}

						break;
					}
					case 4: {
						System.out.print(
								"Digite o preço (sem desconto) do produto desejado na " + nomeConcorrente[3] + " : ");
						int precoProdutoX = teclado.nextInt();
						System.out.println(" ");
						System.out.println("Analisando as taxas de descontos do concorrente," + "3 concluímos: \n"
								+ "O produto desejado custará na " + nomeConcorrente[3] + ": R$"
								+ (precoProdutoX - (precoProdutoX * descAvista[3]) / 100) + " à vista e R$"
								+ (precoProdutoX - (precoProdutoX * descCredito[3]) / 100) + " no crédito.");
						System.out.println(" ");
						System.out.println(
								"Notamos que você é uma pessoa legal. Portanto, verificaremos o seu desconto \nem "
										+ "nossa loja para esse produto... ");
						System.out.println(" ");
						System.out.println("Pronto! Segue abaixo os nossos super descontos:");
						System.out.println("Desconto de " + (descAvista[3] + aumentoDescVekAvista)
								+ "% para compras à vista;\n" + "Desconto de "
								+ (descCredito[3] + aumentoDescVekCredito) + "% para compras no crédito;");
						System.out.println(" ");
						System.out.println("Sendo assim, o produto desejado irá custar em nossa loja: \n" + "R$"
								+ (precoProdutoX - (precoProdutoX * (descAvista[3] + aumentoDescVekAvista)) / 100)
								+ " à vista; \nR$"
								+ (precoProdutoX - (precoProdutoX * (descCredito[3] + aumentoDescVekCredito)) / 100)
								+ " no crédito!");
						System.out.println(" ");
						System.out.println("Para confirmar a compra e garantir a reserva"
								+ "do produto digite 1, caso contrário, digite 0: ");
						int confirma = teclado.nextInt();
						if (confirma != 0) {
							System.out.println("Muito bem! Seu produto está esperando por você!\nPara retirá-lo,"
									+ " basta apresentar documento do CPF " + cpf + ".");
							System.out.println("- O comprovante de reserva será encaminhado para o email " + email
									+ ".\n4- Um SMS" + " foi enviado para o telefone " + telefone + ".");
							System.out.println(" ");
							System.out.println("Agradecemos a confiança!");
							System.out.println(" ");
							System.out.println("VEK!");
							System.exit(0);
						} else {
							System.out.println("Muito bem! Aguardamos seu retorno!");
							System.exit(0);
						}

						break;
					}
					case 5: {
						System.out.print(
								"Digite o preço (sem desconto) do produto desejado na " + nomeConcorrente[4] + " : ");
						int precoProdutoX = teclado.nextInt();
						System.out.println(" ");
						System.out.println("Analisando as taxas de descontos do concorrente, concluímos: \n"
								+ "O produto desejado custará na " + nomeConcorrente[4] + ": R$"
								+ (precoProdutoX - (precoProdutoX * descAvista[4]) / 100) + " à vista e R$"
								+ (precoProdutoX - (precoProdutoX * descCredito[4]) / 100) + " no crédito.");
						System.out.println(" ");
						System.out.println(
								"Notamos que você é uma pessoa legal. Portanto, verificaremos o seu desconto \nem "
										+ "nossa loja para esse produto... ");
						System.out.println(" ");
						System.out.println("Pronto! Segue abaixo os nossos super descontos:");
						System.out.println("Desconto de " + (descAvista[4] + aumentoDescVekAvista)
								+ "% para compras à vista;\n" + "Desconto de "
								+ (descCredito[4] + aumentoDescVekCredito) + "% para compras no crédito;");
						System.out.println(" ");
						System.out.println("Sendo assim, o produto desejado irá custar em nossa loja: \n" + "R$"
								+ (precoProdutoX - (precoProdutoX * (descAvista[4] + aumentoDescVekAvista)) / 100)
								+ " à vista; \nR$"
								+ (precoProdutoX - (precoProdutoX * (descCredito[4] + aumentoDescVekCredito)) / 100)
								+ " no crédito!");
						System.out.println(" ");
						System.out.println("Para confirmar a compra e garantir a reserva"
								+ "do produto digite 1, caso contrário, digite 0: ");
						int confirma = teclado.nextInt();
						if (confirma != 0) {
							System.out.println("Muito bem! Seu produto está esperando por você!\nPara retirá-lo,"
									+ " basta apresentar documento do CPF " + cpf + ".");
							System.out.println("- O comprovante de reserva será encaminhado para o email " + email
									+ ".\n- Um SMS" + " foi enviado para o telefone " + telefone + ".");
							System.out.println(" ");
							System.out.println("Agradecemos a confiança!");
							System.out.println(" ");
							System.out.println("VEK!");
							System.exit(0);
						} else {
							System.out.println("Muito bem! Aguardamos seu retorno!");
							System.exit(0);
						}

						break;
					}
					default: {
						System.out.println("Opção inválida!!");
						break;
					}

					}
				}

			}
		}
	}
}

