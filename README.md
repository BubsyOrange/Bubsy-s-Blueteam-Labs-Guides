# Malicious-PowerShell-Analysis-Guide
This is my guide for the Malicious PowerShell Analysis challenge from Blue Team Labs Online.



## Using CyberChef
We first must break the encoded script to understand it's syntax. To do that, we will use a tool known as [CyberChef](https://gchq.github.io/CyberChef). Paste the script into the input and set the output as From Base64 with Decode text UTF-16LE (1200).

## Examining The Syntax
We will then paste to unencoded script to Mousepad (or the text editor of your choice) and sort out the syntax to make sense of the gibberish.

### Question 1
What security protocol is being used for the communication with a malicious domain?

`TLS 1.2`

### Question 2
What directory does the obfuscated PowerShell create? (Starting from \HOME\) 

`\HOME\db_bh30\Yf5be5g\`
- HINT: The `{0}` represents a `\`.

### Question 3
What file is being downloaded (full name)?

`A69S.dll`

### Question 4
What is used to execute the downloaded file?

`rundll32`

### Question 5
What is the domain name of the URI ending in ‘/6F2gd/’

`wm.mcdevelop.net`

### Question 6
Based on the analysis of the obfuscated code, what is the name of the malware? 

`emotet`

- HINT: Go to [URLhaus](https://urlhaus.abuse.ch/) and search for the domain from question 5.
