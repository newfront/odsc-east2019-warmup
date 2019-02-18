### Real-ish Time Predictive Analytics Warm Up
This is the essential prerequist to the May 1st workshop in Boston at the ODSC East Conference.

#### WarmUp DataSet
[Wine Reviews](https://www.kaggle.com/zynicide/wine-reviews) - Thanks to zynicide and kaggle.com for the data set.

#### Technologies
1. [Spark 2.4.0](https://www.apache.org/dyn/closer.lua/spark/spark-2.4.0/spark-2.4.0-bin-hadoop2.7.tgz)
2. [Zeppelin 0.8.1](http://www.apache.org/dyn/closer.cgi/zeppelin/zeppelin-0.8.1/zeppelin-0.8.1-bin-netinst.tgz)
3. [Hadoop 2.7.7](https://www.apache.org/dyn/closer.cgi/hadoop/common/hadoop-2.7.7/hadoop-2.7.7.tar.gz)

#### Spark Local Setup
Just download, untar, and move spark. I usually just drop into usr/local

`tar -xvzf /path/to/spark-2.4.0-bin-hadoop2.7.tgz && mv /path/to/spark-2.4.0-bin-hadoop2.7/ /usr/local/spark-2.4.0/`

#### Zeppelin Setup
[Spark Setup](https://zeppelin.apache.org/docs/0.8.1/interpreter/spark.html)

#### Hadoop Single Node Setup
[Setup Documentation](http://hadoop.apache.org/docs/r2.7.7/hadoop-project-dist/hadoop-common/SingleCluster.html)

#### Local Aliases in .bashrc or .bash_profile
~~~
export SPARK_HOME=/usr/local/spark-2.4.0
export ZEPPELIN_HOME=/usr/local/zeppelin-0.8.1
export HADOOP_HOME=/usr/local/hadoop-2.7.7

# Zeppelin
alias zeppelin_start="$ZEPPELIN_HOME/bin/zeppelin-daemon.sh --config $ZEPPELIN_HOME/conf/ start"
alias zeppelin_stop="$ZEPPELIN_HOME/bin/zeppelin-daemon.sh --config $ZEPPELIN_HOME/conf/ stop"

# Hadoop
alias start_hdfs="$HADOOP_HOME/sbin/start-dfs.sh"
alias stop_hdfs="$HADOOP_HOME/sbin/stop-dfs.sh"
alias hdfs="$HADOOP_HOME/bin/hdfs"
~~~

```
source ~/.bash_profile
```

