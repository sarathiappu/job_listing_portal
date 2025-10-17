Successfully uploaded the four split files (`job_listing_portal_part_aa`, `job_listing_portal_part_ab`, `job_listing_portal_part_ac`, `job_listing_portal_part_ad`) to [https://github.com/sarathiappu/job_listing_portal](https://github.com/sarathiappu/job_listing_portal). However, GitHub won’t automatically reassemble these `.tar.gz` parts into a usable folder, so you will need to download and recombine them.

(`job_listing_portal_part_aa`, `job_listing_portal_part_ab`, `job_listing_portal_part_ac`, `job_listing_portal_part_ad`)

Instructions to Reassemble

Since the files are split parts of the original `job_listing_portal.tar.gz`, your teammate needs to download and recombine them. Here’s what to send them:

#### Instructions:
1. **Clone or Download the Repository:**
   - Option 1: Clone the repo (if they have Git):
     ```
     git clone https://github.com/sarathiappu/job_listing_portal.git
     cd job_listing_portal
     ```
   - Option 2: Download ZIP manually from GitHub (click "Code" > "Download ZIP"), then extract it.

2. **Combine the Split Files:**
   - Ensure all four files (`job_listing_portal_part_aa`, `job_listing_portal_part_ab`, `job_listing_portal_part_ac`, `job_listing_portal_part_ad`) are in the same directory.
   - Run this command to recombine:
     ```
     cat job_listing_portal_part_aa job_listing_portal_part_ab job_listing_portal_part_ac job_listing_portal_part_ad > job_listing_portal.tar.gz
     ```
   - This concatenates the parts into the original `job_listing_portal.tar.gz`.

3. **Extract the Archive:**
   - Extract the recombined file:
     ```
     tar -xzvf job_listing_portal.tar.gz
     ```
   - This creates the `job_listing_portal` folder with `backend/` and `frontend/` subdirectories.

4. **Set Up the Project:**
   - Navigate to backend:
     ```
     cd job_listing_portal/backend
     ```
   - Install dependencies:
     ```
     npm install
     ```
   - Create `.env` with:
     ```
     MONGO_URI=mongodb://localhost:27017/job_listing_portal
     JWT_SECRET=your_secret_key
     PORT=5000
     ```
   - Start the backend:
     ```
     node server.js
     ```
   - In another terminal, navigate to frontend:
     ```
     cd ../frontend
     ```
   - Install dependencies:
     ```
     npm install
     ```
   - Start the frontend:
     ```
     npm start
     ```

5. **Prerequisites:**
   - Install Node.js and npm (e.g., `sudo apt install nodejs npm` on Ubuntu).
   - Install MongoDB (e.g., `sudo apt install mongodb-org -y` and `sudo systemctl start mongod`).

GitHub link: [https://github.com/sarathiappu/job_listing_portal](https://github.com/sarathiappu/job_listing_portal)
