Text embeddings are essential for projects relying on textual context, as computers interpret data as numbers. This project explores converting textual information into machine-readable language using techniques like "TF-IDF," "One-Hot Encoding," "GloVe," and "BERT." Here, I implemented the "Word2Vec" model. 

EXAMPLE : { Skip-gram model }

SENTENCE = "This is a word embeddings project".

    words -> {word, embeddings, project} 
    window size = 2  

    central word = {embeddings}
       context , target     
    {embeddings, word} 
    {embeddings, project}
    {embeddings, a} 
    

STEPS FOR PREDICTING THE TARGET WORDS GIVEN CONTEXT :

    1. extract frequent words and remove noise
    2. perform one-hot encoding for these words(vocabulary)
    3. pass into a neural network model with 3 layers
            -> 1st layer - one-hot encoding layer
            -> 2nd layer - embeddings layer
                {one-hot encodings -> dense vectors}
            -> 3rd layer - softmax  layer
                {calculating the probability}
            -> Training the model
                {calculate the loss and backpropagation}
