# UART

# Introduction

UART stands for Universal Asynchronous Receiver Transmitter. UART is the combination of hardware used for serial communication between computer and any other peripheral devices. As we know, the processing of data in personal computers or any other peripheral devices is in parallel form as it ensures speed. But the data communication in these systems is in serial form, so first the data in parallel form is to be converted to serial form. To do this process, UART is responsible for breaking parallel data into serial form and again convert it to parallel form at the receiver end.

UART is called ‘Universal’ because the data frame and transmission speed can be configured as per the requirement. And ‘Asynchronous’ as the transmitter and receiver are not synchronized by a clock signal. UART needs two signals rx_data and tx_data. Tx_data is output of the UART and rx_data is input to UART. In UART, it consists of two extra bits start and stop bit. When data is sent ‘start bit’ is inserted at the beginning of the data frame and stop bit is inserted at the end of the data frame. The start bit sends a signal to the receiver telling that the data bits are to be sent and force the clock to synchronize with the transmitter clock.

After adding the start bit, the data bits are sent one by one with first sending LSB and then remaining bits. In receiver, the data bits are counted bit by bit using the counter. After every data bit is received it is converted into parallel form and transmitted to other peripheral devices

![image](https://user-images.githubusercontent.com/63600784/174316546-f1bc64b0-8b31-4c5f-a53f-8106800201d2.png)

The clock synchronization is absent between transmitter and receiver. To synchronize transmitter and receiver start bit and stop bit is used. UART design for FPGA can act as an interface for FPGA based embedded system which used soft core processors. This reduces external routing problems and cost as FPGA contains huge number of logic gates unused. Using FPGA can be good solutions for reconfiguration of the hardware devices.

# Transmitter FSM

![Transmitter FSM](https://user-images.githubusercontent.com/63600784/174316768-614bae37-1688-400b-900e-4f07aa16f694.png)

# Receiver FSM

![Receiver FSM](https://user-images.githubusercontent.com/63600784/174316800-146e112a-82bc-4ed6-98bb-0bd7d4036319.png)

# Transmitter Simulation Output

![Transmitter Simulation Output](https://user-images.githubusercontent.com/63600784/174316836-013534a7-043e-403b-be10-257b72606fdc.png)

# Receiver Simulation Report

![Receiver Simulation Output](https://user-images.githubusercontent.com/63600784/174316877-576ddbb8-9950-4f2e-86ad-c8685e49b3ac.png)
