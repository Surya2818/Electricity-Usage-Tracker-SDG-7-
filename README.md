****ELECTRICITY USAGE TRACJER (SDG 7)****

INTRODUCTION :

The Electricity Usage Tracker is a Python-based program used to monitor daily electricity consumption.

FEATURES :

🔹Input daily electricity usage.

🔹Set usage limit.

🔹Display daily usage report.

🔹Calculate total and average usage.

🔹Alert when usage exceeds limit ⚠️.

🔹Promote energy saving.

HOW TO RUN :

🔹Step 1:

Open Python IDLE.

🔹Step 2:

Copy the code and paste it.

🔹Step 3:

Save as 👉 electricity.py.

🔹Step 4:

Click Run (F5).

🔹Step 5:

Enter inputs when asked:

PROGRAM :

```
usage_data = []

days = int(input("Enter number of days: "))
limit = float(input("Enter daily usage limit (units): "))

# Input usage
for i in range(days):
    units = float(input(f"Day {i+1} electricity usage: "))
    usage_data.append(units)

print("\n⚡ Electricity Usage Report ⚡")
total = 0

for i in range(days):
    print(f"Day {i+1}: {usage_data[i]} units")
    total += usage_data[i]
    
    if usage_data[i] > limit:
        print("⚠️ High electricity usage!")

# Average calculation
average = total / days

print("\nTotal Usage:", total, "units")
print("Average Usage:", round(average, 2), "units")

# Final suggestion
if average > limit:
    print("⚠️ Reduce electricity consumption!")
else:
    print("Good job! Efficient usage 👍")
```

OUTPUT :

<img width="679" height="559" alt="image" src="https://github.com/user-attachments/assets/a40c73a5-8eea-49cf-b937-29433a2b2cde" />

RESULT :

The Electricity Usage Tracker is a Python-based program used to monitor daily electricity consumption was successfully completed. 
