# AWS_Boto3

This lambda will create a full flow
1) create policy
2) create role
3) attache the policy for the role
4) create the lambda and connect all the parts

if some of the parts are exists it will get the ARN and use it
i create the cloudwatch targets and Schedule

the lambda function "def __create_lambda(self)" can get any zip file you want ( aws format ) and be upload
my E.g. delete users and you can see in the class
```json
        self.lambda_policy = {
             "Version": "2012-10-17",
                "Statement": [{
                        "Sid": "VisualEditor1",
                        "Effect": "Allow",
                        "Action": [
                            "iam:DeleteUser",
                            "iam:DeleteAccessKey",
                            "iam:DetachUserPolicy",
                            "iam:AttachRolePolicy",
                            "iam:PutRolePolicy",
                            "iam:List*",
                            "iam:Get*",
                            "iam:AttachUserPolicy",
                            "iam:AttachGroupPolicy",
                            "iam:PutUserPolicy"
                        ],
                        "Resource": [
                            "arn:aws:iam::*:policy/*",
                            "arn:aws:iam::*:user/*",
                            "arn:aws:iam::*:role/*",
                            "arn:aws:iam::*:group/*"
```
 you will need to change it to what evere you want to give lambda permission

 Have Fun
 Noam Greenberg
 Noam.greenberg@gmail.com-NOSPAM
