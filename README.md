# Getting Started with Create React App

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).


# MyReact Application

This project is a React-based web application that implements several essential features, including input handling, event handling, navigation, and session management. Below is the detailed documentation of the project and its functionalities.

---

## Features

### 1. Input Fields with Event Handling
- **Description**: Users can enter their `Name` and `Surname` in the input fields. Event handling is implemented using the `onChange` event to dynamically detect and process input changes.
- **Implementation**:
  ```jsx
  <input type="text" name="txt1" onChange={myclickdata} />
  <input type="text" name="txt2" onChange={myclickdata} />
  ```
- **Event Handler**:
  The `myclickdata` function processes the input changes, logs relevant details in the console, and displays an alert message.
  ```jsx
  function myclickdata(e) {
    alert("Button Clicked");
    console.log("Type is " + e.type);
    console.warn("Name is " + e.target.name);
    console.log("Value is " + e.target.value);
  }
  ```

### 2. Button with Click Event
- **Description**: A button component triggers a click event that executes the `myclickdata` function.
- **Code**:
  ```jsx
  <button
    name="btn1"
    value="ImButton"
    onClick={myclickdata}
  >
    ClickMe
  </button>
  ```

### 3. Navigation using React Router
- **Description**: Provides seamless navigation between different components (`Home`, `About`, `Contact`, `Counter`, `CounterHook`, `Countersum`) using `react-router-dom`.
- **Implementation**:
  ```jsx
  <Router>
    <div>
      <Link to="/">Home</Link> |
      <Link to="/about">About</Link> |
      <Link to="/Contact">Contact</Link> |
      <Link to="/Count">Counter</Link> |
      <Link to="/CounterHook">CounterHook</Link> |
      <Link to="/Countersum">Countersum</Link>
    </div>
    <Routes>
      <Route path="/" element={<Home />} />
      <Route path="/about" element={<About />} />
      <Route path="/contact" element={<Contact />} />
      <Route path="/Count" element={<Count />} />
      <Route path="/CounterHook" element={<CounterHook />} />
      <Route path="/Countersum" element={<Countersum />} />
    </Routes>
  </Router>
  ```

### 4. Counter Value and "Sorry" Message Alignment
- **Description**: Ensures proper alignment for the counter value and the "Sorry" message by wrapping them in separate `<div>` elements.
- **Code**:
  ```jsx
  <div style={{ marginTop: "10px" }}>5</div>
  <div style={{ marginTop: "10px" }}>Sorry</div>
  ```
- **Output**:
  - Counter value (`5`) and the "Sorry" message are displayed on new lines below the navigation links.

---

## Prerequisites

Make sure you have the following installed on your system:

- [Node.js](https://nodejs.org/) (v14 or later)
- [npm](https://www.npmjs.com/) or [yarn](https://yarnpkg.com/)

---

## Installation

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd <repository-directory>
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

---

## Usage

1. Start the development server:
   ```bash
   npm start
   ```

2. Open the application in your web browser at `http://localhost:3000`.

---

## Project Structure

```plaintext
├── public/             # Static assets (CSS, JS, images)
├── src/                # Source code
│   ├── components/     # Reusable components
│   ├── App.js          # Main application file
│   ├── index.js        # Entry point
├── package.json        # Project dependencies and scripts
├── README.md           # Project documentation
```

---

## Future Enhancements

- **Styling**: Add custom CSS for a more polished UI.
- **Validation**: Implement input validation for forms.
- **Dynamic Updates**: Enhance the "Sorry" message to reflect real-time data changes.

---

## Contributing

Contributions are welcome! To contribute:

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Commit your changes and push them to your branch.
4. Create a pull request.

---





