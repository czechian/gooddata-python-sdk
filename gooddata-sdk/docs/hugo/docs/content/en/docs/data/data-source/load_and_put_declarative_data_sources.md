---
title: "load_and_put_declarative_data_sources"
linkTitle: "load_and_put_declarative_data..."
weight: 110
superheading: "catalog_data_source."
---

<!-- TODO -->

``load_and_put_declarative_data_sources(layout_root_path: Path = Path.cwd(), credentials_path: Optional[Path] = None, test_data_sources: bool = False)``

This method combines [load_declarative_data_sources](../load_and_put_declarative_data_sources) and [put_declarative_data_sources](../put_declarative_data_sources) methods to load and set layouts stored using [store_declarative_data_sources](../store_declarative_data_sources).

## Example

The load and put can be done two ways.

Either by one call:

```Python
# Load and put declarative data sources
sdk.catalog_data_source.load_and_put_declarative_data_sources(
    layout_root_path=Path("abc"),
    credentials_path=Path("credentials")
)
```
Or by two separate calls:

```Python
#Load the data source
data_sources = sdk.catalog_data_source.get_declarative_data_sources()

#Put the data source
sdk.catalog_data_source.put_declarative_data_sources(
    declarative_data_sources=data_sources
    layout_root_path=Path("abc"),
    credentials_path=Path("credentials")
)
```

The result is identical.
