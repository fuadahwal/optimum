## Installation
To install pydfs-lineup-optimizer, simply:
```
$ pip install pydfs-lineup-optimizer
```

## Support
Now it's support following dfs sites:

League | Yahoo | Fanduel | DraftKings | FantasyDraft
----- | ----- | ----- | ----- | -----
NFL | + | + | + | +
NBA | + | + | + | +
NHL | + | + | + | +
MLB | + | + | + | -


## Example
Here is a example for evaluating optimal lineup for Yahoo fantasy NBA. It's loads players list from "yahoo-NBA.csv" and select 10 best lineup with 4 Oklahoma City Thunder players.
```python
from pydfs_lineup_optimizer import Site, Sport, get_optimizer


optimizer = get_optimizer(Site.YAHOO, Sport.BASKETBALL)
optimizer.load_players_from_CSV("yahoo-NBA.csv")
lineup_generator = optimizer.optimize(10)
for lineup in lineup_generator:
    print(lineup)
```
