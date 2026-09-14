# Mars Rover Mission Control
## Mission Brief

Your team is working on Mars Rover Mission Control, a software system that remotely controls exploration rovers on Mars.

### System Overview

The rover communicates with Mission Control through a communication link. Engineers must be able to:
- Send movement commands to the rover.
- Receive rover location and health data.
- Detect communication failures.
- Prevent unauthorized commands.
- Automatically place the rover into a safe state when a critical fault is detected.
- Store mission events for later investigation.

### Key Constraints

The system has limited communication bandwidth and a communication delay of several minutes. Therefore, commands cannot simply be sent repeatedly without confirmation.

---

## Engineering Notes

### Initial Requirements

1. The rover shall receive commands from Mission Control and execute valid commands.
2. The rover shall report its current position, battery level, temperature, and communication status.
3. Only authenticated Mission Control operators shall be allowed to issue commands.
4. The system shall reject invalid or unauthorized commands.
5. If the rover detects a critical battery or thermal condition, it shall enter Safe Mode.
6. Mission Control shall receive command execution status.
7. All commands and critical rover events shall be recorded with timestamp and operator ID.
8. The system shall continue operating despite temporary communication interruptions.
9. Command processing should normally complete within 5 seconds after a command is received by the rover.
10. The system should support communication with multiple rovers simultaneously.
