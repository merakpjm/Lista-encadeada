# Lista-encadeada
package árvore;

public class arvoremain {

	public static void main(String[] args) {
		
		Arvore<Integer> arvore = new Arvore <Integer>();
		arvore.adicionar(10);
		arvore.adicionar(15);

	}

}

package árvore;

public class Arvore <TIPO extends Compareble> {
	

	public static void main(String args[]) {
		
		private Elemento<TIPO> raiz;
		
		public Arvore(){
			this.raiz = null;
			
		}
		
	    public void adicionar (TIPO valor) {
	    	Elemento<TIPO> novoElemento = new Elemento<TIPO>(valor);
	    	if (raiz == null){
			this.raiz = novoElemento;
	    	}else{
	    		Elemento<TIPO> atual = this.raiz;
	    		
	    	while (true) {
	    		if (novoElemento.getValor() .comparebleTo (atual.getValor()) == -1) {
	    			if (atual.getEsquerda() != null) {
	    				atual = atual.getEsquerda();
	    				
	    			}else{
	    				atual.setEsquerda(novoElemento);
	    				break;
	    			}
	    			
	    		}else{
	    			if (atual.getDireita() != null) {
	    				atual = atual.getDireita();
	    				
	    			}else{
	    				atual.setDireita(novoElemento);
	    				break;
	    			
	    		}
	    	}
	    	}
	    }
	
	}

}

package árvore;

public class Elemento<TIPO>{
	private TIPO valor;
	private Elemento<TIPO> esquerda;
	private Elemento<TIPO> direita;
	
	public Elemento (TIPO novovalor) {
		this.valor = novovalor;
		this.esquerda = null;
		this.direita = null;
	}

	public TIPO getValor() {
		return valor;
	}

	public void setValor(TIPO valor) {
		this.valor = valor;
	}

	public Elemento<TIPO> getEsquerda() {
		return esquerda;
	}

	public void setEsquerda(Elemento<TIPO> esquerda) {
		this.esquerda = esquerda;
	}

	public Elemento<TIPO> getDireita() {
		return direita;
	}

	public void setDireita(Elemento<TIPO> direita) {
		this.direita = direita;
	}
	
	
	
	

}
