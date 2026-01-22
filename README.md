# Hotel Room Reservation System (SDE 3 Assessment)

A React-based optimal room allocation system that minimizes travel time for guests based on specific proximity rules.

## 🚀 Live Demo
**[Insert Your Vercel/Netlify Link Here]**

## 🛠 Tech Stack
* **Frontend:** React (Vite), TypeScript
* **Styling:** Tailwind CSS
* **Algorithm:** Weighted Proximity Search (Graph/Grid Logic)

## 🧠 Optimization Logic
The system uses a **Candidate Pivot Algorithm** to ensure mathematically optimal room assignment:

1.  **Priority 1 (Same Floor):** The system first scans all floors using a **Sliding Window** approach ($O(N)$) to find the tightest cluster of rooms on a single floor.
2.  **Priority 2 (Cross-Floor):** If no single floor suffices, the system treats every available room as a "Pivot." It calculates the travel time (Vertical + Horizontal) from that pivot to all other rooms, sorts them by proximity, and selects the optimal cluster.

**Time Complexity:** $O(R \cdot \log R)$ where $R$ is the number of available rooms (due to sorting). Given $R=97$, this is instantaneous.

## 🏃‍♂️ How to Run Locally
1.  Clone the repository:
    ```bash
    git clone https://github.com/Rishicreates20/hotel-reservation-assessment
    ```
2.  Install dependencies:
    ```bash
    npm install
    ```
3.  Start the server:
    ```bash
    npm run dev
    ```
