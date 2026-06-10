# CloudStorage-iOS Project Plan

## Goal

Create a small UIKit-based cloud storage client that demonstrates practical iOS development skills.

The project should show:

* UIKit without Storyboard
* Modern collection views
* MVVM architecture
* Coordinator navigation
* Protocol-based service layer
* File management with FileManager
* Async upload/download simulation
* Local file cache
* Testable services
* Unit tests
* Basic performance and memory management
* GitHub Actions CI

## Important Note

For demo purposes, the project uses a mock cloud service.

The goal is not to build a production cloud backend.
The goal is to demonstrate clean iOS architecture, async flows, file handling, state management and testability.

The architecture should allow replacing `MockCloudStorageService` with a real network-based service later.

## Main Screens

1. Files List
2. File Details
3. Upload
4. Search
5. Settings

## Core Features

### Files List

* Display files and folders
* Show file name
* Show file type
* Show file size
* Show modified date
* Support loading state
* Support error state
* Support empty state
* Support pull to refresh
* Support folder navigation

### File and Folder Actions

* Create folder
* Rename file or folder
* Delete file or folder
* Open file details
* Search files and folders

### Upload

* Select file for upload
* Start upload using mock service
* Display upload progress
* Display upload success state
* Display upload failure state
* Cancel upload operation

### Download

* Start file download using mock service
* Display download progress
* Save downloaded file to local cache
* Open cached file details
* Cancel download operation

### File Details

* Display file name
* Display file type
* Display file size
* Display created date
* Display modified date
* Display local cache status

### Search

* Search files and folders by name
* Show search results
* Show empty state
* Show error state

## Technical Features

### UI

* UIKit without Storyboard
* UICollectionView
* DiffableDataSource
* Auto Layout in code
* Custom cells
* Reusable UI components
* Context menu actions for files and folders

### Architecture

* MVVM
* Coordinator
* Dependency Injection
* Service layer
* Protocol-oriented design

### Cloud Storage Service

* CloudStorageServiceProtocol
* MockCloudStorageService
* UploadTask simulation
* DownloadTask simulation
* Progress updates
* Cancellable async operations

### File Cache

* LocalFileCache
* FileManager
* Cache directory management
* Save downloaded files locally
* Remove cached files
* Check if file exists in cache

### Models

* CloudItem
* CloudItemType
* UploadState
* DownloadState
* CloudStorageError

### Performance

* Efficient UICollectionView updates with DiffableDataSource
* Avoid unnecessary UI reloads
* Cancel upload/download operations when needed
* Avoid blocking the main thread during file operations

### Memory Management

* Avoid retain cycles in closures
* Use weak references in coordinators and delegates where needed
* Cancel long-running operations when ViewModel is deallocated
* Add basic deallocation tests for ViewModels and Coordinators

### Testing

* Unit tests for FilesListViewModel
* Unit tests for UploadViewModel
* Unit tests for SearchViewModel
* Unit tests for MockCloudStorageService
* Unit tests for LocalFileCache
* Unit tests for upload/download state transitions
* Basic deallocation tests for ViewModels and Coordinators

### CI

* GitHub Actions workflow
* Build project
* Run unit tests
* Run SwiftLint

## Planned Folder Structure

```text
CloudStorage-iOS
├── App
│   ├── AppDelegate.swift
│   ├── SceneDelegate.swift
│   └── AppCoordinator.swift
│
├── Core
│   ├── CloudStorage
│   │   ├── CloudStorageServiceProtocol.swift
│   │   ├── MockCloudStorageService.swift
│   │   ├── CloudStorageError.swift
│   │   ├── UploadState.swift
│   │   └── DownloadState.swift
│   │
│   ├── FileCache
│   │   ├── LocalFileCache.swift
│   │   ├── LocalFileCacheProtocol.swift
│   │   └── FileCacheError.swift
│   │
│   ├── Models
│   │   ├── CloudItem.swift
│   │   └── CloudItemType.swift
│   │
│   └── Extensions
│
├── Features
│   ├── FilesList
│   │   ├── FilesListViewController.swift
│   │   ├── FilesListViewModel.swift
│   │   └── FileCell.swift
│   │
│   ├── FileDetails
│   │   ├── FileDetailsViewController.swift
│   │   └── FileDetailsViewModel.swift
│   │
│   ├── Upload
│   │   ├── UploadViewController.swift
│   │   └── UploadViewModel.swift
│   │
│   ├── Search
│   │   ├── SearchViewController.swift
│   │   └── SearchViewModel.swift
│   │
│   └── Settings
│       ├── SettingsViewController.swift
│       └── SettingsViewModel.swift
│
├── Resources
├── Tests
└── UITests
```

## Development Stages

### Stage 1: Repository Setup

* Create repository
* Add README
* Add project plan
* Add planned folder structure

### Stage 2: UIKit Project Setup

* Create Xcode project
* Remove Storyboard
* Configure root view controller in code
* Add AppCoordinator
* Add basic FilesList screen

### Stage 3: Files List + Mock Service

* Add CloudItem model
* Add CloudItemType model
* Add CloudStorageServiceProtocol
* Add MockCloudStorageService
* Add FilesListViewModel
* Inject CloudStorageServiceProtocol into FilesListViewModel
* Add UICollectionView
* Add DiffableDataSource
* Add FileCell
* Add loading / error / empty states

### Stage 4: File and Folder Actions

* Add folder creation
* Add rename action
* Add delete action
* Add file details screen
* Add folder navigation

### Stage 5: Upload and Download

* Add UploadState
* Add DownloadState
* Add upload simulation
* Add download simulation
* Add progress updates
* Add cancel operation support
* Add upload and download error handling

### Stage 6: Local File Cache

* Add LocalFileCacheProtocol
* Add LocalFileCache
* Add FileManager-based cache directory
* Save downloaded files locally
* Remove cached files
* Check cache status
* Add cache error handling

### Stage 7: Search

* Add Search screen
* Add SearchViewModel
* Add filtering logic
* Add empty state
* Add error state

### Stage 8: Tests and Memory Management

* Add FilesListViewModelTests
* Add UploadViewModelTests
* Add SearchViewModelTests
* Add MockCloudStorageServiceTests
* Add LocalFileCacheTests
* Add upload/download state transition tests
* Add basic deallocation tests for ViewModels
* Add basic deallocation tests for Coordinators

### Stage 9: CI

* Add GitHub Actions workflow
* Run build
* Run tests
* Add SwiftLint
* Add CI badge to README

### Stage 10: Final Polish

* Add screenshots
* Improve README
* Add architecture description
* Add demo GIF
* Prepare project for resume
