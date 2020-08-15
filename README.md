# RSocket CLI

## You should probably use rsc instead

For general rsocket command line you probably want https://github.com/making/rsc

## Description

Simple RSocket CLI focused on sending basic traffic to servers built using RSocket e.g. help debug a mobile <=> server integration issue. 

Supports ws and wss URIs

# Build Status

<a href='https://travis-ci.org/rsocket/rsocket-cli/builds'><img src='https://travis-ci.org/rsocket/rsocket-cli.svg?branch=master'></a> 


## Build and Run

To build the RSocket CLI:
```
./gradlew --console plain installDist
```

To run:
```
./build/install/rsocket-cli/bin/rsocket-cli --help
```

The build and run:
```
$ ./rsocket-cli --help
```


## Install via Homebrew

Use tab completion for help with specifying the operation type.

```
$ brew install yschimke/tap/rsocket-cli
```

## Examples


A generic interaction:
```
$ rsocket-cli --request --debug wss://rsocket-demo.herokuapp.com/rsocket      
```

A spring routed request to query tweets:

```
$ rsocket-cli --route=searchTweets -i Sunday wss://rsocket-demo.herokuapp.com/rsocket
```

