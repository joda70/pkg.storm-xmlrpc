# RPM packaging for StoRM Xmlrpc

## Usage

`build-images.sh` builds the Docker images used to create the packages:


- `italiangrid/pkg.storm-xmlrpc:centos6
- `italiangrid/pkg.storm-xmlrpc:centos7

These images depend on the following common images:

- italiangrid/build-centos6
- italiangrid/build-centos7

`push-images.sh` pushes the images to a private Docker registry whose host
must be defined with the `DOCKER_REGISTRY_HOST` environment variable.

## Parameters

Both images support the following parameters (expressed as environment variables)

| **PARAMETER**   | **DEFAULT VALUE**                                    | **MEANING**                                            |
| --------------- | ---------------------------------------------------- | ------------------------------------------------------ |
| BUILD_TAG       | develop                                              | The storm-xmlrpc branch to build                       |
| BUILD_REPO      | git://github.com/italiangrid/storm-xmlrpc.git        | URL of the GIT  repo                                   |
| BUILD_NUMBER    | N/A                                                  | User provided build number. Used for internal builds   |

Packages are built in the following directories: 
- /home/build/rpmbuild/RPMS
- /home/build/rpmbuild/SRPMS

## Example usage

```
