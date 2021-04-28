---
description: Festlegen von DXVA-HD-Zuzuständen
ms.assetid: 7f339ee8-01e6-4bbb-8563-020ff0e02499
title: Festlegen von DXVA-HD-Zuzuständen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91766e3eb10399d908ab361e13db4b94fe07b653
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108092698"
---
# <a name="setting-dxva-hd-states"></a><span data-ttu-id="62ce3-103">Festlegen von DXVA-HD-Zuzuständen</span><span class="sxs-lookup"><span data-stu-id="62ce3-103">Setting DXVA-HD States</span></span>

<span data-ttu-id="62ce3-104">Während der Videoverarbeitung behält das Gerät DXVA-HD (Microsoft DirectX Video Acceleration High Definition) einen persistenten Zustand von einem Frame zum nächsten bei.</span><span class="sxs-lookup"><span data-stu-id="62ce3-104">During video processing, the Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device maintains a persistent state from one frame to the next.</span></span> <span data-ttu-id="62ce3-105">Jeder Zustand verfügt über einen dokumentierten Standardwert.</span><span class="sxs-lookup"><span data-stu-id="62ce3-105">Each state has a documented default.</span></span> <span data-ttu-id="62ce3-106">Nachdem Sie das Gerät konfiguriert haben, legen Sie alle Zustände fest, die Sie von den Standardwerten ändern möchten.</span><span class="sxs-lookup"><span data-stu-id="62ce3-106">After you configure the device, set any states that you wish to change from their defaults.</span></span> <span data-ttu-id="62ce3-107">Bevor Sie die einzelnen Frames verarbeiten, aktualisieren Sie alle Zustände, die sich ändern sollten.</span><span class="sxs-lookup"><span data-stu-id="62ce3-107">Before you process each frame, update any states that should change.</span></span>

> [!Note]  
> <span data-ttu-id="62ce3-108">Dieser Entwurf unterscheidet sich von DXVA-VP.</span><span class="sxs-lookup"><span data-stu-id="62ce3-108">This design differs from DXVA-VP.</span></span> <span data-ttu-id="62ce3-109">In DXVA-VP muss die Anwendung alle VP-Parameter mit jedem Frame angeben.</span><span class="sxs-lookup"><span data-stu-id="62ce3-109">In DXVA-VP, the application must specify all of the VP parameters with each frame.</span></span>

 

<span data-ttu-id="62ce3-110">Gerätezustände lassen sich in zwei Kategorien unterteilen:</span><span class="sxs-lookup"><span data-stu-id="62ce3-110">Device states fall into two categories:</span></span>

-   <span data-ttu-id="62ce3-111">*Streamzustände* wenden jeden Eingabestream separat an.</span><span class="sxs-lookup"><span data-stu-id="62ce3-111">*Stream* states apply each input stream separately.</span></span> <span data-ttu-id="62ce3-112">Sie können auf jeden Stream unterschiedliche Einstellungen anwenden.</span><span class="sxs-lookup"><span data-stu-id="62ce3-112">You can apply different settings to each stream.</span></span>
-   <span data-ttu-id="62ce3-113">*Blit-Zustände* gelten global für den gesamten Blit-Videoverarbeitungs-Blit.</span><span class="sxs-lookup"><span data-stu-id="62ce3-113">*Blit* states apply globally to the entire video processing blit.</span></span>

<span data-ttu-id="62ce3-114">Die folgenden Streamzustände werden definiert.</span><span class="sxs-lookup"><span data-stu-id="62ce3-114">The following stream states are defined.</span></span>



