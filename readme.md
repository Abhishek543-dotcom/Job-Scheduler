
# Job Scheduler

## Project Overview
The **Job Scheduler** is a command-line tool built to help users manage and organize their daily jobs by scheduling them at specific times. It uses a Binary Search Tree (BST) to store and efficiently retrieve jobs based on their start times. The application allows users to add, view, and remove scheduled jobs, ensuring that there are no time conflicts between tasks.

### Features
- **Add a Job:** Allows the user to add a new job with a specified start time, duration, and name. The job is inserted into the BST if there is no time conflict with other scheduled jobs.
- **View Scheduled Jobs:** Displays the list of all jobs scheduled for the day in order of their start times.
- **Remove a Job:** Allows the user to remove a job based on its start time, duration, and name, and updates the schedule.
- **Persistent Data Storage:** The job schedule is stored in a `data.txt` file, and all changes (addition and removal) are reflected in this file.

### Binary Search Tree (BST) Usage
The **Binary Search Tree (BST)** is employed to manage the jobs efficiently:
- Each node in the BST represents a job with the following properties:
  - Start time
  - Duration
  - End time
  - Job name
- Jobs are inserted into the BST based on their start times. The structure ensures that the jobs are stored in sorted order, allowing for efficient scheduling and time conflict detection.

### How it Works
1. The program starts by loading any existing job data from `data.txt` into the BST.
2. Users are prompted with a menu to either view the current day's jobs, add a new job, remove a job, or quit the program.
3. When a job is added, the system checks for potential conflicts by ensuring that the new job's time slot does not overlap with any existing jobs.
4. When a job is removed, it is deleted from the BST and the file is updated accordingly.

### Technologies Used
- **Python**: Core programming language.
- **Binary Search Tree (BST)**: Data structure for storing and managing jobs.
- **File Handling**: Persistent storage of job schedules in a text file (`data.txt`).

---

### Example Usage
1. **Add a Job**  
   The user inputs the start time, duration (in minutes), and job name. If the time slot is available, the job is added to the schedule.

2. **View Scheduled Jobs**  
   The system prints all jobs for the current day in chronological order.

3. **Remove a Job**  
   The user specifies the job details, and the job is removed from the schedule and the text file.

---

### File Descriptions
- **job_scheduler.py**: Contains the main logic for the job scheduling system, including user interaction, adding/removing jobs, and maintaining the job list.
- **bst_demo.py**: Implements the Binary Search Tree for handling job scheduling. It includes methods for inserting, deleting, and searching for jobs.

---

### How to Run
1. Clone the repository or download the project files.
2. Ensure you have Python installed.
3. Run the script `job_scheduler.py` using the command:
   ```bash
   python job_scheduler.py
   ```
4. Follow the on-screen prompts to manage your job schedule.

