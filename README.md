# Web Scraper with AI-Powered Design Suggestions

A Python-based web scraper that analyzes websites and leverages Claude AI for design and SEO recommendations.

## Project Overview
Build a web scraper that:
1. Scrapes web pages using Fetch API
2. Extracts relevant HTML/CSS/content
3. Sends data to Claude AI via API
4. Returns actionable design and SEO suggestions

## Technical Requirements
- Python 3.9+
- aiohttp for async Fetch API calls
- Anthropic API access
- PostgreSQL 14+ for data storage
- Docker
- pytest for testing

## Project Milestones

### Milestone 1: Basic Scraper Setup (PR #1)
- Implement async web scraper using Fetch
- Extract HTML structure, CSS, and meta tags
- Set up PostgreSQL with Alembic migrations
- Store raw data in PostgreSQL
- Include tests for scraper functionality
- PR Requirements: Video explaining async implementation choices

### Milestone 2: Data Processing (PR #2)
- Parse extracted HTML/CSS
- Identify key design elements and SEO factors
- Create structured format for AI input
- Add data processing tests
- Set up Docker configuration
- PR Requirements: Video covering data structure decisions

### Milestone 3: AI Integration (PR #3)
- Set up Anthropic API connection
- Create prompt engineering for design analysis
- Implement response parsing
- Add unit tests for AI integration
- PR Requirements: Video explaining prompt engineering approach

### Milestone 4: Recommendations Engine (PR #4)
- Process AI suggestions into actionable items
- Categorize recommendations (Critical/Important/Minor)
- Generate detailed reports
- Add report generation tests
- PR Requirements: Video covering recommendation logic

### Milestone 5: API Endpoints (PR #5)
- Create FastAPI endpoints for:
  - Submitting URLs for analysis
  - Retrieving recommendations
  - Accessing historical analyses
- Create OpenAPI documentation
- Add API tests
- PR Requirements: Video explaining API design choices

## Getting Started

1. Clone repository
2. Run with Docker: `docker-compose up`
3. Manual setup (alternative):
   - Install dependencies: `pip install -r requirements.txt`
   - Set up PostgreSQL database
   - Run migrations: `alembic upgrade head`
4. Configure environment variables:
   ```
   ANTHROPIC_API_KEY=your_key
   DATABASE_URL=your_db_url
   ```
5. Run tests: `pytest`

## Branching Strategy
- main: Production-ready code
- develop: Integration branch
- feature/*: Individual feature branches
- release/*: Release preparation
- hotfix/*: Emergency fixes

## Pull Request Guidelines
- Each PR must include:
  - Comprehensive tests
  - Updated documentation
  - 5-10 minute video explanation
  - Passing CI checks
  - Code review responses
  - Database migrations (if applicable)
  - Updated API documentation (if applicable)

## API Documentation
API documentation is available at `/docs` using Swagger UI