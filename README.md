# Yggdrasil

This projects aim's to replace [hosts-sources](https://github.com/external-sources/hosts-sources) as it is an outdated
and unpractical way to collect, store and search for records.

## Goals

1. Import external sources, such as hosts, json, plain text files and MariaDB
2. Load the data into some Database; this could be json, CSV or MariaDB.
3. Sort by first domain, then URI, at last by category.
4. Keep track of the sources for domain and URI records
5. Make a search command that can sort and list results
   1. Sort output by source, then records
   2. Sort output sorted (clean format), no sources
   3. Output from none DNS sources like EasyList, uBlock and Adguard.
   4. Output records from My Privacy DNS project [Matrix](https://github.com/mypdns/matrix)
   5. Output MyPDNS RPZ records, extract directly from MariaDB
6. Manage Matrix records. (Add,Delete.Alter) to:
   1. PowerDNS Auth server's API <https://docs.powerdns.com/authoritative/http-api/zone.html>
   2. Alter the source files within the Matrix [source/](https://github.com/mypdns/matrix/tree/master/source)
      directory.
7. Incorporate PyFunceble for availability test before committing
8. Future, working with a webcrawler that can categorize sites and scripts to search for primarily trackers and adult
   sites
9. Add a GUI to manage all of this, rather than console as we also have to work with several categories per record.
   1. Suggested to use gtk-rs, or maybe relm, which wraps gtk-rs (https://matrix.to/#/!ifW4td0it0scmZpEM6:computer.surgery/$PA9YBwGw53VA6HNePqQ4hrOIbVpWktIlrnytCOQRLZo?via=computer.surgery&via=matrix.org&via=mozilla.org)
