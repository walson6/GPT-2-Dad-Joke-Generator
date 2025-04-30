# Dad Joke Generator with GPT-2

## Objective
To create a GPT-2 based model fine-tuned on a dad jokes dataset that generates creative and humorous dad jokes with customizable parameters for originality and coherence.

## Implementation

### 1. Data Preparation
- Utilized the `dad-a-base-of-jokes` dataset containing a collection of dad jokes in CSV format.
- Cleaned and preprocessed the dataset to ensure proper format for fine-tuning.
- The dataset was loaded into memory for easy access during the fine-tuning process.

### 2. Model Training and Fine-Tuning

#### GPT-2 Fine-Tuning
- **Architecture**: Fine-tuned the pre-trained GPT-2 model on the dad jokes dataset, leveraging its transformer architecture to generate jokes based on the input data.
- **Training**: Fine-tuned for 500 steps with a learning rate optimized for text generation.
- **Performance**: Evaluated joke generation using different temperatures, top-k, and top-p values to balance creativity and coherence.
- **Observations**: 
  - Lower temperatures (0.7) produced more coherent but repetitive jokes.
  - Higher temperatures (1.2 and above) generated more creative but occasionally nonsensical jokes.
  - Top-k and top-p sampling further refined the joke generation by limiting the model's choice of words based on likelihood.

#### Hyperparameter Exploration
- **Temperature**: Experimented with various temperatures ranging from 0.7 to 1.5 to control joke originality and randomness.
- **Top-K Sampling**: Tested different values for top-k (0 to 80) to restrict the word selection process and improve output coherence.
- **Top-P Sampling**: Adjusted top-p (0.8 to 1.0) to dynamically sample words from the cumulative probability distribution.

### 3. Joke Generation
- Generated multiple samples of dad jokes with varying levels of creativity using custom parameters.
- The model was set to produce 100 jokes per run and saved them to a text file for easy access and further review.
- Evaluated output using different configurations of temperature, top-k, and top-p to analyze how these parameters influence the generated jokes.

## Skills Demonstrated
- Python programming for machine learning and text generation workflows.
- Fine-tuning of a pre-trained GPT-2 model using TensorFlow/Keras.
- Data preprocessing and handling of text datasets.
- Experimentation with hyperparameters like temperature, top-k, and top-p to control text generation.
- Visualization and analysis of generated jokes for evaluating creativity and coherence.

## Tools and Libraries Used
- Python  
- TensorFlow 2.x  
- gpt-2-simple  
- pandas  
- NumPy  
- Kaggle API for dataset management
