
# Terminal Spinner

This Go project implements a terminal spinner to indicate progress or ongoing operations in command-line applications. It provides a simple and customizable spinner component that can be easily integrated into any Go application.

## Features

- Simple and easy-to-use API
- Customizable frame rate and output writer
- Predefined spinner frames for a smooth visual effect

## Installation

To use this spinner in your Go project, you can add it as a dependency using `go get`:

```sh
go get github.com/tz3/terminal-spinner/spinner
```

## Usage

Here is an example of how to use the spinner in your application:

```go
package main

import (
    "log"
    "time"

    "github.com/tz3/terminal-spinner/spinner"
)

func main() {
    s := spinner.New(spinner.Config{})

    log.Println("Starting the spinner")
    s.Start()

    time.Sleep(time.Second * 5)
    s.Stop()

    log.Println("Spinner stopped")
}
```

## Configuration

You can customize the spinner by providing a `Config` struct when creating a new spinner. The `Config` struct allows you to specify the output writer and the frame rate.

```go
s := spinner.New(spinner.Config{
    Writer:    os.Stdout,
    FrameRate: time.Millisecond * 100,
})
```

## Testing

The project includes unit tests to ensure the spinner works as expected. You can run the tests using the following command:

```sh
go test ./spinner
```

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
