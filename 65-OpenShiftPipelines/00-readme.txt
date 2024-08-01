https://github.com/PacktPublishing/Building-CI-CD-systems-using-Tekton/blob/main/chapter-8/guess-result.yaml

firefox https://console-openshift-console.apps.ocp4.example.com &
Download tkn CLI
cd ~/Downloads; ls -rtl
tar xvzf ~/Downloads/*.tar.gz
mkdir -p ~/.local/bin
cp tkn ~/.local/bin


al
oc new-project aa
oc new-project bb

vim -c 'set paste' guess-result.yaml
vim -c 'set paste' critical-hit.yaml



$ oc apply -f ./guess-result.yaml
	task.tekton.dev/random-number-generator created
	pipeline.tekton.dev/guess-result created

$ tkn pipeline start guess-result --showlog
	PipelineRun started: guess-result-run-f4c2j
	Waiting for logs to be available...

	[generate : generate-number] Random number picked, result is 3
	[win : log] [20/05/2021 12:04:14] - You win



$ oc apply -f ./critical-hit.yaml
	

$ tkn pipeline start results --showlog
	
