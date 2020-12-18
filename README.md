


# DAC8551

Arduino library for DAC8551 SPI Digital Analog Convertor

## Description

not tested extensively

## Interface

- **DAC8551(uint8_t slaveSelect)** Constructor for hardware SPI, 
since 0.2.0 the slaveSelect pin needs to be defined.
- **DAC8551(uint8_t spiData, uint8_t spiClock, uint8_t slaveSelect)** Constructor for the software SPI
- **void begin()** initializes all pins to default state
- **void setValue(uint16_t value)** set the value of the channel
- **uint16_t getValue()** returns the last value written
- **void setPowerDown(uint8_t powerDownMode)** sets power down mode. 0 - 3,
check datasheet for details.
- **uint8_t getPowerDownMode()** returns last written mode.

| Power down mode         | Value |
|:------------------------|:-----:|
| DAC8551_POWERDOWN_NORMAL   | 0 |
| DAC8551_POWERDOWN_1K       | 1 |
| DAC8551_POWERDOWN_100K     | 2 |
| DAC8551_POWERDOWN_HIGH_IMP | 3 |


## Operation

See examples

**demo_hw_spi.ino**
- write a sawtooth to channel A followed by a sinus 
- uses HW SPI

**demo_sw_spi.ino**
- write a sawtooth to channel A followed by a sinus 
- uses SW SPI

**demo_powerdown.ino**
- idem

## TODO

more testing
