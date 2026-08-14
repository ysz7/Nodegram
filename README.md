

# Nodegram

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](./LICENSE)
![Node.js](https://img.shields.io/badge/Node.js-18%2B-green)
![React](https://img.shields.io/badge/React-18-blue)
![TypeScript](https://img.shields.io/badge/TypeScript-5-blue)
![Vite](https://img.shields.io/badge/Vite-6-purple)
![Zustand](https://img.shields.io/badge/State-Zustand-orange)

A modern React application for managing nodes and their connections, built with Feature-Sliced Design (FSD) architecture.

## 📸 Screenshots

<div align="center">
  <img src="assets/ng_workspace_2.png" alt="Workspace Overview" width="800"/>
  <p><em>Visual workspace with node connections</em></p>
</div>

<div align="center">
  <img src="assets/ng_workspace_5.png" alt="Large Graph View" width="800"/>
  <p><em>Complex network graph visualization</em></p>
</div>

<div align="center">
  <img src="assets/ng_workspace_4.png" alt="Node Types" width="800"/>
  <p><em>Multiple node types and creation interface</em></p>
</div>

## 🎯 Overview

Nodegram is a visual workspace application that allows you to create, organize, and connect nodes representing different types of information. It provides an intuitive interface for managing complex relationships between data points.

## 📁 Repository Structure

This is a monorepo that contains:

- **`client/`** - Web application (React + TypeScript + Vite)
  - Open source and available to everyone
  - Can be used as a standalone web application
  - Full source code access

**Future additions (planned):**
- **`desktop/`** - Desktop application (Electron/Tauri)
- **`mobile/`** - Mobile application (React Native/Flutter)

## ✨ Features

- **🔗 Node Management**: Create, edit, delete, and organize nodes of various types
- **📊 Visual Connections**: Connect nodes to represent relationships
- **🎨 Multiple Node Types**: Support for 17 different node types (Begin Node, Event, Team, Person, Inventory, Orders, Finance, Branch, Document, Timeline, Synapse, Documentation, Tasks, Chronology, Big Image)
- **💾 Workspace Management**: Multiple workspaces with local storage persistence
- **🖱️ Interactive Graph**: Pan, zoom, and navigate through your workspace
- **🎭 Modern UI**: Built with Material-UI and D3.js for smooth interactions

## 🛠️ Tech Stack

- **React 18.3** - UI library
- **TypeScript** - Type safety
- **Vite** - Build tool and dev server
- **Zustand** - State management
- **D3.js** - Graph visualization
- **Material-UI v7** - Component library
- **React Router v7** - Routing

## 📂 Project Structure

### Repository Structure

```
├── client/          # Web application (React + TypeScript)
│   ├── src/         # Source code
│   └── package.json
├── desktop/         # Desktop app (planned)
├── mobile/          # Mobile app (planned)
├── assets/          # Screenshots and images
└── README.md        # This file
```

### Web Application Structure (client/)

The web application follows the Feature-Sliced Design (FSD) architecture:

```
client/src/
├── app/           # Application initialization, providers
├── pages/         # Page components
├── widgets/       # Complex UI blocks (NodeGraph, WorkspaceToolbar, etc.)
├── features/     # Business features (create-node, node-connection, etc.)
├── entities/     # Business entities (node, workspace)
├── shared/       # Shared resources (UI components, utilities, API, store)
└── utils/        # Utility functions
```

### Architecture Layers

- **app**: Application setup, providers, routing
- **pages**: Page-level components
- **widgets**: Complex UI compositions
- **features**: Business features (user actions)
- **entities**: Business entities (domain models)
- **shared**: Reusable resources (UI kit, utilities, API, store)

## 🚀 Getting Started

### Prerequisites

- Git
- Node.js 18+ 
- npm or yarn

### Installation

1. Clone the repository:
```bash
git clone https://github.com/ysz7/Nodegram.git
cd Nodegram/client
```

> **Note:** The `client/` directory contains the complete, open-source web application. All source code is available and can be used independently.

2. Install dependencies:
```bash
npm install
```

3. Start the development server:
```bash
npm run dev
```

The application will be available at `http://localhost:5173`

### Build for Production

```bash
npm run build
```

The production build will be in the `dist` directory.

## 📜 Available Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run preview` - Preview production build
- `npm run lint` - Run ESLint
- `npm run type-check` - Run TypeScript type checking
- `npm run format` - Format code with Prettier
- `npm run format:check` - Check code formatting

## 🗄️ State Management

The application uses Zustand for state management. The main store is located in `client/src/shared/store/workspaceStore.ts` and manages:

- Workspace state (nodes, links, calendar)
- UI state (modals, loading states)
- Workspace management (current workspace, workspaces list)

## 💾 Data Persistence

Data is stored locally in the browser's localStorage. Each workspace is saved with a unique workspace ID (wid).

## 🤝 Contributing

Please read [CONTRIBUTING.md](./CONTRIBUTING.md) for details on our code of conduct and the process for submitting pull requests.

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](./LICENSE) file for details.

## 📚 Documentation

- [ARCHITECTURE.md](./ARCHITECTURE.md) - Detailed architecture documentation
- [CONTRIBUTING.md](./CONTRIBUTING.md) - Contribution guidelines
- [CODE_OF_CONDUCT.md](./CODE_OF_CONDUCT.md) - Code of conduct
- [CHANGELOG.md](./CHANGELOG.md) - Changelog

## 💬 Support

For issues and feature requests, please use the GitHub Issues page.
