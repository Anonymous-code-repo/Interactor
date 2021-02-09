# Interactor

The implement of "Fast Semantic Matching via Flexible Contextualized Interaction"

1. [Model](#Model)
2. [Dataset](#Dataset)

## Model
![Imgur](https://i.imgur.com/B4KTwRj.png)
### Requirements

- Python 3.7.4
- torch 1.2
- transformers 3.0.1


### Project Structure

```

    └── Crawler                    # Crawler folder
        ├── steam_products.py      # Get all the products information on steam
        ├── steam_reviews.py       # Get all the reviews of one app
        └── main.py                # Main files    
    └── Code                       # Model folder
        └── CGR                    # Model  
            ├── data_process.py    # Preprocessed data
            ├── Evolve_model.py    # Model file
            └── main.py            # Main file
        ├── Dataset                # The data folder
        ├── Dataset_case           # Raw data case folder
        └── other                  # other

```



## Hyperparams
example:
[parameters]
```
batch_size = 32
lr_set = [1,0.1,0.001,0.0001,0.00001]
logdir = 'logdir'

min_user_cnt = 5
min_item_cnt = 5
hidden_units = 512
time_steps = 3
num_epochs = 20
dropout_rate_set = [0.3,0.5,0.7]
alpha_set = [0.0,1.0] # min, max
```


## Usage

1. Install all the required packages

2. process the raw data into the formats according to CGR/data_process.py

3. Run python main.py



