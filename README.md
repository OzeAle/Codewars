# Century From Year

Introduction
The first century spans from the year 1 up to and including the year 100, the second century - from the year 101 up to and including the year 200, etc.

Task
Given a year, return the century it is in.

Examples
1705 --> 18
1900 --> 19
1601 --> 17
2000 --> 20
Note: this kata uses strict construction as shown in the description and the examples, you can read more about it here

SOLUTION:

function century(year) {
  var century = 0;
  
  for(var i = 0; i < year; i++) {
    if(i % 100 == 0) {
      century++;
    }
  }
  return century;
}

# Extract the domain name from a URL

Write a function that when given a URL as a string, parses out just the domain name and returns it as a string. For example:

* url = "http://github.com/carbonfive/raygun" -> domain name = "github"
* url = "http://www.zombie-bites.com"         -> domain name = "zombie-bites"
* url = "https://www.cnet.com"                -> domain name = cnet"


SOLUTION:

function domainName(url){
  url = url.replace("https://", '');
  url = url.replace("http://", '');
  url = url.replace("www.", '');
  return url.split('.')[0];
};
