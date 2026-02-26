# Leve

> "Emagreça de dentro para fora" — App de emagrecimento focado em saúde mental
>
> *"Lose weight from the inside out" — Mental health-focused weight loss app*

![Status](https://img.shields.io/badge/Status-Em_Desenvolvimento-yellow)
![Flutter](https://img.shields.io/badge/Flutter-02569B?style=flat&logo=flutter&logoColor=white)

---

## Visão Geral | Overview

O Leve é um app mobile que aborda o emagrecimento através de reprogramação mental. Em vez de focar apenas em dietas e exercícios, ele trata as causas raiz do ganho de peso — fome emocional, ansiedade e comportamento compulsivo — através de sessões de áudio terapêutico, rastreamento emocional, exercícios guiados de respiração e treinos com avaliação profissional.

O app também oferece conteúdo dedicado para usuários de medicamentos GLP-1 (Mounjaro/Ozempic).

*Leve is a mobile app that approaches weight loss through mental reprogramming. Instead of focusing only on diets and exercise, it addresses the root causes of weight gain — emotional eating, anxiety, and compulsive behavior — through therapeutic audio sessions, emotional tracking, guided breathing exercises, and professional-reviewed workouts. The app also provides dedicated support content for users of GLP-1 medications (Mounjaro/Ozempic).*

---

## Funcionalidades Planejadas | Planned Features

**Áudios Guiados de Reprogramação Mental**
- Relaxamento profundo e visualização guiada
- Reprogramação mental para hábitos alimentares
- Conteúdo dedicado para usuários de medicamentos GLP-1

**Diário Emocional**
- Check-in diário de humor
- Rastreamento de peso e bioimpedância
- Reconhecimento de padrões emocionais ao longo do tempo

**Exercícios de Respiração**
- Técnica de respiração 4-7-8
- Animações guiadas para prática em tempo real

**Treinos com Feedback Profissional**
- Biblioteca de vídeos de exercícios
- Feedback real de profissionais certificados
- Acompanhamento de progresso

**Gamificação & Progresso**
- Streaks diários e conquistas
- Gráficos de evolução do peso
- Celebrações de marcos alcançados

---

## Arquitetura | Architecture

```
┌──────────────────────────────────────────────────┐
│              App Flutter (Android + iOS)           │
│                                                    │
│  ┌──────────┐  ┌──────────┐  ┌────────────────┐  │
│  │ Features  │  │Providers │  │    Core        │  │
│  │ (Módulos) │  │(Riverpod)│  │ (Tema, Utils,  │  │
│  │           │  │          │  │  Router,       │  │
│  └──────────┘  └──────────┘  │  Widgets)      │  │
│                               └────────────────┘  │
│  Features: Splash, Onboarding, Auth, Home,         │
│  Áudio, Diário, Respiração, Progresso, Perfil      │
└──────────────────────┬───────────────────────────┘
                       │
┌──────────────────────▼───────────────────────────┐
│                Serviços Firebase                   │
│  Auth | Firestore | Storage | Cloud Messaging      │
└──────────────────────────────────────────────────┘
                       │
┌──────────────────────▼───────────────────────────┐
│             RevenueCat (Assinaturas)                │
│       Compras in-app e gestão de planos            │
└──────────────────────────────────────────────────┘
```

---

## Stack Tecnológica | Tech Stack

| Camada | Tecnologia |
|--------|-----------|
| **Framework** | Flutter (Android + iOS) |
| **Linguagem** | Dart |
| **Gerenciamento de Estado** | Riverpod |
| **Navegação** | GoRouter |
| **Backend** | Firebase (Auth, Firestore, Storage, Messaging) |
| **Pagamentos** | RevenueCat (assinaturas) |
| **Áudio** | just_audio |
| **Arquitetura** | Estrutura modular baseada em features |

---

## Estrutura do Projeto | Project Structure

```
lib/
├── core/          # Tema, widgets reutilizáveis, utils, router
├── models/        # Models globais (user, subscription)
├── services/      # Firebase e integrações externas
├── providers/     # Riverpod providers globais
└── features/      # Módulos por funcionalidade
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

*Este é um repositório vitrine. O código-fonte está em um repositório privado. Atualmente em desenvolvimento ativo.*

*This is a showcase repository. The source code is in a private repository. Currently in active development.*
