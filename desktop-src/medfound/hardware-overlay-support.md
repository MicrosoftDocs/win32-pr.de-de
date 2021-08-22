---
description: Beschreibt die Verwendung von Hardwareüberlagerungen in Direct3D 9.
ms.assetid: fa9d5bf5-4c0f-471a-b639-d329b0cd89a4
title: Hardwareüberlagerungsunterstützung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f537c91bc217344206c0a23cf5ca8a14254a9c983e4ae550e96457bbb055e5d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119600400"
---
# <a name="hardware-overlay-support"></a>Hardwareüberlagerungsunterstützung

Eine Hardwareüberlagerung ist ein dedizierter Bereich des Videospeichers, der auf der primären Oberfläche überlagert werden kann. Es wird keine Kopie ausgeführt, wenn die Überlagerung angezeigt wird. Der Überlagerungsvorgang wird auf Hardware ausgeführt, ohne die Daten auf der primären Oberfläche zu ändern.

Die Verwendung von Hardwareüberlagerungen für die Videowiedergabe war in früheren Versionen von Windows üblich, da Überlagerungen für Videoinhalte mit hoher Bildfrequenz effizient sind. Ab Windows 7 unterstützt Direct3D 9 Hardwareüberlagerungen. Diese Unterstützung ist in erster Linie für die Videowiedergabe vorgesehen und unterscheidet sich in einigen Punkten von früheren DirectDraw-APIs:

-   Die Überlagerung kann nicht verkleinert, gespiegelt oder deinterlaced werden.
-   Quellfarbschlüssel und Alphablending werden nicht unterstützt.
-   Überlagerungen können gestreckt werden, wenn die Überlagerungshardware dies unterstützt. Andernfalls wird Stretching nicht unterstützt. In der Praxis unterstützen nicht alle Grafiktreiber Stretching.
-   Jedes Gerät unterstützt höchstens eine Überlagerung.
-   Die Überlagerung erfolgt mithilfe eines Zielfarbschlüssels, aber die Direct3D-Runtime wählt automatisch die Farbe aus und zeichnet das Zielrechteck. Direct3D verfolgt automatisch die Position des Fensters und aktualisiert die Überlagerungsposition, sobald **PresentEx** aufgerufen wird.

### <a name="creating-a-hardware-overlay-surface"></a>Erstellen einer Hardwareüberlagerungsoberfläche

Um Die Overlayunterstützung abzufragen, rufen **Sie IDirect3D9::GetDeviceCaps auf.** Wenn der Treiber Hardwareüberlagerungen unterstützt, wird das **D3DCAPS \_ OVERLAY-Flag** in **D3DCAPS9 festgelegt. Caps-Member.**

Um herauszufinden, ob ein bestimmtes Überlagerungsformat für einen bestimmten Anzeigemodus unterstützt wird, rufen [**Sie IDirect3D9ExOverlayExtension::CheckDeviceOverlayType auf.**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9exoverlayextension-checkdeviceoverlaytype)

Um die Überlagerung zu erstellen, rufen Sie **IDirect3D9Ex::CreateDeviceEx** auf, und geben Sie den Swapeffekt **D3DSWAPEFFECT \_ OVERLAY an.** Der Hintergrundpuffer kann ein Nicht-RGB-Format verwenden, wenn die Hardware dies unterstützt.

Für Überlagerungsoberflächen gelten die folgenden Einschränkungen:

-   Die Anwendung kann nicht mehr als eine Überlagerungstauschkette erstellen.
-   Die Überlagerung muss im Fenstermodus verwendet werden. Sie kann nicht im Vollbildmodus verwendet werden.
-   Der Overlayaustauscheffekt muss mit der **IDirect3DDevice9Ex-Schnittstelle** verwendet werden. Sie wird für **IDirect3DDevice9** nicht unterstützt.
-   Multisampling kann nicht verwendet werden.
-   Die **Flags D3DPRESENT \_ DONOTFLIP** und **D3DPRESENT \_ FLIPRESTART** werden nicht unterstützt.
-   Präsentationsstatistiken sind für die Überlagerungsoberfläche nicht verfügbar.

