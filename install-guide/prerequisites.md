# Pre-requisites

Before installing Gluster server, each node in the cluster needs to have
specific setup done so that it can work effectively as a Gluster node. These
instructions use CentOS 7 as the base

## Minimum machine requirements

## Setup NTP

## Setup DNS

## Setup filesystem

## Setup firewall

## Setup SELinux
On CentOS and RHEL, SELinux is set to Enforcing by default. If you have
modified this, we recommend setting it to Enforcing. To set SELinux to
Enforcing, execute the following:

    $ sudo setenforce 1


- A **trusted pool** refers collectively to the hosts in a given Gluster
  Cluster.
- A **node** or “server” refers to any server that is part of a trusted pool.
  In general, this assumes all nodes are in the same trusted pool.
- A **brick** is used to refer to any device (really this means filesystem)
  that is being used for Gluster storage.
- An **export** refers to the mount path of the brick(s) on a given server, for
  example, /export/brick1
- The term **Global Namespace** is a fancy way of saying a Gluster volume
- A **Gluster volume** is a collection of one or more bricks (of course,
  typically this is two or more). This is analogous to /etc/exports entries for
  NFS.
- **GNFS** and **kNFS**. GNFS is how we refer to our inline NFS server. kNFS
  stands for kernel NFS, or, as most people would say, just plain NFS. Most
  often, you will want kNFS services disabled on the Gluster nodes. Gluster NFS
  doesn't take any additional configuration and works just like you would
  expect with NFSv3. It is possible to configure Gluster and NFS to live in
  harmony if you want to.
