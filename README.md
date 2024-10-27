<h1 align="center">Simulador de Maquina de Turing</h1> 
<p align="center">Trabalho realizado na matéria de Teoria da Computação, de implementar um Simulador de Maquina de Turing Finitos</p>

## 🚀 Maquina de Turing



## 💻 Sobre o projeto

A ferramenta recebe um arquivo do tipo JSON com as especificações da maquina desejada no seguinte padrão:

```
{
    "initial" : 0,
    "final" : [4],
    "white" : "_",
    "transitions" : [
        {"from": 0, "to": 1, "read": "a", "write": "A", "dir":"R"},
        {"from": 1, "to": 1, "read": "a", "write": "a", "dir":"R"},
        {"from": 1, "to": 1, "read": "B", "write": "B", "dir":"R"},
        {"from": 1, "to": 2, "read": "b", "write": "B", "dir":"L"},
        {"from": 2, "to": 2, "read": "B", "write": "B", "dir":"L"},
        {"from": 2, "to": 2, "read": "a", "write": "a", "dir":"L"},
        {"from": 2, "to": 0, "read": "A", "write": "A", "dir":"R"},
        {"from": 0, "to": 3, "read": "B", "write": "B", "dir":"R"},
        {"from": 3, "to": 3, "read": "B", "write": "B", "dir":"R"},
        {"from": 3, "to": 4, "read": "_", "write": "_", "dir":"L"}      
    ]
}
```

Junto com um arquivo txt com as entradas, da seguinte forma:

```
aabb
```

E então o arquivo de saida, que armazena a fita resultante ao final de todas as operações. Na linha de comando é mostrado se a entrada foi ou não aceita.

```
AABB_
```

## ⚙️ Executando 

Para executar o programa utiliza-se o comando 
```
$ python simulador.py <arquivo_da_maquina_de_turing.json> <arquivo_de_entrada.in> <arquivo_de_saida.out>
```

E é necessario que contenha o nome dos três arquivos a serem utilizados para funcionar
