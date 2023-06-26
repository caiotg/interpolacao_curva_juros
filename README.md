# Interpolação curva de Juros

A interpolação é um método utilizado para estimar valores intermediários entre pontos conhecidos em uma curva de taxa de juros. Isso é útil em situações em que você possui dados limitados, mas precisa de estimativas precisas para valores ausentes. Essa técnica é amplamente utilizada no mercado financeiro para precificar instrumentos financeiros, como títulos de dívida, swaps e derivativos.

Existem várias abordagens para a interpolação de curva de juros, sendo as mais comuns a interpolação linear e a interpolação cúbica. Vou explicar brevemente cada uma delas:

* **Interpolação Linear:** A interpolação linear é uma técnica simples de interpolação utilizada para estimar valores intermediários entre dois pontos conhecidos em uma curva ou uma série de dados. Essa técnica assume uma relação linear entre os pontos conhecidos e utiliza essa relação para estimar o valor desconhecido.
* **Interpolação Cúbica:** A interpolação cúbica é um método mais avançado de interpolação que utiliza um polinômio cúbico para ajustar uma curva suave entre os pontos conhecidos. Ao contrário da interpolação linear, que assume uma relação linear entre os pontos, a interpolação cúbica leva em conta tanto os valores das taxas de juros como as inclinações (derivadas) em cada ponto conhecido. A interpolação cúbica geralmente produz estimativas mais suaves e precisas das taxas de juros desconhecidas.

É importante ressaltar que a interpolação é uma técnica de estimativa e, portanto, está sujeita a algumas limitações. Por exemplo, se houver grandes variações ou descontinuidades na curva de juros, a interpolação pode não fornecer resultados precisos. Além disso, a qualidade dos resultados depende da qualidade e da representatividade dos pontos conhecidos da curva de juros.

# Observações sobre o Código

* Para fazer a interpolação da curva de juros é preciso ter os vértices (dias uteis) entre a data atual e a data da expectativa;
* Eu utilizo a interpolação cúbica por ela gerar estimativas mais suaves que a interpolação linear;
* Para fazer uma estimativa mais precisa é possível utilizar a lista de feriados nacionais ao invés de BDay() do pandas.
