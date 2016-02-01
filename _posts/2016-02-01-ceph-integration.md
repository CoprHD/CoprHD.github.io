---
layout: post
title: "Ceph Integration Prototype"
date: 2016-02-01
---

Another Storage Integration: Ceph 
---------------------------------

![Ceph](https://avatars2.githubusercontent.com/u/1015767 "yay Ceph") 

When we first announced that we were open sourcing CoprHD, lots of people were skeptical, thinking we weren't serious about a real
open source community or project. The proof, they said, would be in the proverbial pudding: would we support non-EMC storage systems?
Would the CoprHD team support contributions from EMC competitors? 

I'm happy to say that, in addition to creating a [southbound API](https://coprhd.atlassian.net/wiki/display/COP/Southbound+SDK+for+Storage+Device+Drivers) 
to support the easier integration of storage systems, we're now adding support for open source storage software, in this particular 
case a [Ceph driver](https://github.com/cloudscaling/coprhd-controller/tree/ceph-review). What you'll find at that link is a CoprHD
branch that includes support for provisioning storage on Ceph volumes. This is early preview code - I'm sure there are lots of things 
that won't work yet. We will eventually fold the work from this branch into the current release branch of CoprHD, hopefully in time 
for the next release later this spring. Note that this code is based on the CoprHD 2.4 release. As the code firms up, we'll rebase
from CoprHD master. 

So take a look and let us know how it works for you. If you need a primer on getting started with CoprHD, head to the 
['Getting Started' Wiki page](https://coprhd.atlassian.net/wiki/display/COP/Getting+Started+Guide+for+Users). 

If you need assistance, check out the [CoprHD Google Group](https://groups.google.com/forum/?hl=en#!forum/coprhd). 

* [Check out the ceph-review branch](https://github.com/cloudscaling/coprhd-controller/tree/ceph-review)

Happy hacking!

-John Mark
