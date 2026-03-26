Bitcoin Price Prediction using LSTM

What’s this project about?
I’ve always been fascinated by how data tells a story, especially in the volatile world of Crypto. This project is my first deep dive into transitioning from a Data Analyst mindset to AI Engineering. I built a predictive model using LSTM (Long Short-Term Memory) to see if we can actually "tame" Bitcoin’s price movements.

The Tech I Used
I kept it professional but effective:

The Brain: TensorFlow & Keras (LSTM Layers).

The Data: Real-time prices via the yfinance API.

The Tools: Python, Pandas, NumPy, and Scikit-Learn.

The "Real" Challenges (The fun part!)
Building the model wasn't just about writing code; it was about solving headaches that any real-world dev faces:

The NaN Nightmare: Financial data is messy. I had to implement a solid cleaning pipeline using Forward Fill (ffill) to make sure the model didn't "choke" on missing values.

Taming the Gradients: At one point, the numbers went wild (Exploding Gradients). I fixed this by implementing Gradient Clipping, which acted as a safety net for the model during training.

Scaling: Used MinMaxScaler to keep the data in a range the neural network could actually understand without losing its mind.

Model Breakdown
Architecture: Used Stacked LSTMs with Dropout (0.2) layers. Why? To make sure the model doesn't just "memorize" the past but actually learns to generalize for the future.

Optimization: Adam optimizer with MSE loss – simple, classic, and it works.
’ve saved the final "trained brain" as btc_lstm_model.h5. You can skip the training and load it directly
