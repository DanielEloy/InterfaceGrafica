# InterfaceGrafica
 Simples de  introdução
/**
 * @author Daniel Eloy
 *
 */
package teste;
import javax.swing.JOptionPane;

public class nome1{
	public static void main(String[] args) {
		String nome = null;
		String sobrenome = null;
		String idade = null;
		String apelido = null;
		
		nome = JOptionPane.showInputDialog("Qual é o seu nome?");
		sobrenome = JOptionPane.showInputDialog("Qual é o seu sobrenome ?");
		idade = JOptionPane.showInputDialog("Qual é sua idade?");
		apelido = JOptionPane.showInputDialog("Qual é sua idade?");
		
		JOptionPane.showConfirmDialog(null, "O seu nome é " + nome + "\nSeu sobrenome é "+ sobrenome + "\nSua apelido é "+ apelido + "?");
	}
}
