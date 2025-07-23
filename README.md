# brain-to-text25-TeamLomas
Competition entry for Kaggle competition "Brain-to-Text '25"

## Exploratory Data Analysis
1. How long are the timeseries and how much do the lengths vary?
2. How strong is the correlation between timeseries length and target sentence length?
3. What is the variation in signal amplitude? Should any normalization be applied to scale the timeseries?
4. Are data from spoken and silent sentences noticeably different in any way?
5. Are data from each sentence corpus different in any way? 

## Model development
1. Write dataloader and collator for timeseries input/labels
2. Use PatchTST to produce generalized latents for timeseries inputs (https://github.com/yuqinie98/DLinear-Benchmarks)
4. Use pretrained GPT2-small or FLAN-T5-small decoder for generative text prediction

## Model training and testing 
1. First try fine-tuning the whole model
2. If too heavy, train free encoder and frozen decoder with peft adaptors 

## Ideas
1. Add spoken or silent class tag to decoder outputs. Encouraging the model to differentiate between the two. 
