import serial
import sys
import bottle



@bottle.route('/arduino/')
def getArduino():
	ser = serial.Serial('/dev/tty.usbserial-A900ceuF',9600)
	a = ser.readline()
	d = {}
	d['val']=a
	return d

@bottle.route('/')
def index():
	return open('index.html','r')
	

bottle.debug(True)
bottle.run(reloader = True )
