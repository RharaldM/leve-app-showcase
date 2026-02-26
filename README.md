# Leve

> "Lose weight from the inside out" — Mental health-focused weight loss app

![Status](https://img.shields.io/badge/Status-In_Development-yellow)
![Flutter](https://img.shields.io/badge/Flutter-02569B?style=flat&logo=flutter&logoColor=white)

---

## Overview

Leve is a mobile app that approaches weight loss through mental reprogramming. Instead of focusing only on diets and exercise, it addresses the root causes of weight gain — emotional eating, anxiety, and compulsive behavior — through therapeutic audio sessions, emotional tracking, guided breathing exercises, and professional-reviewed workouts.

The app also provides dedicated support content for users of GLP-1 medications (Mounjaro/Ozempic).

---

## Planned Features

**Guided Audio Sessions**
- Deep relaxation and guided visualization
- Mental reprogramming for eating habits
- Dedicated content for GLP-1 medication users

**Emotional Diary**
- Daily mood check-ins
- Weight and bioimpedance tracking
- Emotional pattern recognition over time

**Breathing Exercises**
- 4-7-8 breathing technique
- Guided animations for real-time practice

**Workouts with Professional Feedback**
- Exercise video library
- Real feedback from certified professionals
- Progress tracking

**Gamification & Progress**
- Daily streaks and achievements
- Weight evolution charts
- Milestone celebrations

---

## Architecture

```
┌──────────────────────────────────────────────────┐
│              Flutter App (Android + iOS)           │
│                                                    │
│  ┌──────────┐  ┌──────────┐  ┌────────────────┐  │
│  │ Features  │  │Providers │  │    Core        │  │
│  │ (Modules) │  │(Riverpod)│  │ (Theme, Utils, │  │
│  │           │  │          │  │  Router, Widgets│  │
│  └──────────┘  └──────────┘  └────────────────┘  │
│                                                    │
│  Features: Splash, Onboarding, Auth, Home,         │
│  Audio, Diary, Breathing, Progress, Profile        │
└──────────────────────┬───────────────────────────┘
                       │
┌──────────────────────▼───────────────────────────┐
│                Firebase Services                   │
│  Auth | Firestore | Storage | Cloud Messaging      │
└──────────────────────────────────────────────────┘
                       │
┌──────────────────────▼───────────────────────────┐
│              RevenueCat (Subscriptions)             │
│           In-app purchases & plan management        │
└──────────────────────────────────────────────────┘
```

---

## Tech Stack

| Layer | Technology |
|-------|-----------|
| **Framework** | Flutter (Android + iOS) |
| **Language** | Dart |
| **State Management** | Riverpod |
| **Navigation** | GoRouter |
| **Backend** | Firebase (Auth, Firestore, Storage, Messaging) |
| **Payments** | RevenueCat (subscriptions) |
| **Audio** | just_audio |
| **Architecture** | Feature-based modular structure |

---

## Project Structure

```
lib/
├── core/          # Theme, reusable widgets, utils, router
├── models/        # Global models (user, subscription)
├── services/      # Firebase and external integrations
├── providers/     # Riverpod global providers
└── features/      # Feature modules
    ├── splash/
    ├── onboarding/
    ├── auth/
    ├── home/
    ├── audio/
    ├── diary/
    ├── breathing/
    ├── progress/
    └── profile/
```

---

*This is a showcase repository. The source code is in a private repository. Currently in active development.*
