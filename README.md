# nudanos-router

The NuDanOS router meta-package: installing it installs the milestone-1
package set (the Vyatta configuration system, FRR, VRRP and the services of
milestone 1), forwarding in the Linux kernel through `vyatta-kernel-forwarding`.

Its `Depends` are every binary in the NuDanOS archive except development and
debug packages and those
[`docs/kernel-forwarding.md`](https://github.com/nudanos/distro/blob/main/docs/kernel-forwarding.md)
leaves out with a reason. Regenerate them with
`tools/router_deps.py` in [nudanos/distro](https://github.com/nudanos/distro);
its `--check` mode fails the nightly build when they drift.
