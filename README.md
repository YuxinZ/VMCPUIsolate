# VMCPUIsolate
Patches from community to isolate VM CPU eliminating unnecessary VMexit

Base 3.6-rc4

Patches 1~21 (KVM: x86: CPU isolation and direct interrupts delivery to guests)
https://lkml.org/lkml/2012/9/6/148

patch 30~33 to avoid parallel module loading exhausting percpu var memory.
without these patches, kvm load will fail with "PERCPU: allocation failed"
These patches are merged with minor modification.
	0d21b0e3477 module: add new state MODULE_STATE_UNFORMED.
 	1fb9341ac34 module: put modules in list much earlier.
  
