# rpmbuild-ec2-expire-snapshots

Create a ec2-expire-snapshots RPM for RHEL/CentOS.

## Requirements

To download package sources and install build dependencies

    yum -y install rpmdevtools yum-utils

## Build process

To build the package follow the steps outlined below

    git clone https://github.com/linuxhq/rpmbuild-ec2-expire-snapshots.git rpmbuild
    mkdir rpmbuild/SOURCES
    spectool -g -R rpmbuild/SPECS/ec2-expire-snapshots.spec
    yum-builddep rpmbuild/SPECS/ec2-expire-snapshots.spec
    rpmbuild -ba rpmbuild/SPECS/ec2-expire-snapshots.spec

## License

BSD

## Author Information

This package was created by [Taylor Kimball](http://www.linuxhq.org).
