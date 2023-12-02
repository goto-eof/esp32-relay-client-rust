# ESP32 Relay Client (Rust)

This application, developed in Rust programming language, allows to control remotely a relay controlled by an ESP32 device kit. Please check the `Configuration` section to build the project.

# How it works?

The application tries to connect to the WiFi, if the connection fails, then it will retry until it succeeds. After a connection is established, the application downloads the configuration from a remote server. The configuration contains information about the status that should have the device: on or off. So that the relay is disabled or enabled in base of the configuration JSON received by the remote server.

# Configuration

Before you proceed with building the project, you need to rename the `/src/configuration/configuration-sample.rs` to `/src/configuration/configuration.rs`. Then you shall edit the variables in the `configuration.rs` file (WiFi SSID, WiFi Password and Configuration Server Endpoint)

# Run the project on your ESP32 device

```
cargo run
```

# Photo

![relay rust](/images/esp32-relay-client-rust.jpg)

note: not yet tested on an ESP32 device (need to implement some server logic).