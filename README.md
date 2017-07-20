# Return to Harvard
A manifesto for returning to known personal computing - just an idea to pick holes in.

## What did we lose when we went from 8-bit home computers and consoles to PCs with hard disks?

- Operating Systems (OK, BASICs) that would boot immediately, and more importantly, identically, every time power was applied.
- OSs on ROM, which could not be modified by any form of software bug.
- Applications on tape - software bugs could not permanently modify applications without the user pressing "record".
- Applications and games on ROM - no modification possible.
- Data on tape - software could only modify your data when you physically pressed record.

I do recognise that we gained one or two minor things since the 80s, but we should be striving for the penny and the bun.

The current state of computing, especially Android (where I caught the built-in keyboard App sending my data abroad) is not acceptable.

## How can we get these benefits back?

Modern computers use a Modified-Harvard architecture, just an optimised version of Von Neumann architecture, where programs and data exist in the same RAM.  OSs, applications and user data are likewise saved on the same disk.

This used to be the only affordable way of doing things when computers' performance was limited and hard disks were expensive.

A pure Hardvard architecture splits code from data.

This eliminates the majority of attack vectors.

## The RtH Machine

The RtH Machine has a CPU with two, distinct, read-only sources of instructions, the Kernel Storage Device and Application Storage Devices.

These are not 80's-style ROM chips.  They are flash storage devices to which the RtH CPU cannot physically write, heavily cached with on-device RAM and separated CPU caches.

The RtHM has conventional Random Access Memory.

The RtH CPU physically cannot execute instructions from RAM.

The RtHM has multiple, removable, writeable storage devices, WSDs.  These have a physical write-enable button which makes them writable for a short period of time.

## What about Software Developers?

Software developers will use a dual ported device which plugs in as both a WSD and an ASD.

## What about Data Centres?

Data centres, where multiple servers need to have ASDs updated, can use special Network Writeable ASDs.

## Implementation Plans

- Perhaps a RISC-V core could be modified to this design and implemented on an FPGA?
- Perhaps 100's of 74xxx logic chips?

## Source of this Madness?

I'm lucky enough to have to write code for Harvard-Architecture AVR chips at work.  It's so much more fun than writing code for Android - the target doesn't keep moving and mutating before your eyes.

## Thoughts?

Pull requests welcome...
