# Proof of Concept - Maven multi-module forest

POC to check the workflows for Maven multi-module forest is single Git repository.

# Build Workflows

Procedure to execute after initial checkout or branch switch:

mvn -f aggregator/pom.xml -Dinit clean install


Usual build:

mvn -f aggregator/pom.xml clean install


# Selecting Build Scope

The modules in the root aggregator are skipped if a file exists in build-control directory.

| Module | Control file |
| -- | -- |
| api | build-control/skip-api |
| bar | build-control/skip-bar |
| foo | build-control/skip-foo |
| parent | build-control/skip-parent |
| tools | build-control/skip-tools |
