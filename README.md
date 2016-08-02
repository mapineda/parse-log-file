# Parse-Log-File


## Description
Parse stdin as W3C extended log file format and print out json lines.

## How it Works:
Url decode each field value
The field cs-uri-query is turned into it's own nested json object
Include the preceding log file directives in every entry.
Include a raw field with the original log line.

Combine with a tool like jq to make it very easy to query your logs.


## Getting Started:
Example usage:
```
npm install
cat sample-input.txt | node parse-extended-log-file.js | jq '.'
```
