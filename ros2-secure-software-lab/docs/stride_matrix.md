# STRIDE Threat Analysis Matrix

| STRIDE Category | Affected Element | Identified Threat | Associated Kinetic Risk |
| :--- | :--- | :--- | :--- |
| **Spoofing** | Topic `/odom` | False odometry data injection over local network. | Trajectory drift, incorrect positioning calculations, and high-speed collision. |
| **Tampering** | Topic `/cmd_vel` | Modification of velocity commands in transit. | Uncontrolled acceleration or sudden turns near obstacles or humans. |
| **Repudiation** | Diagnostic Logs | Deletion or alteration of system error logs. | Inability to perform post-accident forensic auditing. |
| **Info Disclosure** | Topic `/camera/image_raw` | Video stream interception on unencrypted Wi-Fi. | Industrial espionage or privacy violation of the operational environment. |
| **Denial of Service** | ROS Message Bus | Message flooding on the DDS network. | Control loop stalling and loss of emergency stop (E-Stop) commands. |
| **Elevation of Priv.** | Python Node (as `root`) | Remote command injection spawning an interactive shell. | Complete hardware takeover and disabling of safety brakes/interlocks. |