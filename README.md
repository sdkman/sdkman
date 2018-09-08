# SDKMAN! Golang CLI

This repo is home to the next generation of SDKMAN Command Line Interface written in [Go](https://golang.org/). It marks a complete rewrite of the original CLI written in [bash](https://www.gnu.org/software/bash/).

The benefits of rewriting it in Go can be summarised as follows:
* no more dependency on the shifting sands of bash/ZSH as foundation
* allows natively compiled binaries for all popular architecture
* easier testing support through [Godog](https://github.com/DATA-DOG/godog), a version of [Cucumber](https://cucumber.io/) written in Go.
* statically typed compiled language, allowing us to catch bugs earlier during development
* allows us to rethink some core behaviours of the current implementation of SDKMAN
* allows for more collaboration and contribution from the community

### Development

#### Prerequisites

Ensure that you have [installed Go](https://golang.org/doc/install) on your system.

Optionally, you can install Godog for running the Cucumber specifications directly:

    $ go get github.com/DATA-DOG/godog/cmd/godog

#### Running the tests

To run all the tests using Go's builtin test support (unit and cukes):

    $ cd path/to/the/repo/sdk
    $ go test --godog.format=pretty

If you installed Godog earlier, you can run the cukes directly in isolation with the following command:

    $ godog

### Run

To kick the tyres before building:

    $ go run sdk.go version

### Build

To build and run the binary executable:

    $ go build
    $ ./sdk