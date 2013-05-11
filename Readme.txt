A simplified version of the Gnutella Protocol Version 0.6, which we shall refer to as Simpella. Simpella is a  unix command line version of Gnutella Protocol to share, search and download files over the network. Simpella is entirely distributive in nature.

Four phases are covered in this project:
- Connecting to the network.
- Searching for files
- Downloading files
- Traffic Monitoring.
Brief overview:
Connecting to the network: Whenever any node joins the system it will send the "PING" message to the node to which it connects. Receiving this ping message the receiver node will forward this ping message to its adjacency and so on. When last node receives this message it will revert with PONG message that represent it gets the information of the incoming node.
Searching for files: Same rule follow while searching for file, the node sends the search query to one node in the network and that node will forward this search message to its adjacency plus search for this file on its own system. At last combine all the result and return back to the query client.
Downloading files: After receiving the file list client will also get the ip address and port number of the other client who has this file so it will connect directly(outside of simpella network) to download the file.
Traffic Monitoring: Hop count is taken as 7 which will decrease whenever any node forward a message to its adjacency to avoid the network flooding.
