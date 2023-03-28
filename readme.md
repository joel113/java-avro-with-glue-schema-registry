# Avro with Glue Schema Registry and Avro

## Code from the Glue Schema Registry Serializers and Deserializers

```
String schema = schemaObject.getSchemaDefinition();
byte[] data = DESERIALIZER_DATA_PARSER.getPlainData(buffer);

log.debug("Length of actual message: {}", data.length);

DatumReader<Object> datumReader = datumReaderCache.get(schema);

BinaryDecoder binaryDecoder = getBinaryDecoder(data, 0, data.length);
Object result = datumReader.read(null, binaryDecoder);

log.debug("Finished de-serializing Avro message");
```

https://github.com/awslabs/aws-glue-schema-registry/blob/master/serializer-deserializer/src/main/java/com/amazonaws/services/schemaregistry/deserializers/avro/AvroDeserializer.java

## Glue Schema Registry References

https://github.com/awslabs/aws-glue-schema-registry

https://github.com/awslabs/aws-glue-schema-registry/blob/master/serializer-deserializer/src/main/java/com/amazonaws/services/schemaregistry/serializers/avro/AWSKafkaAvroSerializer.java

https://github.com/awslabs/aws-glue-schema-registry/blob/master/serializer-deserializer/src/main/java/com/amazonaws/services/schemaregistry/deserializers/avro/AWSKafkaAvroDeserializer.java

https://github.com/awslabs/aws-glue-schema-registry/blob/master/serializer-deserializer/src/main/java/com/amazonaws/services/schemaregistry/deserializers/avro/AvroDeserializer.java

https://github.com/awslabs/aws-glue-schema-registry/blob/master/examples/src/main/java/com/amazonaws/services/schemaregistry/examples/kds/PutRecordGetRecordExample.java

https://docs.python.org/3/library/zlib.html
