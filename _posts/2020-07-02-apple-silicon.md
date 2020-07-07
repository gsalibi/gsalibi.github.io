---
layout: post
title: "Apple Silicon: Everything you need to know about the new ARM processors"
summary: Impacts on developers, users and the market
author: Gustavo Salibi
date: '2020-07-02 00:00:23 +0530'
category: Apple
thumbnail: /assets/img/posts/apple-silicon.png
---
Widgets, app clips, iOS 14, watchOS, macOS Big Sur. There were several new features presented during Apple's annual
event, WWDC, but one of them certainly stands out: Apple Silicon. The adoption of this new architecture, expected for all of the company's computers by 2022, will entail several internal changes and, perhaps, for the technology market as a whole.

Apple Silicon is the name of the new processors family that will start to be used in new Apple computers until the end
of this year. But this is far from being a simple processor upgrade. It is an implementation in a completely different
architecture, which means that no current software would be able to run in the new version – but, obviously, that would
be unsustainable and Apple announced ways to work around this problem, as we will see later in this article –.

<br>
#### What are the differences between the current and the new architecture?

The current processors use the x86_64 architecture (also called AMD64) and are produced by Intel, while the new Apple
Silicon will use the ARM64 architecture and will be produced by Apple itself. Intel processors are based on a complex
instruction set (CISC), while the new Apple chip will use a reduced instruction set (RISC).

This implies several differences: CISC processors typically have higher clock rate, are more expensive to produce and tend to be
more powerful in performance. However, they are bigger and consume more energy. Processors that use RISC, on the other
hand, usually result in smaller, cheaper and less energy-consuming designs. This makes them widely adopted in the
smartphone market.

Another important difference is the instruction set. When writing a program in some high-level language (such as Java,
Python or C), it needs, at some point, to be transcribed into the processor's instructions using a type of assembly
language. A set of CISC instructions produces smaller programs, in terms of code, which was important in the past, since
the memory, divided between the data of the running program and the stored code, was limited. While a RISC set has far
fewer instructions available, which produces software that uses much more code to perform the same task, which makes
them more difficult to program directly.

<br>

<script src="https://gist.github.com/gsalibi/9ce18048c8951818e837da863da9981c.js"></script>
<p style="text-align: center;">X86 assembly code example</p>
<br>

<script src="https://gist.github.com/gsalibi/ba691628fee09cef97b001a7d5f0ed81.js"></script>
<p style="text-align: center;">Same example in ARM</p>
<br>

Unlike what many people think, ARM need not necessarily be aimed at less demanding projects. ARM can indeed scale very
well. An example of this is the current fastest supercomputer in the world, the Japanese machine Fugaku , which is based
on ARM.

<br>
<hr>
<br>

## Why change now?

In fact, an exchange of this magnitude involving Apple is not unprecedented. Before adopting Intel's x86 chips,
processors with the PowerPC architecture - which, by the way, were RISC - were already used on Apple computers. And
before that, there was another big change in the 90s. The difference this time is in the fact that the chips are
produced by Apple itself.


<br>
<p style="text-indent: 0px; text-align: center;"><img src="/assets/img/posts/performance_vs_power.png" style="max-width: 100%;"></p>
<br>

A very important metric of the new architecture, when dealing with portable devices like the MacBook, is the best performance per watt, which guarantees greater battery life. This has been pursued by Apple since before the transition to Intel, as the chips of that time, G3 and G4, equipped laptops, but the G5, the most powerful and energy-consuming chip, was never able to integrate a laptop. Another important point is the lower heating caused by the processor, which allows computers to have less cooling equipment and to make them even thinner.

Although other companies could use it in the past, currently only Intel, AMD and VIA are licensed to develop x86_64 chips. While ARM chip designs are licensed to several other companies, including, now, Apple. This, by itself, is already a major commercial factor, since it no longer depends on Intel, which in recent years delayed the release of new versions of processors, making the launch date for Apple computers not fully controllable - have you noticed that, unlike other products, Macs do not follow a release date pattern? -. In addition, the technologies implemented are entirely dependent on Intel. Along with all this, the cost to ship each chip in Apple devices is increased, since they are purchased from that other company.

