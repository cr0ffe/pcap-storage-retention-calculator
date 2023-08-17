# pcap-storag-retention-timeline-calculator.html

## Overview
This HTML file provides a user interface and functionality to calculate storage requirements based on various user inputs.

## User Input Components

- **Customer Name**: A text input for the user to enter a customer name.
  
- **Rate Input**: A text input for the user to enter a rate in Gbps.

- **Utilization Input**: A text input for the user to enter a utilization percentage.

- **Compression Options**: A series of checkboxes that allow the user to select different levels of estimated encrypted traffic, from 10% to 70%. There's also a checkbox to indicate whether compression calculations should be skipped.

- **Duplex Mode**: Two checkboxes to select between full-duplex and half-duplex modes.

- **File Transfer Rate**: A dropdown to select the rate of file transfer, either "Normal" or "High".

- **RAID Configuration**: A dropdown to select between two RAID configurations: "2U RAID 5/6" and "4U RAID 5/6".

- **Duration**: A dropdown to select the number of days for which the storage calculation should be performed, ranging from 1 day to 365 days.

- **Calculate Button**: A button that, when clicked, triggers the storage calculation based on the above inputs.

## Calculations

1. **Compression Calculation**: Based on the selected encrypted traffic percentage, a compression multiplier is applied to the total storage calculation.

2. **Duplex Mode**: The total storage can be adjusted based on whether the traffic is full-duplex or half-duplex.

3. **RAID Configuration**: The total storage calculation considers the selected RAID configuration.

4. **Final Storage Calculation**: The total storage required, with considerations for metadata and the selected RAID configuration, is calculated based on the average utilization and the number of days selected. The result is displayed in Petabytes (PB).

5. **Event Calculations**: Estimates for packets per second and events per second are provided based on the average utilization and average packet size.

6. **Save to File**: The calculated results, along with other input details and notes, can be saved to a text file with a filename based on the customer name and the current date.
