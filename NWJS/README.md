We go the following route

package and ship nwjs with graalvm ce latest with a modifyed starter app that exposes

graalvm.*

as api

while also support nativeMessaging via creating a manifest for the nativeMessaging host dynamical 
and manage that files.

file api can be taken from node

## connection patterns
- reuse the nativeMessaging host to pass single messages and start a process for every message
- take the native messaging host as process manager and keep a single server online
- exchange the connection endpoint via the nativeMessaging host and then switch to a native connection method like wss or http3 webrtc
- depending on your needs or reuse the binary protocol of the native messaging host. but remember it has 1mb limit for incoming messages.

## pros
also deployable as browser extension can be seen as boilerplate to code chromium addons that use graalvm as runtime or as aot compiled app.
