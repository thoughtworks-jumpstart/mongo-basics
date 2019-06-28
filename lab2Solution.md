## Find Pokemon

1. with with english name Mew

```bash
db.pokemon.find({"name.english": "Mew"}).count() // 1
```

2.  with Attack greater than

```
db.pokemon.find({"base.Attack": {\$gt: 120}}).count() // 67
```

3. with Attack greater than 120 and Speed less than equal to 50 // 13

```
db.pokemon.find({"base.Attack": {$gt: 120}, "base.Speed": {$lte: 50}}).count() // 13
```

4. With Attack greater than 120 or Speed less than equal to 50 // 341

```
db.pokemon.find({$or: [{"base.Attack": {$gt: 120}}, {"base.Speed": {\$lte: 50}}]}).count()
```

5. ONLY Psychic type

```
db.pokemon.find({type: ["Psychic"]}).count()
```

6.  ONLY Flying and Psychic type

```
db.pokemon.find({type: {\$all: ["Flying", "Psychic"]}}).count()
```

7. contains Psychic

```
db.pokemon.find({type: {\$in: ["Psychic"]}}).count() // 82
```

8. contains Psychic or Flying type // 174

```
db.pokemon.find({type: {\$in: ["Psychic", "Flying"]}}).count() // 174
```