Apple is not the first company to think about using ARM on computers in recent times. Microsoft has been trying this for many years, although it still doesn't have any commercial versions of Windows with ARM.

<br>
#### System on a chip

<br>
<p style="text-indent: 0px; text-align: center;"><img src="/assets/img/posts/system_on_a_chip.jpg" style="max-width: 100%;"></p>
<br>

Currently, Intel-based Macs already have multiple cores, a discrete GPU (separate memory from the CPU) and an extra T2 chip produced by Apple itself and used to control Mac-integrated devices that allow features like Apple Pay, TouchID and Hey Siri.

With the new Apple Silicon SoC (system on a chip), all currently used components will be combined into a single chip. This allows the system a unified memory architecture, without having to pass data over PCIe communication.

In addition, unlike Intel processors, where all cores have similar performance, Silicon will have asymmetric multiprocessing (AMP), which will allow more customizable processor usage patterns according to more or less intensive processing needs by applications . This can be setted by the programmer through quality of service (QoS) classes that indicate to the system whether the greatest demand is for speed or energy efficiency.

<br>
<p style="text-indent: 0px; text-align: center;"><img src="/assets/img/posts/asymmetric-multiprocessing.png" style="max-width: 100%;"></p>
<br>

Improvements in machine learning were also announced, with the use of several accelerators, compression, SIMD (parallel computing where the same instruction is applied simultaneously to different data to produce more results) and a neural engine embedded in the chip. In addition to a coprocessor dedicated to encoding and decoding videos combined with machine learning accelerators for matrix multiplication.

<br>
#### Security

Building the chip itself allowed Apple to develop more advanced security devices for the iPhone and iPad. Now they will bring this to the Mac as well. The news is:

* *Write XOR Execute (WˆX):* The memory pages will no longer be able to be written and executed at the same time. And this will work with threads, so that different processes may have different permissions for the same page, which is very useful for multi-threaded JITs (such as those used in Java and JavaScript).
* *Kernel Integrity Protection:* Through hardware support, the memory controller will make the kernel code immutable. Both for modifications of the current code and for loading new ones.
* *Pointer authentication codes (PACs):* Are codes stored in unused high bits of a pointer to check when it is being used. This prevents pointers from being misused and can protect against attacks such as return-oriented programming. It will initially be available in the kernel codes, in the system applications and in the system services.
* *Device isolation:* On Intel-based Macs, macOS offers all devices a shared view of system memory, since PCIe devices access memory through an IOMMU (input–output memory management unit). On Apple Silicon, on the other hand, all devices receive separate memory mappings. This restricts devices to access only the memory intended for them.

<br>
<hr>
<br>

<br>
<p style="text-indent: 0px; text-align: center;"><img src="/assets/img/posts/logo-apple-developer.png" style="max-width: 100%;"></p>
<br>

## What are the impacts on developers?

In general, development activities will not change much. The same APIs we currently use (CoreML, Metal, etc.) will automatically run optimally on Apple Silicon.

As for device isolation, new devices must use the IOMapper API. But you only need to worry about it if you develop this kind of lower level code. Some older drivers that access memory through physical segments will no longer work. Therefore, these drivers will need to update to the latest API before migrating to the new platform. The old API would only work for drivers written as a kernel extension.

Apple encourages such new developments using DriverKit (available from macOS Catalina). With it, the created drivers will run in user-space, which increases the stability and security of the system.

#### Rosetta 2

For applications currently compiled on x86, apple will use a solution with the name Rosetta, the same one used in the transition from PowerPC to Intel. Through Rosetta 2, when installing a new application downloaded from the App Store or that uses package installation, the code will be automatically ported to ARM64. In the case of applications that use other means of installation, this will be done on the first app launch. However, there are some limitations due to hardware compatibility restrictions. It will not be possible, for example, to emulate an x86 system in a virtual machine written in x86.

