# AVLtree / Arvore AVL
Este código ajuda você a compreender como é o algoritmo AVLtree ou em português Arvore AVL
Meu algoritmo foi dividido em 4 Classes, sendo elas: 

  - Principal.java
  - NoAvl.java
  - Corpo.java
  - ArvoreAVL.java
  
### Requisitos de código
O código de exemplo está em Java ([versão 1.8] (https://java.com/en/download/) ou superior funcionará).

### Descrição
  Segundo o Wikipedia Árvore AVL é uma árvore binária de busca balanceada[2], ou seja, uma árvore balanceada (árvore completa) são as árvores que minimizam o número de comparações efetuadas no pior caso para uma busca com chaves de probabilidades de ocorrências idênticas.
  Ou seja: serve para organizar itens e depois conseguir encontrar tais itens com mais facilidade.
            
  Funciona de tal forma:<br>
<img align="center" src="https://github.com/wesleyvicen/AVLtree/blob/master/imgs/AVLtree.gif">


Classe `Corpo.java` 
tem o Menu, esté a baixo
```java
		while (opcao != 0) {
			System.out.println("\n1 INSERIR");
			System.out.println("2 REMOVER");
			System.out.println("3 EXIBIR ( Em-ordem )");
			System.out.println("0 SAIR");
			opcao = scan.nextInt();
			if (opcao == 1)
				inserir();
			else if (opcao == 2)
				remover();
			else if (opcao == 3)
				exibir();

		}
``` 

 Você pode selecionar qualquer função da lista, `INSERIR` seria para inserir itens na Arvore, `remover` seria para remover e `EXIBIR`, seria para exibir os itens da arvore, isso em Pre ordem. e por fim tem a função `SAIR`

Classe `NOavl.java`
Seria o NO, onde armazena informações da arvore
Atributos usados no NO
```java
    	protected int altura;       // altura = Balanco
    	protected int valor;
        protected NoAvl esquerda, direita;
``` 

Classe `ArvoreAVL.java`
Está é a classe onde se encontra tudo, todos os métodos e funções necessarias para que a mesma funcione em percefeita armonia.

Um dos metodos é o inserir, este logo abaixo.
```java
		if (no == null) {
			no = new NoAvl(x, null, null);
		} else if (x == no.valor)
			System.out.println("elemento j? presente!");
		else if (x < no.valor) {
			System.out.println("  Inserindo " + x + " a esquerda de " + no.valor);
			no.esquerda = inserir(x, no.esquerda);
		} else if (x > no.valor) {
			System.out.println("  Inserindo " + x + " a direita de " + no.valor);
			no.direita = inserir(x, no.direita);

		}
		no = balance(no);
``` 

### Execução
Para compilar o código, simplesmente execute o `javac principal.java`.
Para executar o código, digite `java principal`

`` `
javac principal.java
java principal
`` `
