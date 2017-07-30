.. Copyright © 2014-2017 Martin Ueding <dev@martin-ueding.de>

#######
wlan-qr
#######

Creating a QR code for a wlan access point should not be hard. It was rather
hard to find one that create it offline, though. I think it is ridiculous to
let a web service process *your* wireless *password*. So this uses the program
``qrencode`` to create a QR code for you.

If you want to create it yourself, you just have to create a QR code with the
following contents where you replace ``{ssid}`` with the name of the network
and ``{psk}`` with your pre-shared-key (password)::

    WIFI:S:{ssid};T:WPA;P:{psk};;

To simplify this, I created a Python program which you can use like this::

    wlan-qr SSID PSK output-file-name
