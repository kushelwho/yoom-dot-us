# Yoom - A Zoom Clone

A feature-rich video conferencing application built with the latest web technologies, replicating the core functionalities of Zoom. This application provides secure authentication, real-time video/audio streaming, and comprehensive meeting management features.

## ✨ Features

- **🔐 Secure Authentication**: Robust user login and registration system powered by Clerk, supporting social sign-on and traditional email/password methods.
- **📹 Create & Start Meetings**: Instantly create new meetings with a unique meeting ID.
- **🤝 Join Meetings**: Seamlessly join existing meetings using the meeting link.
- **🗓️ Schedule Meetings**: Plan meetings for a future date and time.
- **📺 Meeting Views**: View upcoming, previous, and recorded meetings in dedicated sections.
- **🏠 Personal Room**: A dedicated personal meeting room with a permanent link for instant meetings.
- **🎥 In-Meeting Controls**: Full control over camera, microphone, screen sharing, and participant management.
- **📱 Responsive Design**: A mobile-first design that ensures a consistent and optimal experience across all devices.

## ⚙️ Tech Stack

- **Framework**: [Next.js](https://nextjs.org/)
- **Language**: [TypeScript](https://www.typescriptlang.org/)
- **Authentication**: [Clerk](https://clerk.com/)
- **Video & Audio**: [Stream](https://getstream.io/)
- **Styling**: [Tailwind CSS](https://tailwindcss.com/)
- **UI Components**: [shadcn/ui](https://ui.shadcn.com/)

## 🚀 Getting Started

Follow these instructions to set up and run the project on your local machine.

### Prerequisites

Make sure you have the following installed:

- [Node.js](https://nodejs.org/en) (v18 or later recommended)
- [npm](https://www.npmjs.com/) (Node Package Manager)

### 1. Clone the Repository

First, clone the project repository to your local machine:

```bash
git clone https://github.com/adrianhajdin/zoom-clone.git
cd zoom-clone
```

### 2. Install Dependencies

Install the necessary project dependencies using npm:

```bash
npm install
```

### 3. Set Up Environment Variables

This step is crucial for the application to function correctly. Create a new file named `.env.local` in the root of your project and add the following environment variables:

```env
NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=
CLERK_SECRET_KEY=

NEXT_PUBLIC_STREAM_API_KEY=
STREAM_SECRET_KEY=
```

You need to replace the placeholder values with your actual credentials from the following services:

- **Clerk**: Get your keys from your [Clerk Dashboard](https://dashboard.clerk.com/).
- **Stream**: Get your keys from your [Stream Dashboard](https://dashboard.stream-io.com/).

### 4. Run the Development Server

Once the setup is complete, you can run the development server:

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser to see the application in action.

## 📂 Folder Structure

Here is a high-level overview of the project's folder structure:

```
/
├── actions/            # Server-side actions (e.g., token generation)
├── app/                # Next.js App Router, contains all pages and layouts
│   ├── (auth)/         # Authentication-related pages (sign-in, sign-up)
│   ├── (root)/         # Core application pages after login
│   └── layout.tsx      # Root layout of the application
├── components/         # Reusable UI components
│   └── ui/             # Components from shadcn/ui
├── constants/          # Application constants (e.g., navigation links)
├── hooks/              # Custom React hooks
├── lib/                # Utility functions
├── providers/          # React Context providers (e.g., Stream client)
├── public/             # Static assets (icons, images)
└── ...                 # Configuration files
```
