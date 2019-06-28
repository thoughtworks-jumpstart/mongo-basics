# Lab 1 Importing data

## Import data

```
mongoimport --db pokedex --collection pokemons --type json --file ./pokemons.json --jsonArray --drop
```

## Start the mongo client

```
  mongo
```

## Use the Pokedex db

```
show dbs
use pokedex
```

## verify the data is inserted correctly

```
show collections
db.pokemons.count()
```
