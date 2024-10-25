# chunk-strategies-for-rag
## 1. Fixed size chunking:
divide o texto de acordo com um numero pré definido de caracteres.

**Exemplo:**

```palintext

"Machine learning é uma área da inteligência artificial que permite que sistemas aprendam e façam previsões a partir de dados."

Dividindo em chunks de 20 caracteres:
1. "Machine learning é um"
2. "a área da inteligênc"
3. "ia artificial que pe"
4. "rmite que sistemas a" 
```
## 2. Recursive chunking
divide o texto de acordo com pontuações (exemplos: '.', ':', '!', '?', )

```palintext
"A análise de dados é essencial. Ela permite identificar padrões. Pode revelar insights profundos!"

Chunks:
1. "A análise de dados é essencial."
2. "Ela permite identificar padrões."
3. "Pode revelar insights profundos!"
```



## 3. Recursive character chunking
Similar ao chunk de tamanho fixo, porém há uma sobreposição de caracteres caso haja necessidade, onde um chunk pode iniciar com os ultimos 'n' caracteres do chunk anterior.

**Exemplo:**

```palintext
"A segmentação de texto facilita a análise e compreensão."

Dividindo em chunks de 20 caracteres com uma sobreposição de 5 caracteres:
1. "A segmentação de text"
2. "de texto facilita a a"
3. "cilita a análise e co"
```

## 4. Semantic chunking 
Divide o texto de acordo com base na semântica e significado, utiliza modelo de embeddings para tal, e cria divisões onde há uma mudança de idéia ou contexto.

**Exemplo utilizado no código:**

![Gráfico](./grafico.png)



