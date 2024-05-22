# Recon Notes For Bug Bountry/Penetration Testing

## Tools:

* wfuzz 
* gobuster
* dig
* shodan
* nmap
* ffuf
* dirb
* nslookup
* whois
* amass
* waybackurls
* httprobe
* sublist3r
* theHarvester
* wpscan
* Google Dorking

### Nmap Scan:
`nmap -A -F -T1 <website link> -v`
### Dir Enumeration:
`ffuf -w <wordlist> -u https://domain.com/FUZZ`

`dirb <website link>`
### DNS Recon:
`nslookup <website link>`

`whois <website link>`

### Sub Domain Enumeration:

`amass Enum -passive -d <domain name>`

`cat <domain list> | ./waybackurls > <output file>`   -by tomnomnom GitHub

`cat <domain list from waybackurls> | httprobe > <output file>` - this is used to find the valid links from a junk of links

`crt.sh` - [website](https://crt.sh/)

`sublist3r -d <domain>`

`ffuf -w <wordlist> -u https://FUZZ.domain.com/ -p 2`

### WordPress Scan:

`wpscan --url https://domain.com -e ap --plugins-detection aggressive -o <output file>`

### OSINT Recon tool:

`theHarvester -d <domain name> -b <source>`

### Google Dorking
[Google Dork](https://github.com/roshan142/Notes/blob/main/google_dorking.md)
