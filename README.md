# links-to-json-resources

(I originally labelled this `awesome-json`, but then I realized [awesome-json](https://github.com/burningtree/awesome-json) already exists and is ... awesome, so make sure to look at that too if you haven't previously!)

This is a list of some of the tips and tricks processing JSONs efficiently at scale, with a bias towards production data science/data engineering.

Inspired by [awesome-pipeline](https://github.com/pditommaso/awesome-pipeline).

## Inherent limitations
* [JSON does not have distinct types for integers and floating-point values](https://json-schema.org/understanding-json-schema/reference/numeric.html)
* [How to escape special characters in building a JSON string](https://stackoverflow.com/questions/19176024/how-to-escape-special-characters-in-building-a-json-string)
* Quora on ["how do you send binary data in JSON"](https://www.quora.com/How-do-you-send-binary-data-in-JSON) (TL;DR: no "blessed" option, base64 is ubiquitous, a naive string representation is not allowed)

## Command line
* [jq](https://jqlang.github.io/jq/) - an exremely versatile, albeit complex, query language for processing JSON documents on the command line. Has an excellent syntax highlighting mode. Caveat emptor: simple one liners are simple, but it makes for very tough engineering.
* [jc](https://github.com/kellyjonbrazil/jc) - a utility that wraps many common Linux commands to have a well structured JSON format.

## Java
* [Jackson](https://github.com/FasterXML/jackson), "the Java JSON library" - heavily opinionated to convert between JSON structures to strongly-typed Java objects, as old as the world and extremely elaborate.

## Online tools
* Quora Answer on "[Is it safe to use online XML/JSON formatter for confidential coding](https://www.quora.com/Is-it-safe-to-use-online-XML-JSON-formatter-for-confidential-coding)" (TL;DR: no)

## Schemas
* [json-schema](https://json-schema.org/) - a way of specifying JSON schemas (the JSON schema is encoded in a JSON data structure). Has validators in most programming languages known to me.

## Security
* [JSON interoperability vulnerabilities](https://bishopfox.com/blog/json-interoperability-vulnerabilities)

## Postgres
* [Query JSON data with Postgresql](https://medium.com/@AaronSchlegel/query-json-data-with-postgresql-73512884212c) - a discussion on how to use Postgres as a JSON-based documents store, including some examples of queries and indexes.
* [JSON Functions and Operators](https://www.postgresql.org/docs/current/functions-json.html) - from the official Postgres docs.

## Protobuf
* [Value](https://protobuf.dev/reference/protobuf/google.protobuf/#value) - representing arbitrary JSON data in well-structured protobufs.
* A canonic way to convert between JSON and Protobuf: [Java](https://www.baeldung.com/java-convert-json-protobuf), [Python](https://googleapis.dev/python/protobuf/latest/google/protobuf/json_format.html)

## Python
* [ijson](https://pypi.org/project/ijson/), Iterative ("online") JSON parser
* [ujson](https://pypi.org/project/ujson/) a very high performance JSON encoder/decoder for Python
* [dataclasses-json](https://pypi.org/project/dataclasses-json/) - convert simple Python dataclass structurs to/from JSON.
* [Pydantic](https://docs.pydantic.dev/latest/) - a strongly opinionated library for strong typing of Python data structures, which also supports JSONs, jsonschema and more.
* [pprint module in the standard library](https://docs.python.org/3/library/pprint.html) - an easy way out for printing tree objects (such as memory representations of JSON files)
