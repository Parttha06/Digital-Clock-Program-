# ⏰ Digital Clock

A sleek and modern Digital Clock built with HTML, CSS, and JavaScript. Displays the current time in 12-hour format with AM/PM indicator, updating in real-time!

## 📸 Preview

![Digital Clock Demo](<img width="1919" height="1079" alt="Screenshot 2025-12-25 220741" src="https://github.com/user-attachments/assets/8865f58a-5031-457e-9177-619829ce5e35" />
)
> *Add a screenshot of your Digital Clock here!*

## ✨ Features

- 🕐 **12-Hour Format** - Easy-to-read time display with AM/PM
- ⚡ **Real-Time Updates** - Clock updates every second
- 🎨 **Clean Design** - Modern and minimalist interface
- 📱 **Responsive Layout** - Works perfectly on all screen sizes
- 🌟 **Always Accurate** - Syncs with system time

## 🛠️ Built With

- **HTML5** - Structure and layout
- **CSS3** - Styling and visual design
- **JavaScript** - Time logic and real-time updates

## 📂 Project Structure

```
digital-clock/
│
├── index.html          # Main HTML file
├── style.css           # Styling
├── script.js           # Clock logic
└── README.md           # Project documentation
```

## 💻 How It Works

### Clock Logic
```javascript
function updateClock() {
    const now = new Date();
    let hours = now.getHours();
    let minutes = now.getMinutes();
    let seconds = now.getSeconds();
    let ampm = hours >= 12 ? 'PM' : 'AM';
    
    // Convert to 12-hour format
    hours = hours % 12;
    hours = hours ? hours : 12; // 0 should be 12
    
    // Add leading zeros
    hours = hours < 10 ? '0' + hours : hours;
    minutes = minutes < 10 ? '0' + minutes : minutes;
    seconds = seconds < 10 ? '0' + seconds : seconds;
    
    const timeString = `${hours}:${minutes}:${seconds} ${ampm}`;
    document.getElementById('clock').textContent = timeString;
}

// Update every second
setInterval(updateClock, 1000);
updateClock(); // Initial call
```

### Key JavaScript Concepts

- **`new Date()`** - Gets current date and time
- **`getHours()`** - Returns hour (0-23)
- **`getMinutes()`** - Returns minutes (0-59)
- **`getSeconds()`** - Returns seconds (0-59)
- **`setInterval()`** - Executes function repeatedly every 1000ms (1 second)

## 🎯 Getting Started

### Prerequisites
- A web browser (Chrome, Firefox, Safari, etc.)
- A code editor (VS Code, Sublime Text, etc.)

### Installation

1. Clone the repository
```bash
git clone https://github.com/YOUR_USERNAME/digital-clock.git
```

2. Navigate to the project directory
```bash
cd digital-clock
```

3. Open `index.html` in your browser
```bash
# On Windows
start index.html

# On Mac
open index.html

# On Linux
xdg-open index.html
```

Or simply drag and drop the `index.html` file into your browser!

## 🎨 Customization

Personalize your clock:
- **Fonts** - Try digital/LCD style fonts (e.g., "Orbitron", "Digital-7")
- **Colors** - Change text color, background, gradients
- **Size** - Make it bigger or smaller
- **Glow effects** - Add neon glow or shadows
- **Background** - Add images, gradients, or animations
- **Layout** - Center it, add borders, rounded corners

### Popular Font Choices
```css
/* Digital/LCD style */
font-family: 'Orbitron', sans-serif;
font-family: 'Digital-7', monospace;
font-family: 'Audiowide', cursive;

/* Modern clean */
font-family: 'Roboto Mono', monospace;
font-family: 'Space Mono', monospace;
```

## 📚 What I Learned

This project helped me understand:
- ✅ JavaScript Date object and time methods
- ✅ `setInterval()` for repeated execution
- ✅ 12-hour vs 24-hour time conversion
- ✅ String formatting and concatenation
- ✅ DOM manipulation for real-time updates
- ✅ Modulo operator (%) for time conversion
- ✅ Conditional (ternary) operators

## ⏰ Time Format Conversion

### 24-hour to 12-hour conversion:
| 24-hour | 12-hour |
|---------|---------|
| 00:00   | 12:00 AM|
| 01:00   | 01:00 AM|
| 12:00   | 12:00 PM|
| 13:00   | 01:00 PM|
| 23:00   | 11:00 PM|

**Formula**: `hours = hours % 12 || 12`

## 🔮 Future Enhancements

Ideas to level up your clock:
- 📅 **Date Display** - Show day, month, year
- 🌍 **Multiple Time Zones** - Display times from different cities
- ⏱️ **Stopwatch Mode** - Add stopwatch functionality
- ⏲️ **Countdown Timer** - Add timer feature
- 🔔 **Alarm Clock** - Set alarms with notifications
- 🌓 **Day/Night Theme** - Auto-switch based on time
- 🎨 **Format Toggle** - Switch between 12hr and 24hr
- 📊 **Analog Clock** - Add visual analog clock option
- 🌈 **Color Changes** - Different colors for different times of day
- 💾 **User Preferences** - Save format choice in localStorage
- 🗣️ **Voice Announcement** - Speak the time aloud
- 📱 **Full-Screen Mode** - Make it a screensaver
- 🎵 **Chimes** - Play sounds on the hour

## 🌟 Advanced Features Ideas

### Gradient Background by Time of Day
```javascript
function setBackgroundByTime() {
    const hour = new Date().getHours();
    if (hour < 6) return 'night'; // Dark blue
    if (hour < 12) return 'morning'; // Orange/yellow
    if (hour < 18) return 'afternoon'; // Light blue
    return 'evening'; // Purple/pink
}
```

### Multiple Time Zones Display
```javascript
// Show time in different cities
const nyTime = new Date().toLocaleString("en-US", {timeZone: "America/New_York"});
const tokyoTime = new Date().toLocaleString("en-US", {timeZone: "Asia/Tokyo"});
const londonTime = new Date().toLocaleString("en-US", {timeZone: "Europe/London"});
```

## 🎯 Use Cases

Perfect for:
- 🖥️ Desktop widget or screensaver
- 📱 Homepage clock display
- 🏢 Office/workspace decoration
- 📺 TV display mode
- 🎓 Learning JavaScript timing functions
- 🕹️ Base for timer/stopwatch applications

## 🤝 Contributing

Contributions are welcome! Feel free to:
1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is open source and available under the [MIT License](LICENSE).

## 👨‍💻 Author

**Partha Biswas**

- GitHub: [@Parttha06](https://github.com/Parttha06)
- LinkedIn: [Partha Biswas](www.linkedin.com/in/partha-biswass)

## 🙏 Acknowledgments

- Classic digital clock design inspiration
- Built as part of my JavaScript learning journey
- Perfect introduction to working with Date objects and intervals

## ⭐ Show Your Support

Give a ⭐️ if this project helped you keep track of time!

---

<div align="center">
Made with ❤️ and perfect timing by Partha Biswas

⏰ Time well spent! ⏰
</div>
