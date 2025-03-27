# Customized Airthings BLE integration for Home Assistant

This is the Home Assistant core integration for Airthings BLE (core version 2025.3.4) with an additional 
retry mechanism as a workaround for connection failures.

## Usage

Copy the airthings_ble_custom folder to the custom_components folder of your Home Assistant installation 
and restart the system. After the restart, the custom integration should have replaced the default core
integration. Delete the uploaded folder to restore the default core integration.

## The workaround

The integration will retry to fetch data from coupled devices after a connection error with a 5 second delay between each attempt. When 10 attempts have failed, the integration raises an exception.