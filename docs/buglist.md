For more detail and reproduction of the vulnerabilities, download the [log report](https://github.com/Rtkaller/Rtkaller/tree/main/docs/crashes)

| RTOS Version         | Real-time Patch     | Vulnerability Type       | Module                                  | Rtkaller | Syzkaller | Pervious Unknown |
|----------------------|---------------------|--------------------------|-----------------------------------------|----------|-----------|------------------|
| FreeRTOS-5.4.2       |                     | SIGSEGV                  | task/xTaskIncrementTick                 | ✓        |           | ✓                |
| rt-linux-5.0-release | patch-5.0.7-rt4-rt5 | general protection fault | rbtree/rb\_insert\_color\_cached        | ✓        |           | ✓                |
| rt-linux-5.6-ktsan   | patch-5.6.4-rt2-rt3 | kernel-panic             | mm/alloc\_pages\_nodemask               | ✓        | ✓         |                  |
|                      |                     | stack segment fault      | mm/freelist\_dereference                | ✓        |           | ✓                |
| rt-linux-5.6-release | patch-5.6-rt1       | kernel-panic             | net/crda\_timeout\_work                 | ✓        |           | ✓                |
|                      |                     | kernel-panic             | fs/set\_bit                             | ✓        | ✓         |                  |
|                      |                     | kernel-panic             | asm/scr\_memmovew                       | ✓        | ✓         |                  |
| rt-linux-5.4-release | patch-5.4.3-rt1     | use-after-free           | tty/tty\_ioctl                          | ✓        | ✓         |                  |
|                      |                     | stack-overflow           | kernels/swapgs\_restore\_regs           | ✓        |           | ✓                |
|                      |                     | stack-overflow           | drivers/perf\_event\_open               | ✓        |           | ✓                |
|                      |                     | slab-out-of-bounds       | drivers/vcs\_scr\_readw                 | ✓        |           | ✓                |
|                      |                     | NULL-ptr deref           | drivers/do\_con\_write                  | ✓        | ✓         |                  |
|                      |                     | general protection fault | net/devinet\_sysctl\_unregister         | ✓        |           | ✓                |
|                      |                     | deadlock                 | kernel/relay\_alloc\_buf                | ✓        |           | ✓                |
| rt-linux-5.9-release | patch-5.9-rc7-rt10  | use-after-free           | tty/vc\_con\_write\_normal              | ✓        |           | ✓                |
|                      |                     | use-after-free           | drivers/vc\_uniscr\_check               | ✓        |           | ✓                |
|                      |                     | kernel-panic             | kernel/alloc\_pages\_nodemask           | ✓        |           | ✓                |
|                      |                     | deadlock                 | include/page\_cache\_alloc              | ✓        |           | ✓                |
|                      |                     | deadlock                 | kernel/mm\_alloc\_pgd                   | ✓        |           | ✓                |
|                      |                     | deadlock                 | kernel/dup\_task\_struct                | ✓        |           | ✓                |
|                      |                     | slab-out-of-bounds       | tty/do\_update\_region                  | ✓        |           | ✓                |
|                      |                     | general protection fault | include/vma\_interval\_tree\_iter\_next | ✓        |           | ✓                |
|                      |                     | use-after-free           | drivers/clear\_buffer\_attributes       | ✓        |           | ✓                |
|                      |                     | use-after-free           | asm/scr\_memcpyw                        | ✓        | ✓         |                  |
|                      |                     | kernel-panic             | drivers/vc\_uniscr\_alloc               | ✓        | ✓         |                  |
| rt-linux-5.2-release | patch-5.2-rt1       | Bad page map             | lib/systemd\_udevd                      | ✓        |           | ✓                |
|                      |                     | Bad page map             | lib/vsnprintf                           | ✓        |           | ✓                |
|                      |                     | Bad rss-counter state    | mm/handle\_mm\_fault                    | ✓        | ✓         |                  |
|                      |                     | Bad rss-counter state    | kernel/rt\_spin\_lock                   | ✓        | ✓         |                  |
|                      |                     | general protection fault | mm/unlink\_anon\_vmas                   | ✓        | ✓         |                  |
|                      |                     | kernel-panic             | net/xfrm\_policy\_insert\_list          | ✓        | ✓         |                  |
|                      |                     | kernel-panic             | net/restore\_regulatory\_settings       | ✓        |           | ✓                |
|                      |                     | NULL-prt deref           | mm/anon\_vma\_fork                      | ✓        |           | ✓                |
|                      |                     | NULL-prt deref           | mm/anon\_vma\_interval\_tree\_insert    | ✓        |           | ✓                |
|                      |                     | NULL-ptr deref           | net/cleanup\_net                        | ✓        | ✓         |                  |
|                      |                     | NULL-ptr deref           | mm/qlist\_free\_all                     | ✓        | ✓         |                  |
|                      |                     | possible system lock     | kernel/swake\_up\_all\_locked           | ✓        |           | ✓                |
|                      |                     | slab-out-of-bounds       | lib/vsnprintf                           | ✓        |           | ✓                |
|                      |                     | use-after-free           | mm/slab\_post\_alloc\_hook              | ✓        |           | ✓                |
|                      |                     | use-after-free           | drivers/con\_scroll                     | ✓        | ✓         |                  |
|                      |                     | use-after-free           | drivers/csi\_J                          | ✓        | ✓         |                  |
|                      |                     | use-after-free           | drivers/con\_shutdown                   | ✓        | ✓         |                  |
|                      |                     | use-after-free           | drivers/vgacon\_scroll                  | ✓        | ✓         |                  |
|                      |                     | use-after-free           | drivers/complement\_pos                 | ✓        |           | ✓                |
|                      |                     | use-after-free           | drivers/screen\_glyph\_unicode          | ✓        | ✓         |                  |
|                      |                     | use-after-free           | drivers/vcs\_scr\_writew                | ✓        | ✓         |                  |
|                      |                     | use-after-free           | drivers/vgacon\_invert\_region          | ✓        | ✓         |                  |
|                      |                     | use-after-free           | net/xfrm\_policy\_unlink                | ✓        | ✓         |                  |
|                      |                     | use-after-free           | fs/ext4\_xattr\_set\_entry              | ✓        | ✓         |                  |
|                      |                     | use-after-free           | fs/ext4\_expand\_extra\_isize           | ✓        | ✓         |                  |
|                      |                     | use-after-free           | drivers/n\_tty\_receive\_buf\_common    | ✓        | ✓         |                  |
|                      |                     | use-after-free           | drivers/n\_tty\_receive\_buf\_common    |          |           |                  |
| rt-linux-3.10        |                     | Null ptr deref           | dev_remove_pack                         | ✓        |           | ✓                |
|                      |                     | Null ptr deref           | intel_shared_reg_put_constraints        | ✓        |           | ✓                |

