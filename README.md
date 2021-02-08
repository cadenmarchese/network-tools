network-tools
=============

`network-tools` is a collection of tools for debugging OpenShift cluster network issues.
It will contain both debugging scripts (described in the next section) and useful tools that can be used
by network engineers and openshift operators to debug and diagnose issues.

## Debugging Scripts
Debugging scripts are kept in `./debug-scripts`.  The content of that folder is placed in `/usr/bin` in the image.
The debug network scripts should only include debug logic for OpenShift Networking.
These scripts will typically create Kubernetes network objects (pods, services, network policies etc) and perform
a series of tests to diagnose the functionality in the cluster works ok. In case there is a check that fails, we
would dig in the script and provide further checks to point at potential root causes to resolve the issue.
Therefore, the pattern for these scripts is to find issues and *why* those issues exist. Gathering logs is not
in the scope of these scripts and are better suited on the openshift/must-gather image.

## Documentation

* Please see [contributor docs](https://github.com/openshift/network-tools/blob/master/docs/contributor.md) for more information regarding the scope of this repository and how to contribute.
* Users can go to [user docs](https://github.com/openshift/network-tools/blob/master/docs/user.md) for information on how to leverage the tools and scripts shipped by this image.
