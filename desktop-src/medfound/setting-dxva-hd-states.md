---
description: .
ms.assetid: 7f339ee8-01e6-4bbb-8563-020ff0e02499
title: Festlegen von DXVA-HD-Zuständen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e539796aa5d3997b35739e75c80b438a7b5da50b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347854"
---
# <a name="setting-dxva-hd-states"></a><span data-ttu-id="07a42-103">Festlegen von DXVA-HD-Zuständen</span><span class="sxs-lookup"><span data-stu-id="07a42-103">Setting DXVA-HD States</span></span>

<span data-ttu-id="07a42-104">Während der Videoverarbeitung behält das Microsoft DirectX Video Acceleration High Definition-Gerät (DXVA-HD) einen persistenten Zustand von einem Frame zum nächsten bei.</span><span class="sxs-lookup"><span data-stu-id="07a42-104">During video processing, the Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device maintains a persistent state from one frame to the next.</span></span> <span data-ttu-id="07a42-105">Jeder Status weist einen dokumentierten Standardwert auf.</span><span class="sxs-lookup"><span data-stu-id="07a42-105">Each state has a documented default.</span></span> <span data-ttu-id="07a42-106">Nachdem Sie das Gerät konfiguriert haben, legen Sie alle Zustände fest, die Sie von den Standardeinstellungen ändern möchten.</span><span class="sxs-lookup"><span data-stu-id="07a42-106">After you configure the device, set any states that you wish to change from their defaults.</span></span> <span data-ttu-id="07a42-107">Aktualisieren Sie vor dem Verarbeiten der einzelnen Frames alle Zustände, die sich ändern sollten.</span><span class="sxs-lookup"><span data-stu-id="07a42-107">Before you process each frame, update any states that should change.</span></span>

> [!Note]  
> <span data-ttu-id="07a42-108">Dieser Entwurf unterscheidet sich von DXVA-VP.</span><span class="sxs-lookup"><span data-stu-id="07a42-108">This design differs from DXVA-VP.</span></span> <span data-ttu-id="07a42-109">In DXVA-VP muss die Anwendung alle VP-Parameter für jeden Frame angeben.</span><span class="sxs-lookup"><span data-stu-id="07a42-109">In DXVA-VP, the application must specify all of the VP parameters with each frame.</span></span>

 

<span data-ttu-id="07a42-110">Gerätezustände werden in zwei Kategorien unterteilt:</span><span class="sxs-lookup"><span data-stu-id="07a42-110">Device states fall into two categories:</span></span>

-   <span data-ttu-id="07a42-111">*Streamzustände* wenden jeden Eingabedaten Strom separat an.</span><span class="sxs-lookup"><span data-stu-id="07a42-111">*Stream* states apply each input stream separately.</span></span> <span data-ttu-id="07a42-112">Sie können für jeden Stream verschiedene Einstellungen anwenden.</span><span class="sxs-lookup"><span data-stu-id="07a42-112">You can apply different settings to each stream.</span></span>
-   <span data-ttu-id="07a42-113">*Blit* -Zustände gelten global für den gesamten Video Verarbeitungs Blit.</span><span class="sxs-lookup"><span data-stu-id="07a42-113">*Blit* states apply globally to the entire video processing blit.</span></span>

<span data-ttu-id="07a42-114">Die folgenden streamzustände sind definiert.</span><span class="sxs-lookup"><span data-stu-id="07a42-114">The following stream states are defined.</span></span>



