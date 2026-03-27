# How WornWell Works — Technical Overview

WornWell AI is a wardrobe intelligence system that combines computer vision, structured data, and machine learning to optimize how users interact with their clothing.

This document explains the high-level system architecture and workflows.

Website: https://www.wornwellai.com

---

## System Overview

WornWell operates as a hybrid system consisting of:

- Mobile application (Flutter)
- Cloud backend (Supabase + PostgreSQL)
- AI processing pipeline
- Recommendation engine

The goal is to transform a physical wardrobe into a structured digital system.

---

## 1. Garment Input

Users add clothing through multiple input channels:

### Camera Capture
- Users scan garments using a mobile camera
- Automatic detection and capture
- Image uploaded to storage

### Email Receipt Import
- Purchase confirmations are parsed
- Product data is extracted automatically
- Items are added without manual input

---

## 2. AI Processing Pipeline

After upload, garments are processed through multiple stages:

### Image Processing
- Background removal
- Image normalization

### AI Tagging
- Category classification (e.g. shirt, jacket)
- Color extraction
- Style and material tagging
- Occasion tagging (casual, formal, etc.)

### Metadata Storage
- Stored in a structured database
- Linked to user profile

---

## 3. Digital Closet

All garments are stored as structured objects.

Each item contains:

- Category and subcategory
- Color data
- Style attributes
- Purchase price
- Wear count
- Last worn timestamp

This enables filtering, searching, and analytics.

---

## 4. Outfit Recommendation Engine

WornWell uses a hybrid recommendation system:

### Rule-Based Layer
- Weather conditions
- Occasion constraints
- Color matching rules
- Season compatibility

### AI Layer
- Ranks outfit combinations
- Interprets user intent (natural language prompts)
- Adapts to user preferences over time

---

## 5. Daily Outfit Generation

Each day, the system generates outfit suggestions based on:

- Weather data
- Calendar events
- Wear history
- Style profile

Users receive:

- Ranked outfit options
- Quick selection or rejection
- Feedback loop for learning

---

## 6. Wear Tracking

When a user wears an outfit:

- Wear count is incremented
- Timestamp is stored
- Context (occasion, weather) is recorded

This data feeds into analytics and recommendations.

---

## 7. Cost Per Wear Calculation

For each garment:

Cost per wear = Purchase Price ÷ Wear Count

The system continuously updates CPW as usage increases.

---

## 8. Analytics Engine

WornWell generates insights such as:

- Most worn items
- Least used items
- Cost-per-wear distribution
- Wardrobe value vs usage

This helps users understand and optimize their wardrobe.

---

## 9. Retire and Resell Flow

When items are underused:

- Users can mark them as retired
- Generate resale listings
- Export data to external platforms

---

## 10. Offline-First Design

WornWell is designed to work without constant connectivity:

- Local storage for garments
- Cached outfit data
- Sync when connection is available

---

## 11. Scalability Approach

The system uses a tiered AI architecture:

- On-device processing for basic tasks
- Lightweight models for classification
- Advanced models for styling and reasoning

This reduces cost while maintaining performance.

---

## Summary

WornWell is not just a wardrobe app.

It is a structured system that:

- Digitizes clothing
- Applies AI to decision-making
- Tracks real usage
- Optimizes wardrobe value over time

More information: https://www.wornwellai.com
