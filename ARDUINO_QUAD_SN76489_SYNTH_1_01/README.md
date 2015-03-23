Brian Peters Quad SN76489 Synth ported to Arduino MEGA
================

This is a port from the original and amazing synth from Brian Peters that uses 4 SN76489
The original version is made for Teensy 2.0. Since right now I can't buy one, I decided
to make a port using Arduino MIDI library which you can find here:
http://playground.arduino.cc/Main/MIDILibrary

Original Github and Instructables from Brian Peters can be found here:

Instructables:
http://www.instructables.com/id/Quad-SN76489-Synth/

Github: 
https://github.com/brianmarkpeters/CHIP_BASED_SYNTHESIZERS/tree/master/QUAD%20SN76489%20SYNTH

All the specs you need to know about this synth are explained on his videos

------------------------------------------------------------------------------------------

First of all, I started the porting code for both Arduino UNO and Arduino MEGA, but I found that
UNO doesn't has enough pins for using also MIDI. You can still use it by using UNO's PORTD, but
it's not prepared to be used with MIDI Input interface because RX pin used for this, is used for
sending data to the four SN76489.

Also, I don't explain how to implement the hardware for MIDI Input to Arduino MEGA, because I find
the one from Notes and Volts greatly explained :) Check it out here:

http://www.notesandvolts.com/2015/02/midi-for-arduino-input-test.html

------------------------------------------------------------------------------------------

The code preserves the original code from Brian Peters in case you're curious and/or you get some
trouble. Also the code without being modified is made for MEGA. In case you want to test UNO, you
need to add "//" in front of the lines that are meant to use MEGA's PORTC, and uncomment the UNO
lines meant to use UNO's PORTD. I apologize if this causes any confusion, but I left the UNO 
comments in case someone could mix up ports in some way to make it work without using RX pin.

There's not any schematic drawn, but it's all explained in the big comment at the first part of the
code. Feel free to ask if you have any trouble.

Also, I didn't test the code yet, due to not having the SN76489 chips. But I'll let you know
