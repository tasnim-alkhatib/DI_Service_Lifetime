# ASP.NET Core Dependency Injection Lifetimes 🚀

A practical demonstration of **Service Lifetimes** in ASP.NET Core MVC. This project visualizes how the framework manages object instances through Dependency Injection.

---

## 💡 Concept Overview

In ASP.NET Core, services can be registered with three different lifetimes. This project displays unique `Guids` for each type to show when a new instance is created.

### 1. Transient
* **Behavior:** A new instance is created **every time** the service is requested.
* **Observation:** You will see different IDs even within the same page request.

### 2. Scoped
* **Behavior:** A new instance is created **once per HTTP Request**.
* **Observation:** The ID remains the same throughout a single page refresh but changes when you refresh the page.

### 3. Singleton
* **Behavior:** A single instance is created the **first time** it is requested and lives for the **entire lifetime** of the application.
* **Observation:** The ID stays exactly the same no matter how many times you refresh or open different browsers.

---

## 🛠 Project Structure

* **Interfaces & Services:** Contains `ITransientService`, `IScopedService`, and `ISingletonService` with a shared implementation that generates a `Guid`.
* **Controller:** Injects each service twice to demonstrate instance sharing (or lack thereof).
* **View:** Displays the IDs in a clean, readable dashboard.

---

## 🚀 How to Run

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/tasnim-alkhatib/DI_Service_Lifetime.git]