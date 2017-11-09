
History of joker-broker
=======================

#### 0.0.14
* rename interfaces.redis to rediz (for python2 import error)
* python -m joker.broker.default


#### 0.0.13
* remove psycopg2 from requirements
* rewrite userdefault.py (parts moved to joker-cast)


#### 0.0.12
* bug fix: nullredis from_url returns None


#### 0.0.11
* AbstractModel.find(.., many=, limit=, offset=)
* add psycopg2 to requirements.txt


#### 0.0.10
* AbstractModel.delete: multiple primary keys
* AbstractModel.delete_cache


#### 0.0.9
* AbstractModel.find: update_cache() and mark_permanet()
* gen_random_string() now uses os.urandom, and is unexposed


#### 0.0.8
* AbstractModel._update_cache -> AbstractModel.update_cache
* remove AbstractModel.load_with
* new AbstractModel.find, returning objects in stead of pk


#### 0.0.7
* move MultiFernetWrapper away to joker.masquerade


#### 0.0.6
* add SQLInterface.execute
* remove redundant Table cache from SQLInterface, which is done by SQLAlchemy already
* remove client_encoding for sqlite
* start to write README
* setup_userdir, get_resource_broker. No magic at broker.__init__
* less redundancy creating a new @property interface


#### 0.0.5
* add methods `find` and `load_with` to `AbstractModel`


#### 0.0.4
* user directory (`~/.joker`) and default config file creation
* bugfix: StaticInterface.get lacks *args so that `si.get('DEBUG', False)` fails
* joker.broker.interfaces.sql -> ...sequel