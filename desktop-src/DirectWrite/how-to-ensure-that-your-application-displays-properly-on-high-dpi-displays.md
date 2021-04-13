---
title: So stellen Sie sicher, dass die Anwendung auf hoch-dpi-anzeigen (DirectWrite) ordnungsgemäß angezeigt wird
description: Hier wird beschrieben, wie ein Fenster erstellt wird, das auf hoch-dpi-anzeigen ordnungsgemäß angezeigt wird.
ms.assetid: d174a337-c98e-46c7-86d2-c208900882d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 317eb3379963cec600ab9bac7deb3778f0874e59
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315717"
---
# <a name="how-to-ensure-that-your-application-displays-properly-on-high-dpi-displays"></a><span data-ttu-id="f4a0d-103">So stellen Sie sicher, dass Ihre Anwendung auf hoch-dpi-anzeigen ordnungsgemäß angezeigt wird</span><span class="sxs-lookup"><span data-stu-id="f4a0d-103">How to Ensure That Your Application Displays Properly on High-DPI Displays</span></span>

<span data-ttu-id="f4a0d-104">Obwohl [DirectWrite](direct-write-portal.md) viele hochauflösende Probleme behandelt, müssen Sie zwei Schritte durchführen, um sicherzustellen, dass Ihre Anwendung auf hoch-dpi-anzeigen ordnungsgemäß funktioniert:</span><span class="sxs-lookup"><span data-stu-id="f4a0d-104">Although [DirectWrite](direct-write-portal.md) addresses many high-DPI issues for you, there are two steps you should take to ensure that your application works properly on high-DPI displays:</span></span>

