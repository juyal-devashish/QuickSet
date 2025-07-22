# QuickSet

QuickSet is an AI-powered conversational platform for fast and effortless appointment scheduling. Our goal is to minimize user effort—ideally reducing the process to just a natural language query—by leveraging Large Language Models (LLMs) and real-time API integrations.

---

## 🚀 Goal

To enable users to book appointments with minimal clicks or input, using natural language conversations. QuickSet uses an LLM to: A) Understand user intent, B) Identify the correct type of service, C) Extract all required details and D) Submit the data to external appointment booking APIs. The entire process is automatic, intuitive, and optimized for speed and simplicity.

---

## 💬 Example Flow

```plaintext
User: My brakes are squeaky and I need a check-up sometime this week.  
LLM: Got it. I can book a brake inspection for you. What’s your car make and model?  
User: Honda Accord 2019  
LLM: And your zip code?  
User: 48104  
LLM: Perfect. Let me find the nearest Tires Plus with brake inspection availability this week...  
→ [Books appointment]  
→ [Returns confirmation]
```

---

## Prototype
In our case, the MVP supports two types of appointments – car mechanic service at Tires Plus and hair salon service at a generic salon.

### Car Mechanic Appointments (Tires Plus)

- Business: Tires Plus
- Services: Oil change, tire rotation, brake inspection, wheel alignment, engine diagnostics, etc.
- Intent Mapping: The assistant maps natural language inputs (e.g., “My brakes are squeaky”) to the correct service category (e.g., brake service).
- Required Info:
  - Vehicle make, model, and year
  - User’s location or ZIP code
  - Preferred date and time
- Example:
  ```plaintext
  User: My brakes are squeaky and I need a check-up sometime this week.  
  → Recognized as: Brake Service  
  → Assistant asks: car details, ZIP code, scheduling preferences  
  → Books appointment at nearest Tires Plus

### Hair Salon Appointments

- Services: Haircut, beard trim, hair coloring, wash/blow-dry, etc.
- Simplified Flow: This domain has fewer required inputs and assumes a single salon location.
- Required Info:
  - Service type
  - Preferred date and time
  - Optional: Stylist or barber preference
  - Example:
```plaintext
User: Can I get a beard trim tomorrow afternoon?  
→ Recognized as: Beard Trim  
→ Assistant may ask to confirm time and stylist preference  
→ Books appointment at salon
