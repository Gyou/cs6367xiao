# cs6367xiao
For Project Phase1, 
Go to the directory Phase 1, and out/artifacts/My_Agent_jar/ and use the MyAgent.jar. 
Then put the MyAgent.jar under the root of the project you want to test.
Configure the pom.xml file of the project as follows.
<argLine>-javaagent:MyAgent.jar</argLine> <properties> <property> <name>listener</name> <value>phase1.MyListener</value> </property> </properties>
Please note the listener is phase1.MyListener
Then run "mvn clean test" in the command tool.

For Project Phase2, 
Go to the directory Phase 2, and out/artifacts/MyTraceAgent/ and use the MyTraceAgent.jar. 
Then put the MyTraceAgent.jar under the root of the project you want to test.
Configure the pom.xml file of the project as follows.
<argLine>-javaagent:MyTraceAgent.jar</argLine> <properties> <property> <name>listener</name> <value>phase2.MyTraceListener</value> </property> </properties>
Please note the listener is phase2.MyTraceListener
Then run "mvn clean test" in the command tool.

After this, the variable tracing file will be stored under ./tracefiles/ in the root of the project. 
Now, to infer the invariants, put Infer_Invari.py under the root of the project, and run
Python Infer_Invari.py
Please use python3. 
Then, the infered potential invariants are shown in file Potential_Invariants.txt

