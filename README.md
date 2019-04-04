# brigade_kafka_gateway
A gateway for brigade that pulls data from a Kafka instance

To install this, you must have your own Kafka instance to point to including a host ip and port number. 
You must also have a fully functional install of Brigade running and know the Brigade Project's name to specify in the values.yaml file. 

To install simply clone this repo, update the values.yaml file with the appropriate kakfa_host ip, kakfa_topic, kafka_port, brigade_project_name, and change the kafka offset if desired. 

Once you have updated the values.yaml file, you can install by running this command:

helm install --name <desired deployment name> ./chart/
  
From here it will pull the image from Docker Hub and start the kafka gateway in the default kubernetes namespace.
