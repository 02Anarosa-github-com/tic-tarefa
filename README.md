import java.util.Scanner;
public class tarefa{
	public	static	void	main(String[]	args) {
		//	miolo	do	programa	começa	aqui!
		public void criaConta(Evento evento) {
			this.conta = new Conta();
			this.conta.setAgencia(evento.getString("agencia"));
			this.conta.setNumero(evento.getInt("numero"));
			this.conta.setTitular(evento.getString("titular"));
			public void criaConta(Evento evento) {
				String tipo = evento.getSelecionadoNoRadio("tipo");
				if (tipo.equals("Conta Corrente")) {
					this.conta = new ContaCorrente();
				} 
				else if (tipo.equals("Conta Poupança")) {
					this.conta = new ContaPoupanca();
				}
				this.conta.setAgencia(evento.getString("agencia"));
				this.conta.setNumero(evento.getInt("numero"));
				this.conta.setTitular(evento.getString("titular"));
			}
		public class ContaCorrente extends Conta {
			public String getTipo() {
			return "Conta Corrente";
			}
		}
		public class ContaPoupanca extends Conta {
			public String getTipo() {
				return "Conta Poupança";
			}
		}
		public void saca(Evento evento) {
			double valor = evento.getDouble("valorOperacao");
			if (this.conta.getTipo().equals("Conta Corrente")){
				this.conta.saca(valor + 0.10);
			} 
			else {
				this.conta.saca(valor);
			}
		}
	}		
		System.out.println("Minha	primeira	aplicação	Java!!");
		//	fim	do	miolo	do	programa
	}
}
