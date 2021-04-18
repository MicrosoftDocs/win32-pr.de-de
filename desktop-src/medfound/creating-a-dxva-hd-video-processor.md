---
description: .
ms.assetid: 43a97dc8-19b3-412c-a015-339099bf4f6c
title: Erstellen eines DXVA-HD-Video Prozessors
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee524681cad43a8e140421e8e6eff30d44cabcc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343627"
---
# <a name="creating-a-dxva-hd-video-processor"></a>Erstellen eines DXVA-HD-Video Prozessors

Microsoft DirectX Video Acceleration High Definition (DXVA-HD) verwendet zwei primäre Schnittstellen:

-   [**Idxvahd \_ Gerät**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_device). Stellt das DXVA-HD-Gerät dar. Verwenden Sie diese Schnittstelle, um die Gerätefunktionen abzufragen und den Videoprozessor zu erstellen.
-   [**Idxvahd \_ Videoprocessor**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_videoprocessor). Stellt einen Satz von Video Verarbeitungsfunktionen dar. Verwenden Sie diese Schnittstelle, um das Video Processing Blit auszuführen.

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

1.  Füllen Sie eine [**dxvahd \_ - \_ inhaltsinenstruktur**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_content_desc) mit einer Beschreibung des Video Inhalts aus. Der Treiber verwendet diese Informationen als Hinweis, um die Funktionen des Video Prozessors zu optimieren. Die-Struktur enthält keine komplette Formatbeschreibung.
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

    

2.  Rufen Sie [**dxvahd \_ kreatedevice**](/windows/desktop/api/dxvahd/nf-dxvahd-dxvahd_createdevice) auf, um das DXVA-HD-Gerät zu erstellen. Diese Funktion gibt einen Zeiger auf die [**idxvahd- \_ Geräte**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_device) Schnittstelle zurück.
    ```C++
        hr = DXVAHD_CreateDevice(g_pD3DDevice, &desc, DXVAHD_DEVICE_USAGE_PLAYBACK_NORMAL,
            NULL, &pDXVAHD);
    ```

    

3.  Nennen Sie [**idxvahd \_ Device:: getvideoprocesordecoecaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps). Diese Methode füllt eine [**dxvahd \_ vpdevcaps-**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) Struktur mit den Gerätefunktionen aus. Wenn Sie bestimmte Video Verarbeitungsfunktionen benötigen, wie z. b. die Verwendung von Luma oder das Filtern von Bildern, überprüfen Sie Ihre Verfügbarkeit mithilfe dieser Struktur.
    ```C++
        DXVAHD_VPDEVCAPS caps;

        hr = pDXVAHD->GetVideoProcessorDeviceCaps(&caps);
    ```

    

4.  Überprüfen Sie, ob das Gerät DXVA-HD die Eingabe Videoformate unterstützt, die Sie benötigen. Im Thema über [prüfen unterstützter DXVA-HD-Formate wird](checking-supported-dxva-hd-formats.md) dieser Schritt ausführlicher beschrieben.
5.  Überprüfen Sie, ob das Gerät DXVA-HD das Ausgabeformat unterstützt, das Sie benötigen. Dieser Schritt wird im Abschnitt über [prüfen unterstützter DXVA-HD-Formate](checking-supported-dxva-hd-formats.md) ausführlicher beschrieben.
6.  Zuordnen eines Arrays von [**dxvahd- \_ vpcaps-**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps) Strukturen. Die Anzahl der Array Elemente, die zugeordnet werden müssen, wird durch den **videoprocess orcount** -Member der [**dxvahd \_ vpdevcaps-**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) Struktur angegeben, der in Schritt 3 abgerufen wurde.
    ```C++
        // Create the array of video processor caps. 
        
        DXVAHD_VPCAPS *pVPCaps = 
            new (std::nothrow) DXVAHD_VPCAPS[ caps.VideoProcessorCount ];

        if (pVPCaps == NULL)
        {
            return E_OUTOFMEMORY;
        }
    ```

    

7.  Jede [**dxvahd- \_ vpcaps-**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps) Struktur stellt einen eindeutigen Videoprozessor dar. Sie können dieses Array durchlaufen, um die Funktionen der einzelnen Video Prozessoren zu ermitteln. Die Struktur enthält Informationen zu den Funktionen Deinterlacing, telecine und Frameraten Konvertierung des Video Prozessors.
8.  Wählen Sie einen zu Erstell-Videoprozessor aus. Der **vpguid** -Member der [**dxvahd \_ vpcaps-**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps) Struktur enthält eine GUID, die den Videoprozessor eindeutig identifiziert. Übergeben Sie diese GUID an die [**idxvahd \_ Device:: up-**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideoprocessor) Methode. Die-Methode gibt einen [**idxvahd \_ videoprocessor-**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_videoprocessor) Zeiger zurück.
    ```C++
        HRESULT hr = pDXVAHD->GetVideoProcessorCaps(
            caps.VideoProcessorCount, pVPCaps);
    ```

    

9.  Optional können Sie [**idxvahd \_ Device:: createvideosurface**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface) aufrufen, um ein Array von Eingabe Video Oberflächen zu erstellen.

Das folgende Codebeispiel zeigt die gesamte Abfolge von Schritten:


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



In diesem Beispiel wird die Funktion "in der Funktion" in der Funktion "" erstellt, die den Videoprozessor erstellt (Schritte 5 – 7):


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

 

 



