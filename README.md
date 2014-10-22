peerify
=======

peerify is a perl script to lookup the Peering DB and auto-generate BGP peer configuration for a JunOS based device. This script is useful if you are building a peering fabric.

We assume you have a local copy of the peeringDB running on a MySQL server (The Dump is available here: www.peeringdb.com/dbexport/peeringdb.sql ).

Script still in development (ie: it's still rough). 

Output is JunOS (For now). Might add other platforms at another time. 

Usage:


./peerify <MY ASN> <PEER ASN>

