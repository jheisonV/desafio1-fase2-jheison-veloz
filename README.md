# desafio1-fase2-jheison-veloz

Para este desafio levantamos dos instancias de EC2 en AWS, ambas con un servidor de MYSQL, para la creación vía CLI usamos los siguientes scripts:

* Maquina con AMI ami-026b57f3c383c2eec:

aws ec2 run-instances --image-id ami-026b57f3c383c2eec --count 1 --instance-type t3.medium --key-name bootcamp-keys --security-group-ids sg-07f9553270b5607f2 

* Maquina con AMI ami-08c40ec9ead489470

aws ec2 run-instances --image-id ami-08c40ec9ead489470 --instance-type t3.medium --key-name bootcamp-key1 --security-group-ids sg-02ea4ad9c1f33fcda  --count 1 --tag-specifications 'ResourceType=instance, Tags=[{Key=Name,Value=bootcamp-ec2-instance}]' --region us-east-1 --user-data file://userdata.txt --profile bootcamp
