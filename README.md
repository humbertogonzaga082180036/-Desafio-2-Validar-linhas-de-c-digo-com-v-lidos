# -Desafio-2-Validar-linhas-de-c-digo-com-v-lidos
Desafio Relacionando N2 1°Bimestre

importação java.util.Stack;
importação java.util.Scanner;

classe Principal {
  público estático vazio principal(String[] args) {
    tentar{
      Sistema. para fora. println("Digite o conjunto de simbolos que deseja validar (Digite apenas { ( & lt; > ) }" );
      Leitura do scanner = novo Scanner(Sistema. em);
      Símbolos de cordas = leitura. nextLine();

      se(isValid(símbolos){{
        Sistema. para fora. println("Conjuntoválido! " );
      } mais{
        Sistema. para fora. println("Conjunto inválido!" );
      }
    }captura(errode exceção){
      Sistema. para fora. println(erro);
    }
  }

  estático boolean isValid( Conjunto decordas ){
    Stack<Caractere> stackOpenings = nova Pilha();
    para(int i = 0; i < conjunto. comprimento(); eu++){
      se(! isValidChar(definido. charAt(i)){
        Sistema. para fora. println("Um simbolo não faz parte do alfabeto" );
        retorno falso;
      }
      se(isOpen(definido. charAt(i)){
 pilhaSAnças. push (set. charAt(i));
      }mais{
        se(stackApés. isEmpty()){
          retorno falso;
        }
        se(isNotAPairOfSymbol(definido). charAt(i), stackOpenings. espiar()){
          retorno falso;
        }
 pilhaSAnças. pop();
      }
    }
    pilha de retornoApés . isEmpty();
  }

  estático boolean isValidChar( símbolo char){
    símbolo de retorno ==  {'  || símbolo ==  '[ ||  símbolo ==  '('  || símbolo ==  '& lt;'  || símbolo ==  }'  || símbolo ==  '' ||  símbolo ==  )'  || símbolo   == '>';
  }

  isOpen booleano estático ( símbolo char){
    símbolo de retorno ==  {'  || símbolo ==  '[ '  || símbolo ==  '('  || símbolo == '<';
  }

  estático booleano isNotAPairOfSymbol( símbolo charClosed , char symbolAed ){
    símbolo de retornoClosed ==  }'  & amp;& symbolAtocido !=  {'  || símboloClosed ==  ''  & amp;& symbolAtou !=  '[ '  || símboloClosed ==  ') ' &  amp;&  símboloAtou !=  '('  || símboloClosed ==  '>'  & amp;& symbolApesado != '<';
  }
}
