package Swing;

import java.text.SimpleDateFormat;
import java.util.Date;
import java.util.Scanner;
import java.util.logging.Logger;

import javax.swing.JOptionPane;
// @author Daniel Eloy

public class PainelSimples {

	public static void main(String[] args) {
		String nome = null;
		String sobrenome = null;
		String idade = null;
		String apelido = null;
		int resposta = 0;
		String datahora = new SimpleDateFormat("dd/MM/yyyy, HH:mm:ss").format(new Date());
		Logger logger = Logger.getLogger(Scanner.class.getName());

		logger.info("Iniciando Painel");
		
			nome = JOptionPane.showInputDialog("Qual é o seu nome ?");
			sobrenome = JOptionPane.showInputDialog(null, "Qual é o seu sobrenome ?");
			idade = JOptionPane.showInputDialog(null, "Qual é sua idade ?");
			apelido = JOptionPane.showInputDialog(null, "Qual é seu apelido ?");
			
			resposta = JOptionPane.showConfirmDialog(null, "Seu nome é, " + (nome + " " + sobrenome) 
					+ ", tem " +idade+ " anos e o apelido é " + apelido + "?"
					, ("Confirma que:"), JOptionPane.YES_NO_OPTION);	
		if (resposta == JOptionPane.YES_OPTION) {
			JOptionPane.showInternalMessageDialog(null, datahora+ "\nObrigado pela confirmação","Registro",1);
			
			logger.info(datahora 
					+ "\nNome setado: " + nome 
					+ "\nSobrenome setado: " + sobrenome 
					+ "\nidade setado: " + idade 
					+ "\nApelido setado: " + apelido);	
		} else {
			JOptionPane.showMessageDialog(null, "Favor preencher os campos corretamente. ", "Registro: "+datahora,2);
			return;
		}
	}
}

