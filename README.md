# 🌦️ Weather Automation Bot (UiPath)

## 📌 Project Overview
This project is a beginner-to-intermediate level RPA automation built using UiPath Studio.  
The bot takes a city name from the user, fetches weather data from Google, analyzes temperature and weather conditions, and provides intelligent outfit suggestions.

---

## 🎯 Features
- Takes user input (city name)
- Automates Google search
- Extracts temperature and weather condition
- Applies decision logic (Hot / Cold / Rain / Mild)
- Logs execution steps
- Displays final output
- Closes browser after execution

---

## 🛠️ Tech Stack
- RPA Tool: UiPath Studio  
- Automation Type: Web Automation  
- Browser: Microsoft Edge  
- Activities: Input Dialog, Type Into, Click, Get Text, Flowchart, Assign, Log Message, Message Box  

---

## ⚙️ Workflow Logic

### 1. User Input
- Captures city name using Input Dialog  
- Stored in variable: City  

---

### 2. Logging
```
City to scrape: <City>
```

---

### 3. Browser Automation
Search query:
```
"Tomorrow's weather in <City> in degrees Celsius"
```

---

### 4. Data Extraction
- Temperature → Temperature  
- Weather → Weather  

---

### 5. Data Conversion
```vb
TemperatureInt32 = Convert.ToInt32(Temperature)
```

---

### 6. Decision Logic

#### Rain Check
```vb
Weather.ToLower.Contains("rain") OR 
Weather.ToLower.Contains("showers") OR 
Weather.ToLower.Contains("thunderstorm")
```

If true:
```
It's raining, bring an umbrella.
```

---

#### Temperature Check

If Temperature < 15:
```
It's very cold outside, wear a heavy jacket.
```

If Temperature > 25:
```
It's very hot outside, wear a cap and sunglasses.
```

Else:
```
Temperature is mild, bring a light jacket.
```

---

### 7. Final Output
```
The temperature in <City> is <Temp>°C.
Weather is <Condition>.
<Outfit Suggestion>
```

---

### 8. Cleanup
- Browser closes automatically

---

## 🧠 Skills Gained
- UiPath project structure
- User input handling
- Web automation
- Data scraping
- Flowchart logic
- String operations
- Logging and debugging

---

## 🚀 How to Run
1. Open project in UiPath Studio  
2. Install Edge extension  
3. Run workflow  
4. Enter city name  
5. View result  

---

## 📌 Future Enhancements
- Multiple city support  
- Excel integration  
- Email notifications  
- REFramework implementation  

---

## 👨‍💻 Author
Rambharat Patel  
Email: patelrambharat@gmail.com  
LinkedIn: https://www.linkedin.com/in/rambharat-patel-5a208a14b/
