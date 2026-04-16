# Quad Flight Controller

A custom quadcopter project built around a handmade frame, an Arduino-based flight controller, and a wireless handheld controller.

## Overview

This project was an attempt to build a functioning quadcopter flight controller from scratch using low-cost hardware. The quadcopter used a handmade wooden frame, four 2400KV brushless motors, and an Arduino Nano paired with an MPU6050 IMU.

Control input was sent from a separate handmade controller over an RF transceiver link.

## Hardware

- Arduino Nano flight controller
- MPU6050 IMU
- RF transceiver module
- 4x 2400KV brushless motors
- Handmade wooden frame

## What It Does

- Reads orientation data from the IMU
- Receives wireless control input from a custom handheld controller
- Drives the motors for basic stabilization and flight testing

## Repository Structure

- `before PID tuning` — early flight-control program with IMU input, RF controller input, and X/Y PID-based motor mixing
- `controller interfacing` — flight-control variant focused on integrating controller input with full PID-based stabilization
- `first test` — early full-system flight test combining IMU input, controller input, arming logic, PID stabilization, and ESC output
- `hover` — hover-focused stabilization test using IMU feedback and fixed throttle
- `mpulight` — MPU6050 test program for initialization, calibration, and serial angle output
- `PID` — standalone PID control experiment used for tuning and testing control behavior
- `remote` — RF communication test/program for receiving controller joystick data
- `settings.py` — configuration file
- `README.md` — project overview

## Results

The project achieved unstable vertical flight. Yaw control was poor because of low-quality IMU readings, and the overall platform was limited by both the sensor quality and the mechanical build.

## Status

Concluded.

## Future Work

- Replace the IMU with a better sensor
- Improve frame rigidity and mechanical balance
- Refine control tuning and filtering

---

**Note:** This README was AI-generated with my input and review. All other project work is my own.
