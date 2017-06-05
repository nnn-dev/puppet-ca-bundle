## Puppet Labs is now shipping a CA cert bundle!

The ["canonical", up-to-date Cert Authority bundle](https://github.com/bagder/ca-bundle/) currently provides 155 Root certificates. We
are grabbing the Mozilla '[certdata.txt](https://mxr.mozilla.org/mozilla/source/security/nss/lib/ckfw/builtins/certdata.txt?raw=1)', using the 'certdata2pem.py' script from Red Hat to split that into PEM files, and removing anything that is untrusted
(i.e. with anything in the distrust= field), or doesn't explicitly list serverAuth in the openssl-trust field. The result lines up with the linked
[curl bundle above](https://github.com/bagder/ca-bundle/).
