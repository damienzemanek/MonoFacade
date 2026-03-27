# MonoFacade

Monobehaviour facade architecture system with generic type composition, immutable context delivery, blackboard linked runtime state, 
plug-and-play functionality modules, optional FSM design, explicit bind/unbind authority for easy input swapping.

## 💻 Technologies Used

- C#
- Unity3D

# 💎 Features
1. Easily create new facades with the inspector facing `Facade Generator`
2. Separates static configuration with `Config`, Blackboard references and data with `Blackboard`, and transient state context with `ContextData` & `ContextProvider` for clear SRP
3. Modular `Functionality` layer where behaviour is added as a module and composed before runtime
4. Seperate Functionality Modules types
   a. `UnboundFunctionality` for modules that are not invoked via an event
   b. `BoundFunctionality` for modules invoked via an event
   c. `BoundSetFunctionality` for modules that are invoked via an event and receive data
5. Unity Player Loop compatability with `TickFM` execution channels routed through functionality modules
6. Optional `FSM` Integration: Easily create States with pre-existing Functionailty modules just by adding `FSM_ON_ENTER` or `FSM_ON_EXIT` interaface labels
7. Easily create transitions between FSM modules
