# Mosquitto Plugin

A simple way to generate ACL and PASSWORD plugins for usage with the mosquitto
broker.

Requires that mosquitto_plugin.h mosquitto.h files are installed on the system,
on linux systems this is usually achieved through the mosquitto-dev packages.
Not tested on windows.

To pass additional (clang) arguments to the clang invocation from `bindgen`, set
`MOSQUITTO_PLUGIN_CLANG_EXTRA_ARGS` for e.g a special search path for the
mosquitto headers: "-I ../mosquitto-2.0.4/include".

The optional functions are not implemented here.

## Supported

    - ease of access to write own mosquitto plugins
    - auth_opt_<key> value in the mosquitto_conf
    - mutable access to the structure between calls
    - ACL implementations
    - username/password implementatations

## Example usage

There is an example usage in the github repo under "example-acl" folder.
