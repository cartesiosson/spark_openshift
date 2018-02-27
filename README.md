"# spark_openshift

1.- Instalar el template de Oshinko

oc create -f http://radanalytics.io/resources.yaml

2.- Build desde GitHub bajamos la aplicación y los recursos del cluster de Spark.

oc new-app --template oshinko-java-spark-build-dc -p APPLICATION_NAME=sparkpi -p GIT_URI=https://github.com/cartesiosson/spark_openshift -p APP_FILE=SparkPiBoot-0.0.1-SNAPSHOT.jar

3.- Creamos la route para la aplicacion

oc expose svc/sparki

4.- Accedemos

http://XXXXXX/sparki


" 
