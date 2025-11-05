# 2CS-Project-Integration 🤖

A comprehensive distributed robotics control system developed as a team project, featuring real-time control, computer vision, and system monitoring capabilities.

## 📦 Project Components

| Component | Role | Technologies | Repository |
|-----------|------|--------------|------------|
| **Main Control Application** | Central GUI & system coordinator | Python, Threading | [:link: View Repository](https://github.com/7afidhou/2CS_Project_Full-Robot-Control-App) |
| **Robotic Arm Control** | Inverse kinematics & servo control | Python, Robotics, GPIO | [:link: View Repository](https://github.com/7afidhou/2CS_Project_Arm-code) |
| **Vehicle Control System** | Navigation & motor control | Python, Motor Drivers, PWM | [:link: View Repository](https://github.com/7afidhou/2CS_Project_Car-control-code) |
| **Live Streaming Module** | Real-time video & computer vision | Python, OpenCV, Streaming | [:link: View Repository](https://github.com/7afidhou/2CS_Project_Livestream-code) |
| **System Monitoring** | Hardware health & status monitoring | Python, System Monitoring | [:link: View Repository](https://github.com/7afidhou/2CS_Project_RaspberryPi-status-code) |

## 🏗️ System Architecture

```mermaid
graph TB
    subgraph "User Interface Layer"
        GUI[Main Control App<br/>GUI]
    end

    subgraph "Control Layer"
        ARM[Robotic Arm Controller<br/>Inverse Kinematics]
        VEH[Vehicle Controller<br/>Navigation]
        STR[Live Streaming<br/>Computer Vision]
    end

    subgraph "Hardware Layer"
        HW1[Robotic Arm<br/>Servo Motors]
        HW2[Vehicle Base<br/>DC Motors]
        HW3[Cameras<br/>Sensors]
        HW4[Raspberry Pi<br/>Compute Unit]
    end

    subgraph "Monitoring Layer"
        MON[System Monitoring<br/>Health & Status]
    end

    GUI --> ARM
    GUI --> VEH
    GUI --> STR
    
    ARM --> HW1
    VEH --> HW2
    STR --> HW3
    
    HW4 --> MON
    HW1 --> MON
    HW2 --> MON
    HW3 --> MON
    
    MON --> GUI

```
## 🔄 System Workflow
User Input → Main Control App receives commands via GUI

Command Distribution → Control app routes commands to appropriate subsystems

Hardware Execution → Arm/Vehicle/Streaming modules control physical hardware

Real-time Feedback → System monitoring collects status data

Visual Feedback → Live streaming provides video feedback to user

Status Updates → All components report back to main control app

## 🎯 Key Technical Features

### Integrated Control Architecture
- Distributed system design with modular components

- Real-time inter-process communication

- Fault-tolerant error handling

- State synchronization across subsystems

### 🦾 Advanced Robotic Arm System
- Inverse kinematics algorithms for precise positioning

- Servo motor control with smooth trajectory planning

- Coordinate space transformations

- Collision avoidance and safety limits

### Intelligent Vehicle Navigation
- Differential drive control for precise movement

- Motor PWM management and speed control

- Sensor integration for environmental awareness

- Path execution and odometry tracking

### Computer Vision Pipeline
- Multi-camera streaming infrastructure

- Real-time video processing with OpenCV

- Frame synchronization and buffering

- Visual feedback for operational awareness

### System Health Monitoring
- Resource utilization tracking (CPU, memory, temperature)

- Hardware status monitoring and alerting

- Performance metrics collection

- Log aggregation and analysis
