---
layout: page
navbar: yes
title: History
joomla_id: 6
joomla_url: emc-history
date: 2006-02-27 14:44:52.000000000 -07:00
---
#A short history of LinuxCNC

**EMC (the Enhanced Machine Controller)** was created by
[NIST](http://www.nist.gov/), the National Institute of Standards and
Technology, which is an agency of the Commerce Department of the United
States government.

NIST first became interested in writing a motion control package as a
test platform for concepts and standards. Early sponsorship from General
Motors resulted in an adaptation of the fledgling version of EMC using
PMAC intelligent control boards running under a "real time" version of
Windows NT and controlling a large milling machine.

As is required of all "work product" of US federal government employees,
the resulting software and the report about it are required to be in the
public domain and a report about it was duly published, including on the
Internet. It was there that Matt Shaver discovered EMC. He contacted NIST
and entered into discussions with Fred Proctor about adapting the code
for use in controlling less expensive hardware to be used for upgrades
and replacements of CNC controls that were obsolete or just plain dead.
NIST was intrigued because they too wanted something less expensive.
In order to launch a cooperative effort, a formal agreement was created
which guaranteed that the resulting code and design would remain in the
public domain.

Early considerations focused on replacing the expensive and temperamental
"real time" Windows NT system. It was proposed that a relatively new (at
the time) real time extension of the Linux operating system be tried. This
idea was pursued with success. Next up was the issue of the expensive
intelligent motion control boards. By this time the processing power of
a PC was considered great enough to directly take control of the motion
routines. A quick search of available hardware resulted in the selection
of a [Servo-To-Go](http://www.servotogo.com/) interface board as the first
platform for letting the PC directly control the motors. Software for
trajectory planning and PID loop control was added to the existing user
interface and RS274 interpreter. Matt successfully used this version to
upgrade a couple of machines with dead controls and this became the EMC
system that first caught the attention of the outside world. Mention of
EMC on the Rec.Crafts.Metalworking USENET discussion group resulted in
early adopters like Jon Elson building systems to take advantage of EMC.

NIST set up a mailing list for people interested in EMC. As time went
on, others outside NIST became interested in improving EMC. Many people
requested or coded small improvements to the code. Ray Henry wanted to
refine the user interface. Since Ray was reluctant to try tampering with
the C code in which the user interface was written, a simpler method
was sought. Fred Proctor of NIST suggested a scripting language and
wrote code to interface the Tcl/Tk scripting language to the internal
NML communications of EMC. With this tool Ray went on to write a Tcl/Tk
program that became the predominant user interface for EMC at the time.

For NIST's perspective, see this
[paper](use-of-open-source-distribution-for-a-machine-tool-controller.pdf)
written by William Shackleford and Frederick Proctor, describing the
history of EMC and its transition to open source.

By this time interest in EMC as beginning to pick up substantially. As
more and more people attempted installation of EMC, the difficulty of
patching a Linux kernel with the real time extensions and of compiling
the EMC code became obvious. Many attempts to document the process and
write scripts were attempted, some with moderate success. The problem
of matching the correct version of the patches and compilers with the
selected version of Linux kept cropping up. Paul Corner came to the rescue
with the BDI (brain dead install) which was a CD from which a complete
working system (Linux, patches, and EMC) could be installed.  The BDI
approach opened the world of EMC to a much larger user community. As
this community continued to grow, the EMC mailing list and code archives
were moved to [SourceForge](http://www.sourceforge.net/projects/emc/)
and the LinuxCNC web site was established.

With a larger community of users participating, EMC became a major focus
of interest at the on-going CNC exhibits at NAMES and NAMES became the
annual meeting event for EMC. For the first couple of years, the meetings
just happened because the interested parties were at NAMES. In 2003 the
EMC user community had its first announced public meeting. It was held
the Monday after NAMES in the lobby of the arena where the NAMES show
was held. Organization was loose, but the idea of a hardware abstraction
layer (HAL) was born and the movement to restructure the code for ease
of development (**EMC2**) was proposed.

The EMC2 open-source project was sued by the EMC Corporation in 2011
and rebranded to the LinuxCNC name used today.