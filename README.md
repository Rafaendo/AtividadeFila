# AtividadeFila

#include <stdio.h>
#include <stdlib.h>
#include "fila.h"

int main(void) {

  enfileirar(1);
  enfileirar(2);
  enfileirar(3);
  
  exibir();

int fila[TAM_FILA], ultimaPosicao=0;

void enfileirar(int valor){

  if(cheia()){

    printf("Fila cheia!");

  }
  else{

    fila[ultimaPosicao] = valor;
    ultimaPosicao++;

  }

}

int desenfileirar(){
  
  int itemRetirado = 0;

  if(vazia()){

    printf("Fila vazia!");

  }
  else{

    itemRetirado = fila[0];
    for(int i=0; i < ultimaPosicao-1; i++){
      fila[i] = fila[i+1];
    }

    ultimaPosicao--;

  }

  return itemRetirado;

}

int vazia(){

  if(ultimaPosicao == 0){
    return 1;
  }
  else{
    return 0;
  }

}

int cheia(){

  if(ultimaPosicao == TAM_FILA){
    return 1;
  }
  else{
    return 0;
  }

}

void exibir(){

int vazia()
{
    int resultado = 1;
    //Se resultado=1 significa que todos estão vazios e se for = 0 ele tem algum espaço cheio.
    for (int i = 0; i < TAM_FILA; i++) {
        //Checa cada item para ver se não estão vazios
        if (fila[i] != 0) {
            resultado = 0;
        }
    }
    return resultado;
}




if(ultimaPosicaoVazia == 0){
    return 1;
  }else{
    return 0;
  }
