# Rokko bundle library

The official library of [Rokko](https://github.com/hugelton) bundles. Rokko reads it from its bundle menu (Bundle Library…); nothing here is meant to be opened by hand.

- `index.json` lists the bundles; `index.json.sig` is its ECDSA P-256 signature. Rokko checks the signature with the key built into it, then each download's size and SHA-256 against the index, before unpacking anything.
- `bundles/` holds one zip per bundle version. Versions are never replaced: a new version is a new file.

To publish a change, the whole folder is rebuilt with the library tool and the signing key, which is never committed here.
