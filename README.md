<h1 align="center">Android PdfViewer</h1><br/>
<p align="center"> 
An Android PDF Library provides developers with the tools to display, manipulate, and create PDF files in Android applications. These libraries make it easier to handle PDFs in an efficient and user-friendly way without needing to develop complex PDF rendering from scratch. Android PDF libraries can handle a variety of tasks such as displaying PDF pages, zooming, annotating, and handling text selection. 🚀
</p>
<br/>

<p align="center">
  
</p>

## Key Features of an Android PDF Library
1.PDF Rendering: Most libraries allow rendering PDF documents within your app, with the ability to display pages, zoom, and scroll. This makes it easy to embed PDFs in apps without needing a separate PDF viewer.

2.Text Selection and Search: Some libraries support selecting text from PDFs and searching for specific terms within the document.

3.Annotations: Many PDF libraries provide annotation features, allowing users to highlight, underline, or add notes to PDF content.

4.Offline PDF Viewing: PDFs can be loaded and displayed offline without requiring a network connection, which is beneficial for users who need access to documents in remote areas.

5.Pagination and Navigation: Users can easily navigate between pages in a document, jump to specific pages, and even create bookmarks for important sections.

6.File Support: Libraries generally support local files (from the app's file system) or remote files (from a URL or cloud storage).

7.Compatibility: These libraries are compatible with different versions of Android, offering a consistent experience across a wide range of devices.

## Including in your project

### Gradle
Add below codes to your **root** `build.gradle` file (not your module build.gradle file) or settings.gradle.
```gradle
allprojects {
  repositories {
    ...
    mavenCentral()
    maven { url 'https://jitpack.io' }
    //If Not Work
    mavenCentral()
     maven { url = uri("https://jitpack.io") }
  }
}
```
And add a dependency code to your **module**'s `build.gradle` file.
```gradle
dependencies {
 implementation 'com.github.shamimcse1:AndroidPdfViewer:1.0'
	}
```

## Basic Usage
Coming Soon......
```kotlin

```
<h1 align="center">Screenshot</h1>
<br/>
## Coming Soon......

## License
```
    Copyright 2023 Md. Shamim Hossain

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
