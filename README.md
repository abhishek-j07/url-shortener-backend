- The URL Shortener Backend is a production-ready web service that converts long URLs into short, shareable links while tracking engagement metrics. The system is built with Spring Boot 3.5.6 and Java 21, using MySQL for persistence and JWT tokens for stateless authentication.

Primary Capabilities
Feature	Description
URL Shortening	Generates 8-character alphanumeric short codes for any URL
Click Tracking	Records every click with timestamp for analytics
User Management	Multi-tenant system with JWT-based authentication
Analytics Dashboard	Time-series click data aggregated by date
Public Redirection	Fast, unauthenticated access to shortened URLs

- Technology Stack

Core Framework
Component	Version	Purpose
Spring Boot	3.5.6	Application framework
Java	21	Runtime platform
Maven	3.9.11	Build tool

- Public Endpoints (No Authentication Required)

/{shortUrl}	GET	Redirect to original URL
/api/auth/public/register	POST	User registration
/api/auth/public/login	POST	User login (returns JWT)

- Protected Endpoints (JWT Required)

/api/urls/shorten	POST	Create shortened URL
/api/urls	GET	Get all URLs for authenticated user
/api/urls/analytics	GET	Get click analytics for specific URL
/api/urls/totalClicks	GET	Get aggregated clicks across all user URLs
