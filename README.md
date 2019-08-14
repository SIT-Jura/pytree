# potree server height profile extractor project

*A [Flask application](http://flask.pocoo.org/)*

## Requirements

1. Python 3.7


## Installation on linux, with docker

1. Clone this repository on your machine
2. Build with docker

```
git clone git@github.com:SIT-Jura/pytree.git
cd pytree
docker build -t jura_pytree .
```

## Testing

In GeoMapFish
1. Edit pytree_config.yaml configuration file if needed
2. build GeoMapFish (with ./clean instance)
3. If the dev server runs fine, the adress https://SERVEUR.jura.ch/INSTANCE/pytree/ will display a demo page

```
docker run --name pytree --rm -ti -v /home/rwunderlich/jura_c2cgeoportal/pytree_config.yaml:/app/pytree.yaml:ro -v /var/sig:/var/sig:ro -p 5001:5001 jura_pytree
https://geo-test.jura.ch/rwunderlich/pytree/
```
