# User Guide

## Introduction

Welcome to the Unity Finite State Machine (FSM) Tool usage guide. This document provides detailed information on the various types of nodes available in the FSM tool and outlines the features of the tool to help you get started with creating and managing FSMs in your Unity projects.

## Types of Nodes

The FSM tool includes several types of nodes, each serving a specific purpose within the state machine. Understanding these nodes is crucial for effectively using the tool.

### FsmStateNode

**Description:**  
The FsmStateNode represents a state within the FSM. It initializes the node with a name and position and sets the type of node as a state.

**Features:**
- **Predefined States:** Includes states such as Idle, Patrol, Chase, Flee, Attack, and Search.
- **Custom Variables:** Displays variables specific to the state for customization.
- **Animation Override:** Allows overriding an animation to run while the state is active.
- **Hit State Override:** Modifies global enemy values during this state.
- **Unique Instance:** Only one instance of a state behavior can exist simultaneously.
- **Connections:** Can receive multiple connections from non-action nodes and can only connect to condition nodes.

### FsmCustomStateNode

**Description:**  
The FsmCustomStateNode allows for custom behavior by attaching any scene component and selecting its functions to execute during the state.

**Features:**
- **Component Selection:** Add any component from the scene and choose a function to execute.
- **Animation and Hit State Override:** Similar to FsmStateNode.
- **Unique Instance:** Only one instance of a state behavior can exist simultaneously.
- **Connections:** Can receive multiple connections from non-action nodes and can only connect to condition nodes.

### FsmVariableNode

**Description:**  
The FsmVariableNode is used to override the value of a variable when connected to another state.

**Features:**
- **Variable Override:** Change the value of a variable for connected states.
- **Connections:** Can only connect to other states.

### FsmTransitionNode

**Description:**  
The FsmTransitionNode manages transitions between states based on specified conditions.

**Features:**
- **Conditions:** Includes conditions based on distance, direct vision, health, noise, and a default forward execution condition.
- **Connections:** Can connect to both states and conditions.
- **Repeatable:** Can be used multiple times with different values.

### FsmDualTransitionNode

**Description:**  
The FsmDualTransitionNode is similar to FsmTransitionNode but has two output ports for true and false conditions.

**Features:**
- **Dual Conditions:** Allows different behaviors based on whether the condition is true or false.
- **Connections:** Can connect to both states and conditions.
- **Repeatable:** Can be used multiple times with different values.

### FsmCustomTransitionNode

**Description:**  
The FsmCustomTransitionNode allows for custom transitions by selecting functions from scene components to execute during the transition.

**Features:**
- **Component Selection:** Add any component from the scene and choose a function to execute.
- **Custom Conditions:** Similar to FsmDualTransitionNode but with custom component functions.

### FsmInitialNode

**Description:**  
The FsmInitialNode marks the starting point of the FSM.

**Features:**
- **Initial State:** Defines the initial state when the FSM is initialized.
- **Unique Instance:** Only one initial node can exist in each FSM graph.
- **Automatic Creation:** Created automatically and cannot be deleted.

### FsmExtensionNode

**Description:**  
The FsmExtensionNode is used for organizing the graph visually.

**Features:**
- **Visual Organization:** Helps in arranging the graph and its connections for better clarity.
- **Creation:** Created by clicking the middle mouse button on a connection line.

## Features of the Unity FSM Tool

The Unity FSM Tool provides several features designed to streamline the creation and management of finite state machines within Unity.

### Visual Editor

**Description:**  
The visual editor offers a user-friendly interface for designing FSMs. It allows users to create, connect, and configure nodes using a drag-and-drop system.

**Features:**
- **Node Creation:** Easily create and place nodes on the canvas.
- **Connections:** Draw connections between nodes to define transitions.
- **Configuration:** Configure node properties and conditions directly within the editor.

### Serialization and Deserialization

**Description:**  
The tool supports saving and loading FSM configurations, allowing for persistent FSMs across sessions.

**Features:**
- **Save FSM:** Save the current FSM configuration to a file.
- **Load FSM:** Load an FSM configuration from a file.

### Inspector Integration

**Description:**  
The tool integrates with the Unity Inspector, allowing for seamless editing of FSM properties.

**Features:**
- **Property Fields:** Edit FSM properties directly in the Inspector.
- **Live Updates:** See real-time updates to FSM configurations within the Inspector.

### Debugging Tools

**Description:**  
Debugging tools help identify and fix issues within the FSM.

**Features:**
- **State Tracking:** Monitor the current state and transitions during runtime.
- **Condition Evaluation:** Evaluate and display condition results to ensure they work as expected.

### Scripting API

**Description:**  
The FSM tool provides a scripting API for advanced users who prefer to configure FSMs programmatically.

**Features:**
- **Create States and Transitions:** Programmatically create and connect states and transitions.
- **Access FSM Properties:** Access and modify FSM properties through code.
