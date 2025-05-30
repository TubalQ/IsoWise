# IsoWise 

**IsoWise** is a simple decision tool that helps you determine whether a service should be deployed in a **Virtual Machine (VM)** or a **Linux Container (LXC)** based on its risk score.



## Features

- 🧠 Guided risk assessment (Simple or Advanced mode)
- 🗾️ Logging of every decision by service name
- ⚖️ Smart scoring system with support for "Unsure" answers
- 🔧 Auto-installs `bc` (used for floating-point math)
- 📁 Log files saved in `logs/{service}.log`



## Usage

1. Clone the repo and make the script executable:

   
   git clone https://github.com/TubalQ/isowise.git
   

2. Add permissions


   chmod +x Isowise
   

3. Run the script:

   
   ./Isowise
   

4. Answer the questions (you can type `y`, `n`, or `u` for unsure)

5. A recommendation will be given and saved in `logs/`


## Example Log Entry

🛠️  Service: synapse
📅 Timestamp: 2025-04-22 13:45:02
📊 Mode: Advanced
🧠 Risk score: 3.5
📋 Questions and Answers:
Q: Is the service exposed to the public internet?
A: Yes
Q: Does it store or process personal or sensitive information?
A: Yes
Q: Will it interact with external APIs or plugins?
A: Unsure

🧱 Recommendation: Run this service in a **Virtual Machine (VM)** for strong isolation.




## 📋 Requirements

-  Linux system
- `bc` (auto-installed by the script if missing)
- `sudo` privileges (for package install)



