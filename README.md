# CVE-2023-36250

CSV Injection vulnerability in GNOME time tracker version 3.0.2, allows local attackers to execute arbitrary code via crafted .tsv file when creating a new record.

## Vulnerability Type

CSV Injection

## Discoverer

Bruno Teixeira

## Reference

http://gnome.com

## Affected Product Code Base

GNOME time tracker v3.0.2

## PoC

Creating a new record using a fomrula (=3+3) in the cmdline field, creates a way to inject formulas when exporting to .tsv.
With this, when someone extract this .tsv file, the sheet software will evaluate as a valid formula and it will execute it.
Note that this is just a sum operation but it's possible to load software that resides on the victim machine, or even create a malicious hyperlink.

![image](https://github.com/BrunoTeixeira1996/CVE-2023-36250/assets/12052283/a59a63a4-223b-4cf6-ac40-fdea77d76bd1)

![image](https://github.com/BrunoTeixeira1996/CVE-2023-36250/assets/12052283/87420f16-432a-4596-9211-bb900fbe9b31)

