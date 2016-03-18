# Readme

## What is this?

This is a BGP test network topology in my home, covered with guests access.

## How to use?

* Install `GNS3`, and then download the latest `c7200-advipservicesk9-mz.152-4.S5` from [cisco tools download](http://tools.cisco.com/ITDIT/CFN/jsp/SearchBySoftware.jsp) page.

(Different version may be various, recommend to use the version mentioned above.)

* Import the ios image into the `GNS3`.

* Import configs from this repo's **root** directory.

## How does the networks go in this topology?

![image](https://raw.githubusercontent.com/zhangjingye03/ZJYHOME_network_test/master/topology.png)

Just like the image above.

`WR703n` runs `AS65002` alone.

`WR941n` runs `AS65001` alone.

`VMware`, `WDR7500` and `WDR4310` run `AS65000`.

All routers run BGP.

Routers in `AS65000` runs OSPF as IGP to broadcast their interfaces' addresses.

EBGP is used as EGP between AS and AS.

I don't want to paste much useless route table in this README. Just clone it and `sh ip ro` or `sh ip bgp`~

All interfaces are pingable from another router. Try `traceroute` on any router.

## I can't understand why you don't obey `KISS`(Keep It Simple and Stupid) principle?

When there is a test, there may be a success. Trying is helpful in the future's work.

## How is it licensed?

This project follows `CC BY-NC-SA 3.0` license.

## There is a bug in your network topology! / I cannot comprehend at all!

Please open an issue. I'll try my best to answer your questions.
