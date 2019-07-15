## requirements  
Spark with pyspark

## spark-submit with pyspark simple template
A simple usage example of pyspark with spark-submit, including:  
- passing arguments
- creating spark context and sql context
- loading your project source code (src directory )
- loading pip modules (with simple requirements file) 


## preparing libraries (source and pip modules)
from terminal, run:  
```pip install -r ./requirements.txt -t ./pip_modules && jar -cvf pip_modules.jar -C ./pip_modules .   ```

```jar -cvf src.jar -C ./src .   ```

## running spark-submit
from terminal, run:  
```spark-submit main.py --some_arg=some_value --pip_modules=pip_modules.jar --src=src.jar  ```


## running pyspark interactive shell with pip modules and source code
- run: pyspark
- from within pyspark interactive shell, run the following:   
```sc.addPyFile("src.jar")```   
```sc.addPyFile("pip_modules.jar")```   
