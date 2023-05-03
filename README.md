# Elasticsearch Duplicate Remover

This script removes duplicates from an Elasticsearch index based on a set of fields. 

## Prerequisites

- Python 3.x
- Elasticsearch 7.x (or compatible version)

## Usage

```
python3 deduplicate_elasticsearch.py [-h] -i INDEX_NAME -k KEYS [-e ES_HOST] [-l {DEBUG,INFO,WARNING,ERROR,CRITICAL}]
```

### Arguments

- `-h, --help`: show help message and exit
- `-i INDEX_NAME, --index-name INDEX_NAME`: name of the Elasticsearch index
- `-k KEYS, --keys KEYS`: comma-separated list of fields to use for determining duplicates
- `-e ES_HOST, --es-host ES_HOST`: Elasticsearch host (default: http://localhost:9200)
- `-l {DEBUG,INFO,WARNING,ERROR,CRITICAL}, --log-level {DEBUG,INFO,WARNING,ERROR,CRITICAL}`: logging level (default: INFO)

## Example

```
python3 deduplicate_elasticsearch.py -i my_index -k first_name,last_name -e http://localhost:9200 -l DEBUG
```

This will remove duplicates from the `my_index` Elasticsearch index based on the `first_name` and `last_name` fields. The Elasticsearch server is assumed to be running on `http://localhost:9200`. The script will output debug messages to the console.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.