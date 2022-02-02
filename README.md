# spanassessment

[![Test](https://github.com/davebehr1/spanassessment/actions/workflows/test.yml/badge.svg?branch=master)](https://github.com/davebehr1/spanassessment/actions/workflows/test.yml)


```
This simple cli is used to load match results via a file or stdin to generate a rank table.
Rules:
  * if a team has won a game they get 3 points
  * if they draw they get one point
  * if they lose they get no points
```

## Run tests:
  make test
  
## modes of execution:
  * ### docker:
    * make docker
    * docker run matchescli args...
 * ### executable:
    * go build -o matchescli
    * ./matchescli grt --f=matches.txt

## Cli commands:

*   ### generateranktable / grt:
     *  Flags:
        * --f
        * --help / help for command

     *   Example:
           *  Go run main.go grt --f=matches.txt’
           *  Go run main.go grt
              * you will get a prompt ```Enter Match Result:``` enter the match result in the format ```cheetahs 1, bulls 2```
              * to conclude entering in match results and see the final rank table type in ```done``` at the next prompt
