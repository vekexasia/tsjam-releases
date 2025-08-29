# tsjam release binaries

This repository contains various versions of fuzzer target for tsjam. 

## how to use the target

```
$tsjam-target-binary
```

It is needed to have the `cwd` set at the same location as the binary as it would need to resolve some of the dependencies that are found within the tar.

The target will automatically listen to `/tmp/jam_target.sock`. And it will run with the **full** chain spec. 

To use it with the **tiny** spec an env variable called `JAM_CONSTANTS` must be set to `tiny`

```
JAM_CONSTANTS=tiny $tsjam-target-binary
```

## About the implementation

The real implemantation lives under under [this repository](https://github.com/vekexasia/tsjam) which at the time of writing is still private but will be made open source.

The above mentioned repository has been timestamped in the [Dot chain](https://polkadot.subscan.io/account/155tk9HmeJGsNZtA5LFasSCGZCdpAb2P2Gs6ej9JeP38sAww) using the remark extrinsic.

## About the binaries

The binaries are built to be working under linux x86_64. As of now there is no plan to realase them for other OSes or platforms.

The performance of the implementation using the binary might not be as good as if it is run directly with the node executable.


