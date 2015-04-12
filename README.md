# daeyun-gentoo-overlay

### Add the overlay

#### Option 1: Using Layman

Install Layman

```
emerge layman
echo 'source /var/lib/layman/make.conf' >> /etc/make.conf
```

Add the overlay

```
layman -o https://github.com/daeyun/daeyun-gentoo-overlay/raw/master/overlay.xml -f -a daeyun
layman -S
```

#### Option 2: Local Overlay

https://wiki.gentoo.org/wiki/Overlay/Local_overlay

```
git clone git@github.com:daeyun/daeyun-gentoo-overlay.git
echo 'PORTDIR_OVERLAY="/path/to/daeyun-gentoo-overlay ${PORTDIR_OVERLAY}"' >> /etc/portage/make.conf
```
