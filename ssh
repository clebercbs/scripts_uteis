from netmiko import ConnectHandler
import sys
import os, re

lista = open(b"hosts","r")

for item in lista:
    Network_Device = {"host": item, 
                  "username": "admin",
                  "password": "admin",
                  "device_type": "cisco_ios",
                  "secret": "admin",
                  }

    Connect = ConnectHandler(**Network_Device)
    Connect.enable()

    To_Issue = "Show cdp neighbor"
    arquivo = open("vizinhos", "a")
    arquivo.write(Connect.send_command(To_Issue))
