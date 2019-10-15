Members of the network can syncronize their metadata in 2 ways:
a) Using a blockchain - by sending updateds to the blockchain and retrieving the metadata from the blockchain.
b) Using a Master Node - Nodes can decide on a master node that receives the metadata updates and provides members with a copy of the metadata.

Configuring a master node:

1)	Identify an IP and port for the master node
2)	Set the master node in a listening mode on the selected IP and Port
3)	To update the master node:
Use the command ‘blockchain push’ to send the JSON file to the master node

4)	To retrieve data from the master node:

-	Use the command ‘blockchain pull to log’ to pull the log file from the master node. The output file will be paced in the blockchain directory. The file name is prefixed by the name of the log file and the suffix is “.new”.
-	Use the command ‘blockchain pull to dbms” to pull the metadata from the master node. The output file is a set of SQL insert statements that will update a local database with the metadata. The file name is prefixed by the name of the log file and the suffix is “.new.sql”.
5)	To update the local copy of the log file, copy the new log file to the be the blockchain log file.
6)	To update the local database with the updates to the metadata, place the insert statement file in the watch directory.
7)	To copy these files from the master node, use the command “file get [source location] [destination location] whereas:
-	“source location” is the path name and file name on the master node.
-	“destination location” is the path name and file name on the requesting node. 