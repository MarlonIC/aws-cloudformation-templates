> Comandos

Creación de stack desde un archivo local
```
aws cloudformation create-stack \
    --stack-name myNameStack \
    --template-body file://myTemplate.yml \
    --parameters \
        ParameterKey=myKey,ParameterValue=myValue \
        ParameterKey=myKey2,ParameterValue=myValue2\\,myValue3 \
    --region us-east-1
```

Creación de stack desde un archivo en AWS S3
```
aws cloudformation create-stack \
    --stack-name myNameStack \
    --template-url https://s3.amazonaws.com/myBucket/myTemplate.yml \
    --parameters \
        ParameterKey=myKey,ParameterValue=myValue \
        ParameterKey=myKey2,ParameterValue=myValue2\\,myValue3 \
    --region us-east-1
```

Actualizar stack
```
aws cloudformation update-stack \
    --stack-name myNameStack \
    --template-body file://myTemplate.yml \
    --region us-east-1
```

Eliminar stack
```
aws cloudformation delete-stack \
    --stack-name myNameStack \
    --region us-east-1
```