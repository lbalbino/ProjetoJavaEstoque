# ProjetoJavaStoque

```java

package com.mycompany.projectestoque;

public class MovimentacaoEstoque {
    
        public int produto;

      public int AdicionarStoque(int produtos) {
           return produto + produtos;                  
       }
      
      public int ReduzirStoque(int produtos) {
           return produto - produtos;                  
       }
}

--- Principal 
package com.mycompany.projectestoque;

import java.util.Scanner;

public class ProjectEstoque {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        MovimentacaoEstoque mov = new MovimentacaoEstoque();
        int opcao = 0;

        do {
            
            System.out.println("produtos no estoque " + mov.produto);
            System.out.println("***** Por Favor escolha as opções Abaixo *****");
            System.out.println(" 1.Depositar ");
            System.out.println(" 2.Retirar ");
            System.out.println(" 3.Sair");
            opcao = sc.nextInt();

            if (opcao == 1) {

                System.out.println("Me informe a Quantidades adicionais no estoque:");
                int valorAdicionado = sc.nextInt();

                mov.produto = mov.AdicionarStoque(valorAdicionado);
                
                
            } else if (opcao == 2) {
                
                System.out.println("Me informe a Quantidades reduzido no estoque:");
                int valorAdicionado = sc.nextInt();

                mov.produto = mov.ReduzirStoque(valorAdicionado);
                
                if(mov.produto < 10){                
                    System.out.println("Cuidado, estoque com poucas unidades!");
                }
            }

        }  while (opcao != 3);

    }
}

```


