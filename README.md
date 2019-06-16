# kickdomain
Kickdomain is a subdomain takeover checker tool

# Usage

pip install kickdomain

add your facebook access token in kickdomain/config.py (get your access token here - https://developers.facebook.com/tools/explorer/)

Enumerate Subdomains only 

kickdomain.py -u target.com 

Enable Takeover check

kickdomain.py -u target.com -t 1

# Use kickdomain as a module

```
import kickdomain

subdomains=kickdomain.getSubdomains('target.com')

results=kickdomain.takeover_check(subdomains)

for i in results:
    if i[1]:

        print(i[0]+' vulnerable to Takeover')

    else:

        print(i[0]+' not vulnerable to Takeover')
        ```
    