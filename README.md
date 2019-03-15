# Seu Nome no Micro:bit
Este programa faz com que o Micro:bit apresente no seu painel de LEDs as letras do seu nome. 

## ~Dica

Qualquer dúvida na construção, use o link (texto azul) para abrir o vídeo que apresenta como realizar aquele passo.

## ~

## Como funciona
1. Baixe o programa no seu computador.
1. Conecte o Micro:bit e transfira o arquivo HEX.
1. Ao término da transferência, o programa iniciará automaticamente em seu Micro:bit.

## Como incluir o seu nome
O programa funciona por meio de um *loop* (ou repetição) infinito chamado ```||basic:sempre||``` em que o bloco  ```||basic:mostrar string||``` define qual o texto que será apresentado no painel de LEDs do Micro:bit. 

1. Para alterar o texto apresentado pelo Micro:bit altere o texto (*string*) presente no bloco ```||basic:mostrar string||```.

Após a alteração confira o resultado no simulador ou baixando a nova versão do código no seu Micro:bit.

## Mostrando dois nomes
É possível fazer com que o programa apresente mais de um nome de cada vez. Veja abaixo:
1. Vá até o grupo ```||basic:Básico||``` e arraste mais um bloco ``||basic:mostrar string||`` logo abaixo do primeiro nome. Você pode repetir este processo e incluir quantos nomes quiser.

```blocks
basic.forever(function () {
    basic.showString("Nome 1")
    basic.showString("Nome 2")
})
```
Após a alteração confira o resultado no simulador ou baixando a nova versão do código no seu Micro:bit.

## Incluindo imagens
Também é possível incluir imagens para separar cada nome. Veja abaixo como fazer.
1. Usando o grupo ```||basic:Básico||``` arraste o bloco ```||basic:mostrar ícone||``` entre o primeiro e o segundo nome.
1. Escolha um ícone na lista.
1. Ainda usando o grupo ```||basic:Básico||``` arraste o bloco ```||basic:mostrar leds||``` logo abaixo do bloco com o ícone. Deixando o conteúdo do ```||basic:mostrar leds||``` vazio o Micro:bit vai desligar os LEDs evitando que o segundo nome se misture com os LEDs do ícone.

```blocks
basic.forever(function () {
    basic.showString("Nome 1")
    basic.showIcon(IconNames.No)
    basic.showLeds(`
        . . . . .
        . . . . .
        . . . . .
        . . . . .
        . . . . .
        `)
    basic.showString("Nome 2")
})
```

## Créditos
Esta atividade foi criado pelo [APRENDER.digital](https://aprender.digital) usando como base o código do [Name Tag](https://makecode.microbit.org/projects/name-tag).
