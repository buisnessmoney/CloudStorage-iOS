# CloudStorage-iOS

UIKit iOS cloud storage app created as a pet project for practicing Swift, UIKit, MVVM, file management, async operations, mock services, unit tests and CI.

## About

CloudStorage-iOS is an educational iOS project that simulates a small cloud storage client.

The project is focused on file management, testable architecture, local file caching and async upload/download flows.
For demo purposes, the project uses a mock cloud service. The architecture allows replacing the mock implementation with a real API later.

## Planned Features

* Files and folders list
* Folder creation
* File upload flow
* File download flow
* Upload and download progress
* Rename file or folder
* Delete file or folder
* File details screen
* Search
* Local file cache
* Loading / error / empty states
* MVVM architecture
* Coordinator navigation
* Protocol-based service layer
* Unit tests
* Basic memory leak prevention
* GitHub Actions CI
* SwiftLint

## Tech Stack

* Swift
* UIKit
* UICollectionView
* DiffableDataSource
* MVVM
* Coordinator
* FileManager
* URLSession
* async/await
* XCTest
* GitHub Actions CI
* SwiftLint

## Architecture

The project will use MVVM with a protocol-based service layer.

Main layers:

* View
* ViewModel
* Model
* CloudStorageService
* LocalFileCache
* UploadService
* DownloadService
* Coordinator

This structure makes the code easier to test, extend and maintain.

## Project Status

In progress.

Current stage:

* Repository created
* Basic project structure planned
* UIKit implementation will be added next

## Roadmap

### Stage 1

* Add project documentation
* Add planned folder structure
* Prepare architecture plan

### Stage 2

* Create UIKit project without Storyboard
* Add AppCoordinator
* Add FilesList module
* Add CloudItem model
* Add CloudStorageServiceProtocol
* Add MockCloudStorageService

### Stage 3

* Implement files and folders list
* Add UICollectionView with DiffableDataSource
* Add loading / error / empty states
* Add folder creation
* Add rename and delete actions

### Stage 4

* Add upload flow
* Add download flow
* Add progress state
* Add LocalFileCache with FileManager
* Add file details screen

### Stage 5

* Add search
* Add unit tests
* Add memory management checks
* Add GitHub Actions CI
* Add SwiftLint

## Author

Created as a pet project for iOS internship preparation.
