# Frank Kane's Taming Big Data with Apache Spark and Python
This is the code repository for [Frank Kane's Taming Big Data with Apache Spark and Python](https://www.packtpub.com/big-data-and-business-intelligence/frank-kanes-taming-big-data-apache-spark-and-python?utm_source=github&utm_medium=repository&utm_campaign=9781787287945), published by [Packt](https://www.packtpub.com/?utm_source=github). It contains all the supporting project files necessary to work through the book from start to finish.
## About the Book
Frank Kane’s Taming Big Data with Apache Spark and Python is your companion to learning Apache Spark in a hands-on manner. Frank will start you off by teaching you how to set up Spark on a single system or on a cluster, and you’ll soon move on to analyzing large data sets using Spark RDD, and developing and running effective Spark jobs quickly using Python.

Apache Spark has emerged as the next big thing in the Big Data domain – quickly rising from an ascending technology to an established superstar in just a matter of years. Spark allows you to quickly extract actionable insights from large amounts of data, on a real-time basis, making it an essential tool in many modern businesses.

Frank has packed this book with over 15 interactive, fun-filled examples relevant to the real world, and he will empower you to understand the Spark ecosystem and implement production-grade real-time Spark projects with ease.
##Instructions and Navigation
All of the code is organized into folders. Each folder starts with a number followed by the application name. For example, Chapter02.



The code will look like the following:
```
from pyspark import SparkConf, SparkContext 

import collections 

conf = SparkConf().setMaster("local").setAppName("RatingsHistogram") 
sc = SparkContext(conf = conf)

lines = sc.textFile("file:///SparkCourse/ml-100k/u.data") 
ratings = lines.map(lambda x: x.split()[2]) 
result = ratings.countByValue() 

sortedResults = collections.OrderedDict(sorted(result.items())) 
for key, value in sortedResults.items(): 
    print("%s %i" % (key, value)) 
```

For this book you’ll need a Python development environment (Python 3.5 or newer), a Canopy installer, Java Development Kit, and of course Spark itself (Spark 2.0 and beyond).


We'll show you how to install this software in first chapter of the book.


This book is based on the Windows operating system, so installations are provided according to it. If you have Mac or Linux, you can follow this URL http://media.sundog-soft.com/spark-python-install.pdf, which contains written instructions on getting everything set up on Mac OS and on Linux.

## Related Products
* [Taming Big Data with Spark Streaming and Scala – Hands On! [Video]](https://www.packtpub.com/big-data-and-business-intelligence/taming-big-data-spark-streaming-and-scala-–-hands-video?utm_source=github&utm_medium=repository&utm_campaign=9781787123915)

* [Taming Big Data with Apache Spark and Python - Hands On! [Video]](https://www.packtpub.com/big-data-and-business-intelligence/taming-big-data-apache-spark-and-python-hands-video?utm_source=github&utm_medium=repository&utm_campaign=9781787129931)

* [Taming Big Data with MapReduce and Hadoop - Hands On! [Video]](https://www.packtpub.com/big-data-and-business-intelligence/taming-big-data-mapreduce-and-hadoop-hands-video?utm_source=github&utm_medium=repository&utm_campaign=9781787125568)

