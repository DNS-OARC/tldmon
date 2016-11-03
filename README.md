# Nagios Plugin Scripts for TLDmon

TLDmon uses two Nagios plugin scripts to implement the service checks.
Both scripts originally come from The Measurement Factory. We've made
some modifications for TLDmon and publish the modified versions here.

## check_zone_auth

We've made some significant changes to this script for TLDmon. The original
version checks a number of properties in a certain order and complains about
the first problem that it finds. Our version only checks one property per
invocation, via command line option. Also, we have added some additional
checks.

## check_zone_rrsig_expiration

The modifications to this script are minor. For TLDmon we've changed
the "critical" result codes to "warning" and also changed the output
format a little.
