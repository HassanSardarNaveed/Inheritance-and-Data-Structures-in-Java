# Homework 1: Vehicle Inheritance and Testing

## Overview

In this assignment, we implemented a basic object-oriented design for vehicles using Java. The main objectives were to:
1. Create a base class `Vehicle` and extend it with subclasses `Car` and `Bike`.
2. Define and test various functionalities of these classes, including refueling, running, and calculating gas consumption.
3. Implement unit tests to ensure that the classes function as expected.

## Classes

### `Vehicle`
The `Vehicle` class is the superclass representing a general vehicle. It includes:
- **Attributes**:
  - `String brand`: The brand of the vehicle.
  - `int year`: The manufacturing year of the vehicle.
  - `int currYear`: The current year.
  - `int gasRemaining`: The amount of gas remaining in the vehicle.
  - `int totalGasConsumed`: The total amount of gas consumed by the vehicle.

- **Methods**:
  - `int getAge()`: Returns the age of the vehicle.
  - `void refuel(int amount)`: Refuels the vehicle.
  - `void run(int hours)`: Simulates running the vehicle and consumes gas.
  - `int getGasRemained()`: Returns the remaining gas.
  - `int getTotalGasConsumed()`: Returns the total gas consumed.
  - `String toString()`: Returns a string representation of the vehicle.

### `Car`
The `Car` class extends `Vehicle` and represents a car. It overrides:
- **Methods**:
  - `void run(int hours)`: Overrides the `run` method to consume gas specific to cars.

### `Bike`
The `Bike` class extends `Vehicle` and represents a bike. It overrides:
- **Methods**:
  - `void run(int hours)`: Overrides the `run` method to simulate running a bike without gas consumption.

## Testing

We used JUnit 5 for testing the functionalities of the `Vehicle`, `Car`, and `Bike` classes.

### Tests Implemented
- **`testVehicle()`**: Verifies the correct initialization of vehicle attributes.
- **`testGetAge()`**: Tests the calculation of vehicle age.
- **`testGetGasRemained()`**: Tests the refueling and gas remaining logic.
- **`testGetTotalGasConsumed()`**: Tests the total gas consumption logic.
- **`testRefuel()`**: Tests the refueling functionality for various cases.
- **`testRun()`**: Tests the running functionality for different scenarios.
- **`testEquals()`**: Tests the equality comparison between vehicles.
- **`testToString()`**: Verifies the string representation of vehicles.

## How to Run the Tests

1. **Compile the Classes**:
   ```sh
   javac -d bin src/transportation/*.java
