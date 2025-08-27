# tsjam release binaries

This repository contains various versions of fuzzer target for tsjam. 

## how to use the target

```
$tsjam-target-binary
```

The target will automatically listen to `/tmp/jam_target.sock`. And it will run with the **full** chain spec. 

To use it with the **tiny** spec an env variable called `JAM_CONSTANTS` must be set to `tiny`

```
JAM_CONSTANTS=tiny $tsjam-target-binary
```

## Changelog


```
jam-fuzzer-target-v0.7.0.1-proto0.7.0 ffa3b3d808f693e84ab3e1a99b9fc029e1e4a720de3237474292b3e50b1d6179 
Added --socket parameter to specify the socket file

```

```
jam-fuzzer-target-v0.7.0-proto0.7.0 fd1ec6cfa3086fe0a9df352af0f6087d125de3abaf98a949893e0912c888342b 
```

## About the implementation

The real implemantation lives under under [this repository](https://github.com/vekexasia/tsjam) which at the time of writing is still private but will be made open source.

The above mentioned repository has been timestamped in the [Dot chain](https://polkadot.subscan.io/account/155tk9HmeJGsNZtA5LFasSCGZCdpAb2P2Gs6ej9JeP38sAww) using the remark extrinsic.

## About the binaries

The binaries are built to be working under linux x86_64. As of now there is no plan to realase them for other OSes or platforms.

The performance of the implementation using the binary might not be as good as if it is run directly with the node executable.


