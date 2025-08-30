Trading Troll 🤖: An AI-Powered Algorithmic Trading Bot
The Trading Troll is a sophisticated algorithmic trading bot built using the Lumibot framework. It leverages a unique blend of sentiment analysis and technical indicators to make automated trading decisions. The bot is designed to be deployed on the Alpaca trading platform, supporting both paper and live trading environments.

Key Features ✨
Sentiment-Based Strategy: The bot's core logic is powered by a FinBERT sentiment analysis model. It scans recent news headlines for a given stock symbol and gauges the market's sentiment (positive or negative).

Adaptive Trading Logic: The bot only executes trades when the sentiment probability is extremely high (greater than 99.9%), ensuring high-conviction trades. It buys on strong positive sentiment and shorts (sells) on strong negative sentiment.

Dynamic Position Sizing: The bot calculates the appropriate trade quantity based on a user-defined "cash at risk" percentage, ensuring disciplined risk management with every trade.

Automated Risk Management: Each trade is placed using a bracket order, which includes pre-set take-profit and stop-loss levels. This helps lock in gains and limit potential losses without manual intervention.

Backtesting Capabilities: The codebase includes a robust backtesting feature using YahooDataBacktesting. This allows users to test the strategy's performance on historical data before risking real capital.

How It Works 🧠
The bot operates on a simple, yet powerful, loop:

Retrieve Data: It fetches the latest stock price and news headlines for the specified symbol.

Analyze Sentiment: The news headlines are fed into the FinBERT model to determine the sentiment and its probability.

Execute Trade:

If sentiment is overwhelmingly positive, it places a buy order with a 20% take-profit and a 5% stop-loss.

If sentiment is overwhelmingly negative, it places a sell (short) order with a 20% take-profit and a 5% stop-loss.

Manage Positions: The bot automatically manages open positions by closing out any existing trades before entering a new one in the opposite direction.

Getting Started 🚀
Clone the repository: git clone [repository-url]

Install dependencies: pip install -r requirements.txt (The main libraries are lumibot, alpaca-trade-api, and finbert-utils).

Configure API Keys: Create a .env file in the root directory and add your Alpaca API credentials.

Run the bot:

For backtesting, use the provided backtest function to evaluate the strategy's performance.

For live/paper trading, uncomment the Trader class and run the script to deploy the bot.

Note: This bot is a demonstration of an algorithmic trading strategy. Trading involves risk, and past performance is not indicative of future results.

















________________________________________________________________________________________________________________________________________
Trading Troll 🤖: Un Bot de Trading Algorítmico Impulsado por IA
El Trading Troll es un sofisticado bot de trading algorítmico construido con el framework Lumibot. Aprovecha una combinación única de análisis de sentimiento e indicadores técnicos para tomar decisiones de trading automatizadas. El bot está diseñado para ser implementado en la plataforma de trading de Alpaca, compatible con entornos de trading de prueba (paper) y en vivo.

Características Principales ✨
Estrategia Basada en Sentimiento: La lógica central del bot se basa en un modelo de análisis de sentimiento FinBERT. Escanea los titulares de noticias recientes de un símbolo de acciones determinado y mide el sentimiento del mercado (positivo o negativo).

Lógica de Trading Adaptativa: El bot solo ejecuta operaciones cuando la probabilidad de sentimiento es extremadamente alta (superior al 99.9%), lo que garantiza operaciones de alta convicción. Compra en caso de un sentimiento fuertemente positivo y se pone en corto (vende) en caso de un sentimiento fuertemente negativo.

Tamaño de Posición Dinámico: El bot calcula la cantidad de acciones apropiada para operar basándose en un porcentaje de "efectivo en riesgo" definido por el usuario, asegurando una gestión de riesgos disciplinada en cada operación.

Gestión de Riesgos Automatizada: Cada operación se realiza utilizando una orden bracket, que incluye niveles preestablecidos de toma de ganancias (take-profit) y de stop-loss. Esto ayuda a asegurar las ganancias y limitar las pérdidas potenciales sin intervención manual.

Capacidades de Backtesting: El código incluye una sólida función de backtesting utilizando YahooDataBacktesting. Esto permite a los usuarios probar el rendimiento de la estrategia con datos históricos antes de arriesgar capital real.

Cómo Funciona 🧠
El bot opera en un ciclo simple pero potente:

Recuperar Datos: Obtiene el precio de las acciones más reciente y los titulares de noticias del símbolo especificado.

Analizar el Sentimiento: Los titulares de noticias se introducen en el modelo FinBERT para determinar el sentimiento y su probabilidad.

Ejecutar la Operación:

Si el sentimiento es abrumadoramente positivo, coloca una orden de compra con un take-profit del 20% y un stop-loss del 5%.

Si el sentimiento es abrumadoramente negativo, coloca una orden de venta (en corto) con un take-profit del 20% y un stop-loss del 5%.

Gestionar Posiciones: El bot gestiona automáticamente las posiciones abiertas, cerrando cualquier operación existente antes de abrir una nueva en la dirección opuesta.

Primeros Pasos 🚀
Clona el repositorio: git clone [url-del-repositorio]

Instala las dependencias: pip install -r requirements.txt (Las bibliotecas principales son lumibot, alpaca-trade-api y finbert-utils).

Configura las Claves API: Crea un archivo .env en el directorio raíz y añade tus credenciales de la API de Alpaca.

Ejecuta el bot:

Para backtesting, usa la función backtest proporcionada para evaluar el rendimiento de la estrategia.

Para trading en vivo/de prueba, descomenta la clase Trader y ejecuta el script para desplegar el bot.

Nota: Este bot es una demostración de una estrategia de trading algorítmica. El trading conlleva riesgos, y el rendimiento pasado no es un indicativo de resultados futuros.
