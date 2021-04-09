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
# <a name="displaying-properly-on-a-high-dpi-display"></a>Ordnungsgemäße Anzeige auf einer High-dpi-Anzeige

Obwohl Direct2D viele hochauflösende Probleme behandelt, müssen Sie zwei Schritte durchführen, um sicherzustellen, dass Ihre Anwendung auf hoch-dpi-anzeigen ordnungsgemäß funktioniert:

-   [Schritt 1: Verwenden des System-dpi beim Erstellen von Fenstern](#step-1-use-the-system-dpi-when-creating-windows)
-   [Schritt 2: deklarieren, dass die Anwendung dpi-fähig ist](#step-2-declare-that-the-application-is-dpi-aware)
-   [Zugehörige Themen](#related-topics)

## <a name="step-1-use-the-system-dpi-when-creating-windows"></a>Schritt 1: Verwenden des System-dpi beim Erstellen von Fenstern

Die [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) -Schnittstelle stellt die [**getdesktopdpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) -Methode zum Abrufen des System-dpi bereit. Sie stellt die horizontale und vertikale Abmessungen der Anzeige in dpi (dots per inch) bereit. Um diese Werte zum Festlegen der Breite eines Fensters zu verwenden, verwenden Sie die folgende Formel:

<*horizontaler dpi* >  \*  < *Breite* in Pixel>/<*standardmäßiger horizontaler dpi* -Wert>

... Dabei ist *horizontaler dpi* der Wert, der von [**getdesktopdpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) abgerufen wird, und der *horizontale Standard dpi* -Wert ist 96. Die Formel ähnelt der vertikalen Größe:

<*vertikaler dpi* >  \*  < *Höhe* in Pixel>/<*standardmäßiger vertikaler dpi*>

... Dabei ist *vertikaler dpi* *-Wert* der Wert, der von der [**getdesktopdpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) 96-Methode abgerufen wird

Im folgenden Code wird die [**getdesktopdpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) -Methode verwendet, um den System-dpi-Wert abzurufen. Anschließend wird ein 640 × 480-Fenster erstellt, das auf das System-dpi skaliert


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
> Ab Windows 8 können Sie die Klasse [**Windows:: Graphics::D isplay::D isplayproperties**](/uwp/api/Windows.Graphics.Display.DisplayProperties) verwenden, um den System-dpi-Wert zu erhalten.

 

## <a name="step-2-declare-that-the-application-is-dpi-aware"></a>Schritt 2: deklarieren, dass die Anwendung DPI-Aware

Wenn sich eine Anwendung als dpi-fähig deklariert, ist es eine-Anweisung, die angibt, dass sich die Anwendung gut bei dpi-Einstellungen bis zu 200 dpi verhält. Wenn in Windows Vista und Windows 7 die dpi-Virtualisierung aktiviert ist, werden Anwendungen, die nicht mit dpi-Werten kompatibel sind, skaliert, und Anwendungen erhalten virtualisierte Daten aus den System-APIs, wie z. b. der [**getsystemmetric**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) -Funktion. Führen Sie die folgenden Schritte aus, um zu deklarieren, dass Ihre Anwendung dpi-fähig ist.

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

[Direct2D und High-dpi](direct2d-and-high-dpi.md)
</dt> </dl>

 

 