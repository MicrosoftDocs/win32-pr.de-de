---
description: Erstellen eines DXVA-HD-Videoprozessors
ms.assetid: 43a97dc8-19b3-412c-a015-339099bf4f6c
title: Erstellen eines DXVA-HD-Videoprozessors
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4945153dfd3e14f1d2caae9b0a84f201745ea24722781bf998930477054138c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974819"
---
# <a name="creating-a-dxva-hd-video-processor"></a>Erstellen eines DXVA-HD-Videoprozessors

Microsoft DirectX Video Acceleration High Definition (DXVA-HD) verwendet zwei primäre Schnittstellen:

-   [**IDXVAHD \_ Gerät**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_device). Stellt das DXVA-HD-Gerät dar. Verwenden Sie diese Schnittstelle, um die Gerätefunktionen abzufragen und den Videoprozessor zu erstellen.
-   [**IDXVAHD \_ VideoProcessor**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_videoprocessor). Stellt eine Reihe von Videoverarbeitungsfunktionen dar. Verwenden Sie diese Schnittstelle, um das Videoverarbeitungs-Blit auszuführen.

Im folgenden Code werden die folgenden globalen Variablen angenommen:


```C++
IDirect3D9Ex            *g_pD3D = NULL;     
IDirect3DDevice9Ex      *g_pD3DDevice = NULL;   // Direct3D device.
IDXVAHD_Device          *g_pDXVAHD = NULL;      // DXVA-HD device.
IDXVAHD_VideoProcessor  *g_pDXVAVP = NULL;      // DXVA-HD video processor.
IDirect3DSurface9       *g_pSurface = NULL;     // Video surface.
        
const D3DFORMAT     RENDER_TARGET_FORMAT = D3DFMT_X8R8G8B8;
const D3DFORMAT     VIDEO_FORMAT         = D3DFMT_X8R8G8B8; 
const UINT          VIDEO_FPS            = 60;
const UINT          VIDEO_WIDTH          = 640;
const UINT          VIDEO_HEIGHT         = 480;
```



So erstellen Sie einen DXVA-HD-Videoprozessor:

1.  Füllen Sie eine [**DXVAHD \_ CONTENT \_ DESC-Struktur**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_content_desc) mit einer Beschreibung des Videoinhalts aus. Der Treiber verwendet diese Informationen als Hinweis, um die Funktionen des Videoprozessors zu optimieren. Die -Struktur enthält keine vollständige Formatbeschreibung.
    ```C++
        DXVAHD_RATIONAL fps = { VIDEO_FPS, 1 }; 

        DXVAHD_CONTENT_DESC desc;

        desc.InputFrameFormat = DXVAHD_FRAME_FORMAT_PROGRESSIVE;
        desc.InputFrameRate = fps;
        desc.InputWidth = VIDEO_WIDTH;
        desc.InputHeight = VIDEO_HEIGHT;
        desc.OutputFrameRate = fps;
        desc.OutputWidth = VIDEO_WIDTH;
        desc.OutputHeight = VIDEO_HEIGHT;
    ```

    

2.  Rufen [**Sie DXVAHD \_ CreateDevice**](/windows/desktop/api/dxvahd/nf-dxvahd-dxvahd_createdevice) auf, um das DXVA-HD-Gerät zu erstellen. Diese Funktion gibt einen Zeiger auf die [**IDXVAHD-Geräteschnittstelle \_**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_device) zurück.
    ```C++
        hr = DXVAHD_CreateDevice(g_pD3DDevice, &desc, DXVAHD_DEVICE_USAGE_PLAYBACK_NORMAL,
            NULL, &pDXVAHD);
    ```

    

