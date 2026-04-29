# Smart Industrial Manufacturing Dashboard

A high-performance, real-time industrial monitoring system developed to provide comprehensive visibility into manufacturing processes. This project leverages Node-RED Dashboard 2.0 and Vue.js to deliver a responsive and interactive interface for tracking production efficiency and machine health.

## Project Overview

This system is designed for modern manufacturing environments, serving as a centralized hub for monitoring multiple production lines. It processes complex data streams from industrial databases to calculate and visualize critical Key Performance Indicators (KPIs) such as First Time Through (FTT%), Parts Per Hour (PPH), and Overall Equipment Effectiveness (OEE).

## Key Features

* **Real-Time KPI Monitoring**: Live calculation and visualization of FTT% and PPH for both Assembly (ASSY) and Inspection (INSP) stages.
* **Multi-Line Scalability**: Support for multiple production lines within a single dashboard, including dedicated views for various factory sections (e.g., TRUCK, VAN, LED lines).
* **Interactive Data Visualization**: 
    * Dynamic status indicators (Green/Orange/Red) based on performance thresholds.
    * Custom Vue.js components for interactive modals and detailed serial number inspections.
    * Auto-scrolling lists for large-scale production data.
* **Comprehensive Reporting**: 
    * Historical data retrieval with filtering by date range and work shifts (Day/Night).
    * Automated error and No Good (NG) summary generation.
    * Data export functionality to CSV for offline analysis.
* **Centralized Configuration**: A Master Settings module allows for real-time adjustment of production targets, cycle times, and machine parameters without downtime.

## Technical Stack

* **Logic Engine**: Node-RED
* **Frontend Framework**: Node-RED Dashboard 2.0 (Vue.js, HTML5, CSS3)
* **Animations**: GSAP (GreenSock Animation Platform)
* **Database**: MariaDB / MySQL
    * Optimized SQL queries utilizing Window Functions for real-time data retrieval.
    * High-concurrency data aggregation across multiple production tables.

## System Architecture

The dashboard operates by polling production data from a centralized SQL database. Data is processed through Node-RED's flow-based logic and pushed to the Vue.js frontend via WebSockets. The UI is built using Single-File Components (SFC) to ensure modularity and high performance.

## Prerequisites

* Node.js (LTS version)
* Node-RED
* @flowfuse/node-red-dashboard (Dashboard 2.0)
* MySQL/MariaDB Instance

## Setup and Installation

1.  Clone this repository to your local machine or server.
2.  Import the provided JSON flow file into your Node-RED instance.
3.  Configure the MySQL/MariaDB node credentials to point to your production database.
4.  Ensure all required custom UI templates and dependencies are installed via the Node-RED Palette Manager.
5.  Deploy the flow and access the dashboard via the `/dashboard` endpoint.

---
*Note: This project is intended for professional industrial use. Ensure proper network security and database access controls are in place before deployment.*
