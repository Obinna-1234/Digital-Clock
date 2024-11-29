# 🕒 Digital Clock ⏰  
[![Live Demo](https://img.shields.io/badge/Live-App-blue?style=flat-square)](https://obinna-1234.github.io/Digital-Clock/)

👉 **[Try the app live here!](https://obinna-1234.github.io/Digital-Clock/)** 👈  

---

## 📸 Preview  
![Digital Clock](https://github.com/Obinna-1234/Digital-Clock/blob/main/clock.png)

*Clean, minimalistic, and always on time.*

---

## 🌟 Features  
- **Real-Time Updates**: Displays the current hour, minute, and second dynamically.  
- **AM/PM Toggle**: Adjusts based on the 12-hour clock system.  
- **Lightweight**: Built with only JavaScript, HTML, and CSS.

---

## 🛠️ How This Works  

### Core JavaScript Code:
```javascript
const hourE1 = document.getElementById("hour");
const minuteE1 = document.getElementById("minute");
const secondE1 = document.getElementById("second");
const ampmE1 = document.getElementById("ampm");

function updateClock() {
    // Get the current time values.
    let h = new Date().getHours(); // Fetches the current hour.
    let m = new Date().getMinutes(); // Fetches the current minute.
    let s = new Date().getSeconds(); // Fetches the current second.
    let ampm = "AM"; // Default value for AM/PM indicator.

    // Convert 24-hour time to 12-hour time and set AM/PM.
    if (h > 12) {
        h = h - 12;
        ampm = "PM";
    }

    // Add a leading zero for single-digit hours, minutes, and seconds.
    h = h < 10 ? "0" + h : h;
    m = m < 10 ? "0" + m : m;
    s = s < 10 ? "0" + s : s;

    // Update the DOM elements with the time values.
    hourE1.innerText = h;
    minuteE1.innerText = m;
    secondE1.innerText = s;
    ampmE1.innerText = ampm;

    // Refresh the clock every second.
    setInterval(() => {
        updateClock();
    }, 1000);
}

// Initialize the clock.
updateClock();
'''
# Key Breakdown:

- **Accessing DOM Elements**:  
  - `getElementById()` fetches HTML elements by their `id` attributes: `hour`, `minute`, `second`, and `ampm`.

- **Getting Current Time**:  
  - `new Date()` retrieves the current system time.  
  - `getHours()`, `getMinutes()`, and `getSeconds()` extract hour, minute, and second values.

- **24-Hour to 12-Hour Conversion**:  
  - If the hour (`h`) is greater than 12, subtract 12 to fit the 12-hour format. Assign "PM". If not, it's "AM".

- **Adding Leading Zeros**:  
  - Single-digit hours, minutes, or seconds are padded with a zero for consistent formatting using a ternary operator.

- **Updating the UI**:  
  - `innerText` dynamically updates the content of the elements to show the current time values.

- **Refreshing the Clock**:  
  - `setInterval()` ensures the `updateClock()` function runs every second (1000 ms).

---

## 🚀 How to Use:

1. **Clone the Repository**:  
   ```bash
   git clone https://github.com/Obinna-1234/Digital-Clock.git

2. **Navigate to the Folder and Open the App**:  
   ```bash
   cd Digital-Clock

3 **Open the App**

Open the `index.html` file in your browser, or deploy it to your favorite hosting platform.

🙏 Credits:
Developed with 💻 and ❤️ by Obinna-1234.
Have feedback or ideas? Feel free to open an issue.
