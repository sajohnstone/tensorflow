# Tensorflow with Node.js

You can download models from [https://github.com/tensorflow/models/blob/master/research/slim/nets/mobilenet_v1.md#pre-trained-models]
once you download a model you need to download the weights binary file(s)
```
cat ./model/model.json | jq -r ".weightsManifest[].paths[0]" | sed 's/^/https:\/\/storage.googleapis.com\/tfjs-models\/tfjs\/mobilenet_v1_1.0_224\//' |  parallel curl -O
```

NB If you are on a mac like me you might need to install 

```
brew install parallel
```

and 

```
brew install jq
```

## Getting Started
```
node script.js model/model.json panda.jpg
```

### Prerequisites



### Installing


## Running the tests
No tests at this time

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details
