---
layout: post
title: "CoprHD Community Announces 2.4 Release, New Projects and Contributors"
date: 2015-12-08
---

## Highlights

*	Intel, Oregon State join effort to produce open source, industry-standard, SDS controller.
*	Community now boasts ECS and ExtremIO v4 support
*	Launches two new projects for storage plugins and OpenStack integration
*	Licensing changes to Apache License v2
*	By-laws approved and implemented

### CoprHD 2.4

CoprHD 2.4 is the first official release by the CoprHD open source community and includes new features, new projects, new community contributors, new licensing, new project by-laws and governance and a technical steering committee. This release expands the scope of platform support to include EMC Elastic Cloud Storage (ECS) object storage array as well as the latest release of XtremIO (v4).

CoprHD 2.4 is <a href="/download/">available for download now</a> in the form of an OVF appliance, vagrant setup and source code. Scroll to the bottom of this post for more details on new features.

### New Contributors

Intel and Oregon State are actively participating in the CoprHD community and contributing core functionality, API plugins and integrations, event logistics and support, marketing and PR, and web site design. Look for most of the code contributions to
surface in future CoprHD releases.

### New Projects

We are also announcing 2 new complementary projects in the CoprHD community:
* <a href="https://coprhd.atlassian.net/wiki/display/COP/Block+Storage+API+For+OpenStack">Storage orchestration for OpenStack</a>
* <a href="https://coprhd.atlassian.net/wiki/display/COP/Southbound+SDK+for+Storage+Device+Drivers">Southbound SDK for pluggable storage</a>
** <a href="https://coprhd.atlassian.net/wiki/display/COP/ScaleIO+Storage+Driver+Based+on+Southbound+SDK">ScaleIO plugin using new SDK</a> - part of the SDK project

EMC is leading a set of projects to provide CoprHD integration for OpenStack. Intel is contributing to this effort by leading a project to integrate Keystone with CoprHD and allow the use of the Cinder API and/or the CoprHD API to provide block storage services for OpenStack. This feature will help organizations maintain interoperability with OpenStack services while providing a single storage management interface with CoprHD. You can find the first code drop in its
<a href="https://review.coprhd.org/projects/CH/repos/coprhd-controller/browse?at=refs%2Fheads%2Ffeature-block-service-cinderapi">respective feature branch</a>.

EMC has developed the preview code for the southbound SDK, available from <a href="https://coprhd.atlassian.net/wiki/display/COP/Southbound+SDK+for+Storage+Device+Drivers">the southbound SDK project page</a>. This will allow storage vendors and other 3rd parties to more easily add support for other storage systems to CoprHD.
The first plugin under development using the southbound SDK is the <a href="https://coprhd.atlassian.net/wiki/display/COP/ScaleIO+Storage+Driver+Based+on+Southbound+SDK">ScaleIO driver</a>, under development by Oregon State University students. This will ultimately replace the ScaleIO driver in the current release and will serve as a test case for development of the southbound SDK.

### Live-streamed town hall December 9, 4pm EST/1pm PST

Live-streamed event: EMC, Intel and Oregon State will produce a <a href="https://www.youtube.com/watch?v=VslEYcUS_8s" target="_blank">live-streamed event on December 9</a> at 4pm Eastern/1pm Pacific to present the new capabilities of CoprHD 2.4, the new projects, and a preview of what’s on the roadmap for the next development cycle.

### CoprHD Governance and License

<a href="https://coprhd.atlassian.net/wiki/display/COP/Bylaws">Community by-laws</a> for the CoprHD project have been released. These go into effect as of this release and will provide the structure for <a href="https://coprhd.atlassian.net/wiki/display/COP/Governance">project governance</a> going forward.

Licensing change – the community has decided that, in the interests of using a license most commonly found in cloud infrastructure, the Apache License v2 would best serve the CoprHD community, effective as of this release.

### Developer Summit January 12 - 14

We will convene on the Oregon State campus on January 12 and 13 to plan out the next release cycle. If you want to contribute to the discussion around new features, see our <a href="https://coprhd.atlassian.net/wiki/display/COP/Roadmap">roadmap</a> and <a href="https://coprhd.atlassian.net/wiki/display/COP/Projects">feature blueprints</a>.


### What is CoprHD?

CoprHD is open source storage automation software. It centralizes and transforms multi-vendor storage into a simple and extensible platform. It abstracts and pools resources to deliver automated, policy driven storage services on demand via a self service catalog. With vendor neutral centralized storage management, CoprHD provide choice through automation of provisioning and reclamation tasks and provides storage-as-a-service for cloud-based infrastructures.

### CoprHD 2.4 Feature detail

* Ingestion of VPLEX Environments. The volume ingestion framework for VPLEX has been enhanced to enable ingestion of the entire volume structure (virtual volume and component storage volumes) on backend arrays. Storage administrators can take control of all on-going volume management features on ingested volumes on VMAX, VNX, XtremIO, and VMAX3 backend storage arrays with both local and distributed configurations.
* VPLEX Automation. VPLEX usage in an OpenStack ecosystem is further strengthened by ViPR Controller's automation of VPLEX to interoperate with third party block storage arrays discovered through OpenStack Cinder. Support for VPLEX Local or Metro configurations enables administrators to:
** Create/delete virtual volumes(s)
** Establish zoning between VPLEX and array
** Export VPLEX virtual volumes
** Manage snapshots for VPLEX volumes
** Perform data migration across virtual storage pools / arrays
*	EMC Elastic Cloud Storage (ECS) Support. Storage administrators now have the ability to discover and provision EMC ECS object storage from ViPR Controller. This initial support lays the foundation for future object storage functionality enhancements in future releases and enables administrators to:
** Discover and monitor object storage pools and replication groups
** Create object virtual pools and map projects
** Create tenants (and associated namespace)
** Perform bucket operations (create, delete, and edit buckets)
* XtremIO Release 4.0 Support. CoprHD Controller supports functionality introduced in the EMC XtremIO 4.0 version for the following features:
** Single XtremIO Management Server (XMS) managing multiple XtremIO clusters.
** Consistency Group (CG) operations
** Snapshot restore and refresh
** Read-only snapshots
* ScaleIO API Support. For ScaleIO 1.32 and onwards, all existing functionalities will be supported via the ScaleIO REST based API. CoprHD Controller will connect via the ScaleIO Gateway Storage Provider to discover ScaleIO systems.
* NAS Performance Based Placement. For VNX arrays and FileSystems (FS) only, ViPR Controller supports the discovery of Virtual Data Movers(VDMs) and their characteristics as virtual NAS (VNAS) servers, as well as, their assignment to projects. To fully utilize the array's capabilities, ViPR Controller intelligently selects the VDM based on load factor when provisioning for parameters such as; number of storage objects, maximum storage capacity, threshold percentage.
