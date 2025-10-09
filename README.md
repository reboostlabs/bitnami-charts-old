Bitnami Charts Registry
=======================

This repository provides a registry for the Bitnami Helm charts that are no longer being release in their original
locations. This allows you to continue using these charts in your projects without needing to immediately migrate to a
different solution.

Why?
----

As announced in the [Bitnami charts repository issue #35164](https://github.com/bitnami/charts/issues/35164), Bitnami is
making significant changes to their public catalog. As of **August 28th, 2025**, many of their existing Helm charts and 
container images will no longer receive updates in their current locations. While the source code remains available, the
pre-packaged charts are being deprecated. This project aims to provide a temporary solution for those who rely on these
charts.

Usage
-----

To use the charts from this repository, you'll need to update your Helm commands to point to the new location.

### Old Way

Previously, you might have installed a chart like this:

Bash

```
helm install my-release oci://registry-1.docker.io/bitnamicharts/common

```

Or by adding the Bitnami repository:

Bash

```
helm repo add bitnami https://charts.bitnami.com/bitnami
helm install my-release bitnami/common

```

### New Way

Now, you can install the same chart from this repository's OCI registry:

Bash

```
helm install my-release oci://ghcr.io/reboostlabs/bitnami-charts/common --version 0.1.0

```


Available Charts
----------------

This repository mirrors the following Bitnami charts:

-   common

-   ...

Contributing
------------

We welcome contributions! If you'd like to help keep these charts updated or add more mirrored charts, please feel free
to open a pull request.

1.  **Fork** the repository.

2.  Create your feature branch (`git checkout -b feature/fooBar`).

3.  Commit your changes (`git commit -am 'Add some fooBar'`).

4.  Push to the branch (`git push origin feature/fooBar`).

5.  Create a new **Pull Request**.

License
-------

This project is licensed under the Apache 2.0 License - see the LICENSE.md file for details. All mirrored charts retain
their original licenses.
