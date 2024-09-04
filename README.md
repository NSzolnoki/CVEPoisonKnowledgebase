# CVEPoisonKnowledgebase
The collection of poisoned code snippets that officially identified with a CVE identifier

## Content of this repository
* Vulnerable code snippets
* Metadata for the vulnerable code snippet
### Vulnerable code snippet
We have them in spearate folders per source and per language, for example at `CWE-mitre\C` you can find the vulnerable codes found in C langauges at source `CWE-mitre` like this:
```
-pwd = getpwnam(getlogin());if (isTrustedGroup(pwd->pw_gid)) {allow();} else {deny();}
```
### Metadata
We have a metadata file for each vulnerable code snippets, for the code snippet above this is the metadata:
```
{
    "original_source": {
        "database(url)": "https://cwe.mitre.org/",
        "software_system(CPE)": [
            "cpe:2.3:a:sendmail:sendmail:8.10:*:*:*:*:*:*:*",
            "cpe:2.3:a:beasts:vsftpd:1.2.0:*:*:*:*:*:*:*"
        ],
        "fix_commit": "",
        "version_end_excluding": {
            "sendmail:sendmail": "unknown",
            "beasts:vsftpd": "unknown"
        },
        "path": {
            "file_path": ""
        }
    },
    "programming_language": "C",
    "licences": {
        "database": "MIT",
        "affected_repository": "Unknown"
    },
    "related_vulnerability_entry": {
        "CVE": [
            "CVE-2001-1349",
            "CVE-2004-2259"
        ],
        "CWE": [
            "CWE-663"
        ]
    }
}
```
* `database(url)` is the source of the vulnerable code snippet
* `software_system(CPE)` is the affected software and its version
* `fix_commit` if the fix is known, we list here
* `programming_language` is the language of the code snippet
* `related_vulnerability_entry` list of related `CVE` and `CWE` identifiers


## How the data has been collected
### CVEFixes
TODO
-----------------------
### CWE-mitre
TODO
-----------------------
### project-KB
TODO
-----------------------

DRAFT:
The collection has been created using three sources to get the code snippets and the [NVD API](https://nvd.nist.gov/developers/vulnerabilities "NVD API") to get the detailed data for the vulnerabilities.
