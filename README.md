Tech Stack Recommender 🚀
The Tech Stack Recommender is a specialized, Python-based recommendation engine designed to bridge the gap between qualitative career aspirations and quantitative data analysis.

By treating job roles as discrete items, the system transforms raw user skills and career goals into objective, mathematically ranked career paths. It evaluates a user's skillset against a dataset of real-world job roles and outputs the top three most relevant career trajectories.

🎯 Core Objectives & Features
Skill Mapping: Aligns qualitative user inputs (e.g., Python, Cloud Computing) with a standardized dataset of technical requirements.

Mathematical Objectivity: Moves away from subjective career advice toward a ranked mathematical output.

Data-Driven Algorithm: Utilizes TF-IDF (Term Frequency-Inverse Document Frequency) weighting to evaluate skill relevance and Cosine Similarity to determine the "angular alignment" between a user's skills and specific professional roles.

Custom Data Preprocessing: Dynamically extracts and cleans job titles directly from URL slugs within the dataset.

🛠️ Technical Pipeline
The system operates through a structured four-stage pipeline:

Input Phase: Accepts an array of technical skills from the user (e.g., ["Python", "Cloud", "Automation"]).

Processing and Vectorization: Aggregates dataset skills by job role and maps them to a vector space using TF-IDF. This lowers the weight of generic terms and highlights niche technical skills.

Scoring via Cosine Similarity: Calculates the mathematical similarity (dot product/angular alignment) between the user's input vector and the vectors of various job roles.

Output Generation: Filters the scores and outputs the Top 3 career paths with their mathematical alignment scores.

⚙️ Prerequisites
Make sure you have Python 3.x installed on your machine. You will also need the following Python libraries:

Bash
pip install pandas scikit-learn

🚀 Installation & Usage
Clone the repository:
Bash
git clone https://github.com/Jamal512-AI/decode-loabs-project-2.git
cd tech-stack-recommender
Ensure your dataset is present:
Make sure the raw_skills.csv file is located in the same directory as the script (or update the dataset_path variable at the bottom of the Python script to point to your local path).

Run the script:

Bash
python tech_stack_recommender.py
📊 Example Output
If you provide the script with the input array ["Python", "Cloud", "Automation"], the engine processes it against the dataset and outputs a ranked hierarchy:

Plaintext
Stage 1: Loading and Preprocessing Data...
Stage 2: Processing and Vectorization (TF-IDF)...
Stage 3: Scoring via Cosine Similarity...
Stage 4: Output Generation...

==================================================
INPUT ARRAY: ['Python', 'Cloud', 'Automation']
==================================================
Rank 1: Enterprise Architect Level
Mathematical Alignment: 0.4415
--------------------------------------------------
Rank 2: IT Enterprise Architect
Mathematical Alignment: 0.4166
--------------------------------------------------
Rank 3: Azure Cloud Engineer
Mathematical Alignment: 0.3540
--------------------------------------------------
(Note: Exact output titles depend on the data present in your raw_skills.csv file)

📂 Dataset Information
The system relies on a dataset (raw_skills.csv) containing:

id: Unique identifier.

raw_skills: An array/list of stringified technical skills (e.g., ['python', 'sql', 'machine learning']).

url: A job posting URL from which the engine extracts the specific job title (e.g., Data Scientist, DevOps Engineer).

🤝 Contributing
Contributions, issues, and feature requests are welcome! Feel free to check the issues page if you want to contribute.
