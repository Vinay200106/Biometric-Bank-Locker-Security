# Biometric-Bank-Locker-Security

# Overview
This project uses an LPC2148 ARM7 microcontroller, R305 fingerprint module, and I2C EEPROM to implement a two-level authentication system for bank lockers.
A locker will only open if both the password and fingerprint match.

# Features

1.Two-level security: Password + Fingerprint
2.Passwords stored in I2C EEPROM
3.Fingerprint enroll, delete, and search options
4.Edit password and fingerprint via external interrupt
5.DC motor control for locker open/close
6.LCD display and 4x4 keypad for user interaction

# Hardware

1.LPC2148 Development Board
2.R305 Fingerprint Sensor
3.AT24C256 EEPROM (I2C)
4.4x4 Matrix Keypad
5.16x2 LCD
6.L293D Motor Driver + DC Motor
7.Push button for interrupt menu

# 💻 Software Requirements

1.Keil uVision (ARM Compiler)
2.Flash Magic (for flashing code to LPC2148)
3.Embedded C
4.Basic I2C, UART, GPIO, and External Interrupt knowledge

# How It Works

## 1.Unlock Mode
1.User enters User ID
2.Enters 4-digit password (stored in EEPROM)
3.Places finger on R305 sensor
4.If both password and fingerprint match → Locker opens

## 2.Edit Mode (Triggered via External Interrupt Button)

Edit Password:
Ask for User ID
Ask for current password
Set and confirm new password
Save to EEPROM
Edit Fingerprint:
Enroll new fingerprint
Delete specific fingerprint
Delete all fingerprints

## 3.Motor Control

Forward rotation → Locker open
Reverse rotation → Locker close



