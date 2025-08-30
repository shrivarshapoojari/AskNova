# AskNova 🚀

A modern Q&A platform built with Next.js 15, TypeScript, and Appwrite. AskNova provides a seamless experience for users to ask questions, provide answers, and build their reputation through community engagement.

## Project Overview

AskNova is a Stack Overflow-inspired platform that allows users to:
- Ask and answer questions
- Vote on content quality
- Build reputation through community contributions
- Manage their profile and track activity

**Tech Stack:**
- **Frontend**: Next.js 15, TypeScript, Tailwind CSS, Radix UI
- **Backend**: Appwrite (Authentication, Database, Storage)
- **State Management**: Zustand with Immer
- **UI Components**: Radix UI, Tabler Icons, Lucide React

## 🚀 How to Run the Project

### Prerequisites
- Node.js 18+
- npm or yarn
- Appwrite account

### Installation & Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/shrivarshapoojari/AskNova.git
   cd AskNova/asknova
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Environment Configuration**
   
   Create a `.env.local` file in the root directory:
   ```env
   NEXT_PUBLIC_APPWRITE_HOST_URL=https://cloud.appwrite.io/v1
   NEXT_PUBLIC_APPWRITE_PROJECT_ID=your_project_id
   APPWRITE_API_KEY=your_api_key
   ```

4. **Set up Appwrite Database**
   
   Create the following collections in your Appwrite project:
   - `questions` - Store questions
   - `answers` - Store answers  
   - `votes` - Store voting data
   - `comments` - Store comments

5. **Run the development server**
   ```bash
   npm run dev
   ```
   
   Open [http://localhost:3000](http://localhost:3000) to view the application.

## 🚢 How to Deploy the Project

### Deploy on Vercel (Recommended)

1. **Push your code to GitHub**
   ```bash
   git add .
   git commit -m "Ready for deployment"
   git push origin main
   ```

2. **Deploy on Vercel**
   - Go to [vercel.com](https://vercel.com)
   - Import your GitHub repository
   - Add environment variables in Vercel dashboard:
     - `NEXT_PUBLIC_APPWRITE_HOST_URL`
     - `NEXT_PUBLIC_APPWRITE_PROJECT_ID`
     - `APPWRITE_API_KEY`
   - Deploy!

### Alternative Deployment Options

**Netlify:**
```bash
npm run build
# Upload the .next folder to Netlify
```

**Self-hosted:**
```bash
npm run build
npm start
```

**Docker:**
```dockerfile
FROM node:18-alpine
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
RUN npm run build
EXPOSE 3000
CMD ["npm", "start"]
```


 