# Reproducer for [MDEP-711](https://issues.apache.org/jira/browse/MDEP-711)

The POM declares version 3.1.2 for the Maven Dependency Plugin.
Running `mvn dependency:go-offline` fails:

        [ERROR] Failed to execute goal org.apache.maven.plugins:maven-dependency-plugin:3.1.2:go-offline (default-cli) on project mdep-711: org.eclipse.aether.resolution.DependencyResolutionException: Could not find artifact org.projectlombok:lombok:jar:edge-SNAPSHOT -> [Help 1]

Running version 2.8 of the Maven Dependency Plugin, with `mvn org.apache.maven.plugins:maven-dependency-plugin:2.8:go-offline`:

    [INFO] --- maven-dependency-plugin:2.8:go-offline (default-cli) @ mdep-711 ---
    [INFO] Resolved: lombok-edge-20200625.221645-1.jar
