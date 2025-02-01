# BharatFD - Backend Developer Assignment

## Project Overview
The BharatFD project is designed to store FAQs as a model and dynamically display translations using the Google Translate API.

## Tech Stack
- **Backend:** Node.js, Express.js
- **Database:** MongoDB (with Redis for caching)
- **Frontend:** EJS templating
- **APIs:** REST API structure
- **Caching:** Redis

## Assumptions
1. **Backend-Centric:** The project primarily focuses on backend development.
2. **Simple Authentication:** Admin login uses hardcoded credentials for simplicity.
3. **Minimal UI Framework:** EJS is used for fast rendering and dynamic content.

## Installation Guide
Follow these steps to set up and run the project:

1. Download and extract the project zip file.
2. Open a terminal and navigate to the project folder:
   ```bash
   cd BharatFd
   ```
3. Install dependencies:
   ```bash
   npm install
   ```
4. Create a `.env` file and set the following environment variables:
   ```env
   MONGO_DB_URL=your_mongo_connection_url
   PROJECT_ID=your_google_translate_api_project_id
   ```
5. Start the application:
   ```bash
   node app.js
   ```
6. Log in using the following credentials:
   - **Email:** `admin@example.com`
   - **Password:** `admin`

Upon login, you will be redirected to `/api/faqs`.

## API Usage Examples

### Fetch FAQs in English (default)
```bash
curl http://localhost:8000/api/faqs/
```

### Fetch FAQs in Hindi
```bash
curl http://localhost:8000/api/faqs/?lang=hi
```

### Fetch FAQs in Bengali
```bash
curl http://localhost:8000/api/faqs/?lang=bn
```

### Fetch a Specific FAQ by ID
```bash
curl http://localhost:8000/api/faqs/:faqid
```

## Using Docker
To run the project in a Docker container, follow these steps:

1. Build the Docker image:
   ```bash
   docker build -t bharatfd .
   ```
2. Run the Docker container using Docker Compose:
   ```bash
   docker-compose up
   ```
3. Verify that the app is running by visiting: [http://localhost:8000](http://localhost:8000)

This will start the backend API, MongoDB, and Redis services as defined in `docker-compose.yml`.

## Contribution Guidelines
We welcome contributions! Please follow these steps to collaborate effectively:

1. Fork the repository and clone it to your local machine.
2. Create a new feature branch:
   ```bash
   git checkout -b feature-branch-name
   ```
3. Make your changes following ES6+ standards.
4. Run tests before pushing:
   ```bash
   npm test
   ```
5. Commit your changes with a clear and concise message:
   ```bash
   git commit -m "feat: added multilingual support"
   ```
6. Push your changes to GitHub and open a Pull Request (PR).

## Future Improvements
- Implement JWT-based authentication for enhanced security.
- Build a modern UI using React for a more interactive user experience.

---
Thank you, **BharatFD**, for this opportunity!

