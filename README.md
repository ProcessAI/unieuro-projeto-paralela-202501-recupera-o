# unieuro-projeto-paralela-202501-recupera-o
Atividade de Recuperação de Paralela


## Atividade

O Aluno deve paralelizar o código base e montar o relatório com tabela e gráficos de tempo, eficiência e speedup.
A solução deve ser publicada em um repositório do GitHub, o relatário deve ser escrito no readme e o link do github no AVA.

* Implemente uma versão paralela com threads da função soma_serial.
* Divida o vetor em partes iguais entre as threads.
* Cada thread deve calcular a soma da sua parte.
* Ao final, junte os resultados parciais para obter a soma total.
* Meça o tempo de execução, speedup e eficiência para 1, 2, 4 e 8 threads.


## Código Base

```
import time
import random

def gerar_vetor(tamanho):
    return [random.randint(1, 100) for _ in range(tamanho)]

def soma_serial(vetor):
    soma = 0
    for valor in vetor:
        soma += valor
    return soma

if __name__ == "__main__":
    tamanho_vetor = 100_000_000
    vetor = gerar_vetor(tamanho_vetor)

    inicio = time.time()
    resultado = soma_serial(vetor)
    fim = time.time()

    print(f"Soma: {resultado}")
    print(f"Tempo (serial): {fim - inicio:.4f} segundos")

```