Wenn die Hardware stretching nicht unterstützt, wird empfohlen, eine Austauschkette so groß wie der Anzeigemodus zu erstellen, damit die Größe des Fensters in beliebige Dimensionen geändert werden kann. Das Erneute Erstellen der Swapkette ist keine optimale Möglichkeit, die Größe des Fensters zu ändern, da dies zu schwerwiegenden Renderingartefakten führen kann. Aufgrund der Art und Weise, wie die GPU den Überlagerungsspeicher verwaltet, kann die Neuerstellung der Swapkette dazu führen, dass der Videospeicher für eine Anwendung nicht mehr verfügbar ist.

### <a name="new-d3dpresent_parameters-flags"></a>Neue \_ D3DPRESENT-PARAMETERflags

Die folgenden **D3DPRESENT \_ PARAMETERS-Flags** werden zum Erstellen von Überlagerungen definiert.



| Flag                                      | Beschreibung                                                                                                                                                                        |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **D3DPRESENTFLAG \_ OVERLAY \_ LIMITEDRGB**   | Der RGB-Bereich beträgt 16 bis 235. Der Standardwert ist 0 bis 255. <br/> Erfordert die **D3DOVERLAYCAPS \_ LIMITEDRANGERGB-Funktion.**<br/>                                                 |
| **D3DPRESENTFLAG \_ OVERLAY \_ YCbCr \_ BT709** | YUV-Farben verwenden die BT.709-Definition. Der Standardwert ist BT.601. <br/> Erfordert die **D3DOVERLAYCAPS \_ YCbCr \_ BT709-Funktion.**<br/>                                      |
| **D3DPRESENTFLAG \_ OVERLAY \_ YCbCr \_ xvYCC** | Ausgabe der Daten mithilfe von erweitertem YCbCr (xvYCC).<br/> Erfordert die **Funktion D3DOVERLAYCAPS \_ YCbCr \_ BT601 \_ xvYCC** oder **D3DOVERLAYCAPS \_ YCbCr \_ BT709 \_ xvYCC.**<br/> |



 

### <a name="using-hardware-overlays"></a>Verwenden von Hardwareüberlagerungen

Um die Überlagerungsoberfläche anzuzeigen, ruft die Anwendung **IDirect3DDevice9Ex::P resentEx auf.** Die Direct3D-Runtime zeichnet automatisch den Zielfarbschlüssel.

Die folgenden **PresentEx-Flags** sind für Überlagerungen definiert.



| Flag                              | Beschreibung                                                                                                                                                                                                                                                                           |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **D3DPRESENT \_ UPDATECOLORKEY**    | Legen Sie dieses Flag fest, wenn Desktopfenster-Manager Komposition (DWM) deaktiviert ist. Dieses Flag bewirkt, dass Direct3D den Farbschlüssel neu gezeichnet.<br/> Wenn DWM aktiviert ist, ist dieses Flag nicht erforderlich, da Direct3D den Farbschlüssel einmal auf der Oberfläche zeichnet, die DWM für die Umleitung verwendet.<br/> |
| **D3DPRESENT \_ HIDEOVERLAY**       | Blendet die Überlagerung aus.                                                                                                                                                                                                                                                                    |
| **D3DPRESENT \_ UPDATEOVERLAYONLY** | Aktualisiert die Überlagerung, ohne den Inhalt zu ändern.<br/> Dieses Flag ist nützlich, wenn das Fenster verschoben wird, während das Video angehalten wird.<br/>                                                                                                                                           |



 

Eine Anwendung sollte darauf vorbereitet sein, die folgenden Fälle zu verarbeiten:

