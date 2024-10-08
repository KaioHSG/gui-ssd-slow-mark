[![Release](https://img.shields.io/github/v/release/KaioHSG/gui-ssd-slow-mark)](https://github.com/KaioHSG/gui-ssd-slow-mark/releases/latest)
[![Java 8](https://img.shields.io/badge/java_8-u402-blue)](https://wiki.openjdk.org/display/jdk8u)
[![Downloads](https://img.shields.io/github/downloads/KaioHSG/gui-ssd-slow-mark/total)](https://github.com/KaioHSG/gui-ssd-slow-mark/releases)
[![VirusTotal](https://img.shields.io/badge/virustotal-status-navy)](https://www.virustotal.com/gui/file/7d64de237e38666c29b0351919d1ae927119bccf0960484b2aaf6c3de6618384)
[![Results](https://img.shields.io/badge/results-📈-green)](https://github.com/KaioHSG/gui-ssd-slow-mark/discussions/categories/results)

# GUI SSD Slow Mark

*Check how slow your SSD is.*

## Why GUI SSD Slow Mark?

After discovering that conventional programs like *CrystalDiskMark* only measure the so-called [SLC cache](https://www.technipages.com/what-is-slc-caching), which normally does not exceed 10 GB. I decided to use *SSD SlowMark*, and realized that I could create an interface for it and make it easier for everyone. So I created the **GUI SSD Slow Mark**, which is an unofficial version of [*SSD SlowMark*](https://github.com/tools4free/SsdSlowMark).

### Comparison

* *Other tools*:

[![Other tools](https://github.com/KaioHSG/gui-ssd-slow-mark/assets/96930584/d744945f-465f-4bb0-94cd-0ac8e3d2ec58)](#)

* *SSD SlowMark*:

[![SSD SlowMark](https://github.com/KaioHSG/gui-ssd-slow-mark/assets/96930584/fb5e4369-8b2a-44bf-8e86-9c3b32cf595a)](#)

## How to test?

1. Download the [**GUI SSD Slow Mark**](https://github.com/KaioHSG/gui-ssd-slow-mark/releases/latest).
2. Now run **`GUI-SSD-Slow-Mark`**.

[![GUI SSD Slow Mark](https://github.com/KaioHSG/gui-ssd-slow-mark/assets/96930584/4da2274c-e794-47ab-abbd-02a54fd8029e)](#)

### You can already use it, but here are some explanations:

|Option|Description|
|-|-|
|`File count`|Count of generated files.|
|`File size`|Size of every file.|
|`Block size`|Minimum amount of reading and writing.|
|`Dump folder`|Folder where the files generated for the test are located. You can change the disk to be tested by changing to a valid path within it.|
|`Results folder`|Test results folder. It must be kept in the program directory.|
|`Images`|Configuration for generated images.|
|`Test type`|Indicates what type of test. For reading testing, files must be previously generated.|

**Note:** `File count` × `File size` = Total size of all files.

### List of terminal commands:

|Command|Description|
|-|-|
|`fc`|Number of files.|
|`fs`|Size of files (MB).|
|`bs`|Block size (KB).|
|`dump`|Dump directory ("path").|
|`res`|Results folder ("path").|
|`iw`|Width of images (px).|
|`ih`|Height of images (px).|
|`ip`|Padding of images (px).|
|`test`|Write (w) / read (r) / write and read (wr).|
|`log`|Log GUI (true / false).|

**Exemple:**

``` console
java -jar GUI-SSD-Slow-Mark.jar fc=40 fs=512
```

**Note:** `fc` × `fs` = Total size of all files.

## What's in report?

In generated report you will find:

* Averaged summary, where most important things are:

  * Portion of data written at highest speed - This typically correspond to size of SLC cache available currently.

  Note: some drives may perform either constantly bad, this means it does not have SLC cache. Or constantly good, this means either it has quick memory like [3D XPoint](https://en.wikipedia.org/wiki/3D_XPoint) or you did not yet rech end of SLC cache area which in same cases may take 20-30% of disk drive.

  * Max read speed - How quickly your programs start depends on that.

  * Most typical write speed - How quickly you can fill your disk depends on that.

  [![Report Averages](https://github.com/KaioHSG/gui-ssd-slow-mark/assets/96930584/cde456f2-c7bf-4e09-90cd-bf919c3eee66)](#)

* Detailed chart of read and write test:

  [![Report Chart](https://github.com/KaioHSG/gui-ssd-slow-mark/assets/96930584/eb944387-3238-46ed-ada2-d799fbda70d4)](#)

* Raw metrics are collected into CSV files. You may use them to build aggregated data for multiple drives in Excel or similar tool.

## User results

You can post your results and discuss them on the [results](https://github.com/KaioHSG/gui-ssd-slow-mark/discussions/categories/results) page.

## Problems & bugs

You can post your problems and bugs on the [problems & bugs](https://github.com/KaioHSG/gui-ssd-slow-mark/discussions/categories/problems-bugs) page. 
(Note: the program has been forked, so I don't have full knowledge to solve more complex problems, but I should try to fix any inconsistencies.)

## Credits

This is all a fork of [*SSD SlowMark*](https://github.com/tools4free/SsdSlowMark) created by [tools4free](https://github.com/tools4free). I just made a interface.

*SSD SlowMark* website: https://tools4free.github.io/ssd-slow-mark
