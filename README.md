# Proof of Concept - Maven multi-module forest

POC to check the workflows for Maven multi-module forest is single Git repository.

# Build Workflows

Procedure to execute after initial checkout or branch switch:

mvn -f aggregator/pom.xml -P init clean install


Usual build:

mvn -f aggregator/pom.xml clean install
