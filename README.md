# Pick-and-Place Mechanism using Siemens PLC (Ladder Logic)
 
## Project Description

This project demonstrates a **Pick-and-Place Mechanism** using **Siemens PLC** with **Ladder Logic**, featuring 4 outputs and 8 timers. The system is controlled by a single push button input and is designed to automate a sequence of object handling on a conveyor system, ultimately moving the object to transport. The system runs until a predefined cycle count is reached, after which the process stops.

*(Note: Please refer to the PDF provided above, as the image shown below is not clear and may not fully convey the necessary details.)*

https://github.com/user-attachments/assets/bf14cf67-d5f5-4500-ba03-96df0cbc5363

![pick and place robot logic - converted_page-0001](https://github.com/user-attachments/assets/49e42776-747d-4755-bf2c-da4a28e68670)


### Key Components:
- **Single Push Button (I0.0)**: The only input, responsible for starting and controlling the process. 
- **Emergency Button (I0.1)**: Halts all operations immediately when activated.
- **8 Timers**: Ensure proper delays at each stage of the process.
- **4 Outputs (Q0.0 to Q0.3)**: Control different stages of the system.
- **Counter**: Tracks the number of cycles.
- **Equal Comparator**: Ensures that the process stops after the set number of cycles.

### Process Flow:

1. **Push Button Activation**:
   - A single push button initiates the entire process.

2. **Operations via Outputs**:
   - **Q0.0**: The system senses the object and moves the conveyor belt.
   - **Q0.1**: The robot arm picks the object from the conveyor belt and places it into the manufacturing process.
   - **Q0.3**: The robot arm picks the object from the manufacturing line and places it on the output conveyor belt.
   - **Q0.3**: The conveyor belt senses the object and moves it to transport, completing the process.

3. **Timers**:
   - **T1 to T8**: Control various stages of the process, providing appropriate delays for sensing, picking, placing, and transport.

4. **Counter and Cycle Termination**:
   - A **counter** counts the number of cycles.
   - Once the counter reaches the specified count, an **equal comparator** stops the process.

### System Components:
- **Input**:
   - Single Push Button (I0.0)
- **Outputs**:
   - Q0.0: Controls the conveyor belt and senses the object.
   - Q0.1: Controls the robot arm to pick and place the object into the manufacturing process.
   - Q0.3: Controls the robot arm to place the object onto the output conveyor belt.
   - Q0.3: Senses the object and moves it to transport, completing the process.
- **Timers**:
   - T1 to T8: Manage different stages of the operation with time delays.
- **Counter**:
   - C1: Tracks and counts the number of cycles.
- **Equal Comparator**:
   - Ensures the process stops after reaching the specified cycle count.

## How It Works:

1. **Push Button Press**: Starts the pick-and-place operation.
2. **Timers**: Ensure delays at each stage—sensing, picking, placing, and transporting.
3. **Outputs**:
   - **Q0.0**: Senses and moves the conveyor belt.
   - **Q0.1**: Picks and places into the manufacturing process.
   - **Q0.3**: Picks and places the object on the output conveyor belt and moves it to transport.
4. **Counter and Equal Comparator**: Once the process completes a specified number of cycles, the counter stops the system.

---
