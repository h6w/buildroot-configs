# buildroot-configs
Useful Buildroot Defconfigs not included in the normal release

# VirtualBox disk configs (with Xorg, nodm, and openbox)
x86_64-efi

After building, convert the disk image to a vdi with:
VBoxManage convertfromraw output/images/disk.img output/images/disk.vdi

If you have rebuilt the disk image, it won't match the UUID kept in your Virtualbox database, so get it from the error box and update it with:
VBoxManage internalcommands sethduuid "/full/path/to/buildroot/output/images/disk.vdi" [UUID]
