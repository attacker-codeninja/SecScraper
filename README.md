# SecScraper

Reports and articles scraper for bug bounty hunters.

The script will fetch the article links for you, based on your query. Enter anything you want to search, whether a vulnerability description, or a bug writeup on Medium, or a public report on Hackerone, this tool will scrape everything relevant for you, with the specified result count.

![SecScraper Demo](secscraper.gif)

## Usage

You need to have Python version 3.4+

```bash
sudo apt-get install python3
```
Downloading and setting up the tool:

```bash
git clone https://github.com/bittentech/SecScraper.git
cd SecScraper
pip3 install -r requirements.txt
```

Syntax: 
```bash
scraper.py -t TYPE -q QUERY -c [COUNT] -o [OUTPUT_FILE]
```
Type: The platform where the content needs to be searched

Current options for type:
1. Medium
2. Hackerone

Query: The string to search, for e.g., "sql injection", "file upload", "graphql", etc.

Count: The result count to fetch, for e.g., number of articles/reports (default: 10)

Output: Save the scan results in the specified file

Examples: 
```bash
python3 scraper.py -t medium -q "sql injection"

python3 scraper.py -t hackerone -q "authentication bypass" -c 50

python3 scraper.py -t hackerone -q "authentication bypass" -c 50 -o /tmp/output.txt
```
Please report functionality issues and bugs if found.

## License
[GNU GPLv3](https://www.gnu.org/licenses/gpl-3.0.en.html)