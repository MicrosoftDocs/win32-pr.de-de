---
title: Ordnungsgemäße Anzeige auf einer High-dpi-Anzeige
description: Hier wird beschrieben, wie ein Fenster erstellt wird, das auf hoch-dpi-anzeigen ordnungsgemäß angezeigt wird.
ms.assetid: 72a4b076-1cf0-4dc9-bd75-43b5173fc2a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58b3e82951dfa77e6f61c661b87064dad5cb9f08
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103949023"
---
# <a name="displaying-properly-on-a-high-dpi-display"></a><span data-ttu-id="b6e19-103">Ordnungsgemäße Anzeige auf einer High-dpi-Anzeige</span><span class="sxs-lookup"><span data-stu-id="b6e19-103">Displaying properly on a high-DPI display</span></span>

<span data-ttu-id="b6e19-104">Obwohl Direct2D viele hochauflösende Probleme behandelt, müssen Sie zwei Schritte durchführen, um sicherzustellen, dass Ihre Anwendung auf hoch-dpi-anzeigen ordnungsgemäß funktioniert:</span><span class="sxs-lookup"><span data-stu-id="b6e19-104">Although Direct2D addresses many high-DPI issues for you, there are two steps you should take to ensure that your application works properly on high-DPI displays:</span></span>

