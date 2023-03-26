PROJECT_NAME:=cloudformation-cfn-init

deploy-default:
	aws cloudformation deploy \
		--capabilities CAPABILITY_NAMED_IAM \
		--template-file 1_userdata.yaml \
		--stack-name $(PROJECT_NAME)-default

destroy-default:
	aws cloudformation delete-stack \
		--stack-name $(PROJECT_NAME)-default

deploy-signal:
	aws cloudformation deploy \
		--capabilities CAPABILITY_NAMED_IAM \
		--template-file "2_userdata with signal.yaml" \
		--stack-name $(PROJECT_NAME)-signal

destroy-signal:
	aws cloudformation delete-stack \
		--stack-name $(PROJECT_NAME)-signal
