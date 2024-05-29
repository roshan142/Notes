# Recon Notes For Bug Bountry/Penetration Testing

## Tools:

* wfuzz 
* gobuster
* dig
* shodan
* Google Dorking

### Port Scaning:
* Nmap
* Naabu

`nmap -A -F -T1 <website link> -v`

`naabu domain.com -o output.txt`

### DNS Recon:
* nslookup
* whois

`nslookup <website link>`

`whois <website link>`

### Dir Enumeration:
* ffuf
* dirb

`ffuf -w <wordlist> -u https://domain.com/FUZZ`

`dirb <website link>`

### Sub Domain Enumeration:
* ffuf
* assetfinder
* findomain
* amass
* waybackurls
* httprobe
* crt.sh
* sublist3r
  
`amass Enum -passive -d <domain name>`

`cat <domain list> | ./waybackurls > <output file>`   -by tomnomnom GitHub

`cat <domain list from waybackurls> | httprobe > <output file>` - this is used to find the valid links from a junk of links

`crt.sh` - [website](https://crt.sh/)

`sublist3r -d <domain>`

`ffuf -w <wordlist> -u https://FUZZ.domain.com/ -p 2`

`assetfinder --subs-only domain.com`

`findomain -t domain.com -u output_file.txt`

### WordPress Scan:
* wpscan
  
`wpscan --url https://domain.com -e ap --plugins-detection aggressive -o <output file>`

### OSINT Recon tool:
* theHarvester
`theHarvester -d <domain name> -b <source>`

### Google Dorking
[Google Dork](https://github.com/roshan142/Notes/blob/main/google_dorking.md)
