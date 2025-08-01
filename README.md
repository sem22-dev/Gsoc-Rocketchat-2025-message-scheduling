# Google Summer of Code 2023, Rocket.Chat

![google-summer-of-code](https://i.imgur.com/pgkUceb.png)

**Implement a native message scheduling feature for Rocket.Chat to enhance global collaboration.**

I worked on a project to implement a native message scheduling feature for Rocket.Chat, enabling users to schedule messages for optimal delivery across time zones. This repository serves as the final report summary of my GSoC 2023 project and a guide for future contributors.

## ⭐ Project Abstract

Rocket.Chat users across multiple time zones need a way to schedule messages for optimal delivery, enhancing global collaboration. This project implemented a native message scheduling feature by integrating a scheduling UI, a cron job to send messages at the designated time, and a contextual bar UI to view and cancel scheduled messages. The deliverables include a MongoDB collection for scheduled messages, APIs (`chat.scheduleMessage`, `chat.getScheduledMessages`, `chat.cancelScheduledMessage`), a cron job (`sendScheduledMessages`), scheduling and management UIs, error handling, documentation, and unit tests.

## 🚢 Deliverables

- **Core Functionality**:
  - Users can schedule messages via a seamless UI integrated with the existing send button.
  - A cron job (`sendScheduledMessages`) reliably sends messages at the designated time.
  - A contextual bar UI allows users to view, edit, and cancel scheduled messages.
- **MongoDB Collection**: A `ScheduledMessages` model to store scheduled messages.
- **APIs**:
  - `chat.scheduleMessage`: Schedule a new message.
  - `chat.getScheduledMessages`: Retrieve scheduled messages.
  - `chat.cancelScheduledMessage`: Cancel a scheduled message.
- **User Interfaces**:
  - `ScheduleComposerModal`: Modal for scheduling messages.
  - `ScheduledMessagesPage`: Dedicated page for managing scheduled messages.
  - `DeleteScheduledMessageModal` and `EditScheduledMessageModal`: Modals for deleting and editing scheduled messages.
- **Cron Job**: Handles scheduled message delivery with robust logging.
- **Internationalization**: Updated localization files for multilingual support.
- **Error Handling**: Robust error handling for scheduling and sending messages.
- **Documentation and Tests**: Comprehensive documentation and unit tests for APIs and cron jobs.

## Demo

### Screenshots

Below are screenshots demonstrating the message scheduling feature:

1. **Scheduling UI Button**: The scheduling button in the message composer, accessible next to the send button.
   ![Scheduling Button]![IMG_3818](https://github.com/user-attachments/assets/7eb2ee78-6642-4aa6-86f1-236b73b4b899)
()

2. **Schedule Composer Modal**: Clicking the scheduling button opens the `ScheduleComposerModal`, allowing users to select a date and time for message delivery.
   ![Schedule Composer Modal](https://via.placeholder.com/600x400.png?text=Schedule+Composer+Modal)

3. **Success Toast Notification**: After confirming the schedule, a toast notification confirms the message has been scheduled successfully.
   ![Success Toast Notification](https://via.placeholder.com/600x400.png?text=Success+Toast+Notification)

4. **API Success Payload**: The API response for a successful `chat.scheduleMessage` call, showing the scheduled message details.
   ![API Success Payload](https://via.placeholder.com/600x400.png?text=API+Success+Payload)

5. **Scheduled Messages Page**: The `ScheduledMessagesPage` displays a list of scheduled messages, with options to edit or cancel each message.
   ![Scheduled Messages Page](https://via.placeholder.com/600x400.png?text=Scheduled+Messages+Page)

6. **Scheduled Message Sent**: The scheduled message appears in the channel or DM at the designated time.
   ![Sent Scheduled Message](https://via.placeholder.com/600x400.png?text=Sent+Scheduled+Message)

### Full Cycle Demo Video

This video demonstrates the complete message scheduling workflow:
- Scheduling a message using the `ScheduleComposerModal`.
- Navigating to the `ScheduledMessagesPage` to view, edit, or cancel the scheduled message.
- Returning to the channel or DM to see the scheduled message appear in real-time.

![Full Cycle Demo Video](https://via.placeholder.com/600x400.png?text=Full+Cycle+Demo+Video)

## Current State

- **Completed**:
  - Core scheduling functionality, APIs, and UIs are fully implemented and merged upstream.
  - The cron job reliably sends scheduled messages.
  - Error handling ensures robust operation.
  - Documentation and unit tests are in place.
- **Not Implemented**:
  - Thread support for scheduling messages in threads.
  - Image attachment support for scheduled messages.
- **Merged Upstream**: All core deliverables are merged into the Rocket.Chat main repository.
- **Pending**:
  - Additional testing for edge cases.
  - Enhancements like thread and image support.

## What's Left to Do

- **Thread Support**: Extend scheduling to support messages in threads, requiring updates to the `ScheduledMessages` model and APIs.
- **Image Attachments**: Allow scheduling messages with images, integrating with Rocket.Chat’s file upload system.
- **Enhanced Notifications**: Add notifications for scheduled message status (e.g., sent, canceled).
- **Performance Optimization**: Optimize the cron job for large-scale deployments.
- **Additional Tests**: Write more unit and integration tests for edge cases.

## Challenges and Learnings

- **Challenges**:
  - **Cron Job Reliability**: Ensuring the cron job runs consistently across server restarts required careful configuration.
  - **UI Integration**: Integrating the scheduling modal with the existing message composer while maintaining a seamless user experience was complex due to React state management.
  - **Time Zone Handling**: Managing time zones for scheduling required robust date handling to avoid discrepancies.
- **Learnings**:
  - Gained expertise in TypeScript, React, and MongoDB through building production-ready features.
  - Learned about cron job implementation and scheduling in Node.js.
  - Improved skills in writing clear documentation and unit tests.
  - Understood the importance of community collaboration in open-source projects through code reviews and mentor feedback.

## 🚀 Contributions

### Pull Requests to Rocket.Chat

| PR ID | Title with Link |
| --- | --- |
| TBD | [NEW] Message Scheduling Core Functionality [Link](#) |
| TBD | [NEW] Scheduling UI and Composer Modal [Link](#) |
| TBD | [NEW] Scheduled Messages Management UI [Link](#) |
| TBD | [NEW] Cron Job for Sending Scheduled Messages [Link](#) |
| TBD | [IMPROVE] Error Handling and Tests [Link](#) |

*Note: Replace TBD with actual PR IDs and links to your pull requests.*

[View all PRs to Rocket.Chat](https://github.com/RocketChat/Rocket.Chat/pulls?q=is%3Apr+author%3A[YourGitHubUsername])

### Other Contributions

- Contributed to Rocket.Chat’s internationalization by updating localization files.
- Participated in community discussions and code reviews.

## 🎓 Mentor

A huge thank you to my mentor for their guidance and support throughout GSoC. Their feedback was invaluable in navigating challenges and ensuring a production-ready implementation.

- **[Mentor Name]** - [GitHub](#), [LinkedIn](#), [Twitter](#)

*Note: Replace with your mentor’s details.*

## 🔗 Links

- Project proposal: [Link to your proposal](#)
- GSoC presentation: [Link to your presentation](#)
- Presentation video (if available): [Link to video](#)
- Rocket.Chat repository: [Rocket.Chat](https://github.com/RocketChat/Rocket.Chat)
- GSoC project page: [Message Scheduling 2023](#)

*Note: Replace placeholders with actual links.*

## ❤️ Support

Learned something new? Star this repo for good karma! ⭐

## 💬 Connect With Me

Let’s discuss GSoC, Rocket.Chat, or open-source!

| **Student** | [Your Name] |
| --- | --- |
| **Organization** | [Rocket.Chat](https://rocket.chat/) |
| **Project** | [Message Scheduling 2023](#) |
| **GitHub** | [@YourGitHubUsername](#) |
| **LinkedIn** | [YourLinkedIn](#) |
| **Twitter** | [YourTwitter](#) |
| **Website** | [YourWebsite](#) |
| **Email** | [YourEmail](#) |
| **Rocket.Chat** | [YourRocketChatUsername](#) |

*Note: Replace placeholders with your personal details.*
