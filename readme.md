# Calculator App

## Overview

This project is a simple calculator app developed for Android using Jetpack Compose. The main goal of this project was to learn and understand the process of creating an Android app while exploring the capabilities of Jetpack Compose. The app allows users to perform basic arithmetic operations, such as addition, subtraction, multiplication, and division, in a visually appealing and user-friendly interface.

![Calculator App Demonstration](https://i.gyazo.com/7514a7fbeb766f3489dac5c4d055ecb0.gif)

## Key Learning Points

Throughout the development of this project, several key components and concepts were explored and implemented:

1. **Jetpack Compose**: The app was built using Jetpack Compose, a modern and declarative UI toolkit for building native Android apps. Compose simplifies UI development by utilizing a reactive and composable approach.

2. **State Management with ViewModel**: The `CalculatorViewModel` class was utilized for managing the app's state. Jetpack Compose's `mutableStateOf` was used to create reactive state variables, updating the UI automatically when the state changes.

3. **Sealed Classes for Actions and Operations**: The project employed sealed classes to represent different types of actions and operations that the calculator can perform. This allowed for clear and concise handling of user interactions and mathematical operations.

4. **User Interface Design**: The app's user interface was carefully designed to provide an intuitive and visually appealing experience for users. Compose's flexible layout system made it easy to arrange buttons and display elements in a clean and organized manner.

## Files Overview

Here is a brief overview of the key files and their functionalities in the project:

1. **CalculatorViewModel.kt**: This Kotlin class represents the ViewModel of the calculator app. It manages the app's state and handles user interactions and mathematical operations.

2. **CalculatorState.kt**: This Kotlin data class defines the structure of the calculator's state, including the numbers entered and the selected operation.

3. **CalculatorButton.kt**: This Composable function represents a calculator button in the UI. It is customizable and can be reused throughout the app.

4. **Calculator.kt**: This Composable function defines the main calculator UI layout. It displays the numbers, operation symbol, and handles user interactions with the calculator buttons.

5. **MainActivity.kt**: This is the main activity of the Android app. It sets up the app's theme, initializes the ViewModel, and composes the calculator UI.

## How the Components Work Together

1. **ViewModel, State, and Compose**: The `CalculatorViewModel` is responsible for managing the app's state using Jetpack Compose's state management system. The `mutableStateOf` property in the ViewModel holds the current state of the calculator, which consists of the numbers entered and the selected operation. When a user interacts with the UI, such as pressing a button, the ViewModel updates the state, triggering a recomposition of the Composable UI elements.

2. **Calculator Composable**: The `Calculator.kt` file contains the main calculator UI layout, defined as a Composable function. It takes the current state from the ViewModel as a parameter and displays the numbers and operation symbol on the screen. Additionally, it handles user interactions by calling the appropriate functions in the ViewModel when a calculator button is pressed.

3. **CalculatorButton Composable**: The `CalculatorButton.kt` file defines a reusable Composable function for calculator buttons. It takes the button symbol, a modifier, and an onClick lambda as parameters. The `onClick` lambda is called when the button is pressed, and it invokes the corresponding action in the ViewModel.

4. **MainActivity**: In `MainActivity.kt`, the app's theme is set up using the `CalculatorTheme`. The ViewModel is initialized using Jetpack Compose's `viewModel` function. The `Calculator` Composable is then composed, passing the ViewModel's state and the `onAction` lambda, which allows the UI to interact with the ViewModel's actions and update the state accordingly.

## The Use of `@Composable` Annotation

In Jetpack Compose, the `@Composable` annotation is used to indicate that a function is a Composable function. Composable functions are responsible for defining the UI elements and their behavior. When a Composable function is called, Jetpack Compose builds a composition tree, allowing it to efficiently update only the parts of the UI affected by state changes.

The `@Composable` annotation also enables the use of Compose's state management system. Composable functions can read and modify state variables, and any changes to these variables will automatically trigger a recomposition of the affected UI elements.

The use of `@Composable` ensures that the UI remains in sync with the app's state, making it easier to build reactive and dynamic user interfaces. It allows developers to focus on defining the UI components and their interactions, while Compose takes care of efficiently rendering and updating the UI.

## Finally...

Creating this calculator app using Jetpack Compose was a valuable learning experience, providing insights into modern Android app development and UI design. The use of sealed classes for actions and operations, along with the ViewModel for state management, demonstrated effective and organized approaches to building robust applications.
