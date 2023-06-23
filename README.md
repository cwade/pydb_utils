# db_utils
Utilities for querying an oracle database. Planning to eventually expand to other database types.

The three methods in this package, run_query, run_command, and load_data, all require a yaml config file. For convenience, we assume this file is located in /Users/username/configs/config-default.yml.

### Installation

```
pip install git+ssh://git@github.com/cwade/db_utils.git
```

### Usage

```
import db_utils as db

# Assuming your config file is located at /Users/myname/configs/config-default.yml

# Pull all the data from a table into a data frame
df = db.run_query('select * from my_table')

# Delete all the data in that same table
db.run_command('delete from my_table')

# Put all the data back into the 
db.load_data(df, 'my_table')
```

