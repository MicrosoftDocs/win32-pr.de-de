---
title: So stellen Sie sicher, dass Ihre Anwendung auf Bildschirmen mit hohem DPI-Code ordnungsgemäß angezeigt wird (DirectWrite)
description: Beschreibt, wie Sie sicherstellen können, dass Ihre Anwendung ein Fenster erstellt, das auf Bildschirmen mit hohem DPI-Grad ordnungsgemäß angezeigt wird.
ms.assetid: d174a337-c98e-46c7-86d2-c208900882d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71166d312fe666644c683fe2ece7dd3ced59f765
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406423"
---
# <a name="how-to-ensure-that-your-application-displays-properly-on-high-dpi-displays"></a><span data-ttu-id="9d6b2-103">So stellen Sie sicher, dass Ihre Anwendung ordnungsgemäß auf Bildschirmen mit hohem DPI-Leistung angezeigt wird</span><span class="sxs-lookup"><span data-stu-id="9d6b2-103">How to Ensure That Your Application Displays Properly on High-DPI Displays</span></span>

<span data-ttu-id="9d6b2-104">[Obwohl DirectWrite](direct-write-portal.md) viele Probleme mit hohen DPI-Adressen für Sie behandelt, müssen Sie zwei Schritte ausführen, um sicherzustellen, dass Ihre Anwendung auf Bildschirmen mit hohem DPI-Code ordnungsgemäß funktioniert:</span><span class="sxs-lookup"><span data-stu-id="9d6b2-104">Although [DirectWrite](direct-write-portal.md) addresses many high-DPI issues for you, there are two steps you should take to ensure that your application works properly on high-DPI displays:</span></span>

