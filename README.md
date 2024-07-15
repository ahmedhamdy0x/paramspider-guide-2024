## How to Install and Use ParamSpider

**Created by [Ahmed Hamdy](https://github.com/ahmedhamdy0x/) from [GenTiL Security](https://www.youtube.com/@gentil.security)**

### Installation of ParamSpider
To install ParamSpider, you can follow these steps:

1. **Install Python 3:** Make sure you have Python 3 installed on your machine.

2. **Download the tool:**

   Open the terminal and execute the following commands:
   ```bash
   git clone https://github.com/devanshbatham/ParamSpider.git
   cd ParamSpider
   pip install .
   ```

### Using the Tool
After installation, you can use ParamSpider to gather parameters from a specific website. The following example demonstrates how to use the tool:

```bash
sudo paramspider -d example.com
```

### Main Options of the Tool
- `-d`: Specify the domain name of the target website.
- `-l`: Specify the crawling depth level.
- `-o`: Specify the output file name to save the results.
- `-e`: Specify the extensions you want to crawl, such as `.php`, `.html`, `.js`.

### Practical Examples
A simple example of using ParamSpider on a website (example.com) with a crawling depth level of 1 and saving the results to a file:

```bash
python3 paramspider.py -d example.com -l 1 -o results.txt
```

### Common Issues with ParamSpider and Their Solutions

#### Issue 1: Error with urllib3 and chardet Library Versions
**Description:**
When running the tool, you may encounter the following message:
```
/usr/lib/python3/dist-packages/requests/init.py:87: RequestsDependencyWarning: urllib3 (2.1.0) or chardet (5.2.0) doesn't match a supported version!
warnings.warn("urllib3 ({}) or chardet ({}) doesn't match a supported")
```

**Solution:**
This issue can be resolved by updating the required libraries using pip:
```bash
pip install --upgrade urllib3 chardet
```

#### Issue 2: Error Creating the Output File
**Description:**
When running the tool to gather parameters from a specific site, you may see the following message:
```
FileNotFoundError: [Errno 2] No such file or directory: 'index.html'
```

**Solution:**
This issue can be resolved by manually creating the required directory before running the tool:
```bash
mkdir -p results
```

#### Issue 3: Error Gathering Target Information
**Description:**
When running the tool, you may encounter the following message:
```
Cannot get target information
```

**Solution:**
Ensure the target domain format is correct and the target site is accessible. You can check connectivity using commands like `ping` or `curl`.

#### Issue 4: URL Files Not Found
**Description:**
This issue occurs when the tool cannot find any files containing valid URLs.

**Solution:**
Ensure you are using the correct domain and the site contains valid links. You can use other tools like `waybackurls` to gather additional links.
