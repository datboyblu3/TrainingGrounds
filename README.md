# TrainingGrounds
This repo contains my notes/walkthroughs of practice boxes from vulnhub and hackthebox

# Run Vulnhub Boxes on M1/M2 Macbooks

### Convert vmdk to qcow2
```JavaScript
qemu-img convert -p -O qcow2 Sample-TEST.vmdk Sample-TEST.qcow2
```

1. Open UTM and select Emulate
2. Select other and ensure "Skip ISO Boot" is selected
3. Choose x86_64 or 32bit for your VM, the amount of RAM and CPU Cores 
4. Select or leave the size of the drive
5. Name your VM
6. Select your VM from the left panel and then select the settings in the upper right corner
7. Under "Drives" select "IDE Drive" and delete it
8. Select "New Drive" and click Import
9. Select the converted drive. It should have the *.qcow* extension
10. When complete, select QEMU from the left pane, under Tweaks, uncheck "UEFI Boot" and save it
11. Now run the VM
