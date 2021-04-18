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
# <a name="creating-a-dxva-hd-video-processor"></a><span data-ttu-id="f222e-103">Erstellen eines DXVA-HD-Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="f222e-103">Creating a DXVA-HD Video Processor</span></span>

<span data-ttu-id="f222e-104">Microsoft DirectX Video Acceleration High Definition (DXVA-HD) verwendet zwei primäre Schnittstellen:</span><span class="sxs-lookup"><span data-stu-id="f222e-104">Microsoft DirectX Video Acceleration High Definition (DXVA-HD) uses two primary interfaces:</span></span>

-   <span data-ttu-id="f222e-105">[**Idxvahd \_ Gerät**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_device).</span><span class="sxs-lookup"><span data-stu-id="f222e-105">[**IDXVAHD\_Device**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_device).</span></span> <span data-ttu-id="f222e-106">Stellt das DXVA-HD-Gerät dar.</span><span class="sxs-lookup"><span data-stu-id="f222e-106">Represents the DXVA-HD device.</span></span> <span data-ttu-id="f222e-107">Verwenden Sie diese Schnittstelle, um die Gerätefunktionen abzufragen und den Videoprozessor zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f222e-107">Use this interface to query the device capabilities and create the video processor.</span></span>
-   <span data-ttu-id="f222e-108">[**Idxvahd \_ Videoprocessor**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_videoprocessor).</span><span class="sxs-lookup"><span data-stu-id="f222e-108">[**IDXVAHD\_VideoProcessor**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_videoprocessor).</span></span> <span data-ttu-id="f222e-109">Stellt einen Satz von Video Verarbeitungsfunktionen dar.</span><span class="sxs-lookup"><span data-stu-id="f222e-109">Represents a set of video processing capabilities.</span></span> <span data-ttu-id="f222e-110">Verwenden Sie diese Schnittstelle, um das Video Processing Blit auszuführen.</span><span class="sxs-lookup"><span data-stu-id="f222e-110">Use this interface to perform the video processing blit.</span></span>

<span data-ttu-id="f222e-111">Im folgenden Code werden die folgenden globalen Variablen angenommen:</span><span class="sxs-lookup"><span data-stu-id="f222e-111">In the code that follows, the following global variables are assumed:</span></span>


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



<span data-ttu-id="f222e-112">So erstellen Sie einen DXVA-HD-Videoprozessor:</span><span class="sxs-lookup"><span data-stu-id="f222e-112">To create a DXVA-HD video processor:</span></span>

1.  <span data-ttu-id="f222e-113">Füllen Sie eine [**dxvahd \_ - \_ inhaltsinenstruktur**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_content_desc) mit einer Beschreibung des Video Inhalts aus.</span><span class="sxs-lookup"><span data-stu-id="f222e-113">Fill in a [**DXVAHD\_CONTENT\_DESC**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_content_desc) structure with a description of the video content.</span></span> <span data-ttu-id="f222e-114">Der Treiber verwendet diese Informationen als Hinweis, um die Funktionen des Video Prozessors zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="f222e-114">The driver uses this information as a hint to optimize the capabilities of the video processor.</span></span> <span data-ttu-id="f222e-115">Die-Struktur enthält keine komplette Formatbeschreibung.</span><span class="sxs-lookup"><span data-stu-id="f222e-115">The structure does not contain a complete format description.</span></span>
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

    

2.  <span data-ttu-id="f222e-116">Rufen Sie [**dxvahd \_ kreatedevice**](/windows/desktop/api/dxvahd/nf-dxvahd-dxvahd_createdevice) auf, um das DXVA-HD-Gerät zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f222e-116">Call [**DXVAHD\_CreateDevice**](/windows/desktop/api/dxvahd/nf-dxvahd-dxvahd_createdevice) to create the DXVA-HD device.</span></span> <span data-ttu-id="f222e-117">Diese Funktion gibt einen Zeiger auf die [**idxvahd- \_ Geräte**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_device) Schnittstelle zurück.</span><span class="sxs-lookup"><span data-stu-id="f222e-117">This function returns a pointer to the [**IDXVAHD\_Device**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_device) interface.</span></span>
    ```C++
        hr = DXVAHD_CreateDevice(g_pD3DDevice, &desc, DXVAHD_DEVICE_USAGE_PLAYBACK_NORMAL,
            NULL, &pDXVAHD);
    ```

    

3.  <span data-ttu-id="f222e-118">Nennen Sie [**idxvahd \_ Device:: getvideoprocesordecoecaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps).</span><span class="sxs-lookup"><span data-stu-id="f222e-118">Call [**IDXVAHD\_Device::GetVideoProcessorDeviceCaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps).</span></span> <span data-ttu-id="f222e-119">Diese Methode füllt eine [**dxvahd \_ vpdevcaps-**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) Struktur mit den Gerätefunktionen aus.</span><span class="sxs-lookup"><span data-stu-id="f222e-119">This method fills in a [**DXVAHD\_VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) structure with the device capabilities.</span></span> <span data-ttu-id="f222e-120">Wenn Sie bestimmte Video Verarbeitungsfunktionen benötigen, wie z. b. die Verwendung von Luma oder das Filtern von Bildern, überprüfen Sie Ihre Verfügbarkeit mithilfe dieser Struktur.</span><span class="sxs-lookup"><span data-stu-id="f222e-120">If you require specific video processing features, such as luma keying or image filtering, check their availability by using this structure.</span></span>
    ```C++
        DXVAHD_VPDEVCAPS caps;

        hr = pDXVAHD->GetVideoProcessorDeviceCaps(&caps);
    ```

    

