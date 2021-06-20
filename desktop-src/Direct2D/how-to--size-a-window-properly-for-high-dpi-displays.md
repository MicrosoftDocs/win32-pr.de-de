---
title: Ordnungsgemäße Anzeige auf einer Anzeige mit hohem DPI-Anteil
description: Beschreibt die Schritte zum Erstellen eines Fensters für Ihre Anwendung, das ordnungsgemäß auf Anzeigen mit hohen DPI-Daten angezeigt wird.
ms.assetid: 72a4b076-1cf0-4dc9-bd75-43b5173fc2a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dd45b4b654556fc251575410cc11f9b66961263
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406153"
---
# <a name="displaying-properly-on-a-high-dpi-display"></a><span data-ttu-id="c1cdc-103">Ordnungsgemäße Anzeige auf einer Anzeige mit hohem DPI-Anteil</span><span class="sxs-lookup"><span data-stu-id="c1cdc-103">Displaying properly on a high-DPI display</span></span>

<span data-ttu-id="c1cdc-104">Obwohl Direct2D viele Probleme mit hohen DPI-Daten für Sie behandelt, sollten Sie zwei Schritte ausführen, um sicherzustellen, dass Ihre Anwendung ordnungsgemäß auf Anzeigen mit hohen DPI-Daten funktioniert:</span><span class="sxs-lookup"><span data-stu-id="c1cdc-104">Although Direct2D addresses many high-DPI issues for you, there are two steps you should take to ensure that your application works properly on high-DPI displays:</span></span>

