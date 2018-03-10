# struct_attrib

get meta info in a data.

## Usage

> example_1:

```
get_metadata_from_data_dict({"var": ["text1", "text2", "text3", "text4", 1, 2, 3, "text5", "text6", "text7", "text8", "text9"]})

{
    "var":{
        "meaning_type":"textual",
        "storage_types":[
            "number",
            "string"
        ],
        "unique_values":[
            1,
            2,
            "text2",
            "text4",
            3,
            "text9",
            "text1",
            "text3",
            "text7",
            "text6",
            "TRUNCATED"
        ],
        "number_of_unique_values":12,
        "nullable":false
    }
}
```

> example_2:

```
get_metadata_from_data_dict({"var": ["1.2", -0.2, "3.4", 2.4, "2.1", 5.6, 1.2, 2.3, 10.2, 11.3, 24.1]})

{
    "var":{
        "meaning_type":"numeric",
        "buckets":[
            -0.2,
            0.53,
            1.2,
            1.88,
            2.28,
            2.4,
            3.66,
            6.7,
            10.6,
            17.44,
            24.1
        ],
        "min":-0.2,
        "median":2.4,
        "max":24.1,
        "nullable":false
    }
}
```
