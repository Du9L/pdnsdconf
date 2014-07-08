pdnsdconf
=========

`pdnsd.conf` config file for [pdnsd](http://members.home.nl/p.a.rombouts/pdnsd/) (along with `resolvconf.conf` for [openresolv](http://roy.marples.name/projects/openresolv) framework) that might be useful.

These config files are tested on [Arch Linux](https://www.archlinux.org/), and *may or may not* work with other Linux distributions.

Licensed under The MIT License by [Xiaodu, Du9L.com](http://du9l.com).

How to use
----------

1. Make sure you have pdnsd and openresolv installed.

   On Arch Linux that would be `# pacman -S pdnsd openresolv`

2. Modify `pdnsd.conf` according to your own network and ISP.

   For example, if you don't have IPv6, you can delete the `run_ipv4` line.

   If you prefer IPv6 over IPv4, you can delete the IPv4 `ip` lines.

   Finally, if your ISP pollutes NXDOMAIN results, you can fill in the `reject` line in `local` block.

3. Put `pdnsd.conf` and `resolvconf.conf` into `/etc/`.

4. Update openresolv with `# resolvconf -u`, then start pdnsd daemon.
