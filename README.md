<b>User Data for Dependencies installations for AMAZON Linux 2:-</b>

#!/bin/bash<br />
sudo yum -y update<br />
sudo yum -y install ruby<br />
sudo yum -y install wget<br />
cd /home/ec2-user<br />
wget https://aws-codedeploy-ap-south-1.s3.ap-south-1.amazonaws.com/latest/install<br />
sudo chmod +x ./install<br />
sudo ./install auto<br />
sudo yum install -y python-pip<br />
sudo pip install awscli<br />

![image](https://github.com/Siddhartha082/aws_cicd_pipeline_codedeploy_on_EC2_instances/assets/110781138/ad5d5b99-26d2-40dc-bf0e-6c38a4775766)

![image](https://github.com/Siddhartha082/aws_cicd_pipeline_codedeploy_on_EC2_instances/assets/110781138/995d0db7-6e1f-49db-a3fe-6e7d5b6f48fd)

# 1st Create two roles in IAM

![image](https://github.com/Siddhartha082/aws_cicd_pipeline_codedeploy_on_EC2_instances/assets/110781138/e63a44ec-aabe-4e0a-a2e4-96d74d685086)

![image](https://github.com/Siddhartha082/aws_cicd_pipeline_codedeploy_on_EC2_instances/assets/110781138/8e9af455-1a0f-4431-a254-cb3f4cba6358)

![image](https://github.com/Siddhartha082/aws_cicd_pipeline_codedeploy_on_EC2_instances/assets/110781138/1e67c3ca-41f6-4dba-aa95-4c94416f89eb)

#  Add Permissions

![image](https://github.com/Siddhartha082/aws_cicd_pipeline_codedeploy_on_EC2_instances/assets/110781138/9220843e-f0bc-4d93-add9-955e9e4ac9f6)

![image](https://github.com/Siddhartha082/aws_cicd_pipeline_codedeploy_on_EC2_instances/assets/110781138/0c1c5d7f-a942-467f-87e1-6162421599db)

![image](https://github.com/Siddhartha082/aws_cicd_pipeline_codedeploy_on_EC2_instances/assets/110781138/30720e8d-1bf6-4e4d-b40e-b9e6ca4557e0)

![image](https://github.com/Siddhartha082/aws_cicd_pipeline_codedeploy_on_EC2_instances/assets/110781138/3cb317ad-1b95-4948-942f-921fb3111f8f)

![image](https://github.com/Siddhartha082/aws_cicd_pipeline_codedeploy_on_EC2_instances/assets/110781138/ef637695-640a-405b-9094-4d72db5a8d42)

# Role Created 

![image](https://github.com/Siddhartha082/aws_cicd_pipeline_codedeploy_on_EC2_instances/assets/110781138/f4360e7e-4809-4390-af67-c0f9ff48a310)

![image](https://github.com/Siddhartha082/aws_cicd_pipeline_codedeploy_on_EC2_instances/assets/110781138/e0542ab4-87d3-4f81-8b2c-1b06ff032128)

# create another role

![image](https://github.com/Siddhartha082/aws_cicd_pipeline_codedeploy_on_EC2_instances/assets/110781138/130181f8-7792-4dd6-a552-83da70f607e0)

# Select

![image](https://github.com/Siddhartha082/aws_cicd_pipeline_codedeploy_on_EC2_instances/assets/110781138/024da66a-10fd-4769-b2ff-806c67c3d825)

![image](https://github.com/Siddhartha082/aws_cicd_pipeline_codedeploy_on_EC2_instances/assets/110781138/6190cd5a-bbd9-4ffb-9126-3f8bb491434c)

![image](https://github.com/Siddhartha082/aws_cicd_pipeline_codedeploy_on_EC2_instances/assets/110781138/55fda416-9a8b-4259-8d73-5956727b1e53)

![image](https://github.com/Siddhartha082/aws_cicd_pipeline_codedeploy_on_EC2_instances/assets/110781138/53f8a805-28b3-442c-af23-b852535556bc)

![image](https://github.com/Siddhartha082/aws_cicd_pipeline_codedeploy_on_EC2_instances/assets/110781138/06b5ffa5-c498-464e-90e7-c6e7b713e91c)

![image](https://github.com/Siddhartha082/aws_cicd_pipeline_codedeploy_on_EC2_instances/assets/110781138/531bd03c-6edc-47b7-bc48-0ce1bb6f2e62)

# Two Roles Created

![image](https://github.com/Siddhartha082/aws_cicd_pipeline_codedeploy_on_EC2_instances/assets/110781138/90c40f37-46ca-4785-a18a-61d6822ef41a)

# now Create EC2 Instances Region – Virginia

![image](https://github.com/Siddhartha082/aws_cicd_pipeline_codedeploy_on_EC2_instances/assets/110781138/37a54092-2fa7-465c-b964-2c8ce4ab2af5)

![image](https://github.com/Siddhartha082/aws_cicd_pipeline_codedeploy_on_EC2_instances/assets/110781138/2ec5541e-e3ae-422c-85b6-35330f2ae315)

![image](https://github.com/Siddhartha082/aws_cicd_pipeline_codedeploy_on_EC2_instances/assets/110781138/abfb608d-3909-440a-a83f-1cf978ef68ee)

![image](https://github.com/Siddhartha082/aws_cicd_pipeline_codedeploy_on_EC2_instances/assets/110781138/5fc63474-a42d-43e6-b979-45c25c6c1a67)

![image](https://github.com/Siddhartha082/aws_cicd_pipeline_codedeploy_on_EC2_instances/assets/110781138/8e33df43-84a0-47e3-a6c1-3b6d4a54362d)

![image](https://github.com/Siddhartha082/aws_cicd_pipeline_codedeploy_on_EC2_instances/assets/110781138/3d60f875-27ad-4e02-98a7-ad509c64d12b)

![image](https://github.com/Siddhartha082/aws_cicd_pipeline_codedeploy_on_EC2_instances/assets/110781138/a929fe36-1253-426b-8c25-d0d0fd2c63f5)

# update user data

![image](https://github.com/Siddhartha082/aws_cicd_pipeline_codedeploy_on_EC2_instances/assets/110781138/e41274d3-73b3-48e5-9682-82eda5ca7c92)

![image](https://github.com/Siddhartha082/aws_cicd_pipeline_codedeploy_on_EC2_instances/assets/110781138/43e3d3f6-ddd8-4ce4-bc6a-87d1d685a8b6)

# now Search for Codedeploy

![image](https://github.com/Siddhartha082/aws_cicd_pipeline_codedeploy_on_EC2_instances/assets/110781138/3ccf9831-1eff-4718-92c4-c61b218194bd)

![image](https://github.com/Siddhartha082/aws_cicd_pipeline_codedeploy_on_EC2_instances/assets/110781138/da69d970-3a7d-4151-a697-322f6aba2e18)

![image](https://github.com/Siddhartha082/aws_cicd_pipeline_codedeploy_on_EC2_instances/assets/110781138/4656d3cf-f899-44aa-a02f-f2a2b9100038)

# Go 2 codedeploy – click  applications – create applications

![image](https://github.com/Siddhartha082/aws_cicd_pipeline_codedeploy_on_EC2_instances/assets/110781138/d1fa0b53-d434-4981-b0de-82342a868a89)

![image](https://github.com/Siddhartha082/aws_cicd_pipeline_codedeploy_on_EC2_instances/assets/110781138/40ea8568-7cb9-4263-8d9d-a504a2d29935)

# Create Deployment group

![image](https://github.com/Siddhartha082/aws_cicd_pipeline_codedeploy_on_EC2_instances/assets/110781138/67325ee4-b2cb-4087-b942-97ff7d6d39ff)

![image](https://github.com/Siddhartha082/aws_cicd_pipeline_codedeploy_on_EC2_instances/assets/110781138/ca3d637f-6203-49ea-b7b8-a7d56d75a06f)

![image](https://github.com/Siddhartha082/aws_cicd_pipeline_codedeploy_on_EC2_instances/assets/110781138/d32ab1ef-a302-4fb9-aa5a-7ddc22e6a883)

![image](https://github.com/Siddhartha082/aws_cicd_pipeline_codedeploy_on_EC2_instances/assets/110781138/1eed9a25-a941-4e19-aab7-91f7ba2f6916)

![image](https://github.com/Siddhartha082/aws_cicd_pipeline_codedeploy_on_EC2_instances/assets/110781138/75ec9014-64f2-4023-a358-dd368587e5fd)

![image](https://github.com/Siddhartha082/aws_cicd_pipeline_codedeploy_on_EC2_instances/assets/110781138/bbfb30a4-d716-4607-8d6c-75225cc628b0)

![image](https://github.com/Siddhartha082/aws_cicd_pipeline_codedeploy_on_EC2_instances/assets/110781138/ba80f7b7-64db-4001-876c-67471d1764df)

![image](https://github.com/Siddhartha082/aws_cicd_pipeline_codedeploy_on_EC2_instances/assets/110781138/ba5daa06-c93b-442a-847e-2562a27b55d8)

# now Go to Codepipeline

![image](https://github.com/Siddhartha082/aws_cicd_pipeline_codedeploy_on_EC2_instances/assets/110781138/2526522c-68a7-46d7-a02c-b04129488809)

![image](https://github.com/Siddhartha082/aws_cicd_pipeline_codedeploy_on_EC2_instances/assets/110781138/7101272e-7ac4-4cd4-a96c-440109147b55)

![image](https://github.com/Siddhartha082/aws_cicd_pipeline_codedeploy_on_EC2_instances/assets/110781138/099d0d3e-c06b-4417-ade4-0ef2f5b314ff)

![image](https://github.com/Siddhartha082/aws_cicd_pipeline_codedeploy_on_EC2_instances/assets/110781138/54b3f557-2fa2-4e91-b7d7-e65238c34909)

![image](https://github.com/Siddhartha082/aws_cicd_pipeline_codedeploy_on_EC2_instances/assets/110781138/32334eb2-c5ed-4139-91b6-d1fb60113bf8)

![image](https://github.com/Siddhartha082/aws_cicd_pipeline_codedeploy_on_EC2_instances/assets/110781138/3d11e610-b2bb-4d64-8065-a4fc622ad7c1)

![image](https://github.com/Siddhartha082/aws_cicd_pipeline_codedeploy_on_EC2_instances/assets/110781138/3c14bb78-4f71-43bb-b03e-33cd9f8f097c)

![image](https://github.com/Siddhartha082/aws_cicd_pipeline_codedeploy_on_EC2_instances/assets/110781138/457920c6-56ca-429f-9741-68e1a99b0d17)

![image](https://github.com/Siddhartha082/aws_cicd_pipeline_codedeploy_on_EC2_instances/assets/110781138/9533bf8e-9dc3-46bb-99bd-f0a0067f5a88)

![image](https://github.com/Siddhartha082/aws_cicd_pipeline_codedeploy_on_EC2_instances/assets/110781138/3869a95a-cdcc-4699-9e3e-8331855ff285)

![image](https://github.com/Siddhartha082/aws_cicd_pipeline_codedeploy_on_EC2_instances/assets/110781138/981f9002-683c-4b21-8630-34c819066100)

![image](https://github.com/Siddhartha082/aws_cicd_pipeline_codedeploy_on_EC2_instances/assets/110781138/47178cca-8633-4fe0-8ab3-7a431da50a5e)

![image](https://github.com/Siddhartha082/aws_cicd_pipeline_codedeploy_on_EC2_instances/assets/110781138/65f62374-46aa-478b-b18d-59c2d7da98eb)

# Skip below 

![image](https://github.com/Siddhartha082/aws_cicd_pipeline_codedeploy_on_EC2_instances/assets/110781138/a386c07a-b69d-4521-8bf6-6bf2eba4e3c1)

![image](https://github.com/Siddhartha082/aws_cicd_pipeline_codedeploy_on_EC2_instances/assets/110781138/1c4115a2-2fb8-4920-b2d7-497434e7c3e2)

![image](https://github.com/Siddhartha082/aws_cicd_pipeline_codedeploy_on_EC2_instances/assets/110781138/bc58c9fb-aaaa-4577-b156-db5ac75378ab)

# Review

![image](https://github.com/Siddhartha082/aws_cicd_pipeline_codedeploy_on_EC2_instances/assets/110781138/b01a347b-c076-4199-9c34-723f0943461e)

![image](https://github.com/Siddhartha082/aws_cicd_pipeline_codedeploy_on_EC2_instances/assets/110781138/97c465b3-30c1-403f-8c4f-01904bde542a)

![image](https://github.com/Siddhartha082/aws_cicd_pipeline_codedeploy_on_EC2_instances/assets/110781138/190f4781-4c83-4fd9-aa17-15917072fce0)

![image](https://github.com/Siddhartha082/aws_cicd_pipeline_codedeploy_on_EC2_instances/assets/110781138/e67adc64-e774-4e11-b786-220f4311f64d)

# Pipeline created successfully

![image](https://github.com/Siddhartha082/aws_cicd_pipeline_codedeploy_on_EC2_instances/assets/110781138/b54f8e8d-c6b2-4d5a-8c92-b4acb3fed41f)

# Go 2 EC2 instance check for Security group 

![image](https://github.com/Siddhartha082/aws_cicd_pipeline_codedeploy_on_EC2_instances/assets/110781138/8b7e36d3-31e9-45e5-b5f7-7467cfa29774)

# Go to Security groups -- make inbound rule enable http @ port 80

![image](https://github.com/Siddhartha082/aws_cicd_pipeline_codedeploy_on_EC2_instances/assets/110781138/f84af460-e8e8-4973-8353-86080aa42687)

![image](https://github.com/Siddhartha082/aws_cicd_pipeline_codedeploy_on_EC2_instances/assets/110781138/4fa095ad-f045-4fe3-a101-4e288951bdd3)

![image](https://github.com/Siddhartha082/aws_cicd_pipeline_codedeploy_on_EC2_instances/assets/110781138/8e2078c5-54c1-4b34-8a64-29e5b2fb365d)

![image](https://github.com/Siddhartha082/aws_cicd_pipeline_codedeploy_on_EC2_instances/assets/110781138/616f3ada-e4a8-4bf9-8513-a1f7c039c529)

![image](https://github.com/Siddhartha082/aws_cicd_pipeline_codedeploy_on_EC2_instances/assets/110781138/a395f8d8-46af-4328-8bd7-9f9fec695232)

# HTTP – Output – code deployed

![image](https://github.com/Siddhartha082/aws_cicd_pipeline_codedeploy_on_EC2_instances/assets/110781138/61be11bd-d636-4f81-8efd-5991bef76cc7)


# Verify whether code has been deployed or not

# make some changes in index.html @ github repo & commit the changes made .. see the changes ( test commit)

![image](https://github.com/Siddhartha082/aws_cicd_pipeline_codedeploy_on_EC2_instances/assets/110781138/0f710fc6-9be9-4825-abfb-bbb0ef308755)

![image](https://github.com/Siddhartha082/aws_cicd_pipeline_codedeploy_on_EC2_instances/assets/110781138/5f534bc0-f542-410e-9046-fa83c24cd85f)

# Below highlighted .. test commit displayed

![image](https://github.com/Siddhartha082/aws_cicd_pipeline_codedeploy_on_EC2_instances/assets/110781138/013372b7-4e20-4e96-8f5b-724d7b6292f8)

![image](https://github.com/Siddhartha082/aws_cicd_pipeline_codedeploy_on_EC2_instances/assets/110781138/6d9af983-f6a0-4087-b065-e8ae68183eae)

# Output changed 

![image](https://github.com/Siddhartha082/aws_cicd_pipeline_codedeploy_on_EC2_instances/assets/110781138/495b2bab-4550-400b-bad6-6bfb4e8ca451)























































