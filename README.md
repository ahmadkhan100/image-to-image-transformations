# image-to-image-transformations


## Setup

### Client

The client is a react app built with yarn: 

```sh
cd client
yarn install && yarn dev
```

By default, the client runs on port `5173`.

### Server

To run the server, create a python virtual environment and install the dependencies in `requirements.txt`. Then, in the root directory, run 

```sh
python3 run.py
```

By default, the server runs on port `3000`. The only function of the server is to parse requests from the client and submit to our model endpoint (see below). 

## Web deployment

The client and flask server is deployed on [Render](https://render.com/). 

## Model deployment

All models are deployed on [ModelBit](https://www.modelbit.com/), and all model inference requires around 4GB RAM. The deployment script is very simple and lives in `modelbit.ipynb`. One thing to note when deploying is that the python package `image-to-image-translation-server` must be self-contained, i.e., it will not have access to a `.env`. This means that `server/config.py` must be modified to include actual values rather than what is included right now.

## TODO

- finish the remainder of the models
- update the gallery with actual results
