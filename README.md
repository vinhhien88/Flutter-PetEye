# 🐾 PET EYE — Smart Pet Care & Boarding Platform

> A Flutter-first platform for booking pet services, managing pet health records, and operating pet-care businesses.

## Overview

PET EYE brings pet owners and service providers—clinics, spas, and boarding facilities—into one mobile workflow. Customers can discover nearby shops, book services, manage pet records, pay for bookings, and communicate with providers; shop owners and administrators have dedicated operational views for bookings, services, customers, finance, and moderation.

The project is centred on a cross-platform Flutter application, backed by a Spring Boot API for business workflows, access control, payments, real-time messaging, media, and AI-assisted interactions.

## Links

- Source code (Mobile App): https://github.com/PRM393-BOOKING-APP/APP
- Source code (Backend): https://github.com/PRM393-BOOKING-APP/BE_APP

## 📸 Demo

[▶️ Watch video demo](https://youtube.com/shorts/PvS8uDcq0VY)

## Tech Stack

| Area | Technologies |
| --- | --- |
| Mobile | Flutter, Dart, Provider, GoRouter, Material Design, Google Fonts, Flutter SVG, cached_network_image, fl_chart |
| Backend | Java 21, Spring Boot 3.5, Spring MVC, Spring Security, OAuth2 Resource Server, Spring Data JPA, Hibernate, MapStruct, Lombok, Spring Mail, Spring WebSocket/STOMP, Springdoc OpenAPI, Maven |
| Data | MySQL, Redis |
| Integrations | Google Sign-In, PayOS, Cloudinary, Goong Maps, Gemini, SMTP email |
| DevOps / tooling | Docker, Docker Compose, MediaMTX |

## Highlights

- **Role-based mobile experiences:** separate customer, shop-owner, and administrator flows, backed by JWT-protected endpoints and role-level authorization.
- **End-to-end booking workflow:** service discovery, slot selection, pet and boarding details, vouchers, status tracking, reviews, medical-record gates, and PayOS or cash-deposit payment paths.
- **Real-time chat:** STOMP-over-WebSocket messaging with authenticated connections, typing events, reactions, attachments, and voice-message recording/playback in the Flutter client.
- **Location-aware discovery:** nearby-shop search with GPS permissions plus filters for price and rating; the backend integrates Goong geocoding and distance-matrix APIs.
- **Pet-care operations:** pet profiles, vaccinations, medical records, care logs, staff tasks, boarding cages, and camera-management APIs; MediaMTX is included for live-stream infrastructure.
- **AI-assisted flows:** a Gemini-backed orchestration layer with function tools for shop/service search, pet lookup, and booking preparation. The current backend exposes **24 controllers**, **209 request mappings**, and **37 entity classes**.

## Architecture

The mobile app follows a presentation-oriented structure: **screens/widgets → Provider state management → service/API layer → models**. GoRouter handles navigation, while feature-specific providers and services keep UI state and HTTP/WebSocket transport separate.

The Spring Boot backend uses a layered **Controller → Service → Repository → Entity** design. DTOs and MapStruct mappers separate API contracts from persistence; Spring Security protects REST and WebSocket access. Supporting infrastructure includes MySQL for persistent data, Redis, MediaMTX, and Docker Compose.

## My Role

**Primary Flutter Developer; targeted Backend Contributor**

- Built and refined the Flutter application across customer, shop-owner, and admin experiences, with major work in authentication (including Google sign-in and OTP flows), booking, service/customer management, vouchers, shop discovery, dashboards, and reusable UI components.
- Implemented and iterated on real-time messaging UI, including chat entry points, message screens, shared toast/error handling, and widget decomposition for maintainability.
- Contributed focused backend changes for Google login, shop filtering by GPS/price/rating, voucher workflows, booking-related updates, and supporting seed/configuration changes.

## Project Scale

- **1** cross-platform Flutter application with dedicated customer, shop-owner, and administrator experiences.
- **24** Spring Boot controller classes and **209** REST API mappings.
- **37** JPA entity classes, **31** repository classes, and **5** MapStruct mapper classes in the backend.
