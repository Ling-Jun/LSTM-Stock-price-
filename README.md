# Web-App for LSTM powered stock prediction

## Development
Set up environment

* Setup up virtual environment with Anaconda, or VENV

>
    $ conda create --name env_name
>
    $ conda activate env_name

* Install Python 3.7.6

* Install dependencies with pip:

>
    $ pip install -r requirements.txt

## Folder structure
├── .flake8
├── .gitignore
├── Flask_webapp
│   ├── app.py
│   ├── data_preparation_objects
│   │   └── scaler.pkl
│   ├── models
│   │   ├── model_IBM_2_epochs.h5
│   │   └── model_IBM_60_epochs.h5
│   ├── static
│   └── templates
│       ├── index.html
│       └── predict.html
├── LSTM_predictor
│   ├── setup.py
│   └── stockPredictor
│       ├── dataGenerator.py
│       ├── predict.py
│       ├── preload.py
│       └── train.py
├── README.md
├── requirements.txt
└── runtime.txt


## Dataset
* We now allow users to provide a simple stock ticker, the price data will be fetched from Yahoo finance.



# Background Information on Long Short-Term Memory(LSTM)
Long short-term memory (LSTM) unit is a building unit for layers of a recurrent neural network (RNN). A **RNN** composed of LSTM units is often called an LSTM network. A common LSTM unit is composed of a cell, an input gate, an output gate and a forget gate. The cell is responsible for "remembering" values over arbitrary time intervals; hence the word "memory" in LSTM. Each of the three gates can be thought of as a "conventional" artificial neuron, as in a multi-layer (or feedforward) neural network.

An LSTM is well-suited to classify, process and predict time series given time lags of unknown size and duration between important events. LSTMs were developed to deal with the exploding and vanishing gradient problem when training traditional RNNs.
<img src="https://cdn-images-1.medium.com/max/1600/0*LyfY3Mow9eCYlj7o.">
Source: [Medium](https://codeburst.io/generating-text-using-an-lstm-network-no-libraries-2dff88a3968). <br>


## Components of LSTMs
* Forget Gate “f” ( a neural network with sigmoid)
* Candidate layer “C"(a NN with Tanh)
* Input Gate “I” ( a NN with sigmoid )
* Output Gate “O”( a NN with sigmoid)
* Hidden state “H” ( a vector )
* Memory state “C” ( a vector)

* Inputs to the LSTM cell at any step are X<sub>t</sub> (current input) , H<sub>t-1</sub> (previous hidden state ) and C<sub>t-1</sub> (previous memory state).  
* Outputs from the LSTM cell are H<sub>t</sub> (current hidden state ) and C<sub>t</sub> (current memory state)
