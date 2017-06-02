Your answers to the questions go here.
- What is an Agent - an agent is a small application that installs directly onto the host and is responsible for collecting data from the host, integrations and custom application metrics and then forwarding this data on to the DataDog application
- Agent Check Code 
Configuration File - matt_random.yaml
init_config:
 min_collection_interval: 20
instances:
    [{}]
Python Script - matt_random.py
	import random
	from checks import AgentCheck
	class MattCheck(AgentCheck):
	    def check(self, instance):
	        self.gauge('test.support.random', random.random())
- Difference Between Timeboard and Screenboard - The primary difference is that all graphs show the same timescope where screenboards are capable of showing a variety of timescales. Screenboards are primarily used for dashboarding system information where timeboards are very effective for troubleshooting issues by correlating disperate events over the same time period.

NOTE: 
- Exercise Answers.pdf includes screenshots and further details on the work done.
- Work - How I got here and errors.pdf shows all of the steps I took, wrong turns I made and includes some of my notes about unfamiliar technologies.