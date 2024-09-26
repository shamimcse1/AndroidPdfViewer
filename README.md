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
## ProGuard
If you are using ProGuard, add following rule to proguard config file:

```proguard
-keep class com.shockwave.**
```
## Include PDFView in your layout

``` xml
 <com.codercamp.shamimpdfviewer.PDFView
        android:id="@+id/pdfView"
        android:layout_width="match_parent"
        android:layout_height="match_parent"/>

```

## Load a PDF file

All available options with default values:
``` java
pdfView.fromUri(Uri)
or
pdfView.fromFile(File)
or
pdfView.fromBytes(byte[])
or
pdfView.fromStream(InputStream) // stream is written to bytearray - native code cannot use Java Streams
or
pdfView.fromSource(DocumentSource)
or
pdfView.fromAsset(String)
    .pages(0, 2, 1, 3, 3, 3) // all pages are displayed by default
    .enableSwipe(true) // allows to block changing pages using swipe
    .swipeHorizontal(false)
    .enableDoubletap(true)
    .defaultPage(0)
    // allows to draw something on the current page, usually visible in the middle of the screen
    .onDraw(onDrawListener)
    // allows to draw something on all pages, separately for every page. Called only for visible pages
    .onDrawAll(onDrawListener)
    .onLoad(onLoadCompleteListener) // called after document is loaded and starts to be rendered
    .onPageChange(onPageChangeListener)
    .onPageScroll(onPageScrollListener)
    .onError(onErrorListener)
    .onPageError(onPageErrorListener)
    .onRender(onRenderListener) // called after document is rendered for the first time
    // called on single tap, return true if handled, false to toggle scroll handle visibility
    .onTap(onTapListener)
    .onLongPress(onLongPressListener)
    .enableAnnotationRendering(false) // render annotations (such as comments, colors or forms)
    .password(null)
    .scrollHandle(null)
    .enableAntialiasing(true) // improve rendering a little bit on low-res screens
    // spacing between pages in dp. To define spacing color, set view background
    .spacing(0)
    .autoSpacing(false) // add dynamic spacing to fit each page on its own on the screen
    .linkHandler(DefaultLinkHandler)
    .pageFitPolicy(FitPolicy.WIDTH) // mode to fit pages in the view
    .fitEachPage(false) // fit each page to the view, else smaller pages are scaled relative to largest page.
    .pageSnap(false) // snap pages to screen boundaries
    .pageFling(false) // make a fling change only a single page like ViewPager
    .nightMode(false) // toggle night mode
    .load();
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
