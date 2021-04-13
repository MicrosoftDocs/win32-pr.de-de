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
# <a name="how-to-ensure-that-your-application-displays-properly-on-high-dpi-displays"></a>So stellen Sie sicher, dass Ihre Anwendung auf hoch-dpi-anzeigen ordnungsgemäß angezeigt wird

Obwohl [DirectWrite](direct-write-portal.md) viele hochauflösende Probleme behandelt, müssen Sie zwei Schritte durchführen, um sicherzustellen, dass Ihre Anwendung auf hoch-dpi-anzeigen ordnungsgemäß funktioniert:

-   [Schritt 1: Verwenden des System-dpi beim Erstellen von Fenstern](#step-1-use-the-system-dpi-when-creating-windows)
    -   [Direct2D](#direct2d)
    -   [GDI](#gdi)
-   [Schritt 2: deklarieren, dass die Anwendung dpi-fähig ist](#step-2-declare-that-the-application-is-dpi-aware)
-   [Zugehörige Themen](#related-topics)

## <a name="step-1-use-the-system-dpi-when-creating-windows"></a>Schritt 1: Verwenden des System-dpi beim Erstellen von Fenstern

Dies kann mithilfe von [Direct2D](../direct2d/direct2d-portal.md) oder mithilfe von [GDI](../gdi/windows-gdi.md)erfolgen.

### <a name="direct2d"></a>Direct2D

Die [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) -Schnittstelle stellt die [**getdesktopdpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) -Methode zum Abrufen des System-dpi bereit. Sie stellt die horizontale und vertikale Abmessungen der Anzeige in dpi (dots per inch) bereit. Um diese Werte zum Festlegen der Breite eines Fensters zu verwenden, verwenden Sie die folgende Formel:

<*horizontaler dpi* >  \*  < *Breite* in Pixel>/<*standardmäßiger horizontaler dpi* -Wert>

... Dabei ist *horizontaler dpi* der Wert, der von getdpi abgerufen wird, und der *horizontale Standard dpi* -Wert ist 96. Die Formel ähnelt der vertikalen Größe:

<*vertikaler dpi* >  \*  < *Höhe* in Pixel>/<*standardmäßiger vertikaler dpi*>

... Dabei ist *vertikaler dpi* *-Wert* der Wert, der von der [**getdesktopdpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) 96-Methode abgerufen wird

Im folgenden Code wird die [**getdesktopdpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) -Methode zum Erstellen eines 640 x 480-Fensters verwendet, das auf den dpi-Wert des Systems skaliert wird. (Im folgenden Code ist *m \_ spD2DFactory* ein intelligenter Zeiger auf eine [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) -Instanz.)


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

[GDI](interoperating-with-gdi.md) stellt die [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) -Funktion zum Abrufen von Geräteinformationen bereit. Sie können dpi-Informationen abrufen, indem Sie die Indexwerte *logpixelsx* und *logpixelsy* übergeben. Die Formel zum Ermitteln der horizontalen und vertikalen Größe eines Fensters ist mit dem oben genannten [Direct2D](../direct2d/direct2d-portal.md) -Beispiel identisch.

Im folgenden Code wird die [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) -Funktion zum Erstellen eines 640 x 480-Fensters verwendet, das auf den dpi-Wert des Systems skaliert wird.


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



## <a name="step-2-declare-that-the-application-is-dpi-aware"></a>Schritt 2: deklarieren, dass die Anwendung DPI-Aware

Wenn sich eine Anwendung als dpi-fähig deklariert, ist es eine-Anweisung, die angibt, dass sich die Anwendung gut bei dpi-Einstellungen bis zu 200 dpi verhält. Wenn in Windows Vista und Windows 7 die dpi-Virtualisierung aktiviert ist, werden Anwendungen, die nicht mit dpi-Werten kompatibel sind, skaliert, und Anwendungen erhalten virtualisierte Daten aus den System-APIs, wie z. b. der [**getsystemmetric**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) -Funktion. Führen Sie die folgenden Schritte aus, um zu deklarieren, dass Ihre Anwendung dpi-fähig ist.

1.  Erstellen Sie eine Datei mit dem Namen "declaredpiaware. Manifest".
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

    

3.  Fügen Sie in der VCPROJ-Datei des Projekts in den einzelnen Konfigurationselementen unter visualstudioproject/Konfigurationen den folgenden Eintrag hinzu:
    ```C++
    <Tool
        Name="VCManifestTool"
        AdditionalManifestFiles="DeclareDPIAware.manifest"
    />
    ```

    

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct2D und High-dpi](../direct2d/direct2d-and-high-dpi.md)
</dt> </dl>

 

 