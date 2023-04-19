#### This Repo contains patches, created Ahmet Deliktas, to bypass all common vm-detection vectors in al-khaser and pafish.

For educational purposes only.

1. 
Hardened kvm for amd svm Linux Gentoo Kernel 5.15.102 with rdtsc exit timer spoofing and locky trick (instant sequence).
It provides a sysctl interface to adjust the rdtsc timer dividers at runtime.
```bash
# sudo sysctl -w rdtsc_timediffdivider=300
# sudo sysctl -w rdtsc_timediffdividersecond = 10
```

2. Spoof Qemu Q35 edk2-ovmf firmware

3. Spoof Qemu serials/identifiers

4. Toggle/Disable Hypervisor Cpu Flag at runtime via Qemu QMP command with:
```bash
# virsh qemu-monitor-command --domain win10 --cmd '{"execute": "toggle-hypervisor"}' 
```
5. Qemu hardened VM conf with vfio for gaming with any Anticheat! (Vanguard untested)

#### Credits:
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
https://github.com/lexi-src/kernel-rdtsc-patch
-for the base rdtsc_interception

https://gitlab.com/DonnerPartyOf1/kvm-hidden/
-for the edk2 spoof patch
-for the base qemu spoof patch
-for the base kvm/qemu toggle hypervisor flag patch

https://gist.github.com/PiMaker/70d01cc27792418e8e14e9b2b442129c
-for the base kvm/qemu hide-hypervisor-QMP-command patch
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

If my repo was able to help you and save your time, please consider donating a Pizza or Coffee worth to my BTC or XMR addr. in my profile!

Feel free to message me. Help requests that don't show any invested time/efforts or huge lack of understanding will get ignored.