4.  <span data-ttu-id="f222e-121">Überprüfen Sie, ob das Gerät DXVA-HD die Eingabe Videoformate unterstützt, die Sie benötigen.</span><span class="sxs-lookup"><span data-stu-id="f222e-121">Check whether the DXVA-HD device supports the input video formats that you require.</span></span> <span data-ttu-id="f222e-122">Im Thema über [prüfen unterstützter DXVA-HD-Formate wird](checking-supported-dxva-hd-formats.md) dieser Schritt ausführlicher beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f222e-122">The topic [Checking Supported DXVA-HD Formats](checking-supported-dxva-hd-formats.md) describes this step in more detail.</span></span>
5.  <span data-ttu-id="f222e-123">Überprüfen Sie, ob das Gerät DXVA-HD das Ausgabeformat unterstützt, das Sie benötigen.</span><span class="sxs-lookup"><span data-stu-id="f222e-123">Check whether the DXVA-HD device supports the output format that you require.</span></span> <span data-ttu-id="f222e-124">Dieser Schritt wird im Abschnitt über [prüfen unterstützter DXVA-HD-Formate](checking-supported-dxva-hd-formats.md) ausführlicher beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f222e-124">The section [Checking Supported DXVA-HD Formats](checking-supported-dxva-hd-formats.md) describes this step in more detail.</span></span>
6.  <span data-ttu-id="f222e-125">Zuordnen eines Arrays von [**dxvahd- \_ vpcaps-**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps) Strukturen.</span><span class="sxs-lookup"><span data-stu-id="f222e-125">Allocate an array of [**DXVAHD\_VPCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps) structures.</span></span> <span data-ttu-id="f222e-126">Die Anzahl der Array Elemente, die zugeordnet werden müssen, wird durch den **videoprocess orcount** -Member der [**dxvahd \_ vpdevcaps-**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) Struktur angegeben, der in Schritt 3 abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="f222e-126">The number of array elements that must be allocated is given by the **VideoProcessorCount** member of the [**DXVAHD\_VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) structure, obtained in step 3.</span></span>
    ```C++
        // Create the array of video processor caps. 
        
        DXVAHD_VPCAPS *pVPCaps = 
            new (std::nothrow) DXVAHD_VPCAPS[ caps.VideoProcessorCount ];

        if (pVPCaps == NULL)
        {
            return E_OUTOFMEMORY;
        }
    ```

    

7.  <span data-ttu-id="f222e-127">Jede [**dxvahd- \_ vpcaps-**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps) Struktur stellt einen eindeutigen Videoprozessor dar.</span><span class="sxs-lookup"><span data-stu-id="f222e-127">Each [**DXVAHD\_VPCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps) structure represents a distinct video processor.</span></span> <span data-ttu-id="f222e-128">Sie können dieses Array durchlaufen, um die Funktionen der einzelnen Video Prozessoren zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="f222e-128">You can loop through this array to discover the capabilities of each video processor.</span></span> <span data-ttu-id="f222e-129">Die Struktur enthält Informationen zu den Funktionen Deinterlacing, telecine und Frameraten Konvertierung des Video Prozessors.</span><span class="sxs-lookup"><span data-stu-id="f222e-129">The structure includes information about the deinterlacing, telecine, and frame-rate conversion capabilities of the video processor.</span></span>
8.  <span data-ttu-id="f222e-130">Wählen Sie einen zu Erstell-Videoprozessor aus.</span><span class="sxs-lookup"><span data-stu-id="f222e-130">Select a video processor to create.</span></span> <span data-ttu-id="f222e-131">Der **vpguid** -Member der [**dxvahd \_ vpcaps-**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps) Struktur enthält eine GUID, die den Videoprozessor eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="f222e-131">The **VPGuid** member of the [**DXVAHD\_VPCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps) structure contains a GUID that uniquely identifies the video processor.</span></span> <span data-ttu-id="f222e-132">Übergeben Sie diese GUID an die [**idxvahd \_ Device:: up-**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideoprocessor) Methode.</span><span class="sxs-lookup"><span data-stu-id="f222e-132">Pass this GUID to the [**IDXVAHD\_Device::CreateVideoProcessor**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideoprocessor) method.</span></span> <span data-ttu-id="f222e-133">Die-Methode gibt einen [**idxvahd \_ videoprocessor-**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_videoprocessor) Zeiger zurück.</span><span class="sxs-lookup"><span data-stu-id="f222e-133">The method returns an [**IDXVAHD\_VideoProcessor**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_videoprocessor) pointer.</span></span>
    ```C++
        HRESULT hr = pDXVAHD->GetVideoProcessorCaps(
            caps.VideoProcessorCount, pVPCaps);
    ```

    

9.  <span data-ttu-id="f222e-134">Optional können Sie [**idxvahd \_ Device:: createvideosurface**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface) aufrufen, um ein Array von Eingabe Video Oberflächen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f222e-134">Optionally, call [**IDXVAHD\_Device::CreateVideoSurface**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface) to create an array of input video surfaces.</span></span>

<span data-ttu-id="f222e-135">Das folgende Codebeispiel zeigt die gesamte Abfolge von Schritten:</span><span class="sxs-lookup"><span data-stu-id="f222e-135">The following code example shows the complete sequence of steps:</span></span>


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



<span data-ttu-id="f222e-136">In diesem Beispiel wird die Funktion "in der Funktion" in der Funktion "" erstellt, die den Videoprozessor erstellt (Schritte 5 – 7):</span><span class="sxs-lookup"><span data-stu-id="f222e-136">The CreateVPDevice function show in this example creates the video processor (steps 5–7):</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="f222e-137">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f222e-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f222e-138">DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="f222e-138">DXVA-HD</span></span>](dxva-hd.md)
</dt> </dl>

 

 



