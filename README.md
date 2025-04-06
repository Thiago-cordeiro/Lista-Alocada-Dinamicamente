# 📚 Sistema de Biblioteca Dinâmica em C

Este é um projeto simples de gerenciamento de biblioteca em linguagem C, utilizando alocação dinâmica de memória. O sistema permite:

- Cadastro de livros
- Empréstimo e devolução de livros
- Consulta por ISBN
- Listagem de todos os livros

## 🛠️ Funcionalidades

- Alocação dinâmica de memória para armazenar os livros
- Redimensionamento automático da estrutura de armazenamento
- Verificação de duplicidade de ISBN
- Marcação de livros emprestados ou disponíveis
- Armazenamento de informações do usuário e data de empréstimo

## 📟 Estrutura dos Arquivos

- `main.c`: Código principal para teste das funcionalidades.
- `biblioteca_dinamica.h`: Cabeçalho com as estruturas e protótipos das funções.
- `biblioteca_dinamica.c`: Implementação das funções da biblioteca.

## 🧪 Exemplo de Uso

```c
Biblioteca b;

inicializarBiblioteca(&b);

cadastrarLivro(&b, "A Metamorfose", "Kafka", 1915, "1111111111111");
cadastrarLivro(&b, "O Pequeno Príncipe", "Saint-Exupéry", 1943, "2222222222222");

listarTodosLivros(&b);

emprestarLivro(&b, "1111111111111", "Ana", "04/04/2025");

devolverLivro(&b, "1111111111111");

consultarLivroPorISBN(&b, "2222222222222");

destruirBiblioteca(&b);
```

## 📦 Compilação

Para compilar o programa, você pode usar o `gcc`:

```bash
gcc main.c biblioteca_dinamica.c -o biblioteca
./biblioteca
```

## 📌 Observações

- O sistema utiliza `malloc` e `realloc` para gerenciar a memória dinamicamente.
- A biblioteca é automaticamente expandida quando atinge sua capacidade máxima.
- O ISBN deve ser único para cada livro.

## ✅ Melhorias Futuras

- Persistência em arquivos (salvar/ler livros em arquivos `.txt` ou `.bin`)
- Interface em modo texto interativo
- Validação de entradas do usuário

## 🧑‍💻 Autor

Projeto desenvolvido como prática de estruturas de dados dinâmicas em C.