-   [<span data-ttu-id="b6e19-105">Schritt 1: Verwenden des System-dpi beim Erstellen von Fenstern</span><span class="sxs-lookup"><span data-stu-id="b6e19-105">Step 1: Use the System DPI When Creating Windows</span></span>](#step-1-use-the-system-dpi-when-creating-windows)
-   [<span data-ttu-id="b6e19-106">Schritt 2: deklarieren, dass die Anwendung dpi-fähig ist</span><span class="sxs-lookup"><span data-stu-id="b6e19-106">Step 2: Declare That the Application is DPI-Aware</span></span>](#step-2-declare-that-the-application-is-dpi-aware)
-   [<span data-ttu-id="b6e19-107">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b6e19-107">Related topics</span></span>](#related-topics)

## <a name="step-1-use-the-system-dpi-when-creating-windows"></a><span data-ttu-id="b6e19-108">Schritt 1: Verwenden des System-dpi beim Erstellen von Fenstern</span><span class="sxs-lookup"><span data-stu-id="b6e19-108">Step 1: Use the System DPI When Creating Windows</span></span>

<span data-ttu-id="b6e19-109">Die [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) -Schnittstelle stellt die [**getdesktopdpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) -Methode zum Abrufen des System-dpi bereit.</span><span class="sxs-lookup"><span data-stu-id="b6e19-109">The [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) interface provides the [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) method for retrieving the system DPI.</span></span> <span data-ttu-id="b6e19-110">Sie stellt die horizontale und vertikale Abmessungen der Anzeige in dpi (dots per inch) bereit.</span><span class="sxs-lookup"><span data-stu-id="b6e19-110">It provides the horizontal and vertical dimensions of the display in dots per inch (DPI).</span></span> <span data-ttu-id="b6e19-111">Um diese Werte zum Festlegen der Breite eines Fensters zu verwenden, verwenden Sie die folgende Formel:</span><span class="sxs-lookup"><span data-stu-id="b6e19-111">To use these values to set the width of a window, use the following formula:</span></span>

<span data-ttu-id="b6e19-112"><*horizontaler dpi* >  \*  < *Breite* in Pixel>/<*standardmäßiger horizontaler dpi* -Wert></span><span class="sxs-lookup"><span data-stu-id="b6e19-112"><*horizontal DPI*> \* <*width*, in pixels> / <*default horizontal DPI*></span></span>

<span data-ttu-id="b6e19-113">... Dabei ist *horizontaler dpi* der Wert, der von [**getdesktopdpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) abgerufen wird, und der *horizontale Standard dpi* -Wert ist 96.</span><span class="sxs-lookup"><span data-stu-id="b6e19-113">...where *horizontal DPI* is the value retrived by [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) and *default horizontal DPI* is 96.</span></span> <span data-ttu-id="b6e19-114">Die Formel ähnelt der vertikalen Größe:</span><span class="sxs-lookup"><span data-stu-id="b6e19-114">The formula is similar for the vertical size:</span></span>

<span data-ttu-id="b6e19-115"><*vertikaler dpi* >  \*  < *Höhe* in Pixel>/<*standardmäßiger vertikaler dpi*></span><span class="sxs-lookup"><span data-stu-id="b6e19-115"><*vertical DPI*> \* <*height*, in pixels> / <*default vertical DPI*></span></span>

<span data-ttu-id="b6e19-116">... Dabei ist *vertikaler dpi* *-Wert* der Wert, der von der [**getdesktopdpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) 96-Methode abgerufen wird</span><span class="sxs-lookup"><span data-stu-id="b6e19-116">...where *vertical DPI* is the value retrieved by the [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) method and *default vertical DPI* is 96.</span></span>

<span data-ttu-id="b6e19-117">Im folgenden Code wird die [**getdesktopdpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) -Methode verwendet, um den System-dpi-Wert abzurufen. Anschließend wird ein 640 × 480-Fenster erstellt, das auf das System-dpi skaliert</span><span class="sxs-lookup"><span data-stu-id="b6e19-117">The following code uses the [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) method to retrieve the system DPI and then creates a 640 × 480 window, scaled to the system DPI.</span></span>


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
> <span data-ttu-id="b6e19-118">Ab Windows 8 können Sie die Klasse [**Windows:: Graphics::D isplay::D isplayproperties**](/uwp/api/Windows.Graphics.Display.DisplayProperties) verwenden, um den System-dpi-Wert zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b6e19-118">Starting with Windows 8, you can use the [**Windows::Graphics::Display::DisplayProperties**](/uwp/api/Windows.Graphics.Display.DisplayProperties) class to get the system DPI.</span></span>

 

## <a name="step-2-declare-that-the-application-is-dpi-aware"></a><span data-ttu-id="b6e19-119">Schritt 2: deklarieren, dass die Anwendung DPI-Aware</span><span class="sxs-lookup"><span data-stu-id="b6e19-119">Step 2: Declare That the Application is DPI-Aware</span></span>

<span data-ttu-id="b6e19-120">Wenn sich eine Anwendung als dpi-fähig deklariert, ist es eine-Anweisung, die angibt, dass sich die Anwendung gut bei dpi-Einstellungen bis zu 200 dpi verhält.</span><span class="sxs-lookup"><span data-stu-id="b6e19-120">When an application declares itself to be DPI-aware, it is a statement specifying that the application behaves well at DPI settings up to 200 DPI.</span></span> <span data-ttu-id="b6e19-121">Wenn in Windows Vista und Windows 7 die dpi-Virtualisierung aktiviert ist, werden Anwendungen, die nicht mit dpi-Werten kompatibel sind, skaliert, und Anwendungen erhalten virtualisierte Daten aus den System-APIs, wie z. b. der [**getsystemmetric**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="b6e19-121">In Windows Vista and Windows 7, when DPI virtualization is enabled, applications that are not DPI-aware are scaled, and applications receive virtualized data from the system APIs, such as the [**GetSystemMetric**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) function.</span></span> <span data-ttu-id="b6e19-122">Führen Sie die folgenden Schritte aus, um zu deklarieren, dass Ihre Anwendung dpi-fähig ist.</span><span class="sxs-lookup"><span data-stu-id="b6e19-122">To declare that your application is DPI-aware, complete the following steps.</span></span>

1.  <span data-ttu-id="b6e19-123">Erstellen Sie eine Datei mit dem Namen "declaredpiaware. Manifest".</span><span class="sxs-lookup"><span data-stu-id="b6e19-123">Create a file called DeclareDPIAware.manifest.</span></span>
2.  <span data-ttu-id="b6e19-124">Kopieren Sie den folgenden XML-Code in die Datei, und speichern Sie ihn:</span><span class="sxs-lookup"><span data-stu-id="b6e19-124">Copy the following xml into the file and save it:</span></span>
    ```C++
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3" >
      <asmv3:application>
        <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">
          <dpiAware>true</dpiAware>
        </asmv3:windowsSettings>
      </asmv3:application>
    </assembly>
    ```

    

3.  <span data-ttu-id="b6e19-125">Fügen Sie in der VCPROJ-Datei des Projekts in den einzelnen Konfigurationselementen unter visualstudioproject/Konfigurationen den folgenden Eintrag hinzu:</span><span class="sxs-lookup"><span data-stu-id="b6e19-125">In the project's .vcproj file, add the following entry inside each Configuration element under VisualStudioProject/Configurations:</span></span>
    ```C++
    <Tool
        Name="VCManifestTool"
        AdditionalManifestFiles="DeclareDPIAware.manifest"
    />
    ```

    

## <a name="related-topics"></a><span data-ttu-id="b6e19-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b6e19-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6e19-127">Direct2D und High-dpi</span><span class="sxs-lookup"><span data-stu-id="b6e19-127">Direct2D and High-DPI</span></span>](direct2d-and-high-dpi.md)
</dt> </dl>

 

 