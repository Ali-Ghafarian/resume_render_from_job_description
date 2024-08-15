# Resume_Render_AIHawk

Welcome to **Resume_Render_AIHawk** – a Python-based tool designed to help you create visually stunning resumes quickly and easily. This application allows you to generate resumes either from scratch or based on job descriptions fetched from URLs.

## Table of Contents

1. [Introduction](#introduction)
2. [Features](#features)
3. [Installation](#installation)
4. [Configuration](#configuration)
   - [Configuring `plain_text_resume.yaml`](#configuring-plain_text_resume_yaml)
   - [Configuring `secrets.yaml`](#configuring-secrets_yaml)
5. [Usage](#usage)
6. [Documentation](#documentation)
7. [Troubleshooting](#troubleshooting)
8. [Conclusion](#conclusion)
9. [Contributors](#contributors)
10. [Credits](#credits)
11. [License](#license)
12. [Disclaimer](#disclaimer)

## Introduction

**Resume_Render_AIHawk** is a powerful Python tool that simplifies the process of creating professional resumes. Whether starting from scratch or tailoring your resume based on job descriptions, this tool offers a range of features to help you craft a resume that stands out.

## Features

- **Interactive Command-Line Interface:** Navigate through options and prompts using a user-friendly CLI.
- **Dynamic Style Management:** Choose from a variety of pre-defined resume styles.
- **Job Description Integration:** Automatically tailor your resume based on a job description URL.

## Installation

To get started with Resume_Render_AIHawk, follow these steps:

1. **Clone the Repository:**

    ```bash
    git clone https://github.com/yourusername/resume_builder_AIHawk.git
    ```

2. **Navigate to the Project Directory:**

    ```bash
    cd resume_builder_AIHawk
    ```

3. **Install Dependencies:**

    Ensure you have `pip` installed, then run:

    ```bash
    pip install -r requirements.txt
    ```

## Dependencies

Ensure the following Python libraries are installed:

- `inquirer`: For interactive command-line prompts.
- `requests`: For fetching job descriptions from URLs.
- `pyyaml`: For handling YAML configuration files.

## Configuration

### Configuring `plain_text_resume.yaml`

The `plain_text_resume.yaml` file is crucial as it contains all your personal details and resume content. Follow these steps to configure it properly:

#### 1. Create the File

Create a file named `plain_text_resume.yaml` in the root directory of your project. This file will store all the necessary details to generate your resume.

#### 2. Define Personal Information

Fill in your personal information. This section includes your basic details and contact information:

```yaml
personal_information:
  name: [Name]
  surname: [Surname]
  date_of_birth: "[DD/MM/YYYY]"
  country: [Country]
  city: [City]
  address: [Address]
  phone_prefix: "[+Country Code]"
  phone: "[Phone Number]"
  email: [Email Address]
  github: [GitHub URL]
  linkedin: [LinkedIn URL]
```

- **name**: Your first name.
- **surname**: Your last name.
- **date_of_birth**: Your date of birth in the format `DD/MM/YYYY`.
- **country**: The country where you live.
- **city**: The city where you live.
- **address**: Your home address.
- **phone_prefix**: Your phone number prefix, e.g., `+1` for the USA.
- **phone**: Your phone number.
- **email**: Your email address.
- **github**: Your GitHub profile URL (optional).
- **linkedin**: Your LinkedIn profile URL (optional).

#### 3. Provide Education Details

List your educational qualifications. You can add multiple degrees:

```yaml
education_details:
  - degree: [Degree Type]
    university: [University Name]
    gpa: "[GPA]"
    graduation_year: "[Graduation Year]"
    field_of_study: [Field of Study]
    exam:
      [Course Name]: "[Grade]"
      [Course Name]: "[Grade]"
      [Course Name]: "[Grade]"
  - degree: [Degree Type]
    university: [University Name]
    gpa: "[GPA]"
    graduation_year: "[Graduation Year]"
    field_of_study: [Field of Study]
    exam:
      [Course Name]: "[Grade]"
      [Course Name]: "[Grade]"
      [Course Name]: "[Grade]"
```

- **degree**: Type of degree (e.g., BSc, MSc, PhD).
- **university**: Name of the university or institution.
- **gpa**: Your GPA (optional).
- **graduation_year**: The year you graduated.
- **field_of_study**: Your field of study (e.g., Computer Science).
- **exam**: List of courses and grades received. Add or remove entries as needed.

#### 4. List Experience Details

Provide information about your work experience. You can include multiple jobs:

```yaml
experience_details:
  - position: [Job Title]
    company: [Company Name]
    employment_period: "[MM/YYYY - MM/YYYY or Present]"
    location: [Location]
    industry: [Industry]
    key_responsibilities:
      - [Responsibility Description]
      - [Responsibility Description]
      - [Responsibility Description]
    skills_acquired:
      - [Skill]
      - [Skill]
      - [Skill]
  - position: [Job Title]
    company: [Company Name]
    employment_period: "[MM/YYYY - MM/YYYY or Present]"
    location: [Location]
    industry: [Industry]
    key_responsibilities:
      - [Responsibility Description]
      - [Responsibility Description]
      - [Responsibility Description]
    skills_acquired:
      - [Skill]
      - [Skill]
      - [Skill]
```

- **position**: Your job title.
- **company**: Name of the company where you worked.
- **employment_period**: The period you worked there (e.g., `01/2020 - 12/2021` or `Present`).
- **location**: City and country of the company's location.
- **industry**: The industry of the company.
- **key_responsibilities**: List of key responsibilities in bullet points.
- **skills_acquired**: List of skills acquired during this role.

#### 5. Detail Your Projects

Include projects that you have worked on:

```yaml
projects:
  - name: [Project Name]
    description: [Project Description]
    link: "[Project URL]"
  - name: [Project Name]
    description: [Project Description]
    link: "[Project URL]"
  - name: [Project Name]
    description: [Project Description]
    link: "[Project URL]"
```

- **name**: Name of the project.
- **description**: A brief description of the project.
- **link**: URL to the project or related resource (optional).

#### 6. Add Achievements

List notable achievements:

```yaml
achievements:
  - name: [Achievement Title]
    description: [Achievement Description]
  - name: [Achievement Title]
    description: [Achievement Description]
  - name: [Achievement Title]
    description: [Achievement Description]
  - name: [Achievement Title]
    description: [Achievement Description]
```

- **name**: Title of the achievement.
- **description**: Description of the achievement.

#### 7. List Certifications

Include any certifications you hold:

```yaml
certifications:
  - [Certification Name]
```

- **certification**: Name of the certification.

#### 8. Detail Your Language Skills

List the languages you speak and your proficiency levels:

```yaml
languages:
  - language: [Language]
    proficiency: [Proficiency Level]
  - language: [Language]
    proficiency: [Proficiency Level]
  - language: [Language]
    proficiency: [Proficiency Level]
```

- **language**: Name of the language.
- **proficiency**: Your proficiency level (e.g., Basic, Intermediate, Advanced).

#### 9. Add Interests

Include your personal interests:

```yaml
interests:
  - [Interest]
  - [Interest]
  - [Interest]
```

- **interest**: List your interests or hobbies.

### Example `plain_text_resume.yaml`

An example `plain_text_resume.yaml` file is provided in the repository to guide you. Copy and modify it according to your personal details.

### Configuring `secrets.yaml`

Create a file named `secrets.yaml` in the root directory to store sensitive information such as API keys. Here’s a sample format:

```yaml
api_keys:
  google_api_key: "[Your Google API Key]"
  linkedin_api_key: "[Your LinkedIn API Key]"

other_secrets:
  secret_key: "[Your Secret Key]"
```

Replace placeholders with your actual API keys and secrets.

## Usage

To run Resume_Render_AIHawk, execute the following command from your terminal:

```bash
python main.py
```

### Interactive CLI

Once you run the application, you'll be presented with an interactive menu:

- **Create Resume:** Generate a new resume using a selected style.
- **Create Resume based on Job Description:** Generate a resume tailored to a specific job description by providing a URL.
- **Exit:** Exit the application.

You will be prompted to select a resume style and, if needed, provide a URL for the job description.

## Documentation

For detailed documentation on the `FacadeManager` class and

 its methods, refer to the inline comments in the code and the `docs/` directory of the project.

## Troubleshooting

- **Issue:** The application does not start.
  - **Solution:** Ensure all dependencies are installed and that you have the correct version of Python.

- **Issue:** The resume is not generated correctly.
  - **Solution:** Check the format and values in your `plain_text_resume.yaml` file for errors.

- **Issue:** Missing styles or configurations.
  - **Solution:** Ensure that the `STYLES_DIRECTORY` is correctly set and contains the necessary style files.

## Conclusion

Resume_Render_AIHawk simplifies the resume creation process by providing a flexible, style-driven approach. By configuring `plain_text_resume.yaml` and using the interactive prompts, you can easily generate professional resumes tailored to your needs.

## Contributors

- [Your Name](https://github.com/yourusername) - Creator and Lead Developer

## Credits

- [Inquirer](https://github.com/inquirer) - For interactive command-line prompts.
- [Requests](https://docs.python-requests.org/en/latest/) - For HTTP requests.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Disclaimer

The information provided by Resume_Render_AIHawk is for general informational purposes only. The project is intended to assist with resume creation and may not cover all specific requirements for every job application.
