---
id: how-to-use
title: How to use
sidebar_label: How to use
---

# Install
There are two ways to get the restcli.

[1] - The fastest way to get rest cli is download jar from [relese tabs](https://github.com/restcli/restcli/releases)

[2] - Install via homebrew
```shell script
brew tap restcli/restcli
brew install restcli
```
# Usage

```
Usage: rest-cli [-hV] [-e=<environmentName>] [-l=<logLevel>]
                [-r=<testReportNames>] FILES...
IntelliJ RestCli
      FILES...    Path to one ore more http script files.
  -e, --env=<environmentName>
                  Name of the environment in config file
                  (http-client.env.json/http-client.private.env.json).
  -h, --help      Show this help message and exit.
  -l, --log-level=<logLevel>
                  Config log level while the executor running.
                  Valid values: NONE, BASIC, HEADERS, BODY
  -r, --report-names=<testReportNames>
                  Custom test report names inside folder "test-reports".
                  The report names must separate by ':' character;
                  If the split string of the report name is empty, then the
                    test request file name will
                  be used for report name
                  Such as:
                  java -jar restcli.jar -r custom_report1::custom_report3 test1.
                    http test2.http test3.http
                  Then the test report for test1.http will be custom_report1.xml
                  test2.http -> test2.xml (Because the report name for test2.
                    http is empty)
                  test3.http -> custom_report3.xml
  -V, --version   Print version information and exit.
```
