<img align="right" height="32" src="https://coinstorm.net/ioc_logo_fund.png">

# Internet of Coins command line wallet


## NOTICE: We have migrated. Find our latest code here: https://github.com/hybrix-io


## Overview

This repository contains the Internet of Coins <i>cli4ioc</i> command line wallet.

## Usage

1. Make sure you are running a GNU/Linux system. Clone the hybridd repository.
```
git clone https://github.com/internetofcoins/cli4ioc
```
2. Clone the nodejs-runtime repository.
```
git clone https://github.com/internetofcoins/nodejs-runtime/
```
3. In the cli4ioc repository root, make a symbolic link to the correct node version for your system architecture (node32, node64 or nodeARM).
```
cd cli4ioc
ln -s ../nodejs-runtime/x86_64 node
```

4. Run the <i>cli4ioc</i> wallet.
```
~/cli4ioc$ ./cli4ioc
```

The wallet should ask you for an account ID and password, and then log in showing asset balances for the account.

In default cli4ioc connects to a public hybridd node and asks for user input on startup. You can, however, also change the wallet behaviour by using the following environment variables.

 CLI4IOC_HOST
 CLI4IOC_USER
 CLI4IOC_PASS


### Command examples:

```
CLI4IOC_HOST="http://127.0.0.1:8080/api" ./cli4ioc
```
```
CLI4IOC_USER="LHH7UZ3EFVW66WB3" CLI4IOC_PASS="IZYQYC6GUCJ47GFW" ./cli4ioc
```
```
export CLI4IOC_HOST="https://wallet.coinstorm.net/api"
export CLI4IOC_USER="LHH7UZ3EFVW66WB3"
export CLI4IOC_PASS="IZYQYC6GUCJ47GFW"
./cli4ioc
```

## More information

The command line wallet for Internet of Coins needs a <i>hybridd</i> node to connect to. These can be safely run on the same system if the user desires a maximum form of decentralization.

The interface is made using the ncurses-like library for NodeJS called 'blessed'.

## Troubleshooting

 <i>What is this supposed to do?</i>
 This wallet is supposed to enable you to use a large variety of cryptocurrencies and tokens from the command line. At the moment it is mostly interesting for tech enthousiasts to experiment with.
 
 <i>Can I use my own version of NodeJS?</i>
 We have included a 32-bit, 64-bit and ARMv7 version of NodeJS to make things work out of the box, but you can certainly use your own. Please amend the symbolic link in the root of the repository if necessary, or install NodeJS on your system.

 <i>What if I get an error?</i>
 Make sure you have correctly configured cli4ioc to connect to a hybridd node. Also check if our default node is operational. If not, you should run your own. If this does not solve your problem, feel free to share the issue with us.
 
## Authors

Joachim de Koning <joachim@internetofcoins.org>

Others: many libraries and code snippets contained herein have other authors and their own licensing included.

## License

This work is licensed under the GNU GPLv3 license. (See the LICENSE file in the root of this repository.)

Copyright (c) 2014-2017 Internet of Coins

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
