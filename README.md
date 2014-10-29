peerify
=======

peerify is a perl script to lookup the Peering DB and auto-generate BGP peer configuration for a JunOS based device. We generate netconf and auto-push the config diff via ssh based on key auth.  

We assume you have a local copy of the peeringDB running on a MySQL server (The Dump is available here: www.peeringdb.com/dbexport/peeringdb.sql ).

Script still in development (ie: it's still rough). 

There are a number of configuration options at the top of the script which you can use to tune your setup:
```perl
## Database Setup
$database="";
$host="";
$port=;
$user="";
$pass="";

## Local variables setup
## TODO: Use GetOps for these. 
$my_asn = shift;
$peer_asn = shift;

## NETCONF details 
$access="ssh";
$login="";
$keyfile="";

# JSON ixp peering-address to hostname mapping
$ixp_to_router_mapping="router.json";
```


Usage:

```
./peerify <MY ASN> <PEER ASN>
```


Notes on config 
===============

I assume that you already have a group configured with import/export policies and various other tunables, and you just want to add new peers to this group. 

Code is still being cleaned up, but should be quite usable right now.
