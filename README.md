- The URL Shortener Backend is a production-ready web service that converts long URLs into short, shareable links while tracking engagement metrics. The system is built with Spring Boot 3.5.6 and Java 21, using PostgreSQL for persistence and JWT tokens for stateless authentication.

- Primary Capabilities :

1. URL Shortening	Generates 8-character alphanumeric short codes for any URL
2. Click Tracking	Records every click with timestamp for analytics
3. User Management	Multi-tenant system with JWT-based authentication
4. Analytics Dashboard	Time-series click data aggregated by date
5. Public Redirection	Fast, unauthenticated access to shortened URLs

- Technology Stack

1. Core Framework
2. Component	Version	Purpose
3. Spring Boot	3.5.6	Application framework
4. Java	21	Runtime platform
5. Maven	3.9.11	Build tool
6. PostgreSQL
7. Render for deployment

- Public Endpoints (No Authentication Required)

1. /{shortUrl}	GET	Redirect to original URL
2. /api/auth/public/register	POST	User registration
3. /api/auth/public/login	POST	User login (returns JWT)

- Protected Endpoints (JWT Required)

1. /api/urls/shorten	POST	Create shortened URL
2. /api/urls	GET	Get all URLs for authenticated user
3. /api/urls/analytics	GET	Get click analytics for specific URL
4. /api/urls/totalClicks	GET	Get aggregated clicks across all user URLs

**WORKING APP LINK - https://abhishektestapps.space**

(Note : The Backend is deployed on Render using Free plan, so when the backend is ideal for long, it automatically goes to sleep/ gets shut down. If you face some delays in getting response. Please wait for 1-2 minutes and try again. In the meantime, the server will restart and will be up again.)
