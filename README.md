# desafio1-fase2-jheison-veloz

Para este desafio levantamos dos instancias de EC2 en AWS, ambas con un servidor de MYSQL, para la creación vía CLI usamos los siguientes scripts:

* Maquina con AMI ami-026b57f3c383c2eec:

aws ec2 run-instances --image-id ami-026b57f3c383c2eec --count 1 --instance-type t3.medium --key-name bootcamp-keys --security-group-ids sg-07f9553270b5607f2 --user-data file://userdata.txt

* Maquina con AMI ami-08c40ec9ead489470

aws ec2 run-instances --image-id ami-08c40ec9ead489470 --instance-type t3.medium --key-name bootcamp-key1 --security-group-ids sg-02ea4ad9c1f33fcda  --count 1 --tag-specifications 'ResourceType=instance, Tags=[{Key=Name,Value=bootcamp-ec2-instance}]' --region us-east-1 --user-data file://userdata.txt


<img width="1528" alt="image" src="https://user-images.githubusercontent.com/63665794/219989459-bf1ebc5b-a350-442d-bf2b-b0741750939c.png">

<img width="746" alt="image" src="https://user-images.githubusercontent.com/63665794/219989481-ed1e526b-118b-46ca-9964-95063ca64051.png">

<img width="631" alt="image" src="https://user-images.githubusercontent.com/63665794/219989497-5421dee6-5de9-4c1a-91f1-e9951f2687dc.png">

<img width="973" alt="image" src="https://user-images.githubusercontent.com/63665794/219989510-f2f45310-beec-47ec-89c5-aa262eb7634a.png">

<img width="683" alt="image" src="https://user-images.githubusercontent.com/63665794/219989530-a852b912-eb29-4fd2-b94a-5a64da3c9211.png">
