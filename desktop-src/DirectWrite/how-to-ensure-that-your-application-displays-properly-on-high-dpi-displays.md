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
# <a name="how-to-ensure-that-your-application-displays-properly-on-high-dpi-displays"></a>So stellen Sie sicher, dass Ihre Anwendung ordnungsgemäß auf Bildschirmen mit hohem DPI-Leistung angezeigt wird

[Obwohl DirectWrite](direct-write-portal.md) viele Probleme mit hohen DPI-Adressen für Sie behandelt, müssen Sie zwei Schritte ausführen, um sicherzustellen, dass Ihre Anwendung auf Bildschirmen mit hohem DPI-Code ordnungsgemäß funktioniert:

-   [Schritt 1: Verwenden des System-DPI beim Erstellen von Windows](#step-1-use-the-system-dpi-when-creating-windows)
    -   [Direct2D](#direct2d)
    -   [Gdi](#gdi)
-   [Schritt 2: Deklarieren, dass die Anwendung DPI-bewusst ist](#step-2-declare-that-the-application-is-dpi-aware)
-   [Verwandte Themen](#related-topics)

## <a name="step-1-use-the-system-dpi-when-creating-windows"></a>Schritt 1: Verwenden des System-DPI beim Erstellen von Windows

Dies kann mit [Direct2D](../direct2d/direct2d-portal.md) oder [GDI erfolgen.](../gdi/windows-gdi.md)

### <a name="direct2d"></a>Direct2D

Die [**ID2D1Factory-Schnittstelle**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) stellt die [**GetDesktopDpi-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) zum Abrufen des System-DPI bereit. Sie stellt die horizontalen und vertikalen Abmessungen der Anzeige in DPI (Dots per Inch, Punkt pro Zoll) zur Seite. Um diese Werte zum Festlegen der Breite eines Fensters zu verwenden, verwenden Sie die folgende Formel:

<*Horizontal DPI* >  \*  < *width* in Pixel>/<*horizontalen DPI*>

... Wobei *horizontaler DPI-Wert* der von GetDpi wiederholte Wert und der horizontale *DPI-Standardwert* 96 ist. Die Formel ist für die vertikale Größe ähnlich:

<*Vertikaler DPI* >  \*  < *Höhe* in Pixel>/<*standardmäßigen vertikalen DPI*>

... Dabei *ist der vertikale DPI-Wert* der von der [**GetDesktopDpi-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) abgerufene Wert und der standardmäßige *vertikale DPI* 96.

Im folgenden Code wird die [**GetDesktopDpi-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) verwendet, um ein 640 x 480-Fenster zu erstellen, das auf den System-DPI skaliert wird. (Im folgenden Code ist *m \_ spD2DFactory* ein intelligenter Zeiger auf eine [**ID2D1Factory-Instanz.)**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)


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



### <a name="gdi"></a>GDI

[GDI](interoperating-with-gdi.md) stellt die [**GetDeviceCaps-Funktion**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) zum Abrufen von Geräteinformationen zur Verfügung. Sie können DPI-Informationen abrufen, indem Sie die *Indexwerte LOGPIXELSX* und *LOGPIXELSY* übergeben. Die Formel zum Bestimmen der horizontalen und vertikalen Größe eines Fensters ist die gleiche wie im [obigen Direct2D-Beispiel.](../direct2d/direct2d-portal.md)

Im folgenden Code wird die [**GetDeviceCaps-Funktion**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) verwendet, um ein 640 x 480-Fenster zu erstellen, das auf den System-DPI skaliert wird.


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



## <a name="step-2-declare-that-the-application-is-dpi-aware"></a>Schritt 2: Deklarieren, dass die Anwendung DPI-Aware

Wenn sich eine Anwendung als DPI-bewusst deklariert, handelt es sich um eine -Anweisung, die annimmt, dass sich die Anwendung bei DPI-Einstellungen von bis zu 200 DPI gut verhält. Wenn in Windows Vista und Windows 7 die DPI-Virtualisierung aktiviert ist, werden Anwendungen, die nicht DPI-fähig sind, skaliert, und Anwendungen erhalten virtualisierte Daten von den System-APIs, z. B. die [**GetSystemMetric-Funktion.**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) Führen Sie die folgenden Schritte aus, um zu deklarieren, dass Ihre Anwendung DPI-bewusst ist.

1.  Erstellen Sie eine Datei mit dem Namen DeclareDPIAware.manifest.
2.  Kopieren Sie den folgenden XML-Code in die Datei, und speichern Sie ihn:
    ```C++
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3" >
      <asmv3:application>
        <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">
          <dpiAware>true</dpiAware>
        </asmv3:windowsSettings>
      </asmv3:application>
    </assembly>
    ```

    

3.  Fügen Sie in der VCPROJ-Datei des Projekts in jedem Configuration-Element unter VisualStudioProject/Configurations den folgenden Eintrag hinzu:
    ```C++
    <Tool
        Name="VCManifestTool"
        AdditionalManifestFiles="DeclareDPIAware.manifest"
    />
    ```

    

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct2D und High-DPI](../direct2d/direct2d-and-high-dpi.md)
</dt> </dl>

 

 