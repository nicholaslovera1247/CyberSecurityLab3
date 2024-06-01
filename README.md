For this lab we were given a website's code that was vulnerable to an XSS attack. After looking over the code in CatCoin_Stock.html, it was clear that the vulnerability was on line 11, when we called for a json file from 
https://jreddy1.w3.uvm.edu/getStock.js. The reason why this made the website vulnerable was because there was no authentication check on the importation of the json file, making it easy for an attacker to import malicous
file instead of the json file we were expecting. By going to www.srihash.org we were able to create a hash that gives us a wall of authentication to ensure that the json file we are looking for is the only one that loads. 
If and when the corrupt file comes through instead, the authentication of the SRI hash will block the file and give a console message saying it was blocked. By doing this we get rid of our vulnerability, and as such
no longer get the corrupt message on our website. 
