helm-template-dev:
	@helm -n istio-dev template maroto-qa-01 . -f ../values-dev.yaml

helm-template-prod:
	@helm -n istio-dev template maroto . -f ../values-prod.yaml

helm-upgrade-dev:
	@helm -n istio-dev upgrade --install maroto-qa-01 . -f ../values-dev.yaml

helm-upgrade-dev-2: helm-upgrade-dev
	@helm -n istio-dev upgrade --install maroto-qa-02 . -f ../values-dev.yaml --set env.serviceName=maroto-qa-01

helm-upgrade-dev-3: helm-upgrade-dev-2
	@helm -n istio-dev upgrade --install maroto-qa-03 . -f ../values-dev.yaml --set env.serviceName=maroto-qa-02

helm-upgrade-dev-4: helm-upgrade-dev-3
	@helm -n istio-dev upgrade --install maroto-qa-04 . -f ../values-dev.yaml --set env.serviceName=maroto-qa-03

helm-upgrade-dev-5: helm-upgrade-dev-4
	@helm -n istio-dev upgrade --install maroto-qa-05 . -f ../values-dev.yaml --set env.serviceName=maroto-qa-04

helm-delete-all:
	@helm -n istio-dev delete maroto-qa-01 maroto-qa-02 maroto-qa-03 maroto-qa-04 maroto-qa-05
