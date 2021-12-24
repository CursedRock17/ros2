# ros2
Ros2 distro for m1 (arm64) macos architecture, based on ros2 rolling.

## Dependencies

Initially, follow the official documentation: https://docs.ros.org/en/rolling/Installation/macOS-Development-Setup.html
If there are deviations / additions / improvements, please write them down here.

### VCS

This isn't mentioned in the docs, but to install vcs: `pip3 install vcstool` 
(pip3, since macos has python 2 installed by default and thus homebrew installs python 3 and pip with the `3` suffix)

### Colcon

To install colcon `pip3 install colcon-common-extensions`

## Patching

To create a patch, fork the upstream repository into this organization. Then change the location to the forked repository in the ros2.repos file and delete the original sources directory from this repository.

Then, `vcs vcs import src < ros2.repos` will do the trick of re-adding the sources but this time from (our) the forked repository.

Forking is important, because it allows us to easily create upstream pull requests in the future should this be desired.
