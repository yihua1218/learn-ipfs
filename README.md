# Learn IPFS

在想使用 IPFS 開發應用前，我想先熟悉操作使用 IPFS。而接觸到 IPFS 則是因為我正在尋找分散式非集中型的檔案系統。

[IPFS.io](https://ipfs.io/)

## Install

### Binary

從 IPFS 的官網下載 [go-ipfs](https://dist.ipfs.io/#go-ipfs)，以 Linux 版本為例，將 tar.gz 解壓縮後，sudo 執行目錄內的 install.sh 即可。

### Source Code

``` bash
$ go get -u -d github.com/ipfs/go-ipfs
$ cd $GOPATH/src/github.com/ipfs/go-ipfs
$ make install
$ ipfs
...
...
  Use 'ipfs <command> --help' to learn more about each command.

  ipfs uses a repository in the local file system. By default, the repo is
  located at ~/.ipfs. To change the repo location, set the $IPFS_PATH
  environment variable:

    export IPFS_PATH=/path/to/ipfsrepo

  EXIT STATUS

  The CLI will exit with one of the following values:

  0     Successful execution.
  1     Failed executions.
```

## Update

Install updater tool for IPFS.
安裝 ipfs-update 更新工具。

``` bash
$ go get -u github.com/ipfs/ipfs-update
$ ipfs-update versions
...
...
v0.4.14-rc1
v0.4.14-rc2
v0.4.14-rc3
v0.4.14
```

## Init

``` bash
$ ipfs init
initializing IPFS node at /Users/yihua/.ipfs
generating 2048-bit RSA keypair...done
peer identity: QmcqDCvqU2jNQwC2eEndBtNL5htAs9XcYiELWmjsyqFCgc
to get started, enter:

	ipfs cat /ipfs/QmS4ustL54uo8FzR9455qaxZwuMiUhyvMcX9Ba8nUH4uVv/readme

```

## Start Daemon

``` bash
$ ipfs daemon
Initializing daemon...
Swarm listening on /ip4/127.0.0.1/tcp/4001
...
...
API server listening on /ip4/127.0.0.1/tcp/5001
Gateway (readonly) server listening on /ip4/127.0.0.1/tcp/8080
...
```

## Web Console

[http://localhost:5001/webui](http://localhost:5001/webui)