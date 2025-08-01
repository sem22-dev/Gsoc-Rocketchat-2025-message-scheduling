# Google Summer of Code 2025 – Rocket.Chat

<div align="center">
  <a href="https://summerofcode.withgoogle.com/programs/2025/projects/NoRi8SdE">
    <img src="https://summerofcode.withgoogle.com/assets/media/logo.svg" alt="Google Summer of Code">
  </a>
</div>

**Implement a native message scheduling feature for Rocket.Chat to enhance global collaboration.**

This project introduces a native message scheduling feature in Rocket.Chat, empowering users to schedule messages for future delivery — especially useful for global teams spread across multiple time zones.

This repository serves as both the final report of my Google Summer of Code 2025 project and a reference guide for future contributors.

---

## 📌 Project Abstract

Rocket.Chat users across different time zones often need to deliver messages at optimal times. This project implements a native message scheduling system that includes:

- A UI-integrated message scheduler
- A backend cron job to deliver messages at the scheduled time
- A management interface to view, edit, or cancel scheduled messages

---

## 🚢 Deliverables

### Core Functionality

- Message scheduling logic and UI implemented
- Cron job `sendScheduledMessages` reliably sends scheduled messages
- Contextual bar UI for viewing, editing, and canceling scheduled messages

### MongoDB

- A `ScheduledMessages` collection to persist scheduled messages

### APIs

- `chat.scheduleMessage`: Schedule a message
- `chat.getScheduledMessages`: Retrieve scheduled messages
- `chat.cancelScheduledMessage`: Cancel a scheduled message
- `chat.updateScheduledMessage`: Update a scheduled message

### Cron Job

- Periodic job that handles message delivery with detailed logging

### Internationalization

- Localization updates for multilingual support

### Error Handling

- Robust error handling across all scheduling and delivery operations

---

## 🎥 Demo

### 📸 Screenshots

1. **Scheduling Button (Clock Icon)**  
   Located next to the send button in the message composer.  
   ![Scheduling Button](https://github.com/user-attachments/assets/7eb2ee78-6642-4aa6-86f1-236b73b4b899)

2. **Schedule Composer Modal**  
   Lets users pick a date and time for message delivery.  
   ![Schedule Composer Modal](https://via.placeholder.com/600x400.png?text=Schedule+Composer+Modal)

3. **Success Toast Notification**  
   Confirms successful scheduling.  
   ![Success Toast Notification](https://via.placeholder.com/600x400.png?text=Success+Toast+Notification)

4. **API Success Payload**  
   Response payload from `chat.scheduleMessage` API.  
   ![API Success Payload](https://via.placeholder.com/600x400.png?text=API+Success+Payload)

5. **Scheduled Messages Page**  
   Manage, edit, and cancel scheduled messages.  
   ![Scheduled Messages Page](https://via.placeholder.com/600x400.png?text=Scheduled+Messages+Page)

6. **Delivered Message**  
   The scheduled message appears in the chat at the scheduled time.  
   ![Sent Scheduled Message](https://via.placeholder.com/600x400.png?text=Sent+Scheduled+Message)

### 🎬 Demo Video

![Full Cycle Demo Video](https://via.placeholder.com/600x400.png?text=Full+Cycle+Demo+Video)

---

## 📈 Project Status

### ✅ Completed

- Full scheduling flow (UI + API + DB) implemented and **merged upstream**
- Cron job and error handling are functional
- UI/UX is consistent with Rocket.Chat design

### ❌ Not Implemented

- **Thread Support**: Scheduling messages inside threads
- **Image Attachments**: Support for scheduling messages with image/file uploads

### 🔧 Pending

- More testing for edge cases
- UX polish and additional scheduling options

---

## 🛠️ Future Work

- **Thread Scheduling**: Enhance support to allow scheduled messages inside threads
- **Media Attachments**: Schedule messages with media (images, videos, files)

---

## 📂 Contributions

### 🔃 Pull Requests

| PR ID | Title |
| --- | --- |
| [#36291](https://github.com/RocketChat/Rocket.Chat/pull/36291) | feat: message scheduling |
| [#36513](https://github.com/RocketChat/Rocket.Chat/pull/36513) | feat: add full scheduled messages management |

---

## 👨‍🏫 Mentors

Huge thanks to my mentors for their support, timely reviews, and guidance throughout the program.

- **Abhinav Kumar** – [GitHub](https://github.com/Abhinav-Kumar-Dev) | [Rocket.Chat](https://open.rocket.chat/direct/abhinav.kumar)
- **Ricardo Garim** – [GitHub](https://github.com/ricardogarim) | [Rocket.Chat](https://open.rocket.chat/direct/ricardo.garim)

---

## 🔗 Useful Links

- 📄 [Project Proposal](https://docs.google.com/document/d/1ODAdD0BKT3o8NvSaxx38VfGNjYDipjMpZv73FaXwv2k/edit?usp=sharing)  
- 💻 [Rocket.Chat Repo](https://github.com/RocketChat/Rocket.Chat)  
- 🌐 [GSoC Project Page](https://summerofcode.withgoogle.com/programs/2025/projects/NoRi8SdE)

---

## 💖 Support

If you found this useful, consider giving this repo a ⭐ for good karma!

---

## 💬 Connect with Me

| --- | --- |
| **Student** | Thotsem Jajo |
| **Organization** | [Rocket.Chat](https://rocket.chat/) |
| **Project** | [Message Scheduling 2025](https://summerofcode.withgoogle.com/programs/2025/projects/NoRi8SdE) |
| **GitHub** | [sem22-dev](https://github.com/sem22-dev/) |
| **LinkedIn** | [Thotsem Jajo](https://www.linkedin.com/in/thotsem-jajo-30909a244/) |
| **Twitter** | [@Thotsem22](https://x.com/Thotsem22) |
| **Email** | thotsemj@gmail.com |
| **Rocket.Chat** | [sem.jajo](https://open.rocket.chat/direct/sem.jajo) |

---

Thank you, Rocket.Chat and Google Summer of Code, for this amazing opportunity!
