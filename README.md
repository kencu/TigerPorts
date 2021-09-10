# TigerPorts
A local repo of  ports configured for 10.4 Tiger and either shadow newer, incompatible versions of ports or are modified to work on Tiger.

To use this overlay repository with MacPorts, download this  repo to /opt/TigerPorts, and use it by making this change in this file
```
/opt/local/etc/macports/sources.conf

$ diff -u /opt/local/etc/macports/sources.conf /opt/local/etc/macports/sources.conf
--- /opt/local/etc/macports/sources.conf
+++ /opt/local/etc/macports/sources.conf
@@ -27,4 +27,7 @@
# sites, etc.), the primary MacPorts source must always be tagged
# "[default]", even if switched from the default "rsync://" URL.

+# override repo
+file:///opt/TigerPorts
+
rsync://rsync.macports.org/macports/release/tarballs/ports.tar [default]
```
