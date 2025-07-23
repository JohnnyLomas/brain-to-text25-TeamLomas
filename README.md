# brain-to-text25-TeamLomas
Competition entry for Kaggle competition "Brain-to-Text '25"

## Exploratory Data Analysis
1. How long are the timeseries and how much do the lengths vary?
2. How strong is the correlation between timeseries length and target sentence length?
3. What is the variation in signal amplitude? Should any normalization be applied to scale the timeseries?

## Model development
1. Write dataloader and collator for timeseries input/labels
2. Use TS2Vec to produce generalized latents for timeseries inputs (https://github.com/zhihanyue/ts2vec)
3. Identify appropriate pretrained LLM decoder to convert latents into text

## Model training and testing 
1. Any special hyperparameters for TS2Vec? Cross-validate to identify the best ones?
2. Pretrain TS2Vec unsupervised or train the whole model with complete forward passes?
