# Julep-Enabled Weather-Based Dining Advisor 🌦️🍽️

This project leverages the **Julep AI client** to create a smart dining recommendation agent that dynamically suggests dishes based on real-time weather conditions and time of day using OpenWeatherMap data.

---

## 📌 Project Purpose

Use Julep's orchestration and LLM capabilities to:

- Query weather using OpenWeatherMap
- Parse results via GPT-4o with custom system instructions
- Deliver curated culinary recommendations

---

## ⚙️ Technologies & APIs

- **Julep AI SDK**: For agent-task orchestration
- **OpenWeatherMap API**: Weather data provider
- **Python**: Scripting and input/output logic
- **GPT-4o**: For natural language processing and culinary reasoning

---

## 🧠 How It Works

### Architecture Overview

```mermaid
graph TD
    A[User Input (City, Time of Day)] --> B[Agent & Task Setup]
    B --> C[Weather Tool Integration via OpenWeatherMap]
    C --> D[Prompt LLM with Weather Data]
    D --> E[Receive Dish Recommendations]
    E --> F[Display to User]
```

---

## 🧾 Step-by-Step Breakdown

1. **Install Julep**
   ```python
   !pip install julep -U --quiet
   ```

2. **Initialize Client**
   - Use a secure API key
   - Set environment to `"production"`

3. **Create Agent**
   - Uses `gpt-4o`
   - Trained for culinary recommendations based on context

4. **Define Task**
   - Weather tool integrates with OpenWeatherMap using your API key
   - LLM prompt crafts a human-like response using:
     - City name
     - Time of day (morning/afternoon/evening)
     - Weather & temperature

5. **Run Execution**
   - Waits up to 30 seconds for task completion
   - Displays dish list, tips, and cooking suggestions

---

## 🖥️ Sample Input & Output

**Input**
```text
City: Tokyo
Time of day: evening
```

**Output**
```text
🍜 Recommended Dishes:
- Hot Ramen
- Grilled Yakitori
- Warm Miso Soup

👨‍🍳 Tips:
- Great time to eat indoors due to rainy weather.
- Serve with hot green tea.
```

---

## 🚀 Running the Script

```bash
python dining_julep_executor.py
```

Ensure `.env` or script contains your:

- Julep API key
- OpenWeatherMap API key

---

## 🔐 Security Notes

- Never expose your API key in shared code
- Use `.env` files for sensitive credentials

---

## 🌱 Future Additions

- UI or chatbot wrapper using Gradio or Streamlit
- Restaurant links via Google Maps API
- Meal plan recommendation history

---

## 📄 License

This project is licensed under the **MIT License**.

---

## 👨‍🍳 Author

Developed by **Subham Agarwal** using the **Julep AI platform** for contextual dining intelligence.
