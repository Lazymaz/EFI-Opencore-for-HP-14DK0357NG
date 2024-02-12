Install: You flash an Big sur image onto an usb, then delete the efi file by doing the following:
    - diskpart
    - lis dis
    - sel dis x (x is the flash drive)
    - lis par
    - del par y override (y is the efi partition. Usually, it's called System on diskpart)
    - cre par pri size=500
    - for fs=fat32 quick
    - (Drag and drop the efi files)
    - set id=c12a7328-f81f-11d2-ba4b-00a0c93ec93b

And then boot!
Currently functioning:
    - Keyboard
    - USB Bus
    - Battery
    - you tell me

And the rest doesn't work
TIP: Before booting, change the serial number of the efi file. Use tools mentioned in the opencore wiki. 

To fine-tune the efi folder:
    - diskpart
    - lis dis
    - sel dis x (x is the usb)
    - lis par
    - sel par y (y is the efi partition. Usually, it's called System on diskpart)
    - set id=ebd0a0a2-b9e5-4433-87c0-68b6b72699c7
    - Fine-tune everything
    - set id=c12a7328-f81f-11d2-ba4b-00a0c93ec93b

If you have any recommendations, fork this project!