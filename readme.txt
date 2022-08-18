1)
To run the code one simplt needs to extract the tar.gz file.
Then, open the server folder and open the terminal from there and run one of the servers (explained in 1.1)
Then open the client folder and open terminals from there (as much as desired) - 
the first client will be activated as explained in 1.1 and the rest by the last operation line in 1.1.

1.1)

SERVER REACTOR:
mvn clean
maven compile
mvn exec:java -Dexec.mainClass="bgu.spl.net.mainReactor" -Dexec.args="127.0.0.1 7777 5"

SERVER TPC:
mvn clean
maven compile
mvn exec:java -Dexec.mainClass="bgu.spl.net.main" -Dexec.args="127.0.0.1 7777"

CLIENT :
make clean
make
bin/BGSclient 127.0.0.1 7777

1.2)
As described in the exmaple section of Assignment 3 - runnig commands are as follows :
REGISTER OMER hardPassword123 20.01.1997
LOGIN OMER hardPassword123 1
LOGOUT
FOLLOW 0 OMER
FOLLOW 1 OMER
POST My message is the current !! is @YONI registered to our app ?
PM OMER hey omer , whats up ??
LOGSTAT
STAT OMER YONI
BLOCK OMER

2)
We defined the forbbiden words inside the ConnectionsImpl contructor - to be put manually