-   [<span data-ttu-id="c1cdc-105">Schritt 1: Verwenden des System-DPI beim Erstellen von Windows</span><span class="sxs-lookup"><span data-stu-id="c1cdc-105">Step 1: Use the System DPI When Creating Windows</span></span>](#step-1-use-the-system-dpi-when-creating-windows)
-   [<span data-ttu-id="c1cdc-106">Schritt 2: Deklarieren, dass die Anwendung DPI-fähige Anwendung ist</span><span class="sxs-lookup"><span data-stu-id="c1cdc-106">Step 2: Declare That the Application is DPI-Aware</span></span>](#step-2-declare-that-the-application-is-dpi-aware)
-   [<span data-ttu-id="c1cdc-107">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="c1cdc-107">Related topics</span></span>](#related-topics)

## <a name="step-1-use-the-system-dpi-when-creating-windows"></a><span data-ttu-id="c1cdc-108">Schritt 1: Verwenden des System-DPI beim Erstellen von Windows</span><span class="sxs-lookup"><span data-stu-id="c1cdc-108">Step 1: Use the System DPI When Creating Windows</span></span>

<span data-ttu-id="c1cdc-109">Die [**ID2D1Factory-Schnittstelle**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) stellt die [**GetDesktopDpi-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) zum Abrufen des System-DPI bereit.</span><span class="sxs-lookup"><span data-stu-id="c1cdc-109">The [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) interface provides the [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) method for retrieving the system DPI.</span></span> <span data-ttu-id="c1cdc-110">Sie stellt die horizontalen und vertikalen Abmessungen der Anzeige in DPI (Dots per Inch) bereit.</span><span class="sxs-lookup"><span data-stu-id="c1cdc-110">It provides the horizontal and vertical dimensions of the display in dots per inch (DPI).</span></span> <span data-ttu-id="c1cdc-111">Verwenden Sie die folgende Formel, um diese Werte zum Festlegen der Breite eines Fensters zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="c1cdc-111">To use these values to set the width of a window, use the following formula:</span></span>

<span data-ttu-id="c1cdc-112"><*Horizontaler DPI* >  \*  < *width*, in Pixeln>/<*horizontalen Standard-DPI*></span><span class="sxs-lookup"><span data-stu-id="c1cdc-112"><*horizontal DPI*> \* <*width*, in pixels> / <*default horizontal DPI*></span></span>

<span data-ttu-id="c1cdc-113">... Dabei ist *horizontaler DPI* der von [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) wiederholte Wert und *horizontaler Standard-DPI* 96.</span><span class="sxs-lookup"><span data-stu-id="c1cdc-113">...where *horizontal DPI* is the value retrived by [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) and *default horizontal DPI* is 96.</span></span> <span data-ttu-id="c1cdc-114">Die Formel ist für die vertikale Größe ähnlich:</span><span class="sxs-lookup"><span data-stu-id="c1cdc-114">The formula is similar for the vertical size:</span></span>

<span data-ttu-id="c1cdc-115"><*Vertikaler DPI* >  \*  < *height*, in Pixeln>/<*vertikaler Standard-DPI*></span><span class="sxs-lookup"><span data-stu-id="c1cdc-115"><*vertical DPI*> \* <*height*, in pixels> / <*default vertical DPI*></span></span>

<span data-ttu-id="c1cdc-116">... dabei ist *vertical DPI* der Wert, der von der [**GetDesktopDpi-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) abgerufen wird, und *der vertikale DPI-Standardwert* ist 96.</span><span class="sxs-lookup"><span data-stu-id="c1cdc-116">...where *vertical DPI* is the value retrieved by the [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) method and *default vertical DPI* is 96.</span></span>

<span data-ttu-id="c1cdc-117">Der folgende Code verwendet die [**GetDesktopDpi-Methode,**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) um den System-DPI abzurufen, und erstellt dann ein 640 × 480-Fenster, das auf den System-DPI skaliert wird.</span><span class="sxs-lookup"><span data-stu-id="c1cdc-117">The following code uses the [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) method to retrieve the system DPI and then creates a 640 × 480 window, scaled to the system DPI.</span></span>


```C++
        // Because the CreateWindow function takes its size in pixels,
        // obtain the system DPI and use it to scale the window size.
        FLOAT dpiX, dpiY;

        // The factory returns the current system DPI. This is also the value it will use
        // to create its own windows.
        m_pDirect2dFactory->GetDesktopDpi(&dpiX, &dpiY);


        // Create the window.
        m_hwnd = CreateWindow(
            L"D2DDemoApp",
            L"Direct2D Demo App",
            WS_OVERLAPPEDWINDOW,
            CW_USEDEFAULT,
            CW_USEDEFAULT,
            static_cast<UINT>(ceil(640.f * dpiX / 96.f)),
            static_cast<UINT>(ceil(480.f * dpiY / 96.f)),
            NULL,
            NULL,
            HINST_THISCOMPONENT,
            this
            );
```



> [!Note]
>
> <span data-ttu-id="c1cdc-118">Ab Windows 8 können Sie die [**Windows::Graphics::D isplay::D isplayProperties-Klasse**](/uwp/api/Windows.Graphics.Display.DisplayProperties) verwenden, um den System-DPI abzurufen.</span><span class="sxs-lookup"><span data-stu-id="c1cdc-118">Starting with Windows 8, you can use the [**Windows::Graphics::Display::DisplayProperties**](/uwp/api/Windows.Graphics.Display.DisplayProperties) class to get the system DPI.</span></span>

 

## <a name="step-2-declare-that-the-application-is-dpi-aware"></a><span data-ttu-id="c1cdc-119">Schritt 2: Deklarieren, dass die Anwendung DPI-Aware</span><span class="sxs-lookup"><span data-stu-id="c1cdc-119">Step 2: Declare That the Application is DPI-Aware</span></span>

<span data-ttu-id="c1cdc-120">Wenn eine Anwendung sich selbst als DPI-fähige Anwendung deklariert, handelt es sich um eine Anweisung, die angibt, dass sich die Anwendung bei DPI-Einstellungen bis zu 200 DPI gut verhält.</span><span class="sxs-lookup"><span data-stu-id="c1cdc-120">When an application declares itself to be DPI-aware, it is a statement specifying that the application behaves well at DPI settings up to 200 DPI.</span></span> <span data-ttu-id="c1cdc-121">Wenn die DPI-Virtualisierung in Windows Vista und Windows 7 aktiviert ist, werden Anwendungen, die nicht DPI-fähig sind, skaliert, und Anwendungen empfangen virtualisierte Daten von den System-APIs, z. B. der [**GetSystemMetric-Funktion.**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics)</span><span class="sxs-lookup"><span data-stu-id="c1cdc-121">In Windows Vista and Windows 7, when DPI virtualization is enabled, applications that are not DPI-aware are scaled, and applications receive virtualized data from the system APIs, such as the [**GetSystemMetric**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) function.</span></span> <span data-ttu-id="c1cdc-122">Führen Sie die folgenden Schritte aus, um zu deklarieren, dass Ihre Anwendung DPI-fähige Anwendung ist.</span><span class="sxs-lookup"><span data-stu-id="c1cdc-122">To declare that your application is DPI-aware, complete the following steps.</span></span>

1.  <span data-ttu-id="c1cdc-123">Erstellen Sie eine Datei namens DeclareDPIAware.manifest.</span><span class="sxs-lookup"><span data-stu-id="c1cdc-123">Create a file called DeclareDPIAware.manifest.</span></span>
2.  <span data-ttu-id="c1cdc-124">Kopieren Sie den folgenden XML-Code in die Datei, und speichern Sie ihn:</span><span class="sxs-lookup"><span data-stu-id="c1cdc-124">Copy the following xml into the file and save it:</span></span>
    ```C++
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3" >
      <asmv3:application>
        <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">
          <dpiAware>true</dpiAware>
        </asmv3:windowsSettings>
      </asmv3:application>
    </assembly>
    ```

    

3.  <span data-ttu-id="c1cdc-125">Fügen Sie in der VCPROJ-Datei des Projekts in jedem Configuration-Element unter VisualStudioProject/Configurations den folgenden Eintrag hinzu:</span><span class="sxs-lookup"><span data-stu-id="c1cdc-125">In the project's .vcproj file, add the following entry inside each Configuration element under VisualStudioProject/Configurations:</span></span>
    ```C++
    <Tool
        Name="VCManifestTool"
        AdditionalManifestFiles="DeclareDPIAware.manifest"
    />
    ```

    

## <a name="related-topics"></a><span data-ttu-id="c1cdc-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c1cdc-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1cdc-127">Direct2D und High-DPI</span><span class="sxs-lookup"><span data-stu-id="c1cdc-127">Direct2D and High-DPI</span></span>](direct2d-and-high-dpi.md)
</dt> </dl>

 

 