| <span data-ttu-id="62ce3-115">Streamzustand</span><span class="sxs-lookup"><span data-stu-id="62ce3-115">Stream State</span></span>                                   | <span data-ttu-id="62ce3-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="62ce3-116">Description</span></span>                                                                                                     |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62ce3-117">**DXVAHD \_ STREAM \_ STATE \_ D3DFORMAT**</span><span class="sxs-lookup"><span data-stu-id="62ce3-117">**DXVAHD\_STREAM\_STATE\_D3DFORMAT**</span></span>           | <span data-ttu-id="62ce3-118">Eingabevideoformat.</span><span class="sxs-lookup"><span data-stu-id="62ce3-118">Input video format.</span></span>                                                                                             |
| <span data-ttu-id="62ce3-119">**DXVAHD \_ STREAM \_ STATE \_ FRAME \_ FORMAT**</span><span class="sxs-lookup"><span data-stu-id="62ce3-119">**DXVAHD\_STREAM\_STATE\_FRAME\_FORMAT**</span></span>       | <span data-ttu-id="62ce3-120">Interlacing.</span><span class="sxs-lookup"><span data-stu-id="62ce3-120">Interlacing.</span></span>                                                                                                    |
| <span data-ttu-id="62ce3-121">**DXVAHD \_ STREAM \_ STATE \_ INPUT \_ COLOR \_ SPACE**</span><span class="sxs-lookup"><span data-stu-id="62ce3-121">**DXVAHD\_STREAM\_STATE\_INPUT\_COLOR\_SPACE**</span></span> | <span data-ttu-id="62ce3-122">Eingabefarbraum.</span><span class="sxs-lookup"><span data-stu-id="62ce3-122">Input color space.</span></span> <span data-ttu-id="62ce3-123">Dieser Zustand gibt den RGB-Farbbereich und die YCbCr-Übertragungsmatrix für den Eingabestream an.</span><span class="sxs-lookup"><span data-stu-id="62ce3-123">This state specifies the RGB color range and the YCbCr transfer matrix for the input stream.</span></span> |
| <span data-ttu-id="62ce3-124">**DXVAHD \_ STREAM \_ STATE \_ OUTPUT \_ RATE**</span><span class="sxs-lookup"><span data-stu-id="62ce3-124">**DXVAHD\_STREAM\_STATE\_OUTPUT\_RATE**</span></span>        | <span data-ttu-id="62ce3-125">Ausgabebildrate.</span><span class="sxs-lookup"><span data-stu-id="62ce3-125">Output frame rate.</span></span> <span data-ttu-id="62ce3-126">Dieser Zustand steuert die Frameratenkonvertierung.</span><span class="sxs-lookup"><span data-stu-id="62ce3-126">This state controls frame-rate conversion.</span></span>                                                   |
| <span data-ttu-id="62ce3-127">**DXVAHD \_ STREAM \_ STATE \_ SOURCE \_ RECT**</span><span class="sxs-lookup"><span data-stu-id="62ce3-127">**DXVAHD\_STREAM\_STATE\_SOURCE\_RECT**</span></span>        | <span data-ttu-id="62ce3-128">Quellrechteck.</span><span class="sxs-lookup"><span data-stu-id="62ce3-128">Source rectangle.</span></span>                                                                                               |
| <span data-ttu-id="62ce3-129">**DXVAHD \_ STREAM \_ STATE \_ DESTINATION \_ RECT**</span><span class="sxs-lookup"><span data-stu-id="62ce3-129">**DXVAHD\_STREAM\_STATE\_DESTINATION\_RECT**</span></span>   | <span data-ttu-id="62ce3-130">Zielrechteck.</span><span class="sxs-lookup"><span data-stu-id="62ce3-130">Destination rectangle.</span></span>                                                                                          |
| <span data-ttu-id="62ce3-131">**DXVAHD \_ STREAM \_ STATE \_ ALPHA**</span><span class="sxs-lookup"><span data-stu-id="62ce3-131">**DXVAHD\_STREAM\_STATE\_ALPHA**</span></span>               | <span data-ttu-id="62ce3-132">Planares Alpha.</span><span class="sxs-lookup"><span data-stu-id="62ce3-132">Planar alpha.</span></span>                                                                                                   |
| <span data-ttu-id="62ce3-133">**\_DXVAHD-STREAMSTATUSPALETTE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="62ce3-133">**DXVAHD\_STREAM\_STATE\_PALETTE**</span></span>             | <span data-ttu-id="62ce3-134">Farbpalette.</span><span class="sxs-lookup"><span data-stu-id="62ce3-134">Color palette.</span></span> <span data-ttu-id="62ce3-135">Dieser Zustand gilt nur für palettierte Eingabeformate.</span><span class="sxs-lookup"><span data-stu-id="62ce3-135">This state applies only to palettized input formats.</span></span>                                             |
| <span data-ttu-id="62ce3-136">**DXVAHD \_ STREAM \_ STATE \_ LUMA \_ KEY**</span><span class="sxs-lookup"><span data-stu-id="62ce3-136">**DXVAHD\_STREAM\_STATE\_LUMA\_KEY**</span></span>           | <span data-ttu-id="62ce3-137">Luma-Taste.</span><span class="sxs-lookup"><span data-stu-id="62ce3-137">Luma key.</span></span>                                                                                                       |
| <span data-ttu-id="62ce3-138">**DXVAHD \_ STREAM \_ STATE \_ ASPECT \_ RATIO**</span><span class="sxs-lookup"><span data-stu-id="62ce3-138">**DXVAHD\_STREAM\_STATE\_ASPECT\_RATIO**</span></span>       | <span data-ttu-id="62ce3-139">Pixel-Seitenverhältnis.</span><span class="sxs-lookup"><span data-stu-id="62ce3-139">Pixel aspect ratio.</span></span>                                                                                             |
| <span data-ttu-id="62ce3-140">**DXVAHD \_ STREAM \_ STATE \_ FILTER \_ Xxxx**</span><span class="sxs-lookup"><span data-stu-id="62ce3-140">**DXVAHD\_STREAM\_STATE\_FILTER\_Xxxx**</span></span>        | <span data-ttu-id="62ce3-141">Bildfiltereinstellungen.</span><span class="sxs-lookup"><span data-stu-id="62ce3-141">Image filter settings.</span></span> <span data-ttu-id="62ce3-142">Der Treiber kann Helligkeit, Kontrast und andere Bildfilter unterstützen.</span><span class="sxs-lookup"><span data-stu-id="62ce3-142">The driver can support brightness, contrast, and other image filters.</span></span>                    |



 