| <span data-ttu-id="07a42-115">Streamstatus</span><span class="sxs-lookup"><span data-stu-id="07a42-115">Stream State</span></span>                                   | <span data-ttu-id="07a42-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07a42-116">Description</span></span>                                                                                                     |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07a42-117">**Dxvahd \_ - \_ streamstatus \_ D3DFORMAT**</span><span class="sxs-lookup"><span data-stu-id="07a42-117">**DXVAHD\_STREAM\_STATE\_D3DFORMAT**</span></span>           | <span data-ttu-id="07a42-118">Eingabe Videoformat.</span><span class="sxs-lookup"><span data-stu-id="07a42-118">Input video format.</span></span>                                                                                             |
| <span data-ttu-id="07a42-119">**dxvahd \_ Stream \_ State- \_ Frame \_ Format**</span><span class="sxs-lookup"><span data-stu-id="07a42-119">**DXVAHD\_STREAM\_STATE\_FRAME\_FORMAT**</span></span>       | <span data-ttu-id="07a42-120">Zeilen Sprung.</span><span class="sxs-lookup"><span data-stu-id="07a42-120">Interlacing.</span></span>                                                                                                    |
| <span data-ttu-id="07a42-121">**dxvahd-Daten \_ Strom- \_ Zustands \_ Eingabe- \_ Farbraum \_**</span><span class="sxs-lookup"><span data-stu-id="07a42-121">**DXVAHD\_STREAM\_STATE\_INPUT\_COLOR\_SPACE**</span></span> | <span data-ttu-id="07a42-122">Eingabefarbraum.</span><span class="sxs-lookup"><span data-stu-id="07a42-122">Input color space.</span></span> <span data-ttu-id="07a42-123">Dieser Zustand gibt den RGB-Farbbereich und die YCbCr-Übertragungs Matrix für den Eingabestream an.</span><span class="sxs-lookup"><span data-stu-id="07a42-123">This state specifies the RGB color range and the YCbCr transfer matrix for the input stream.</span></span> |
| <span data-ttu-id="07a42-124">**dxvahd-Daten \_ Strom- \_ Status- \_ Ausgabe \_ Rate**</span><span class="sxs-lookup"><span data-stu-id="07a42-124">**DXVAHD\_STREAM\_STATE\_OUTPUT\_RATE**</span></span>        | <span data-ttu-id="07a42-125">Ausgabe Frame Rate.</span><span class="sxs-lookup"><span data-stu-id="07a42-125">Output frame rate.</span></span> <span data-ttu-id="07a42-126">Dieser Zustand steuert die Konvertierung von Frameraten.</span><span class="sxs-lookup"><span data-stu-id="07a42-126">This state controls frame-rate conversion.</span></span>                                                   |
| <span data-ttu-id="07a42-127">**dxvahd \_ Stream- \_ Zustands \_ Quelle \_ Rect**</span><span class="sxs-lookup"><span data-stu-id="07a42-127">**DXVAHD\_STREAM\_STATE\_SOURCE\_RECT**</span></span>        | <span data-ttu-id="07a42-128">Quell Rechteck.</span><span class="sxs-lookup"><span data-stu-id="07a42-128">Source rectangle.</span></span>                                                                                               |
| <span data-ttu-id="07a42-129">**dxvahd \_ Stream \_ State \_ \_ Rect**</span><span class="sxs-lookup"><span data-stu-id="07a42-129">**DXVAHD\_STREAM\_STATE\_DESTINATION\_RECT**</span></span>   | <span data-ttu-id="07a42-130">Ziel Rechteck.</span><span class="sxs-lookup"><span data-stu-id="07a42-130">Destination rectangle.</span></span>                                                                                          |
| <span data-ttu-id="07a42-131">**dxvahd \_ Stream \_ State \_ Alpha**</span><span class="sxs-lookup"><span data-stu-id="07a42-131">**DXVAHD\_STREAM\_STATE\_ALPHA**</span></span>               | <span data-ttu-id="07a42-132">Planar alpha.</span><span class="sxs-lookup"><span data-stu-id="07a42-132">Planar alpha.</span></span>                                                                                                   |
| <span data-ttu-id="07a42-133">**dxvahd-Daten \_ Strom- \_ Status \_ Palette**</span><span class="sxs-lookup"><span data-stu-id="07a42-133">**DXVAHD\_STREAM\_STATE\_PALETTE**</span></span>             | <span data-ttu-id="07a42-134">Farbpalette.</span><span class="sxs-lookup"><span data-stu-id="07a42-134">Color palette.</span></span> <span data-ttu-id="07a42-135">Dieser Zustand gilt nur für Paletten-Eingabeformate.</span><span class="sxs-lookup"><span data-stu-id="07a42-135">This state applies only to palettized input formats.</span></span>                                             |
| <span data-ttu-id="07a42-136">**dxvahd- \_ streamstatuszustandsschlüssel \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="07a42-136">**DXVAHD\_STREAM\_STATE\_LUMA\_KEY**</span></span>           | <span data-ttu-id="07a42-137">Luma-Taste.</span><span class="sxs-lookup"><span data-stu-id="07a42-137">Luma key.</span></span>                                                                                                       |
| <span data-ttu-id="07a42-138">**dxvahd-Daten \_ Strom- \_ Status \_ Seiten \_ Verhältnis**</span><span class="sxs-lookup"><span data-stu-id="07a42-138">**DXVAHD\_STREAM\_STATE\_ASPECT\_RATIO**</span></span>       | <span data-ttu-id="07a42-139">Pixel Seitenverhältnis.</span><span class="sxs-lookup"><span data-stu-id="07a42-139">Pixel aspect ratio.</span></span>                                                                                             |
| <span data-ttu-id="07a42-140">**Dxvahd \_ Stream \_ State \_ Filter \_ xxxx**</span><span class="sxs-lookup"><span data-stu-id="07a42-140">**DXVAHD\_STREAM\_STATE\_FILTER\_Xxxx**</span></span>        | <span data-ttu-id="07a42-141">Bild Filtereinstellungen.</span><span class="sxs-lookup"><span data-stu-id="07a42-141">Image filter settings.</span></span> <span data-ttu-id="07a42-142">Der Treiber kann Helligkeit, Kontrast und andere Bild Filter unterstützen.</span><span class="sxs-lookup"><span data-stu-id="07a42-142">The driver can support brightness, contrast, and other image filters.</span></span>                    |



 

