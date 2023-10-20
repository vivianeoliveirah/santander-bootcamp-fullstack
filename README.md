# Santander Bootcamp FullStack

## Diagrama de Classes

^^^mermaid

classDiagram
class User { - id: int - name: string - accounts: Account[] - cards: Card[] - features: Feature[] - news: News[]
}

class Account { - id: int - number: string - agency: string - balance: float - limit: float
}

class Card { - id: int - number: string - limit: float
}

class Feature { - id: int - icon: string - description: string
}

class News { - id: int - icon: string - description: string
}

User "1" _-- "1..\_" Account : has
User "1" _-- "N.._" Feature : has
User "1" \*-- "1.._" Card : has
User "1" \*-- "N..\_" News : has

^^^
