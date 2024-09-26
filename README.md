[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/3YVg2wK-)
[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=16173877&assignment_repo_type=AssignmentRepo)
  
### Após essa implementação observamos: 

- **Na classe `CorpoHumano`, inclua a linha `c1.massa = "2";` logo depois de instanciar o objeto `c1`.**

  **Situação:** Um erro de compilação foi gerado.  
  Isso ocorreu devido ao atributo `massa` ser privado, ou seja, ele não pode ser acessado ou modificado diretamente fora da classe `CorpoHumano`. Para alterar o valor de `massa`, é necessário usar o método `setMassa()`.

- **Na classe `CorpoHumano`, alterando a linha `private double massa` para `public double massa`.**

  **Situação:** Após essa alteração, será possível acessar e modificar o atributo `massa` diretamente através do objeto `c1` (por exemplo, `c1.massa = 2`).  
  Ao tornar o atributo público, o encapsulamento é quebrado, permitindo que outros objetos ou classes modifiquem diretamente o valor do atributo, o que pode gerar inconsistências no controle dos dados da classe. O uso de modificadores de acesso privados e de métodos setters/getters é uma boa prática de programação para proteger os atributos da classe.

- **Na classe `CorpoHumano`, alterando a linha `public void setVolume(double entVolume)` para `private void setVolume(double entVolume)`.**

  **Situação:** Depois de fazer essa alteração, o método `setVolume()` não poderá ser acessado fora da classe `CorpoHumano`. Se tentar invocar o método em outro lugar (como na classe `main`), gera um erro de compilação.  
  Torná-lo um método privado impede que ele seja acessado por outras classes, ou seja, o volume não pode mais ser modificado diretamente após a criação do objeto. Isso mostra a importância de controlar o acesso aos métodos que alteram o estado dos atributos, restringindo alterações indesejadas e protegendo a integridade dos dados.
