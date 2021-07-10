# mrscc
Using the Hugging Face Trainer I use the RoBERTa model to compete in the Microsoft Research Sentence Completion Challenge to achieve an accuracy of 82.6. A CBOW model is also implemented on the MRSCC. Notebooks are provided for both models.

Two notebooks are presented, each notebook presents a different architectural approach to the challenge. One is the CBOW model, the other is the RoBERTa model using the hugging face trainer.

Both have been developed within Colab using a dedicated GPU for training. Please note, that the CBOW model is developed in pytorch, specifically, pytorch lightning has been used to reduce boiler plate code and improve the development experience. Furthermore, Ray Tune has been used to launch optimisation trials for both approaches. 
For the hugging face RoBERTa model, the Hugging Face trainer (which uses Pytorch internally) was used as this offers fantastic and easy to use functionality.

Each main section of each notebook have comparable headings, the general work flow is as follows for both of them.

1. Import libraries
2. Load MRSCC data
3. Load data in datasets for model
4. Declare model and get ready for training.
5. Automatic or manual hyper-parameter tuning over range of parameters.
6. Test model on the MRSCC sentences using a variety of techniques. Declare accuracy.
