# spark3.1.3-scala2.12.11

```bash
mvn clean compile
mvn clean package
```

## 1. 自定义jar

提交任务

```bash
SPARK_HOME=/opt/spark
${SPARK_HOME}/bin/spark-submit \
--master yarn \
--deploy-mode cluster \
--driver-memory 512m \
--executor-memory 512m \
--num-executors 1 \
--class net.xzh.test.WordCountOnYarn \
${SPARK_HOME}/examples/jars/original-spark3-test-1.0-SNAPSHOT.jar \
hdfs://node01:8020/test/input/words.txt \
hdfs://node01:8020/test/output2022
```