<span data-ttu-id="62ce3-143">Die folgenden Blitzustände sind definiert:</span><span class="sxs-lookup"><span data-stu-id="62ce3-143">The following blit states are defined:</span></span>



| <span data-ttu-id="62ce3-144">Blitzustand</span><span class="sxs-lookup"><span data-stu-id="62ce3-144">Blit State</span></span>                                   | <span data-ttu-id="62ce3-145">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="62ce3-145">Description</span></span>                                                                  |
|----------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="62ce3-146">**DXVAHD \_ BLT \_ STATE \_ TARGET \_ RECT**</span><span class="sxs-lookup"><span data-stu-id="62ce3-146">**DXVAHD\_BLT\_STATE\_TARGET\_RECT**</span></span>         | <span data-ttu-id="62ce3-147">Zielrechteck.</span><span class="sxs-lookup"><span data-stu-id="62ce3-147">Target rectangle.</span></span>                                                            |
| <span data-ttu-id="62ce3-148">**DXVAHD \_ BLT \_ STATE \_ BACKGROUND \_ COLOR**</span><span class="sxs-lookup"><span data-stu-id="62ce3-148">**DXVAHD\_BLT\_STATE\_BACKGROUND\_COLOR**</span></span>    | <span data-ttu-id="62ce3-149">Hintergrundfarbe.</span><span class="sxs-lookup"><span data-stu-id="62ce3-149">Background color.</span></span>                                                            |
| <span data-ttu-id="62ce3-150">**DXVAHD \_ BLT \_ STATE \_ OUTPUT \_ COLOR \_ SPACE**</span><span class="sxs-lookup"><span data-stu-id="62ce3-150">**DXVAHD\_BLT\_STATE\_OUTPUT\_COLOR\_SPACE**</span></span> | <span data-ttu-id="62ce3-151">Ausgabefarbraum.</span><span class="sxs-lookup"><span data-stu-id="62ce3-151">Output color space.</span></span>                                                          |
| <span data-ttu-id="62ce3-152">**DXVAHD \_ BLT \_ STATE \_ ALPHA \_ FILL**</span><span class="sxs-lookup"><span data-stu-id="62ce3-152">**DXVAHD\_BLT\_STATE\_ALPHA\_FILL**</span></span>          | <span data-ttu-id="62ce3-153">Alphafüllmodus.</span><span class="sxs-lookup"><span data-stu-id="62ce3-153">Alpha fill mode.</span></span>                                                             |
| <span data-ttu-id="62ce3-154">**DXVAHD \_ BLT \_ STATE \_ CONSTRICTION**</span><span class="sxs-lookup"><span data-stu-id="62ce3-154">**DXVAHD\_BLT\_STATE\_CONSTRICTION**</span></span>         | <span data-ttu-id="62ce3-155">Verengung.</span><span class="sxs-lookup"><span data-stu-id="62ce3-155">Constriction.</span></span> <span data-ttu-id="62ce3-156">Dieser Zustand steuert, ob das Gerät die Ausgabe heruntersampelt.</span><span class="sxs-lookup"><span data-stu-id="62ce3-156">This state controls whether the device downsamples the output.</span></span> |



 