-   [<span data-ttu-id="9d6b2-105">Schritt 1: Verwenden des System-DPI beim Erstellen von Windows</span><span class="sxs-lookup"><span data-stu-id="9d6b2-105">Step 1: Use the System DPI When Creating Windows</span></span>](#step-1-use-the-system-dpi-when-creating-windows)
    -   [<span data-ttu-id="9d6b2-106">Direct2D</span><span class="sxs-lookup"><span data-stu-id="9d6b2-106">Direct2D</span></span>](#direct2d)
    -   [<span data-ttu-id="9d6b2-107">Gdi</span><span class="sxs-lookup"><span data-stu-id="9d6b2-107">GDI</span></span>](#gdi)
-   [<span data-ttu-id="9d6b2-108">Schritt 2: Deklarieren, dass die Anwendung DPI-bewusst ist</span><span class="sxs-lookup"><span data-stu-id="9d6b2-108">Step 2: Declare That the Application is DPI-Aware</span></span>](#step-2-declare-that-the-application-is-dpi-aware)
-   [<span data-ttu-id="9d6b2-109">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="9d6b2-109">Related topics</span></span>](#related-topics)

## <a name="step-1-use-the-system-dpi-when-creating-windows"></a><span data-ttu-id="9d6b2-110">Schritt 1: Verwenden des System-DPI beim Erstellen von Windows</span><span class="sxs-lookup"><span data-stu-id="9d6b2-110">Step 1: Use the System DPI When Creating Windows</span></span>

<span data-ttu-id="9d6b2-111">Dies kann mit [Direct2D](../direct2d/direct2d-portal.md) oder [GDI erfolgen.](../gdi/windows-gdi.md)</span><span class="sxs-lookup"><span data-stu-id="9d6b2-111">This can be done by using [Direct2D](../direct2d/direct2d-portal.md) or by using [GDI](../gdi/windows-gdi.md).</span></span>

### <a name="direct2d"></a><span data-ttu-id="9d6b2-112">Direct2D</span><span class="sxs-lookup"><span data-stu-id="9d6b2-112">Direct2D</span></span>

<span data-ttu-id="9d6b2-113">Die [**ID2D1Factory-Schnittstelle**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) stellt die [**GetDesktopDpi-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) zum Abrufen des System-DPI bereit.</span><span class="sxs-lookup"><span data-stu-id="9d6b2-113">The [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) interface provides the [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) method for retrieving the system DPI.</span></span> <span data-ttu-id="9d6b2-114">Sie stellt die horizontalen und vertikalen Abmessungen der Anzeige in DPI (Dots per Inch, Punkt pro Zoll) zur Seite.</span><span class="sxs-lookup"><span data-stu-id="9d6b2-114">It provides the horizontal and vertical dimensions of the display in dots per inch (DPI).</span></span> <span data-ttu-id="9d6b2-115">Um diese Werte zum Festlegen der Breite eines Fensters zu verwenden, verwenden Sie die folgende Formel:</span><span class="sxs-lookup"><span data-stu-id="9d6b2-115">To use these values to set the width of a window, use the following formula:</span></span>

<span data-ttu-id="9d6b2-116"><*Horizontal DPI* >  \*  < *width* in Pixel>/<*horizontalen DPI*></span><span class="sxs-lookup"><span data-stu-id="9d6b2-116"><*horizontal DPI*> \* <*width*, in pixels> / <*default horizontal DPI*></span></span>

<span data-ttu-id="9d6b2-117">... Wobei *horizontaler DPI-Wert* der von GetDpi wiederholte Wert und der horizontale *DPI-Standardwert* 96 ist.</span><span class="sxs-lookup"><span data-stu-id="9d6b2-117">...where *horizontal DPI* is the value retrived by GetDpi and *default horizontal DPI* is 96.</span></span> <span data-ttu-id="9d6b2-118">Die Formel ist für die vertikale Größe ähnlich:</span><span class="sxs-lookup"><span data-stu-id="9d6b2-118">The formula is similar for the vertical size:</span></span>

<span data-ttu-id="9d6b2-119"><*Vertikaler DPI* >  \*  < *Höhe* in Pixel>/<*standardmäßigen vertikalen DPI*></span><span class="sxs-lookup"><span data-stu-id="9d6b2-119"><*vertical DPI*> \* <*height*, in pixels> / <*default vertical DPI*></span></span>

<span data-ttu-id="9d6b2-120">... Dabei *ist der vertikale DPI-Wert* der von der [**GetDesktopDpi-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) abgerufene Wert und der standardmäßige *vertikale DPI* 96.</span><span class="sxs-lookup"><span data-stu-id="9d6b2-120">...where *vertical DPI* is the value retrieved by the [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) method and *default vertical DPI* is 96.</span></span>

<span data-ttu-id="9d6b2-121">Im folgenden Code wird die [**GetDesktopDpi-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) verwendet, um ein 640 x 480-Fenster zu erstellen, das auf den System-DPI skaliert wird.</span><span class="sxs-lookup"><span data-stu-id="9d6b2-121">The following code uses the [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) method to create a 640 x 480 window, scaled to the system DPI.</span></span> <span data-ttu-id="9d6b2-122">(Im folgenden Code ist *m \_ spD2DFactory* ein intelligenter Zeiger auf eine [**ID2D1Factory-Instanz.)**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)</span><span class="sxs-lookup"><span data-stu-id="9d6b2-122">(In the following code, *m\_spD2DFactory* is a smart pointer to an [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) instance.)</span></span>


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



### <a name="gdi"></a><span data-ttu-id="9d6b2-123">GDI</span><span class="sxs-lookup"><span data-stu-id="9d6b2-123">GDI</span></span>

<span data-ttu-id="9d6b2-124">[GDI](interoperating-with-gdi.md) stellt die [**GetDeviceCaps-Funktion**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) zum Abrufen von Geräteinformationen zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="9d6b2-124">[GDI](interoperating-with-gdi.md) provides the [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) function for retrieving device information.</span></span> <span data-ttu-id="9d6b2-125">Sie können DPI-Informationen abrufen, indem Sie die *Indexwerte LOGPIXELSX* und *LOGPIXELSY* übergeben.</span><span class="sxs-lookup"><span data-stu-id="9d6b2-125">You can retrieve DPI information by passing the *LOGPIXELSX* and *LOGPIXELSY* index values.</span></span> <span data-ttu-id="9d6b2-126">Die Formel zum Bestimmen der horizontalen und vertikalen Größe eines Fensters ist die gleiche wie im [obigen Direct2D-Beispiel.](../direct2d/direct2d-portal.md)</span><span class="sxs-lookup"><span data-stu-id="9d6b2-126">The formula for determining the horizontal and vertical size of a window is the same as with the [Direct2D](../direct2d/direct2d-portal.md) example above.</span></span>

<span data-ttu-id="9d6b2-127">Im folgenden Code wird die [**GetDeviceCaps-Funktion**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) verwendet, um ein 640 x 480-Fenster zu erstellen, das auf den System-DPI skaliert wird.</span><span class="sxs-lookup"><span data-stu-id="9d6b2-127">The following code uses the [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) function to create a 640 x 480 window, scaled to the system DPI.</span></span>


```C++
FLOAT dpiX, dpiY;

HDC screen = GetDC(0);
dpiX = static_cast<FLOAT>(GetDeviceCaps(screen, LOGPIXELSX));
dpiY = static_cast<FLOAT>(GetDeviceCaps(screen, LOGPIXELSY));
ReleaseDC(0, screen);

hWnd = CreateWindow(
         TEXT("DirectWriteApp"),
         TEXT("DirectWrite Demo App"),
         WS_OVERLAPPEDWINDOW,
         CW_USEDEFAULT,
         CW_USEDEFAULT,
         static_cast<INT>(dpiX * 640.f / 96.f),
         static_cast<INT>(dpiY * 480.f / 96.f),
         NULL,
         NULL,
         hInstance,
         NULL
         );
```



## <a name="step-2-declare-that-the-application-is-dpi-aware"></a><span data-ttu-id="9d6b2-128">Schritt 2: Deklarieren, dass die Anwendung DPI-Aware</span><span class="sxs-lookup"><span data-stu-id="9d6b2-128">Step 2: Declare That the Application is DPI-Aware</span></span>

<span data-ttu-id="9d6b2-129">Wenn sich eine Anwendung als DPI-bewusst deklariert, handelt es sich um eine -Anweisung, die annimmt, dass sich die Anwendung bei DPI-Einstellungen von bis zu 200 DPI gut verhält.</span><span class="sxs-lookup"><span data-stu-id="9d6b2-129">When an application declares itself to be DPI-aware, it is a statement specifying that the application behaves well at DPI settings up to 200 DPI.</span></span> <span data-ttu-id="9d6b2-130">Wenn in Windows Vista und Windows 7 die DPI-Virtualisierung aktiviert ist, werden Anwendungen, die nicht DPI-fähig sind, skaliert, und Anwendungen erhalten virtualisierte Daten von den System-APIs, z. B. die [**GetSystemMetric-Funktion.**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics)</span><span class="sxs-lookup"><span data-stu-id="9d6b2-130">In Windows Vista and Windows 7, when DPI virtualization is enabled, applications that are not DPI-aware are scaled, and applications receive virtualized data from the system APIs, such as the [**GetSystemMetric**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) function.</span></span> <span data-ttu-id="9d6b2-131">Führen Sie die folgenden Schritte aus, um zu deklarieren, dass Ihre Anwendung DPI-bewusst ist.</span><span class="sxs-lookup"><span data-stu-id="9d6b2-131">To declare that your application is DPI-aware, complete the following steps.</span></span>

1.  <span data-ttu-id="9d6b2-132">Erstellen Sie eine Datei mit dem Namen DeclareDPIAware.manifest.</span><span class="sxs-lookup"><span data-stu-id="9d6b2-132">Create a file called DeclareDPIAware.manifest.</span></span>
2.  <span data-ttu-id="9d6b2-133">Kopieren Sie den folgenden XML-Code in die Datei, und speichern Sie ihn:</span><span class="sxs-lookup"><span data-stu-id="9d6b2-133">Copy the following xml into the file and save it:</span></span>
    ```C++
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3" >
      <asmv3:application>
        <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">
          <dpiAware>true</dpiAware>
        </asmv3:windowsSettings>
      </asmv3:application>
    </assembly>
    ```

    

3.  <span data-ttu-id="9d6b2-134">Fügen Sie in der VCPROJ-Datei des Projekts in jedem Configuration-Element unter VisualStudioProject/Configurations den folgenden Eintrag hinzu:</span><span class="sxs-lookup"><span data-stu-id="9d6b2-134">In the project's .vcproj file, add the following entry inside each Configuration element under VisualStudioProject/Configurations:</span></span>
    ```C++
    <Tool
        Name="VCManifestTool"
        AdditionalManifestFiles="DeclareDPIAware.manifest"
    />
    ```

    

## <a name="related-topics"></a><span data-ttu-id="9d6b2-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9d6b2-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d6b2-136">Direct2D und High-DPI</span><span class="sxs-lookup"><span data-stu-id="9d6b2-136">Direct2D and High-DPI</span></span>](../direct2d/direct2d-and-high-dpi.md)
</dt> </dl>

 

 