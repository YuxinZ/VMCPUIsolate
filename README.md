# VMCPUIsolate
Patches from community to isolate VM CPU eliminating unnecessary VMexit

Patches 1~21 (KVM: x86: CPU isolation and direct interrupts delivery to guests)
https://lkml.org/lkml/2012/9/6/148

patch 22 make following two patches to work

patch 23/24 to avoid parallel module loading exhausting percpu var memory.
without these patches, kvm load will fail with "PERCPU: allocation failed"
	0d21b0e3477 module: add new state MODULE_STATE_UNFORMED.
  1fb9341ac34 module: put modules in list much earlier.
  
