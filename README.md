# ec-sdk
The Enterprise-Connect SDK. [Visit the wiki to get familiar with EC](https://github.com/Enterprise-connect/ec-sdk/wiki). We track down every single reported issue and are passionate in solving problems. Please leave your feedbacks/concerns [here](https://github.com/Enterprise-connect/ec-sdk/issues). You're encouraged to make a pull request.

[![GitHub version](https://badge.fury.io/gh/Enterprise-connect%2Fec-sdk.svg)](https://badge.fury.io/gh/Enterprise-connect%2Fec-sdk)
[![Hex.pm](https://img.shields.io/hexpm/l/plug.svg)](https://github.com/Enterprise-connect/ec-sdk)
[![Travis branch](https://img.shields.io/travis/rust-lang/rust/master.svg)](https://travis-ci.org/)

## System Requirement
### Hardware
- 7Mb system storage memory
- 32Mb DRAM.

### Instruction/OS
- ARM32/64.(Raspian, Symbian)
-  Windows 32/64
- Android.
- iOS.
- Linux 32/64.
- Mac OS X (Darwin)

### Load Balancing (Optional)
- [Cloud Foundry Diego Cell](https://docs.cloudfoundry.org/concepts/diego/diego-architecture.html)

## Download
```bash
git clone --recursive https://github.com/Enterprise-connect/ec-sdk.git
```

## Extract the Agent
```bash
tar -xvzf ./path/to/ec-sdk/dist/ecagent_linux_sys.tar.gz
```

## Verify the checksum
### Linux
```bash
$ sha256 ./path/to/file/ecagent_linux_sys
b3bf9cd9686e
$ awk 's=index($0,"b3bf9cd9686e") { print "line=" NR, "start position=" s}' checksum.txt 
line=2 start position=1
```
### Mac OS
```
$ shasum -a 256 ./path/to/file/ecagent_linux_sys
b3bf9cd9686e
$ awk 's=index($0,"b3bf9cd9686e") { print "line=" NR, "start position=" s}' checksum.txt 
line=2 start position=1
```
### Windows
```bash
c: \> CertUtil -hashfile C:\path\to\file\ecagent_windows.exe sha256
b3bf9cd9686e (find the checksum in the checksum.txt)
```
## Homebrew installation (experiment)
- This will install the agent binary as well as setup your local Dev environment
```bash
 $ brew install ecagent
 ```

## Contribution
The SDK examples were created in the open-source form with the vision of a greater private cloud and at the same time, making computer network more secure. The EC team recognises every indiviual's contribution and is actively looking for partners who share the same vision.

## Credits
- [Springboot sample app](https://github.com/Enterprise-connect/ec-springboot-II/tree/master) by [avnsri4986](https://github.com/avnsri4986)
- [Python3+ sample app/lib](https://github.com/Enterprise-connect/ec-python3) by [avnsri4986](https://github.com/avnsri4986)

## Release History
### [v1.3.2b-candidate](https://github.com/Enterprise-connect/ec-sdk/releases) current
 - Fix unlock super_conn memory issue. #41 
 - Fix interface conversion error whilst RLock. #38 
 - Fix exception handling error causing deadlock when number of sessions exceeds 50+ #38 #41 
 - Fix mutex rewrite issue. #38 #41 
 - Enable/Disable VLAN forwarding based on VLAN flag.
 - Feature added- VLAN header checking for resource forwarding.
 - Feature added- VLAN ip/port mapping.
 - Add flag -shc to secure the health API.
 
[more](https://github.com/Enterprise-connect/ec-sdk/releases)
