Agora que combinamos as operações, a coisa vai ficando um pouco mais complicada, porque é necessário ter **mais cuidado com a ordem**.

Por exemplo, veja o programa que você escreveu:

``` puppet
program {
  Colocar(Vermelho)
  Mover(Leste)
  Colocar(Preto)
}
```
 
Operacionalmente:

1. Coloca uma vermelha
2. Em seguida se move para o leste
3. Logo coloca uma preta.

Ou seja: coloca uma vermelha na posição inicial, e uma preta ao leste

E agora veja este outro:

``` puppet
program {
  Mover(Leste)
  Colocar(Vermelho)
  Colocar(Preto)
}
```

Operacionalmente:
1. Se move ao leste
2. Em seguida coloca uma vermelha
3. Logo coloca uma preta

Ou seja: coloca uma vermelha e uma preta ao leste da posição inicial.

Moral da história:  não fazem a mesma coisa! Mudar a ordem mudou o _que_.
