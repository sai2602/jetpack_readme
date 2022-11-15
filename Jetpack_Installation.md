# Setting up jetson with emmc
1. Download [nvidia sdk manager](https://docs.nvidia.com/sdk-manager/download-run-sdkm/index.html) and run it. It will open default in STEP 01 (The SDK manager opens a default tab to create an account  with NVIDIA for first time login).
2. Connect the nvidia board to the PC via an USB-B cable and to the internet via ethernet cable (ethernet cable is also needed since the sdk manager uses ssh to update sdk components).
3. After the board is connected to the PC, the sdk manager will automatically detect the connect board (if it doesn't, hit refresh in the "Target Hardware" section).
4. Select the necesssary information in STEP 01 (like the jetpack version, additional sdks) and continue to STEP 02.
5. In STEP 02, at the bottom, there is an option to select download directories. Select locations that have sufficient space (needs about 20GB of space). Agree to the terms and conditions and hit continue to STEP 03.
6. The downloading and installation of dependent components and the image creation should now start.
7. When the sdk manager is ready to start the flashing of the image, a pop-up with automatic or manual flashing comes up. Select manual (since it is the first time jetpack is being flashed) and follow the steps provided by the sdk manager and select flash. (username: anavs, password: anavsisp).
8. To install the CUDA components, the sdk manager needs the jetson's IP address to establish an ssh connection. Connect the jetson to a monitor, keyboard, and mouse. In a terminal, type ifconfig to get the jetson's IP address. After providing the IP address with the credentials, the installion should now complete.
9. Once the jetson is up and running, [port root to M.2 SSD](https://www.forecr.io/blogs/bsp-development/changing-storage-of-the-root-file-system-emmc-to-m-2-ssd) and the system should now boot with the root folder on the external SSD with more space for package installations.