<span data-ttu-id="07a42-143">Die folgenden Blit-Zustände sind definiert:</span><span class="sxs-lookup"><span data-stu-id="07a42-143">The following blit states are defined:</span></span>



| <span data-ttu-id="07a42-144">Blit-Status</span><span class="sxs-lookup"><span data-stu-id="07a42-144">Blit State</span></span>                                   | <span data-ttu-id="07a42-145">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07a42-145">Description</span></span>                                                                  |
|----------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="07a42-146">**dxvahd \_ blt- \_ Zustands \_ Ziel \_ Rect**</span><span class="sxs-lookup"><span data-stu-id="07a42-146">**DXVAHD\_BLT\_STATE\_TARGET\_RECT**</span></span>         | <span data-ttu-id="07a42-147">Ziel Rechteck.</span><span class="sxs-lookup"><span data-stu-id="07a42-147">Target rectangle.</span></span>                                                            |
| <span data-ttu-id="07a42-148">**dxvahd \_ blt- \_ Status \_ Hintergrund \_ Farbe**</span><span class="sxs-lookup"><span data-stu-id="07a42-148">**DXVAHD\_BLT\_STATE\_BACKGROUND\_COLOR**</span></span>    | <span data-ttu-id="07a42-149">Hintergrundfarbe.</span><span class="sxs-lookup"><span data-stu-id="07a42-149">Background color.</span></span>                                                            |
| <span data-ttu-id="07a42-150">**dxvahd \_ blt- \_ Zustands \_ Ausgabe \_ Farbraum \_**</span><span class="sxs-lookup"><span data-stu-id="07a42-150">**DXVAHD\_BLT\_STATE\_OUTPUT\_COLOR\_SPACE**</span></span> | <span data-ttu-id="07a42-151">Ausgabe Farbraum.</span><span class="sxs-lookup"><span data-stu-id="07a42-151">Output color space.</span></span>                                                          |
| <span data-ttu-id="07a42-152">**dxvahd \_ blt \_ State \_ alpha \_ Fill**</span><span class="sxs-lookup"><span data-stu-id="07a42-152">**DXVAHD\_BLT\_STATE\_ALPHA\_FILL**</span></span>          | <span data-ttu-id="07a42-153">Alpha Füllmodus.</span><span class="sxs-lookup"><span data-stu-id="07a42-153">Alpha fill mode.</span></span>                                                             |
| <span data-ttu-id="07a42-154">**dxvahd \_ blt- \_ Zustands \_ Einschränkung**</span><span class="sxs-lookup"><span data-stu-id="07a42-154">**DXVAHD\_BLT\_STATE\_CONSTRICTION**</span></span>         | <span data-ttu-id="07a42-155">Einschränkungen.</span><span class="sxs-lookup"><span data-stu-id="07a42-155">Constriction.</span></span> <span data-ttu-id="07a42-156">Mit diesem Status wird gesteuert, ob die Ausgabe des Geräts herabgestuft wird.</span><span class="sxs-lookup"><span data-stu-id="07a42-156">This state controls whether the device downsamples the output.</span></span> |



 

<span data-ttu-id="07a42-157">Um einen streamstatus festzulegen, müssen Sie die [**idxvahd \_ videoprocessor:: setvideoprocessstreamstate**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessstreamstate) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="07a42-157">To set a stream state, call the [**IDXVAHD\_VideoProcessor::SetVideoProcessStreamState**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessstreamstate) method.</span></span> <span data-ttu-id="07a42-158">Um einen Blit-Status festzulegen, müssen Sie die [**idxvahd \_ videoprocessor:: setvideoprocessbltstate**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessbltstate) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="07a42-158">To set a blit state, call the [**IDXVAHD\_VideoProcessor::SetVideoProcessBltState**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessbltstate) method.</span></span> <span data-ttu-id="07a42-159">Bei beiden Methoden gibt ein Enumerationswert den festzulegenden Zustand an.</span><span class="sxs-lookup"><span data-stu-id="07a42-159">In both of these methods, an enumeration value specifies the state to set.</span></span> <span data-ttu-id="07a42-160">Die Zustandsdaten werden mithilfe einer Zustands spezifischen Datenstruktur angegeben, die von der Anwendung in einen **void \*** -Typ umgewandelt wird.</span><span class="sxs-lookup"><span data-stu-id="07a42-160">The state data is given using a state-specific data structure, which the application casts to a **void\*** type.</span></span>

<span data-ttu-id="07a42-161">Im folgenden Codebeispiel werden das Eingabeformat und das Ziel Rechteck für Stream 0 festgelegt, und die Hintergrundfarbe wird auf schwarz festgelegt.</span><span class="sxs-lookup"><span data-stu-id="07a42-161">The following code example sets the input format and destination rectangle for stream 0, and sets the background color to black.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="07a42-162">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="07a42-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07a42-163">DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="07a42-163">DXVA-HD</span></span>](dxva-hd.md)
</dt> </dl>

 

 



