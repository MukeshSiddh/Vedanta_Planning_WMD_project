# Vedanta_Planning_WMD_project
Developed strategies to optimize job scheduling and manpower utilization for the 2MTPA Alumina refinery

# Proposed Strategy:

Initially we have the all jobs with the following attributes:

• **Initial Data Attributes**:
1. Work Order No
2. Order crtd date (Date on which the work order is created)
3. work duration (Time taken to complete that work)
4. man power (The no. of people required to complete that work)
5. man hrs (Multiplication of work duraion and man power)
6. Asset criticality (How critical is the asset?)
7. Urgency
8. User status (To check the progress of that job)
   
• **Calculated Attributes**:
1. Ageing (calculated in Excel: Today() - Order crtd date)
2. Scheduling Priority (using prioritization algorithm)
3. Week
4. Day (week and day derived from the man power opt algorithm)
5. Cum sum (of man hrs to check man hours capacity efficiency in
the weekly schedule)


# Workflow Steps for strategy:
S1: **Calculate Ageing**

• Input: Job order data with attributes 1 to 8.
• Function: Ageing = Today() - Order crtd date
• Output: Adds the “Ageing” attribute.

S2: **Calculate Scheduling Priority**

• Input: Job order data with attributes 1 to 10.
• Function: Use the algorithm to find “Scheduling priority” using Asset criticality and Urgency.
• Output: Adds the “Scheduling priority” attribute.

S3: **Optimize Man hrs and Time**

• Input: Job order data with attributes 1 to 11.
• Function: Apply the Man hrs and time optimization algorithm.
• Output: Generate a schedule in terms of week and week-day in a new
Excel sheet.

