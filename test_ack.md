# Names

Blablabla. This section tests https://avro.apache.org/docs/current/spec.html#names

## SimpleRecord 

```json
{
  "type" : "record",
  "name" : "Simple",
  "fields" : [ {
    "name" : "id",
    "type" : "int"
  } ]
}
```

| Schema |  |
|---|---|
| canonical | `abcdef` |
| fingerprint | `7195948357588979594` |


## InvalidSimpleRecord

Please note that this is an important and subtle test.  Look for the 9 (nine) in the record name.  This is not allowed, mkay?

```json
{
  "type" : "record",
  "name" : "9.Simple",
  "fields" : [ {
    "name" : "id",
    "type" : "int"
  } ]
}
```

| Schema |  |
|---|---|
| error | true |
| error.msg | That's a terrible name for a schema. |
| java.error.msg | You should feel badly about that schema name. |