-   [<span data-ttu-id="f4a0d-105">Schritt 1: Verwenden des System-dpi beim Erstellen von Fenstern</span><span class="sxs-lookup"><span data-stu-id="f4a0d-105">Step 1: Use the System DPI When Creating Windows</span></span>](#step-1-use-the-system-dpi-when-creating-windows)
    -   [<span data-ttu-id="f4a0d-106">Direct2D</span><span class="sxs-lookup"><span data-stu-id="f4a0d-106">Direct2D</span></span>](#direct2d)
    -   [<span data-ttu-id="f4a0d-107">GDI</span><span class="sxs-lookup"><span data-stu-id="f4a0d-107">GDI</span></span>](#gdi)
-   [<span data-ttu-id="f4a0d-108">Schritt 2: deklarieren, dass die Anwendung dpi-fähig ist</span><span class="sxs-lookup"><span data-stu-id="f4a0d-108">Step 2: Declare That the Application is DPI-Aware</span></span>](#step-2-declare-that-the-application-is-dpi-aware)
-   [<span data-ttu-id="f4a0d-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f4a0d-109">Related topics</span></span>](#related-topics)

## <a name="step-1-use-the-system-dpi-when-creating-windows"></a><span data-ttu-id="f4a0d-110">Schritt 1: Verwenden des System-dpi beim Erstellen von Fenstern</span><span class="sxs-lookup"><span data-stu-id="f4a0d-110">Step 1: Use the System DPI When Creating Windows</span></span>

<span data-ttu-id="f4a0d-111">Dies kann mithilfe von [Direct2D](../direct2d/direct2d-portal.md) oder mithilfe von [GDI](../gdi/windows-gdi.md)erfolgen.</span><span class="sxs-lookup"><span data-stu-id="f4a0d-111">This can be done by using [Direct2D](../direct2d/direct2d-portal.md) or by using [GDI](../gdi/windows-gdi.md).</span></span>

### <a name="direct2d"></a><span data-ttu-id="f4a0d-112">Direct2D</span><span class="sxs-lookup"><span data-stu-id="f4a0d-112">Direct2D</span></span>

<span data-ttu-id="f4a0d-113">Die [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) -Schnittstelle stellt die [**getdesktopdpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) -Methode zum Abrufen des System-dpi bereit.</span><span class="sxs-lookup"><span data-stu-id="f4a0d-113">The [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) interface provides the [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) method for retrieving the system DPI.</span></span> <span data-ttu-id="f4a0d-114">Sie stellt die horizontale und vertikale Abmessungen der Anzeige in dpi (dots per inch) bereit.</span><span class="sxs-lookup"><span data-stu-id="f4a0d-114">It provides the horizontal and vertical dimensions of the display in dots per inch (DPI).</span></span> <span data-ttu-id="f4a0d-115">Um diese Werte zum Festlegen der Breite eines Fensters zu verwenden, verwenden Sie die folgende Formel:</span><span class="sxs-lookup"><span data-stu-id="f4a0d-115">To use these values to set the width of a window, use the following formula:</span></span>

<span data-ttu-id="f4a0d-116"><*horizontaler dpi* >  \*  < *Breite* in Pixel>/<*standardmäßiger horizontaler dpi* -Wert></span><span class="sxs-lookup"><span data-stu-id="f4a0d-116"><*horizontal DPI*> \* <*width*, in pixels> / <*default horizontal DPI*></span></span>

<span data-ttu-id="f4a0d-117">... Dabei ist *horizontaler dpi* der Wert, der von getdpi abgerufen wird, und der *horizontale Standard dpi* -Wert ist 96.</span><span class="sxs-lookup"><span data-stu-id="f4a0d-117">...where *horizontal DPI* is the value retrived by GetDpi and *default horizontal DPI* is 96.</span></span> <span data-ttu-id="f4a0d-118">Die Formel ähnelt der vertikalen Größe:</span><span class="sxs-lookup"><span data-stu-id="f4a0d-118">The formula is similar for the vertical size:</span></span>

<span data-ttu-id="f4a0d-119"><*vertikaler dpi* >  \*  < *Höhe* in Pixel>/<*standardmäßiger vertikaler dpi*></span><span class="sxs-lookup"><span data-stu-id="f4a0d-119"><*vertical DPI*> \* <*height*, in pixels> / <*default vertical DPI*></span></span>

<span data-ttu-id="f4a0d-120">... Dabei ist *vertikaler dpi* *-Wert* der Wert, der von der [**getdesktopdpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) 96-Methode abgerufen wird</span><span class="sxs-lookup"><span data-stu-id="f4a0d-120">...where *vertical DPI* is the value retrieved by the [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) method and *default vertical DPI* is 96.</span></span>

<span data-ttu-id="f4a0d-121">Im folgenden Code wird die [**getdesktopdpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) -Methode zum Erstellen eines 640 x 480-Fensters verwendet, das auf den dpi-Wert des Systems skaliert wird.</span><span class="sxs-lookup"><span data-stu-id="f4a0d-121">The following code uses the [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) method to create a 640 x 480 window, scaled to the system DPI.</span></span> <span data-ttu-id="f4a0d-122">(Im folgenden Code ist *m \_ spD2DFactory* ein intelligenter Zeiger auf eine [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) -Instanz.)</span><span class="sxs-lookup"><span data-stu-id="f4a0d-122">(In the following code, *m\_spD2DFactory* is a smart pointer to an [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) instance.)</span></span>


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



### <a name="gdi"></a><span data-ttu-id="f4a0d-123">GDI</span><span class="sxs-lookup"><span data-stu-id="f4a0d-123">GDI</span></span>

<span data-ttu-id="f4a0d-124">[GDI](interoperating-with-gdi.md) stellt die [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) -Funktion zum Abrufen von Geräteinformationen bereit.</span><span class="sxs-lookup"><span data-stu-id="f4a0d-124">[GDI](interoperating-with-gdi.md) provides the [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) function for retrieving device information.</span></span> <span data-ttu-id="f4a0d-125">Sie können dpi-Informationen abrufen, indem Sie die Indexwerte *logpixelsx* und *logpixelsy* übergeben.</span><span class="sxs-lookup"><span data-stu-id="f4a0d-125">You can retrieve DPI information by passing the *LOGPIXELSX* and *LOGPIXELSY* index values.</span></span> <span data-ttu-id="f4a0d-126">Die Formel zum Ermitteln der horizontalen und vertikalen Größe eines Fensters ist mit dem oben genannten [Direct2D](../direct2d/direct2d-portal.md) -Beispiel identisch.</span><span class="sxs-lookup"><span data-stu-id="f4a0d-126">The formula for determining the horizontal and vertical size of a window is the same as with the [Direct2D](../direct2d/direct2d-portal.md) example above.</span></span>

<span data-ttu-id="f4a0d-127">Im folgenden Code wird die [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) -Funktion zum Erstellen eines 640 x 480-Fensters verwendet, das auf den dpi-Wert des Systems skaliert wird.</span><span class="sxs-lookup"><span data-stu-id="f4a0d-127">The following code uses the [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) function to create a 640 x 480 window, scaled to the system DPI.</span></span>


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



## <a name="step-2-declare-that-the-application-is-dpi-aware"></a><span data-ttu-id="f4a0d-128">Schritt 2: deklarieren, dass die Anwendung DPI-Aware</span><span class="sxs-lookup"><span data-stu-id="f4a0d-128">Step 2: Declare That the Application is DPI-Aware</span></span>

<span data-ttu-id="f4a0d-129">Wenn sich eine Anwendung als dpi-fähig deklariert, ist es eine-Anweisung, die angibt, dass sich die Anwendung gut bei dpi-Einstellungen bis zu 200 dpi verhält.</span><span class="sxs-lookup"><span data-stu-id="f4a0d-129">When an application declares itself to be DPI-aware, it is a statement specifying that the application behaves well at DPI settings up to 200 DPI.</span></span> <span data-ttu-id="f4a0d-130">Wenn in Windows Vista und Windows 7 die dpi-Virtualisierung aktiviert ist, werden Anwendungen, die nicht mit dpi-Werten kompatibel sind, skaliert, und Anwendungen erhalten virtualisierte Daten aus den System-APIs, wie z. b. der [**getsystemmetric**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="f4a0d-130">In Windows Vista and Windows 7, when DPI virtualization is enabled, applications that are not DPI-aware are scaled, and applications receive virtualized data from the system APIs, such as the [**GetSystemMetric**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) function.</span></span> <span data-ttu-id="f4a0d-131">Führen Sie die folgenden Schritte aus, um zu deklarieren, dass Ihre Anwendung dpi-fähig ist.</span><span class="sxs-lookup"><span data-stu-id="f4a0d-131">To declare that your application is DPI-aware, complete the following steps.</span></span>

1.  <span data-ttu-id="f4a0d-132">Erstellen Sie eine Datei mit dem Namen "declaredpiaware. Manifest".</span><span class="sxs-lookup"><span data-stu-id="f4a0d-132">Create a file called DeclareDPIAware.manifest.</span></span>
2.  <span data-ttu-id="f4a0d-133">Kopieren Sie den folgenden XML-Code in die Datei, und speichern Sie ihn:</span><span class="sxs-lookup"><span data-stu-id="f4a0d-133">Copy the following xml into the file and save it:</span></span>
    ```C++
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3" >
      <asmv3:application>
        <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">
          <dpiAware>true</dpiAware>
        </asmv3:windowsSettings>
      </asmv3:application>
    </assembly>
    ```

    

3.  <span data-ttu-id="f4a0d-134">Fügen Sie in der VCPROJ-Datei des Projekts in den einzelnen Konfigurationselementen unter visualstudioproject/Konfigurationen den folgenden Eintrag hinzu:</span><span class="sxs-lookup"><span data-stu-id="f4a0d-134">In the project's .vcproj file, add the following entry inside each Configuration element under VisualStudioProject/Configurations:</span></span>
    ```C++
    <Tool
        Name="VCManifestTool"
        AdditionalManifestFiles="DeclareDPIAware.manifest"
    />
    ```

    

## <a name="related-topics"></a><span data-ttu-id="f4a0d-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f4a0d-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4a0d-136">Direct2D und High-dpi</span><span class="sxs-lookup"><span data-stu-id="f4a0d-136">Direct2D and High-DPI</span></span>](../direct2d/direct2d-and-high-dpi.md)
</dt> </dl>

 

 