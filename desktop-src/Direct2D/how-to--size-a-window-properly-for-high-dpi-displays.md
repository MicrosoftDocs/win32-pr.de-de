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
# <a name="displaying-properly-on-a-high-dpi-display"></a>Ordnungsgemäße Anzeige auf einer Anzeige mit hohem DPI-Anteil

Obwohl Direct2D viele Probleme mit hohen DPI-Daten für Sie behandelt, sollten Sie zwei Schritte ausführen, um sicherzustellen, dass Ihre Anwendung ordnungsgemäß auf Anzeigen mit hohen DPI-Daten funktioniert:

-   [Schritt 1: Verwenden des System-DPI beim Erstellen von Windows](#step-1-use-the-system-dpi-when-creating-windows)
-   [Schritt 2: Deklarieren, dass die Anwendung DPI-fähige Anwendung ist](#step-2-declare-that-the-application-is-dpi-aware)
-   [Verwandte Themen](#related-topics)

## <a name="step-1-use-the-system-dpi-when-creating-windows"></a>Schritt 1: Verwenden des System-DPI beim Erstellen von Windows

Die [**ID2D1Factory-Schnittstelle**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) stellt die [**GetDesktopDpi-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) zum Abrufen des System-DPI bereit. Sie stellt die horizontalen und vertikalen Abmessungen der Anzeige in DPI (Dots per Inch) bereit. Verwenden Sie die folgende Formel, um diese Werte zum Festlegen der Breite eines Fensters zu verwenden:

<*Horizontaler DPI* >  \*  < *width*, in Pixeln>/<*horizontalen Standard-DPI*>

... Dabei ist *horizontaler DPI* der von [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) wiederholte Wert und *horizontaler Standard-DPI* 96. Die Formel ist für die vertikale Größe ähnlich:

<*Vertikaler DPI* >  \*  < *height*, in Pixeln>/<*vertikaler Standard-DPI*>

... dabei ist *vertical DPI* der Wert, der von der [**GetDesktopDpi-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) abgerufen wird, und *der vertikale DPI-Standardwert* ist 96.

Der folgende Code verwendet die [**GetDesktopDpi-Methode,**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) um den System-DPI abzurufen, und erstellt dann ein 640 × 480-Fenster, das auf den System-DPI skaliert wird.


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
> Ab Windows 8 können Sie die [**Windows::Graphics::D isplay::D isplayProperties-Klasse**](/uwp/api/Windows.Graphics.Display.DisplayProperties) verwenden, um den System-DPI abzurufen.

 

## <a name="step-2-declare-that-the-application-is-dpi-aware"></a>Schritt 2: Deklarieren, dass die Anwendung DPI-Aware

Wenn eine Anwendung sich selbst als DPI-fähige Anwendung deklariert, handelt es sich um eine Anweisung, die angibt, dass sich die Anwendung bei DPI-Einstellungen bis zu 200 DPI gut verhält. Wenn die DPI-Virtualisierung in Windows Vista und Windows 7 aktiviert ist, werden Anwendungen, die nicht DPI-fähig sind, skaliert, und Anwendungen empfangen virtualisierte Daten von den System-APIs, z. B. der [**GetSystemMetric-Funktion.**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) Führen Sie die folgenden Schritte aus, um zu deklarieren, dass Ihre Anwendung DPI-fähige Anwendung ist.

1.  Erstellen Sie eine Datei namens DeclareDPIAware.manifest.
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

[Direct2D und High-DPI](direct2d-and-high-dpi.md)
</dt> </dl>

 

 