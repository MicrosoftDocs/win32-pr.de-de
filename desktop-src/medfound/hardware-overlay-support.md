---
description: Beschreibt die Verwendung von Hardware Überlagerungen in Direct3D 9.
ms.assetid: fa9d5bf5-4c0f-471a-b639-d329b0cd89a4
title: Hardware-Overlay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adcae33cdf55de59bdcd074829d52b4c1c43ea5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350517"
---
# <a name="hardware-overlay-support"></a>Hardware-Overlay

Eine Hardware Überlagerung ist ein dedizierter Bereich von Videospeicher, der auf der primären Oberfläche überlastet werden kann. Wenn das Overlay angezeigt wird, wird kein Kopiervorgang durchgeführt. Der Überlagerungs Vorgang wird in Hardware ausgeführt, ohne die Daten auf der primären Oberfläche zu ändern.

Die Verwendung von Hardware Überlagerungen für die Videowiedergabe war in früheren Versionen von Windows üblich, da die Überlagerungen für Videoinhalte mit einer hohen Framerate effizient sind. Ab Windows 7 unterstützt Direct3D 9 Hardware Überlagerungen. Diese Unterstützung ist in erster Linie für die Videowiedergabe gedacht und unterscheidet sich in gewisser Hinsicht von früheren DirectDraw-APIs:

-   Das Overlay kann nicht verkleinert, gespiegelt oder Deinterlacing werden.
-   Quell Farben und Alpha Blending werden nicht unterstützt.
-   Überlagerungen können gestreckt werden, wenn die Überlagerungs Hardware diese unterstützt. Andernfalls wird die Streckung nicht unterstützt. In der Praxis unterstützen nicht alle Grafiktreiber das Stretching.
-   Jedes Gerät unterstützt höchstens ein Overlay.
-   Die Überlagerung wird mithilfe eines Ziel Farb Schlüssels ausgeführt, aber die Direct3D-Laufzeit wählt automatisch die Farbe aus und zeichnet das Ziel Rechteck. Direct3D verfolgt automatisch die Position des Fensters und aktualisiert die Überlagerungs Position, wenn der **presentex** aufgerufen wird.

### <a name="creating-a-hardware-overlay-surface"></a>Erstellen einer Hardware Überlagerungs Oberfläche

Um die Überlagerungs Unterstützung abzufragen, nennen Sie **IDirect3D9:: GetDeviceCaps**. Wenn der Treiber die Hardware Überlagerung unterstützt, wird das **D3DCAPS \_ Overlay** -Flag in D3DCAPS9 festgelegt **. Caps** -Member.

Um herauszufinden, ob ein bestimmtes Überlagerungs Format für einen bestimmten Anzeigemodus unterstützt wird, müssen Sie [**IDirect3D9ExOverlayExtension:: checkdeviceoverlaytype**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9exoverlayextension-checkdeviceoverlaytype)aufrufen.

Um das Overlay zu erstellen, rufen Sie **IDirect3D9Ex:: kreatedeviceex** auf, und geben Sie den **D3DSWAPEFFECT \_ Overlay** -Swap-Effekt an. Der Hintergrund Puffer kann ein nicht-RGB-Format verwenden, wenn es von der Hardware unterstützt wird.

Überlagerungs Oberflächen weisen die folgenden Einschränkungen auf:

-   Die Anwendung kann nicht mehr als eine Überlagerungs Austausch Kette erstellen.
-   Das Overlay muss im Fenstermodus verwendet werden. Sie kann nicht im Vollbildmodus verwendet werden.
-   Der Überlagerungs Swap-Effekt muss mit der **IDirect3DDevice9Ex** -Schnittstelle verwendet werden. Sie wird für **IDirect3DDevice9** nicht unterstützt.
-   Multisampling kann nicht verwendet werden.
-   Die **D3DPRESENT \_ donotflip** -und **D3DPRESENT \_ fliprestart** -Flags werden nicht unterstützt.
-   Die Präsentations Statistik ist für die Überlagerungs Oberfläche nicht verfügbar.