<span data-ttu-id="62ce3-157">Rufen Sie zum Festlegen eines Streamzustands die [**IDXVAHD \_ VideoProcessor::SetVideoProcessStreamState-Methode**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessstreamstate) auf.</span><span class="sxs-lookup"><span data-stu-id="62ce3-157">To set a stream state, call the [**IDXVAHD\_VideoProcessor::SetVideoProcessStreamState**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessstreamstate) method.</span></span> <span data-ttu-id="62ce3-158">Rufen Sie zum Festlegen eines Blitzustands die [**IDXVAHD \_ VideoProcessor::SetVideoProcessBltState-Methode**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessbltstate) auf.</span><span class="sxs-lookup"><span data-stu-id="62ce3-158">To set a blit state, call the [**IDXVAHD\_VideoProcessor::SetVideoProcessBltState**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessbltstate) method.</span></span> <span data-ttu-id="62ce3-159">In beiden Methoden gibt ein -Enumerationswert den festgelegten Zustand an.</span><span class="sxs-lookup"><span data-stu-id="62ce3-159">In both of these methods, an enumeration value specifies the state to set.</span></span> <span data-ttu-id="62ce3-160">Die Zustandsdaten werden mithilfe einer zustandsspezifischen Datenstruktur angegeben, die von der Anwendung in einen void-Typ **umgeformt \*** wird.</span><span class="sxs-lookup"><span data-stu-id="62ce3-160">The state data is given using a state-specific data structure, which the application casts to a **void\*** type.</span></span>

<span data-ttu-id="62ce3-161">Im folgenden Codebeispiel werden das Eingabeformat und das Zielrechteck für Stream 0 und die Hintergrundfarbe auf Schwarz fest.</span><span class="sxs-lookup"><span data-stu-id="62ce3-161">The following code example sets the input format and destination rectangle for stream 0, and sets the background color to black.</span></span>


```C++
HRESULT SetDXVAHDStates(HWND hwnd, D3DFORMAT inputFormat)
{
    // Set the initial stream states.

    // Set the format of the input stream

    DXVAHD_STREAM_STATE_D3DFORMAT_DATA d3dformat = { inputFormat };

    HRESULT hr = g_pDXVAVP->SetVideoProcessStreamState(
        0,  // Stream index
        DXVAHD_STREAM_STATE_D3DFORMAT,
        sizeof(d3dformat),
        &d3dformat
        );

    if (SUCCEEDED(hr))
    { 
        // For this example, the input stream contains progressive frames.

        DXVAHD_STREAM_STATE_FRAME_FORMAT_DATA frame_format = { DXVAHD_FRAME_FORMAT_PROGRESSIVE };
        
        hr = g_pDXVAVP->SetVideoProcessStreamState(
            0, // Stream index
            DXVAHD_STREAM_STATE_FRAME_FORMAT,
            sizeof(frame_format),
            &frame_format
            );
    }

    if (SUCCEEDED(hr))
    { 
        // Compute the letterbox area.

        RECT rcDest;
        GetClientRect(hwnd, &rcDest);

        RECT rcSrc;
        SetRect(&rcSrc, 0, 0, VIDEO_WIDTH, VIDEO_HEIGHT);

        rcDest = LetterBoxRect(rcSrc, rcDest);

        // Set the destination rectangle, so the frame is displayed within the 
        // letterbox area. Otherwise, the frame is stretched to cover the 
        // entire surface.

        DXVAHD_STREAM_STATE_DESTINATION_RECT_DATA DstRect = { TRUE, rcDest };

        hr = g_pDXVAVP->SetVideoProcessStreamState(
            0, // Stream index 
            DXVAHD_STREAM_STATE_DESTINATION_RECT,
            sizeof(DstRect),
            &DstRect
            );
    }

    if (SUCCEEDED(hr))
    { 
        DXVAHD_COLOR_RGBA rgbBackground = { 0.0f, 0.0f, 0.0f, 1.0f };  // RGBA

        DXVAHD_BLT_STATE_BACKGROUND_COLOR_DATA background = { FALSE, rgbBackground };

        hr = g_pDXVAVP->SetVideoProcessBltState(
            DXVAHD_BLT_STATE_BACKGROUND_COLOR,
            sizeof (background),
            &background
            );
    }

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="62ce3-162">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="62ce3-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62ce3-163">DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="62ce3-163">DXVA-HD</span></span>](dxva-hd.md)
</dt> </dl>

 

 



