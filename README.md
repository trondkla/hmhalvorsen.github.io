# The challenge

1. Connect to the nrf52 Development Kit using the Web Bluetooth API. A good start would be to look at "gatt.js", here you are provided with the tools you need.

2. Change the angle of the servo by sending the correct values using the Web Bluetooth API.

  		SERVO-value: Byte 2, values from 0 - 20.
				   Sets the angle of the servo.
				   
				   Example: Sending the decimal value 10, will make the servo turn to the mean angle.

3. Control the LEDs by sending the correct values using the Web Bluetooth API.

		LED-Value: Byte 1, values from 0 - 255. 
				   This value can turn LEDs on the development board on. 
				   Bit[0] = LED 1 (MSB)
				   Bit[1] = LED 2 
				   Bit[2] = LED 3
				   Bit[3] = LED 4
				   
				   Example: Sending the decimal value 64 (binary 01000000) will turn LED 2 on, the rest will turn off.
				   
4. Control the motor by, you guessed it, sending the correct values using the Web Bluetooth API.

    		MOTOR-direction: Byte 14, values either 1 or 0.
					Sets the direction of motor 1, either forwards or backwards.
					
		MOTOR-speed: Byte 10, values from 0 - 255.
					Sets the rotational speed of the motor. 
					
					0 = Minimum speed (None)
					255 = Maximum speed
					
					Example: Setting MOTOR-direction to 1 and MOTOR-speed to 127 will make 
					Motor 1 turn forwards at half speed.

## Extra challenge (adept)

Make a script that controls the cars used in our bachelor thesis!
