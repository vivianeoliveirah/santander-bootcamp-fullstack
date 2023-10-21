# Santander Bootcamp FullStack

## Diagrama de Classes

Você pode usar o Mermaid para criar diagramas de classes no seu README. Aqui está o seu código corrigido:

^^^ mermaid
classDiagram
  class User {
    - id: int
    - name: string
    - accounts: Account[]
    - cards: Card[]
    - features: Feature[]
    - news: News[]
  }

  class Account {
    - id: int
    - number: string
    - agency: string
    - balance: float
    - limit: float
  }

  class Card {
    - id: int
    - number: string
    - limit: float
  }

  class Feature {
    - id: int
    - icon: string
    - description: string
  }

  class News {
    - id: int
    - icon: string
    - description: string
  }

User "1" _-- "1..*" Account : has
User "1" _-- "N..*" Feature : has
User "1" *-- "1..*" Card : has
User "1" *-- "N..*" News : has

^^^
