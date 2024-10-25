# API-Registration
```mermaid
classDiagram
    class Produto {
        +int id
        +String nome
        +String descricao
        +double preco
        +int quantidade

        +cadastrarProduto()
        +editarProduto()
        +excluirProduto()
        +visualizarProduto()
    }

    class Funcionario {
        +int id
        +String nome
        +String cargo
        +String cpf
        +double salario

        +cadastrarFuncionario()
        +editarFuncionario()
        +excluirFuncionario()
        +visualizarFuncionario()
    }

    class SistemaCadastramento {
        +List~Produto~ produtos
        +List~Funcionario~ funcionarios

        +cadastrarNovoProduto(produto: Produto)
        +cadastrarNovoFuncionario(funcionario: Funcionario)
        +visualizarTodosProdutos()
        +visualizarTodosFuncionarios()
    }

    SistemaCadastramento "1" --> "0..*" Produto : gerencia
    SistemaCadastramento "1" --> "0..*" Funcionario : gerencia
