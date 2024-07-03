**[简体中文](https://github.com/Guikong001/slonmonitor/blob/main/README.md)**

## Usage

### Script Usage

Download the script slonmonitor from this repository, grant execution permissions, and use ./slonmonitor to run it. You can also place the file in /usr/bin with root permissions to make it available for all users.

Non-root users can save it in their script directory and add it to their environment variable.

### Bark Setup

Download the Bark app from the iOS App Store, obtain the key from the Bark app, and pass it to the script using the -m option.

If you are using a self-hosted Bark server, use the -s option to pass the server address to the script. Note that if the server is https://abc.example.com, you only need to pass abc.example.com, without adding https. HTTP servers are not supported.

# Command Directory

<br/>

Usage: slonmonitor [options]...

Options:

  -p PID list    Add PID numbers, multiple PIDs can be added, separated by semicolons. If adding multiple PIDs, enclose all PIDs in single quotes.

  -t Title       Change the push notification title.

  -c Interval    Monitoring interval (in seconds).

  -w Process interval   Monitoring interval for currently running processes (in seconds).

  -m Key         Set the Bark push notification service key.

  -s Host        Set your custom Bark server.

  -h, --help     Display this help message and exit.

  -v, --version  Display version information and exit.

<br/>

## Purpose

It can be used to monitor computational programs that require long runtimes during bioinformatics analysis. For example, I use it to monitor long-term, multi-threaded variant detection with GATK 4 during SNP monitoring. It provides a rough estimate of the task completion time.

<br/>

## Future Optimization Plans:

1. Detailed process status retrieval.
2. Key storage functionality.