3.  Rufen Sie [**IDXVAHD \_ Device::GetVideoProcessorDeviceCaps auf.**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps) Diese Methode füllt eine [**DXVAHD \_ VPDEVCAPS-Struktur**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) mit den Gerätefunktionen auf. Wenn Sie bestimmte Videoverarbeitungsfeatures wie luma keying oder image filtering benötigen, überprüfen Sie deren Verfügbarkeit mithilfe dieser Struktur.
    ```C++
        DXVAHD_VPDEVCAPS caps;

        hr = pDXVAHD->GetVideoProcessorDeviceCaps(&caps);
    ```

    

4.  Überprüfen Sie, ob das DXVA-HD-Gerät die benötigten Eingabevideoformate unterstützt. Im Thema [Überprüfen der unterstützten DXVA-HD-Formate](checking-supported-dxva-hd-formats.md) wird dieser Schritt ausführlicher beschrieben.
5.  Überprüfen Sie, ob das DXVA-HD-Gerät das von Ihnen geforderte Ausgabeformat unterstützt. Im Abschnitt [Überprüfen der unterstützten DXVA-HD-Formate](checking-supported-dxva-hd-formats.md) wird dieser Schritt ausführlicher beschrieben.
6.  Ordnen Sie ein Array von [**DXVAHD-VPCAPS-Strukturen \_**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps) zu. Die Anzahl der Arrayelemente, die zugeordnet werden müssen, wird vom **VideoProcessorCount-Element** der [**DXVAHD \_ VPDEVCAPS-Struktur**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) angegeben, die in Schritt 3 abgerufen wurde.
    ```C++
        // Create the array of video processor caps. 
        
        DXVAHD_VPCAPS *pVPCaps = 
            new (std::nothrow) DXVAHD_VPCAPS[ caps.VideoProcessorCount ];

        if (pVPCaps == NULL)
        {
            return E_OUTOFMEMORY;
        }
    ```

    

7.  Jede [**\_ DXVAHD-VPCAPS-Struktur**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps) stellt einen eindeutigen Videoprozessor dar. Sie können dieses Array durchlaufen, um die Funktionen der einzelnen Videoprozessoren zu ermitteln. Die Struktur enthält Informationen über die Funktionen zum Deinterlacing, zum Telekopieren und zur Konvertierung der Bildfrequenz des Videoprozessors.
8.  Wählen Sie einen zu erstellende Videoprozessor aus. Das **VPGuid-Element** der [**DXVAHD-VPCAPS-Struktur \_**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps) enthält eine GUID, die den Videoprozessor eindeutig identifiziert. Übergeben Sie diese GUID an die [**IDXVAHD \_ Device::CreateVideoProcessor-Methode.**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideoprocessor) Die -Methode gibt einen [**IDXVAHD-VideoProcessor-Zeiger \_**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_videoprocessor) zurück.
    ```C++
        HRESULT hr = pDXVAHD->GetVideoProcessorCaps(
            caps.VideoProcessorCount, pVPCaps);
    ```

    

9.  Rufen Sie optional [**IDXVAHD \_ Device::CreateVideoSurface**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface) auf, um ein Array von Eingabevideooberflächen zu erstellen.

Das folgende Codebeispiel zeigt die vollständige Abfolge der Schritte:


```C++
// Initializes the DXVA-HD video processor.

// NOTE: The following example makes some simplifying assumptions:
//
// 1. There is a single input stream.
// 2. The input frame rate matches the output frame rate.
// 3. No advanced DXVA-HD features are needed, such as luma keying or IVTC.
// 4. The application uses a single input video surface.

HRESULT InitializeDXVAHD()
{
    if (g_pD3DDevice == NULL)
    {
        return E_FAIL;
    }

    HRESULT hr = S_OK;

    IDXVAHD_Device          *pDXVAHD = NULL;
    IDXVAHD_VideoProcessor  *pDXVAVP = NULL;
    IDirect3DSurface9       *pSurf = NULL;

    DXVAHD_RATIONAL fps = { VIDEO_FPS, 1 }; 

    DXVAHD_CONTENT_DESC desc;

    desc.InputFrameFormat = DXVAHD_FRAME_FORMAT_PROGRESSIVE;
    desc.InputFrameRate = fps;
    desc.InputWidth = VIDEO_WIDTH;
    desc.InputHeight = VIDEO_HEIGHT;
    desc.OutputFrameRate = fps;
    desc.OutputWidth = VIDEO_WIDTH;
    desc.OutputHeight = VIDEO_HEIGHT;

#ifdef USE_SOFTWARE_PLUGIN    
    HMODULE hSWPlugin = LoadLibrary(L"C:\\dxvahdsw.dll");

    PDXVAHDSW_Plugin pSWPlugin = (PDXVAHDSW_Plugin)GetProcAddress(hSWPlugin, "DXVAHDSW_Plugin");

    hr = DXVAHD_CreateDevice(g_pD3DDevice, &desc,DXVAHD_DEVICE_USAGE_PLAYBACK_NORMAL,
        pSWPlugin, &pDXVAHD);
#else
    hr = DXVAHD_CreateDevice(g_pD3DDevice, &desc, DXVAHD_DEVICE_USAGE_PLAYBACK_NORMAL,
        NULL, &pDXVAHD);
#endif
    if (FAILED(hr))
    {
        goto done;
    }

    DXVAHD_VPDEVCAPS caps;

    hr = pDXVAHD->GetVideoProcessorDeviceCaps(&caps);
    if (FAILED(hr))
    {
        goto done;
    }

    // Check whether the device supports the input and output formats.

    hr = CheckInputFormatSupport(pDXVAHD, caps, VIDEO_FORMAT);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = CheckOutputFormatSupport(pDXVAHD, caps, RENDER_TARGET_FORMAT);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the VP device.
    hr = CreateVPDevice(pDXVAHD, caps, &pDXVAVP);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the video surface for the primary video stream.
    hr = pDXVAHD->CreateVideoSurface(
        VIDEO_WIDTH,
        VIDEO_HEIGHT,
        VIDEO_FORMAT,
        caps.InputPool,
        0,  // Usage
        DXVAHD_SURFACE_TYPE_VIDEO_INPUT,
        1,      // Number of surfaces to create
        &pSurf, // Array of surface pointers
        NULL
        );

    if (FAILED(hr))
    {
        goto done;
    }


    g_pDXVAHD = pDXVAHD;
    g_pDXVAHD->AddRef();

    g_pDXVAVP = pDXVAVP;
    g_pDXVAVP->AddRef();

    g_pSurface = pSurf;
    g_pSurface->AddRef();

done:
    SafeRelease(&pDXVAHD);
    SafeRelease(&pDXVAVP);
    SafeRelease(&pSurf);
    return hr;
}
```



Die In diesem Beispiel gezeigte CreateVPDevice-Funktion erstellt den Videoprozessor (Schritte 5 bis 7):


```C++
// Creates a DXVA-HD video processor.

HRESULT CreateVPDevice(
    IDXVAHD_Device          *pDXVAHD,
    const DXVAHD_VPDEVCAPS& caps,
    IDXVAHD_VideoProcessor  **ppDXVAVP
    )
{
    // Create the array of video processor caps. 
    
    DXVAHD_VPCAPS *pVPCaps = 
        new (std::nothrow) DXVAHD_VPCAPS[ caps.VideoProcessorCount ];

    if (pVPCaps == NULL)
    {
        return E_OUTOFMEMORY;
    }

    HRESULT hr = pDXVAHD->GetVideoProcessorCaps(
        caps.VideoProcessorCount, pVPCaps);

    // At this point, an application could loop through the array and examine
    // the capabilities. For purposes of this example, however, we simply
    // create the first video processor in the list.

    if (SUCCEEDED(hr))
    {
        // The VPGuid member contains the GUID that identifies the video 
        // processor.

        hr = pDXVAHD->CreateVideoProcessor(&pVPCaps[0].VPGuid, ppDXVAVP);
    }

    delete [] pVPCaps;
    return hr;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DXVA-HD](dxva-hd.md)
</dt> </dl>

 

 



