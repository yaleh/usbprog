# Due Usbprog

Use `flashrom` tool and `Arduino Pro Mini` to program flash. Based on [serprog-duino](https://gitorious.org/gnutoo-personal-arduino-projects/serprog-duino/source/8856a3ad962b16383ace64d6d977bae34c56af0b:), refer to [Serprog/Arduino flasher](http://www.flashrom.org/Serprog/Arduino_flasher)

## How To

+ Open sketch `due_usbprog`.
+ Upload it to Arduino Pro Mini
+ Use `flashrom` to program flash. [flashrom](http://flashrom)

## Connections

	Arduino DUE						Flash
		10							  CS
	   MOSI						 	 MOSI
	   MISO                          MISO
	    SCK 						  SCK
	 	GND 						  GND
	 	3V 							  3V

## Commands

### Write

	flashrom -p serprog:dev=/dev/ttyACM0:115200 -w w_fw.bin

### Read
	
	flashrom -p serprog:dev=/dev/ttyACM0:115200 -r r_fw.bin


## Supported Device

[More...](http://www.flashrom.org/Supported_hardware#Supported_flash_chips)