-   Wenn eine andere Anwendung die Überlagerung verwendet, gibt **PresentEx** **D3DERR \_ NOTAVAILABLE zurück.**
-   Wenn das Fenster auf einen anderen Monitor verschoben wird, muss die Anwendung die Swapkette neu erstellen. Andernfalls gibt **PresentEx** **D3DERR \_ INVALIDDEVICE** zurück, wenn die Anwendung **PresentEx** aufruft, um die Überlagerung auf einem anderen Monitor anzuzeigen.
-   Wenn sich der Anzeigemodus ändert, versucht Direct3D, die Überlagerung wiederherzustellen. Wenn der neue Modus die Überlagerung nicht unterstützt, gibt **PresentEx** **D3DERR \_ UNSUPPORTEDOVERLAY** zurück.

### <a name="example-code"></a>Beispielcode

Im folgenden Beispiel wird gezeigt, wie eine Überlagerungsoberfläche erstellt wird.


```C++
const UINT VIDEO_WIDTH = 256;
const UINT VIDEO_HEIGHT = 256;

HRESULT CreateHWOverlay(
    HWND hwnd, 
    IDirect3D9Ex *pD3D, 
    IDirect3DDevice9Ex **ppDevice
    )
{
    *ppDevice = NULL;

    D3DCAPS9                caps;
    ZeroMemory(&caps, sizeof(caps));

    HRESULT hr = pD3D->GetDeviceCaps(
        D3DADAPTER_DEFAULT,
        D3DDEVTYPE_HAL,
        &caps
        );

    if (FAILED(hr))
    {
        return hr;
    }

    // Check if overlay is supported.
    if (!(caps.Caps & D3DCAPS_OVERLAY))
    {
        return D3DERR_UNSUPPORTEDOVERLAY;
    }

    D3DOVERLAYCAPS          overlayCaps = { 0 };

    IDirect3DDevice9Ex           *pDevice = NULL;
    IDirect3D9ExOverlayExtension *pOverlay = NULL;

    // Check specific overlay capabilities.
    hr = pD3D->QueryInterface(IID_PPV_ARGS(&pOverlay));

    if (SUCCEEDED(hr))
    {
        hr = pOverlay->CheckDeviceOverlayType(
            D3DADAPTER_DEFAULT,
            D3DDEVTYPE_HAL,
            VIDEO_WIDTH,
            VIDEO_HEIGHT,
            D3DFMT_X8R8G8B8,
            NULL,
            D3DDISPLAYROTATION_IDENTITY,
            &overlayCaps
            );
    }

    // Create the overlay.
    if (SUCCEEDED(hr))
    {

        DWORD flags =   D3DCREATE_FPU_PRESERVE | 
                        D3DCREATE_MULTITHREADED | 
                        D3DCREATE_SOFTWARE_VERTEXPROCESSING;

        
        D3DPRESENT_PARAMETERS   pp = { 0 };

        pp.BackBufferWidth = overlayCaps.MaxOverlayDisplayWidth;
        pp.BackBufferHeight = overlayCaps.MaxOverlayDisplayHeight;
        pp.BackBufferFormat = D3DFMT_X8R8G8B8;
        pp.SwapEffect = D3DSWAPEFFECT_OVERLAY;
        pp.hDeviceWindow = hwnd;
        pp.Windowed = TRUE;
        pp.Flags = D3DPRESENTFLAG_VIDEO;
        pp.FullScreen_RefreshRateInHz = D3DPRESENT_RATE_DEFAULT;
        pp.PresentationInterval       = D3DPRESENT_INTERVAL_ONE;

        hr = pD3D->CreateDeviceEx(D3DADAPTER_DEFAULT, D3DDEVTYPE_HAL,
            NULL, flags, &pp, NULL, &pDevice);
    }

    if (SUCCEEDED(hr))
    {
        (*ppDevice) = pDevice;
        (*ppDevice)->AddRef();
    }

    SafeRelease(&pD3D);
    SafeRelease(&pDevice);
    SafeRelease(&pOverlay);
    return hr;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D Video-APIs](direct3d-video-apis.md)
</dt> </dl>

 

 




