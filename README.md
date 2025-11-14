# Testes funcionais Caixa Branca UI/UX

## Notação de Grafo de Fluxo
![Descrição da imagem](imagens/Diagrama.jpg)

### Descrição

**Método verificarUsuario**  

**N1** - Início do método  
**N2** - Chama o método conectarDB para receber o objeto de conexão  
**N3** - Monta query SQL  
**N4** - Entra no try  
**N5** - Roda a query através da conexão  
**N6** - Verfica se existe retorno do banco  
**N7** - Define a variável nome como o retornado pelo banco, e a variável result como true  
**N8** - Recebe a exceção em caso de erro  
**N9** - Retorna a variável result  

**Método conectarDB**

**N1** - Início do método  
**N2** - Inicializa variável do tipo Connection  
**N3** - Entra no try  
**N4** - Define a string de conexão com o banco e solicita a conexão   
**N5** - Recebe a exceção em caso de erro  
**N6** - Retorna o objeto de conexão  


## Complexidade Ciclomática

**Método verificarUsuario**  

**E (Arestas)** = 10  
**N (Nós)** = 9  
**P (Componentes)** = 1  

**M (Complexidade)** = 10 - 9 + 2 x 1 = **3**  

**Método concetarDB**  

**E (Arestas)** = 6  
**N (Nós)** = 6  
**P (Componentes)** = 1  

**M (Complexidade)** = 6 - 6 + 2 x 1 = **2**  

**Classe Usuário completa**  
 
**E (Arestas)** = 16  
**N (Nós)** = 15  
**P (Componentes)** = 2  

**M (Complexidade)** = 16 - 15 + 2 x 2 = **5**  


## Caminhos Básicos

**Método verificarUsuario - 3 Caminhos Básicos**  

**Caminho 1 *(Sem erro de exceção e resultado encontrado no banco)*:** 1 -> 2 -> 3 -> 4 -> 5 -> 6 -> 7 -> 9  
**Caminho 2 *(Sem erro de exceção e sem resultado encontrado no banco)*:** 1 -> 2 -> 3 -> 4 -> 5 -> 6 -> 9  
**Caminho 3 *(Com erro de exceção)*:** 1 -> 2 -> 3 -> 4 -> 8 -> 9   

**Método conectarDB - 2 Caminhos Básicos**  

**Caminho 1 *(Sem erro de exceção)*:** 1 -> 2 -> 3 -> 4 -> 6  
**Caminho 2 *(Com erro de exceção)*:** 1 -> 2 -> 3 -> 5 -> 6  
