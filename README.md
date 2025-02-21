Synthetic Retail Data Anonymization
This repository contains a Python script that generates a synthetic retail dataset and applies advanced data anonymization techniques—K-Anonymity, L-Diversity, and T-Closeness—to protect sensitive information. The project serves as a practical example of how privacy can be enhanced while retaining the utility of data for analysis.

Table of Contents
Overview
Features
Installation
Usage
Project Structure
How It Works
Contributing
License
Acknowledgments
Overview
In this project, we generate a synthetic retail dataset using the Faker library. The dataset simulates 30 retail transactions including details such as names, emails, phone numbers, addresses, transaction types, and amounts. To ensure privacy and prevent re-identification, the dataset is anonymized by:

K-Anonymity: Masking and generalizing direct identifiers.
L-Diversity: Ensuring diversity in sensitive attributes within groups.
T-Closeness: Maintaining the statistical distribution of sensitive attributes.
Features
Synthetic Data Generation: Uses Faker to create realistic dummy data.
K-Anonymity: Implements masking for email addresses, phone numbers, and addresses.
L-Diversity: Applies group-based filtering to ensure diverse transaction types.
T-Closeness: Adjusts record sampling to preserve the overall distribution of transaction amounts.
Data Export: Saves the final anonymized dataset to an Excel file (Retail_Stop_Dataset_Final.xlsx).
Installation
Clone the repository:

bash
Copy
Edit
git clone https://github.com/your-username/synthetic-retail-data-anonymization.git
cd synthetic-retail-data-anonymization
Install the required Python packages:

bash
Copy
Edit
pip install pandas tabulate Faker
Usage
Run the script:

bash
Copy
Edit
python anonymize_data.py
Script Output:

The script generates a synthetic dataset.
It displays the original dataset and then the anonymized version in the console.
The final anonymized dataset is saved as an Excel file named Retail_Stop_Dataset_Final.xlsx.
Project Structure
anonymize_data.py
The main Python script that generates the dataset and applies the anonymization techniques.

Retail_Stop_Dataset_Final.xlsx
The Excel file containing the anonymized dataset (generated upon running the script).

README.md
This file, which provides an overview and instructions for the project.

How It Works
Data Generation
Synthetic Records:
Generates 30 retail transaction records with fields such as:
Name, Date, Time, Store Category
Email, Phone Number, Address
Transaction Type, Amount, Zip Code
K-Anonymity
Email Masking:
Retains only the first three characters of the email and replaces the rest with asterisks.
Phone Number Masking:
Partially masks phone numbers to hide sensitive parts.
Address Generalization:
Replaces detailed addresses with generalized Zip Code values.
L-Diversity
Sensitive Attribute Diversity:
Groups data by Store Category and ensures that each group contains at least two distinct Transaction Types. This prevents homogeneous sensitive data within a group.
T-Closeness
Maintaining Distribution:
Adjusts the sample selection for the Amount attribute in each group so that its distribution closely resembles that of the overall dataset, reducing the risk of inference attacks.
Contributing
Contributions are welcome! If you have suggestions, improvements, or bug fixes:

Fork the repository.
Create a new branch (git checkout -b feature/your-feature).
Commit your changes.
Push to your branch.
Open a Pull Request.
License
This project is licensed under the MIT License. See the LICENSE file for details.

Acknowledgments
Faker: For providing an excellent library to generate synthetic data.
pandas & tabulate: For their powerful data manipulation and display capabilities.
