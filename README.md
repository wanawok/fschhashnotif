# fschhashnotif
fschhashnotif is a daemon wirtten in c++ for monitoring any attempt to modfiy a file specified in the watch list.

## Overview
* Generate hash of each file specified in the watch list at startup 
* Store the generated hash to a secure db
* Calculate new hash each time file is changed and compare with the hash stored in the db
* Once a mismatch between the new calculated hash and hash stored in db is noticed, update the state of that file to "tampered".  
* Generate a report of the state of each file in the watch list.