The codes produced by Rosetta 2 will be signed and updated with each new version of the OS.

If you need to debug or create a profile, you can compile and run applications already translated into ARM64 directly in Xcode and create a profile in Instruments. You can also use command line tools like llbd.

Rosetta 2 does not support AVX vector extensions for x86. Applications must verify that the machine supports it before attempting to use them.

#### Native applications (Universal 2)

Despite the existence of Rosetta 2, the ideal remains, of course, for applications to be compiled natively for ARM64. You can generate universal binaries that work on both x86_64 and ARM64 using Xcode 12. macOS will automatically know how to handle these files according to the current architecture. To find out more about this, you can [check the official documentation here.](https://developer.apple.com/documentation/apple_silicon "Official documentation"){:target="_blank"}



Compatible iPad and iPhone apps will also be available to be used directly on macOS, without extra work. To make apps compatible, you can [check this demo.](https://developer.apple.com/videos/play/wwdc2020/10114 "iPhone and iPad Demo"){:target="_blank"}

For those who want to start working with ARM on macOS right now, Apple launched a program where you can get a prototype of the Mac Mini with an A12Z chip (the same one that is in the new iPad Pro), if accepted. The cost is 500 dollars and [you can apply through this link.](https://developer.apple.com/programs/universal "Apply"){:target="_blank"}

<br>
<hr>
<br>

## What are the impacts on users?

Currently Apple already has its applications running natively on ARM, as presented at WWDC. They also worked with some major companies, such as Adobe, to make Creative Cloud available, and Microsoft to bring Office.

<br>
<p style="text-indent: 0px; text-align: center;"><img src="/assets/img/posts/boot.png" style="max-width: 100%;"></p>
<br>

* *Boot security:* On Macs with Apple Silicon, the boot process is based on the secure boot architecture of iOS and iPadOS. Secure boot ensures each start-up component is cryptographically singned by Apple and that the boot happens only after the chain of trust has been verified.
* *Enhancements to support:* Multiple macOS installations (internal or external volumes); Multiple versions of macOS (this will allow future macOS to continue booting previous versions).
* *Start-up and macOS Recovery:* Now all the old commands used for access during boot will be unified in a management screen accessible only by pressing and holding the power or Touch ID button. On this screen you will be able to access all recovery options.
* *Login:* Unified experience with or without using FileVault, with accelerated graphics even before entering the system (this is possible because now macOS is completely loaded without requiring the user to unlock the system).
* *Data protection:* The chips will support always-on volume encryption (similar to T2 for current Macs) and integrity protection and secure hibernation, in addition to preserving the desktop and applications during a low battery event.
* *MacOS recovery:* If macOS is not accessible, you can reinstall and recover your system. If macOS Recovery itself is not accessible, it is currently necessary to access the internet to continue the recovery. While with Silicon, it will be possible to do even offline through the new System Recovery, which consists of a minimal installation of macOS in a hidden container. You will also be able to continue installing with Apple Configurator 2, where all data is erased and reinstalled, including macOS and System Recovery.

#### Boot Camp and Windows installation on Mac

Although microsoft uses Windows running on ARM internally in some applications, there is still no version that can be purchased by the end user. So, at first, it will not be possible to use Windows natively on Macs that come with ARM. There will probably be programs for x86 systems virtualization, but this will be a far from ideal solution.

Even though there was an ARM version of Windows available now, that doesn't mean it would be compatible with the Apple chip, as there must be differences in the instructions. And, assuming Windows is compatible with Silicon, most programs could not be run, since they are written for x86_64.

If Apple maintains a more universal compatibility in its architecture, while also accepting more standard ARM instruction sets on the market, this may allow other systems, such as Windows, to have functional versions on the Mac in the future. However, this is not very likely, after all, we are talking about the company that uses the lightning standard on their smartphones until today.

#### Future of Hackintosh

A parallel market for macOS users has grown a lot in recent years, with the emergence, even, of companies specialized in this. Hackintosh practice consists of installing and using macOS on non-Apple official hardware devices. The legality of the practice is debatable and there is no consensus.

Currently, this activity is possible thanks to the hardware components used by Apple, mainly the processor, are not exclusive and there are several equal or compatible options on the market. However, with the arrival of new chips, that should change.

As Apple Silicon will be exclusive to Apple, it will no longer be possible to use computers legally manufactured by other companies to run macOS. But that shouldn't be an immediate problem, as the new macOS continues to have a native version on x86_64 and, in addition, Apple will support previous versions for years. At least until 2022 the new macOS will have an Intel version.

When Apple starts releasing only ARM64 systems, whose date is uncertain, if the Hackintosh market persists, they may have to resort to chip piracy or emulation, which can greatly impact performance.

<br>
<hr>
<br>

## How can this be reflected in the computer market as a whole?
Many speculations have arisen, but the truth is that there is nothing concrete yet.

#### Use of ARM architecture by other companies
Although the dominance of the end user computer market is almost absolute on the part of the x86 architecture, more and more evidence suggests that this may change. Even before Apple's announcement, CPUs Benchmarks already showed that some ARM chips were capable of outperforming many good x86 processors. An example of this was the iPad Pro 2017, with the A12x chip, which not only got higher scores than the vast majority of processors, but was also able to surpass them in real tasks, especially in the long-running heavy ones, such as rendering of videos. This was due to the fact that traditional x86 chips cannot operate for a long time at close to their maximum power, while the chip present in the iPad can, even with less cooling devices and less physical space than a laptop. This explains its performance four times faster than a Core i7 laptop running Windows in 4K video rendering.

Apple has not given any indication that the prices of the new MacBooks may fall, even with the lower prices of processors. In addition, as everyone knows, its strategy has always been focused on the premium segment, where profit margins are higher. But nothing prevents other brands, with different strategies, from using ARM chips to cheapen their computers and deliver performances similar to those they already deliver today.

#### Intel

Recently, ex-Intel principal engineer François Piednoël made a strong statement about what may have been one of the big reasons why Apple changed its architecture. He said:

"Basically our buddies at Apple became the number one filer of problems in the architecture. And that went really, really bad. When your customer starts finding almost as much bugs as you found yourself, you're not leading into the right place."

In the quote, he refers to the 2015 6th generation Intel Core (Skylake), which would have been the trigger for Apple to make the decision.

Despite this, Intel should not suffer major impacts at first, as it has a very diverse range of customers. Furthermore, its positioning is no longer a company that makes processors, but a company that provides solutions for data centers and the internet of things. However, if the market as a whole is influenced by ARM architectures and Intel remains focused on its x86, it may indeed suffer a severe blow in the future.

<br>
<hr>
<br>

## Links used

* WWDC 2020 Special Event Keynote -  <https://www.apple.com/apple-events/june-2020>{:target="_blank"}
* Supercomputer Fugaku, named after Mt. Fuji, makes its debut -  <http://www.asahi.com/ajw/articles/13462617>{:target="_blank"}
* Explore the new system architecture of Apple Silicon Macs - <https://developer.apple.com/videos/play/wwdc2020/10686>{:target="_blank"}
* Arm Holdings -  <https://www.arm.com>{:target="_blank"}
* Windows 10 on ARM documentation -  <https://docs.microsoft.com/windows/arm>{:target="_blank"}
* Intel insider claims it finally lost Apple because Skylake QA 'was abnormally bad' -  <https://www.pcgamer.com/intel-skylake-why-apple-left>{:target="_blank"}
* Intel | Data Center Solutions, IoT, and PC Innovation -  <https://www.intel.com>{:target="_blank"}
