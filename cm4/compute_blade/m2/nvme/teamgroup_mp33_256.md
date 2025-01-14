# Product Information

| Product | [TEAMGROUP MP33 M.2 PCIe SSD](https://www.teamgroupinc.com/en/product/mp33) |
|:-|:-|
|----|----|
| *Name* | TEAMGROUP MP33 |
| *Model* | TM8FP6256G0C101 |
| *Capacity* | 256GB |
| *Form Factor* | M.2 2280 |
| *Key* | M |
| *Interface* | NVMe |
| *Controller* | Phison PS5013-E13T |
| *NAND* | Intel, Toshiba, or Micron 96L 3D TLC |
| *DRAM* | - |
| *Bootable* | :white_check_mark: |

* [Team Group Unveils MP33 SSDs: Entry-Level PCIe Drives](https://www.anandtech.com/show/14927/team-group-unveils-mp33-ssds-entrylevel-pcie-drives)
* [Team Group MP33 M.2 NVMe SSD Review: NVMe performance at SATA prices](https://www.tomshardware.com/reviews/team-group-mp33-m2-nvme-ssd)

# Device Name

```
# lsblk | grep nvme[01]
nvme0n1     259:0    0 238.5G  0 disk 
```

# Device Information

<details>
  <summary>Click here to expand...</summary>
  
  ```
  # lspci -vvv -s 01:00.0
  01:00.0 Non-Volatile memory controller: Phison Electronics Corporation PS5013 E13 NVMe Controller (rev 01) (prog-if 02 [NVM Express])
    Subsystem: Phison Electronics Corporation PS5013 E13 NVMe Controller
    Control: I/O- Mem+ BusMaster+ SpecCycle- MemWINV- VGASnoop- ParErr- Stepping- SERR- FastB2B- DisINTx+
    Status: Cap+ 66MHz- UDF- FastB2B- ParErr- DEVSEL=fast >TAbort- <TAbort- <MAbort- >SERR- <PERR- INTx-
    Latency: 0
    Interrupt: pin A routed to IRQ 63
    Region 0: Memory at 600000000 (64-bit, non-prefetchable) [size=16K]
    Capabilities: [80] Express (v2) Endpoint, MSI 00
      DevCap:	MaxPayload 256 bytes, PhantFunc 0, Latency L0s unlimited, L1 unlimited
        ExtTag+ AttnBtn- AttnInd- PwrInd- RBE+ FLReset+ SlotPowerLimit 0.000W
      DevCtl:	CorrErr- NonFatalErr- FatalErr- UnsupReq-
        RlxdOrd+ ExtTag+ PhantFunc- AuxPwr- NoSnoop+ FLReset-
        MaxPayload 128 bytes, MaxReadReq 512 bytes
      DevSta:	CorrErr- NonFatalErr- FatalErr- UnsupReq- AuxPwr- TransPend-
      LnkCap:	Port #1, Speed 8GT/s, Width x4, ASPM L1, Exit Latency L1 unlimited
        ClockPM- Surprise- LLActRep- BwNot- ASPMOptComp+
      LnkCtl:	ASPM Disabled; RCB 64 bytes, Disabled- CommClk+
        ExtSynch- ClockPM- AutWidDis- BWInt- AutBWInt-
      LnkSta:	Speed 5GT/s (downgraded), Width x1 (downgraded)
        TrErr- Train- SlotClk+ DLActive- BWMgmt- ABWMgmt-
      DevCap2: Completion Timeout: Range ABCD, TimeoutDis+ NROPrPrP- LTR+
        10BitTagComp- 10BitTagReq- OBFF Not Supported, ExtFmt+ EETLPPrefix-
        EmergencyPowerReduction Not Supported, EmergencyPowerReductionInit-
        FRS- TPHComp- ExtTPHComp-
        AtomicOpsCap: 32bit- 64bit- 128bitCAS-
      DevCtl2: Completion Timeout: 50us to 50ms, TimeoutDis- LTR+ OBFF Disabled,
        AtomicOpsCtl: ReqEn-
      LnkCap2: Supported Link Speeds: 2.5-8GT/s, Crosslink- Retimer- 2Retimers- DRS-
      LnkCtl2: Target Link Speed: 8GT/s, EnterCompliance- SpeedDis-
        Transmit Margin: Normal Operating Range, EnterModifiedCompliance- ComplianceSOS-
        Compliance De-emphasis: -6dB
      LnkSta2: Current De-emphasis Level: -3.5dB, EqualizationComplete- EqualizationPhase1-
        EqualizationPhase2- EqualizationPhase3- LinkEqualizationRequest-
        Retimer- 2Retimers- CrosslinkRes: unsupported
    Capabilities: [d0] MSI-X: Enable+ Count=9 Masked-
      Vector table: BAR=0 offset=00002000
      PBA: BAR=0 offset=00003000
    Capabilities: [e0] MSI: Enable- Count=1/8 Maskable+ 64bit+
      Address: 0000000000000000  Data: 0000
      Masking: 00000000  Pending: 00000000
    Capabilities: [f8] Power Management version 3
      Flags: PMEClk- DSI- D1- D2- AuxCurrent=0mA PME(D0-,D1-,D2-,D3hot-,D3cold-)
      Status: D0 NoSoftRst+ PME-Enable- DSel=0 DScale=0 PME-
    Capabilities: [100 v1] Latency Tolerance Reporting
      Max snoop latency: 0ns
      Max no snoop latency: 0ns
    Capabilities: [110 v1] L1 PM Substates
      L1SubCap: PCI-PM_L1.2+ PCI-PM_L1.1+ ASPM_L1.2+ ASPM_L1.1+ L1_PM_Substates+
          PortCommonModeRestoreTime=10us PortTPowerOnTime=220us
      L1SubCtl1: PCI-PM_L1.2- PCI-PM_L1.1- ASPM_L1.2- ASPM_L1.1-
          T_CommonMode=0us LTR1.2_Threshold=229376ns
      L1SubCtl2: T_PwrOn=220us
    Capabilities: [200 v2] Advanced Error Reporting
      UESta:	DLP- SDES- TLP- FCP- CmpltTO- CmpltAbrt- UnxCmplt- RxOF- MalfTLP- ECRC- UnsupReq- ACSViol-
      UEMsk:	DLP- SDES- TLP- FCP- CmpltTO- CmpltAbrt- UnxCmplt- RxOF- MalfTLP- ECRC- UnsupReq- ACSViol-
      UESvrt:	DLP+ SDES- TLP- FCP+ CmpltTO- CmpltAbrt- UnxCmplt- RxOF- MalfTLP+ ECRC- UnsupReq- ACSViol-
      CESta:	RxErr- BadTLP- BadDLLP- Rollover- Timeout- AdvNonFatalErr-
      CEMsk:	RxErr- BadTLP- BadDLLP- Rollover- Timeout- AdvNonFatalErr+
      AERCap:	First Error Pointer: 00, ECRCGenCap- ECRCGenEn- ECRCChkCap+ ECRCChkEn-
        MultHdrRecCap- MultHdrRecEn- TLPPfxPres- HdrLogCap-
      HeaderLog: 00000000 00000000 00000000 00000000
    Capabilities: [300 v1] Secondary PCI Express
      LnkCtl3: LnkEquIntrruptEn- PerformEqu-
      LaneErrStat: 0
    Kernel driver in use: nvme
  ```
</details>

# Disk Information

```
# fdisk -l /dev/nvme0n1
Disk /dev/nvme0n1: 238.47 GiB, 256060514304 bytes, 500118192 sectors
Disk model: TEAM TM8FP6256G                         
Units: sectors of 1 * 512 = 512 bytes
Sector size (logical/physical): 512 bytes / 512 bytes
I/O size (minimum/optimal): 512 bytes / 512 bytes
```

# Filesystem Information

```
# df -Th /dev/nvme0n1
Filesystem     Type  Size  Used Avail Use% Mounted on
/dev/nvme0n1   ext4  234G   28K  222G   1% /mnt/sda1
```

# Benchmarks

## PiBenchmarks.com

Credit: [James C. Chambers](https://jamesachambers.com/) ([source](https://raw.githubusercontent.com/TheRemote/PiBenchmarks/master/Storage.sh))

Full benchmark: [pibenchmarks.com #67452](https://pibenchmarks.com/benchmark/67452/)

| Category | Test | Result |
|:-|:-|:-|
| DD | Disk Write | 131 MB/s |
| HDParm | Disk Read | 334.73 MB/s |
| HDParm | Cached Disk Read | 325.75 MB/s |
| FIO | 4k Random Read | 37,996 IOPS |
| FIO | 4k Random Write | 10,666 IOPS |
| FIO | 4k Random Read | 15,1985 KB/s |
| FIO | 4k Random Write | 42,666 KB/s |
| IOZone | 4k Read | 16,874 KB/s |
| IOZone | 4k Write | 53,609 KB/s |
| IOZone | 4k Random Read | 33,544 KB/s |
| IOZone | 4k Random Write | 84,121 KB/s |
| **Score** | | 14,386 |

## Jeff Geerling

Credit: [Jeff Geerling](https://www.jeffgeerling.com/) ([source](https://raw.githubusercontent.com/geerlingguy/pi-cluster/master/benchmarks/disk-benchmark.sh))

<details>
  <summary>Click here to expand...</summary>

  ```
  # DEVICE_UNDER_TEST=/dev/nvme0n1 ./disk-benchmark.sh

  Raspberry Pi disk benchmarks
  Running fio sequential read test...
  fio-rand-read-sequential: (g=0): rw=read, bs=(R) 1024KiB-1024KiB, (W) 1024KiB-1024KiB, (T) 1024KiB-1024KiB, ioengine=libaio, iodepth=64
  ...
  fio-3.25
  Starting 4 processes
  Jobs: 4 (f=4): [R(4)][27.3%][r=394MiB/s][r=393 IOPS][eta 00m:08s]
  Jobs: 4 (f=4): [R(4)][36.4%][r=388MiB/s][r=387 IOPS][eta 00m:07s]
  Jobs: 4 (f=4): [R(4)][45.5%][r=394MiB/s][r=393 IOPS][eta 00m:06s]
  Jobs: 4 (f=4): [R(4)][54.5%][r=393MiB/s][r=393 IOPS][eta 00m:05s]
  Jobs: 4 (f=4): [R(4)][63.6%][r=386MiB/s][r=386 IOPS][eta 00m:04s]
  Jobs: 4 (f=4): [R(4)][72.7%][r=397MiB/s][r=397 IOPS][eta 00m:03s]
  Jobs: 4 (f=4): [R(4)][81.8%][r=389MiB/s][r=389 IOPS][eta 00m:02s]
  Jobs: 4 (f=4): [R(4)][90.9%][r=388MiB/s][r=388 IOPS][eta 00m:01s]
  Jobs: 4 (f=4): [R(4)][100.0%][r=393MiB/s][r=392 IOPS][eta 00m:00s]
  fio-rand-read-sequential: (groupid=0, jobs=4): err= 0: pid=1175: Mon Feb 20 16:57:05 2023
    read: IOPS=390, BW=390MiB/s (409MB/s)(4166MiB/10678msec)
      slat (usec): min=122, max=4294, avg=382.78, stdev=589.62
      clat (msec): min=129, max=1628, avg=643.86, stdev=176.77
      lat (msec): min=132, max=1628, avg=644.25, stdev=176.46
      clat percentiles (msec):
      |  1.00th=[  150],  5.00th=[  401], 10.00th=[  489], 20.00th=[  502],
      | 30.00th=[  651], 40.00th=[  651], 50.00th=[  651], 60.00th=[  651],
      | 70.00th=[  651], 80.00th=[  667], 90.00th=[  844], 95.00th=[  978],
      | 99.00th=[ 1318], 99.50th=[ 1485], 99.90th=[ 1603], 99.95th=[ 1620],
      | 99.99th=[ 1636]
    bw (  KiB/s): min=323584, max=472822, per=100.00%, avg=400511.70, stdev=14532.74, samples=80
    iops        : min=  316, max=  461, avg=390.00, stdev=14.20, samples=80
    lat (msec)   : 250=3.17%, 500=11.38%, 750=73.69%, 1000=9.75%, 2000=2.02%
    cpu          : usr=0.10%, sys=4.30%, ctx=4213, majf=0, minf=65641
    IO depths    : 1=0.1%, 2=0.2%, 4=0.4%, 8=0.8%, 16=1.5%, 32=3.1%, >=64=94.0%
      submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
      complete  : 0=0.0%, 4=99.9%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.1%, >=64=0.0%
      issued rwts: total=4166,0,0,0 short=0,0,0,0 dropped=0,0,0,0
      latency   : target=0, window=0, percentile=100.00%, depth=64

  Run status group 0 (all jobs):
    READ: bw=390MiB/s (409MB/s), 390MiB/s-390MiB/s (409MB/s-409MB/s), io=4166MiB (4368MB), run=10678-10678msec

  Disk stats (read/write):
    nvme0n1: ios=16655/148, merge=0/8, ticks=10397372/68785, in_queue=10466805, util=99.39%

  Running iozone 1024K random read and write tests...
    Iozone: Performance Test of File I/O
            Version $Revision: 3.492 $
      Compiled for 64 bit mode.
      Build: linux-arm 

    Contributors:William Norcott, Don Capps, Isom Crawford, Kirby Collins
                Al Slater, Scott Rhine, Mike Wisner, Ken Goss
                Steve Landherr, Brad Smith, Mark Kelly, Dr. Alain CYR,
                Randy Dunlap, Mark Montague, Dan Million, Gavin Brebner,
                Jean-Marc Zucconi, Jeff Blomberg, Benny Halevy, Dave Boone,
                Erik Habbinga, Kris Strecker, Walter Wong, Joshua Root,
                Fabrice Bacchella, Zhenghua Xue, Qin Li, Darren Sawyer,
                Vangel Bojaxhi, Ben England, Vikentsi Lapa,
                Alexey Skidanov, Sudhir Kumar.

    Run began: Mon Feb 20 16:57:05 2023

    Include fsync in write timing
    O_DIRECT feature enabled
    Auto Mode
    File size set to 102400 kB
    Record Size 1024 kB
    Command line used: ./iozone -e -I -a -s 100M -r 1024k -i 0 -i 2 -f /mnt/sda1/iozone
    Output is in kBytes/sec
    Time Resolution = 0.000001 seconds.
    Processor cache size set to 1024 kBytes.
    Processor cache line size set to 32 bytes.
    File stride size set to 17 * record size.
                                                                random    random     bkwd    record    stride                                    
                kB  reclen    write  rewrite    read    reread    read     write     read   rewrite      read   fwrite frewrite    fread  freread
            102400    1024   361344   348280                     330233   363746                                                                

  iozone test complete.

  Running iozone 4K random read and write tests...
    Iozone: Performance Test of File I/O
            Version $Revision: 3.492 $
      Compiled for 64 bit mode.
      Build: linux-arm 

    Contributors:William Norcott, Don Capps, Isom Crawford, Kirby Collins
                Al Slater, Scott Rhine, Mike Wisner, Ken Goss
                Steve Landherr, Brad Smith, Mark Kelly, Dr. Alain CYR,
                Randy Dunlap, Mark Montague, Dan Million, Gavin Brebner,
                Jean-Marc Zucconi, Jeff Blomberg, Benny Halevy, Dave Boone,
                Erik Habbinga, Kris Strecker, Walter Wong, Joshua Root,
                Fabrice Bacchella, Zhenghua Xue, Qin Li, Darren Sawyer,
                Vangel Bojaxhi, Ben England, Vikentsi Lapa,
                Alexey Skidanov, Sudhir Kumar.

    Run began: Mon Feb 20 16:57:06 2023

    Include fsync in write timing
    O_DIRECT feature enabled
    Auto Mode
    File size set to 102400 kB
    Record Size 4 kB
    Command line used: ./iozone -e -I -a -s 100M -r 4k -i 0 -i 2 -f /mnt/sda1/iozone
    Output is in kBytes/sec
    Time Resolution = 0.000001 seconds.
    Processor cache size set to 1024 kBytes.
    Processor cache line size set to 32 bytes.
    File stride size set to 17 * record size.
                                                                random    random     bkwd    record    stride                                    
                kB  reclen    write  rewrite    read    reread    read     write     read   rewrite      read   fwrite frewrite    fread  freread
            102400       4    52069    82526                      37572    79182                                                                

  iozone test complete.

  Disk benchmark complete!
  ```
</details>