Wenn die Hardware keine Streckung unterstützt, wird empfohlen, eine SwapChain so groß wie den Anzeigemodus zu erstellen, damit die Größe des Fensters in beliebige Dimensionen geändert werden kann. Das Neuerstellen der SwapChain ist nicht optimal geeignet, um die Größe des Fensters zu ändern, da es schwerwiegende Renderingartefakte verursachen kann. Aufgrund der Art und Weise, wie die GPU den Überlagerungs Speicher verwaltet, kann das Neuerstellen der Swapkette möglicherweise dazu führen, dass eine Anwendung nicht mehr über den Videospeicher verfügt.

### <a name="new-d3dpresent_parameters-flags"></a>Neue D3DPRESENT \_ Parameter-Flags

Die folgenden **D3DPRESENT \_ Parameter** -Flags werden zum Erstellen von Überlagerungen definiert.



| Flag                                      | Beschreibung                                                                                                                                                                        |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **D3DPRESENTFLAG \_ Overlay \_ limitedrgb**   | Der RGB-Bereich ist 16 – 235. Der Standardwert ist 0 – 255. <br/> Erfordert die **D3DOVERLAYCAPS \_ limitedranger GB** -Funktion.<br/>                                                 |
| **D3DPRESENTFLAG \_ Overlay \_ YCbCr \_ BT709** | YUV-Farben verwenden die BT. 709-Definition. Der Standardwert ist "BT. 601". <br/> Erfordert die **D3DOVERLAYCAPS \_ YCbCr \_ BT709** -Funktion.<br/>                                      |
| **D3DPRESENTFLAG \_ Overlay \_ YCbCr \_ xwycc** | Geben Sie die Daten mithilfe von Extended YCbCr (xwycc) aus.<br/> Erfordert die **D3DOVERLAYCAPS \_ YCbCr \_ BT601 \_ xvYCC** -oder **D3DOVERLAYCAPS \_ YCbCr \_ BT709 \_ xwycc** -Funktion.<br/> |



 

### <a name="using-hardware-overlays"></a>Verwenden von Hardware Überlagerungen

Um die Überlagerungs Oberfläche anzuzeigen, ruft die Anwendung **IDirect3DDevice9Ex::P resentex** auf. Die Direct3D-Laufzeit zeichnet automatisch den Ziel Farbschlüssel.

Die folgenden **presentex** -Flags werden für Überlagerungen definiert.



| Flag                              | Beschreibung                                                                                                                                                                                                                                                                           |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **D3DPRESENT \_ updatecolorkey**    | Legen Sie dieses Flag fest, wenn die Komposition von Desktopfenster-Manager (DWM) deaktiviert ist. Dieses Flag bewirkt, dass Direct3D den Farbschlüssel neu zeichnet.<br/> Wenn DWM aktiviert ist, ist dieses Flag nicht erforderlich, da Direct3D den Farbschlüssel einmal auf der Oberfläche zeichnet, die DWM für die Umleitung verwendet.<br/> |
| **D3DPRESENT \_ hideoverlay**       | Blendet die Überlagerung aus.                                                                                                                                                                                                                                                                    |
| **D3DPRESENT \_ updateoverlayonly** | Aktualisiert das Overlay, ohne den Inhalt zu ändern.<br/> Dieses Flag ist nützlich, wenn das Fenster verschoben wird, während das Video angehalten wird.<br/>                                                                                                                                           |



 

Eine Anwendung sollte darauf vorbereitet sein, die folgenden Fälle zu behandeln:

-   Wenn eine andere Anwendung das Overlay verwendet, gibt **presentex** **D3DERR \_ NotAvailable** zurück.
-   Wenn das Fenster auf einen anderen Monitor verschoben wird, muss die SwapChain von der Anwendung neu erstellt werden. Andernfalls gibt **presentex** **D3DERR \_ invaliddevice** zurück, wenn die Anwendung einen **presentex** aufruft, um die Überlagerung auf einem anderen Monitor anzuzeigen.
-   Wenn sich der Anzeigemodus ändert, versucht Direct3D, die Überlagerung wiederherzustellen. Wenn der neue Modus das Overlay nicht unterstützt, gibt **presentex** **D3DERR \_ unsupportedoverlay** zurück.

### <a name="example-code"></a>Beispielcode

Im folgenden Beispiel wird gezeigt, wie eine Überlagerungs Oberfläche erstellt wird.


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

[Direct3D-Video-APIs](direct3d-video-apis.md)
</dt> </dl>

 

 




