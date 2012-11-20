A modified versiob of "A Step-by-Step Guide to Installing OpenStack on CentOS Using the KVM Hypervisor and GlusterFS Distributed File System" without GlusterFS.
=====================================================================================================================

Original: github.com/beloglazov/openstack-centos-kvm-glusterfs/

What is modified:
1- Without GlusterFS
2- Gateway and Controller are the same device
3- Non of the compute nodes are gateway, they just compute nodes.




Trubleshooting
---------------
Error:

::
	
	Package: python-glance-2012.2-3.el6.noarch (epel)
           Requires: python-swiftclient


Expected Error Message in:

::
	
	05-openstack-controller/12-glance-install

Solution (Not Recommended): Install python-swiftclient manually (http://rpmfind.net/linux/rpm2html/search.php?query=python-swiftclient), for example:

::

	yum install -y ftp://rpmfind.net/linux/epel/testing/6/x86_64/python-swiftclient-1.2.0-2.el6.noarch.rpm
