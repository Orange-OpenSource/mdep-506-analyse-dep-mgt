# mdep-506-analyse-dep-mgt
 Test case for maven-dependency-plugin:analyze-dep-mgt [MDEP-506](https://issues.apache.org/jira/browse/MDEP-506) 

 [![Build Status](https://travis-ci.org/Orange-OpenSource/mdep-506-analyse-dep-mgt.svg?branch=master)](https://travis-ci.org/Orange-OpenSource/mdep-506-analyse-dep-mgt)
 
 
 
 This build is expected to fail with 
 
```
[ERROR] Failed to execute goal org.apache.maven.plugins:maven-dependency-plugin:2.10:analyze-dep-mgt (default) on project child: Execution default of goal org.apache.maven.plugins:maven-dependency-plugin:2.10:analyze-dep-mgt failed. NullPointerException -> [Help 1]

org.apache.maven.lifecycle.LifecycleExecutionException: Failed to execute goal org.apache.maven.plugins:maven-dependency-plugin:2.10:analyze-dep-mgt (default) on project child: Execution default of goal org.apache.maven.plugins:maven-dependency-plugin:2.10:analyze-dep-mgt failed.

	at org.apache.maven.lifecycle.internal.MojoExecutor.execute(MojoExecutor.java:224)
	at org.apache.maven.lifecycle.internal.MojoExecutor.execute(MojoExecutor.java:153)
	at org.apache.maven.lifecycle.internal.MojoExecutor.execute(MojoExecutor.java:145)
	at org.apache.maven.lifecycle.internal.LifecycleModuleBuilder.buildProject(LifecycleModuleBuilder.java:116)
	at org.apache.maven.lifecycle.internal.LifecycleModuleBuilder.buildProject(LifecycleModuleBuilder.java:80)
	at org.apache.maven.lifecycle.internal.builder.singlethreaded.SingleThreadedBuilder.build(SingleThreadedBuilder.java:51)
	at org.apache.maven.lifecycle.internal.LifecycleStarter.execute(LifecycleStarter.java:128)
	at org.apache.maven.DefaultMaven.doExecute(DefaultMaven.java:307)
	at org.apache.maven.DefaultMaven.doExecute(DefaultMaven.java:193)
	at org.apache.maven.DefaultMaven.execute(DefaultMaven.java:106)
	at org.apache.maven.cli.MavenCli.execute(MavenCli.java:862)
	at org.apache.maven.cli.MavenCli.doMain(MavenCli.java:286)
	at org.apache.maven.cli.MavenCli.main(MavenCli.java:197)
	at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
	at sun.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:62)
	at sun.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
	at java.lang.reflect.Method.invoke(Method.java:497)
	at org.codehaus.plexus.classworlds.launcher.Launcher.launchEnhanced(Launcher.java:289)
	at org.codehaus.plexus.classworlds.launcher.Launcher.launch(Launcher.java:229)
	at org.codehaus.plexus.classworlds.launcher.Launcher.mainWithExitCode(Launcher.java:415)
	at org.codehaus.plexus.classworlds.launcher.Launcher.main(Launcher.java:356)
Caused by: org.apache.maven.plugin.PluginExecutionException: Execution default of goal org.apache.maven.plugins:maven-dependency-plugin:2.10:analyze-dep-mgt failed.
	at org.apache.maven.plugin.DefaultBuildPluginManager.executeMojo(DefaultBuildPluginManager.java:145)
	at org.apache.maven.lifecycle.internal.MojoExecutor.execute(MojoExecutor.java:208)
	... 20 more
Caused by: java.lang.NullPointerException
	at org.apache.maven.plugin.dependency.analyze.AnalyzeDepMgt.getMismatch(AnalyzeDepMgt.java:272)
	at org.apache.maven.plugin.dependency.analyze.AnalyzeDepMgt.checkDependencyManagement(AnalyzeDepMgt.java:175)
	at org.apache.maven.plugin.dependency.analyze.AnalyzeDepMgt.execute(AnalyzeDepMgt.java:102)
	at org.apache.maven.plugin.DefaultBuildPluginManager.executeMojo(DefaultBuildPluginManager.java:134)
	... 21 more
[ERROR] 
[ERROR] 
[ERROR] For more information about the errors and possible solutions, please read the following articles:
[ERROR] [Help 1] http://cwiki.apache.org/confluence/display/MAVEN/PluginExecutionException
[ERROR] 
[ERROR] After correcting the problems, you can resume the build with the command
[ERROR]   mvn <goals> -rf :child
```


