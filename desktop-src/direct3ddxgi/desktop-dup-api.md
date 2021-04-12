---
description: Windows 8 deaktiviert standardmäßige Windows 2000-Anzeigetreiber Modell (XDDM)-Spiegelungs Treiber und bietet stattdessen die desktopduplikats-API.
ms.assetid: 523FBFAD-5D78-4EE3-A3B7-8FD5BA39DC46
title: Desktopduplizierungs-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad27f545318254404beb6372344d8dd0cdfdf604
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481078"
---
# <a name="desktop-duplication-api"></a><span data-ttu-id="e05ff-103">Desktopduplizierungs-API</span><span class="sxs-lookup"><span data-stu-id="e05ff-103">Desktop Duplication API</span></span>

<span data-ttu-id="e05ff-104">Windows 8 deaktiviert standardmäßige Windows 2000-Anzeigetreiber Modell (XDDM)-Spiegelungs Treiber und bietet stattdessen die desktopduplikats-API.</span><span class="sxs-lookup"><span data-stu-id="e05ff-104">Windows 8 disables standard Windows 2000 Display Driver Model (XDDM) mirror drivers and offers the desktop duplication API instead.</span></span> <span data-ttu-id="e05ff-105">Die Desktop Duplizierungs-API bietet Remote Zugriff auf ein Desktop Image für Zusammenarbeits Szenarien.</span><span class="sxs-lookup"><span data-stu-id="e05ff-105">The desktop duplication API provides remote access to a desktop image for collaboration scenarios.</span></span> <span data-ttu-id="e05ff-106">Apps können die Desktop Duplizierungs-API verwenden, um auf Frame-an-Frame-Aktualisierungen auf dem Desktop zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="e05ff-106">Apps can use the desktop duplication API to access frame-by-frame updates to the desktop.</span></span> <span data-ttu-id="e05ff-107">Da apps Aktualisierungen des Desktop Abbilds auf einer DXGI-Oberfläche erhalten, können die apps die gesamte Leistungsfähigkeit der GPU nutzen, um die Abbild Aktualisierungen zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="e05ff-107">Because apps receive updates to the desktop image in a DXGI surface, the apps can use the full power of the GPU to process the image updates.</span></span>

-   [<span data-ttu-id="e05ff-108">Aktualisieren der Desktop Image Daten</span><span class="sxs-lookup"><span data-stu-id="e05ff-108">Updating the desktop image data</span></span>](#updating-the-desktop-image-data)
-   [<span data-ttu-id="e05ff-109">Drehen des Desktop Bilds</span><span class="sxs-lookup"><span data-stu-id="e05ff-109">Rotating the desktop image</span></span>](#rotating-the-desktop-image)
-   [<span data-ttu-id="e05ff-110">Aktualisieren des Desktop Zeigers</span><span class="sxs-lookup"><span data-stu-id="e05ff-110">Updating the desktop pointer</span></span>](#updating-the-desktop-pointer)
-   [<span data-ttu-id="e05ff-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e05ff-111">Related topics</span></span>](#related-topics)

## <a name="updating-the-desktop-image-data"></a><span data-ttu-id="e05ff-112">Aktualisieren der Desktop Image Daten</span><span class="sxs-lookup"><span data-stu-id="e05ff-112">Updating the desktop image data</span></span>

<span data-ttu-id="e05ff-113">DXGI bietet eine Oberfläche, die ein aktuelles Desktop Bild durch die neue [**idxgioutputdupli:: acquunesextframe**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) -Methode enthält.</span><span class="sxs-lookup"><span data-stu-id="e05ff-113">DXGI provides a surface that contains a current desktop image through the new [**IDXGIOutputDuplication::AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) method.</span></span> <span data-ttu-id="e05ff-114">Das Format des Desktop Bilds lautet immer [**DXGI- \_ Format \_ B8G8R8A8 \_ unorm**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) , unabhängig vom aktuellen Anzeigemodus.</span><span class="sxs-lookup"><span data-stu-id="e05ff-114">The format of the desktop image is always [**DXGI\_FORMAT\_B8G8R8A8\_UNORM**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) no matter what the current display mode is.</span></span> <span data-ttu-id="e05ff-115">Zusammen mit dieser Oberfläche geben diese [**idxgioutputdupliduplizierungsmethoden**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgioutputduplication) die angezeigten Arten von Informationen zurück, die Ihnen helfen zu bestimmen, welche Pixel auf der Oberfläche verarbeitet werden müssen:</span><span class="sxs-lookup"><span data-stu-id="e05ff-115">Along with this surface, these [**IDXGIOutputDuplication**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgioutputduplication) methods return the indicated types of info that help you determine which pixels within the surface you need to process:</span></span>

-   <span data-ttu-id="e05ff-116">[**Idxgioutputdupli:: getframedirtyrects**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframedirtyrects) gibt geänderte Bereiche zurück, bei denen es sich um nicht überlappende Rechtecke handelt, die die Bereiche des Desktop Bilds angeben, die das Betriebssystem seit der Verarbeitung des vorherigen Desktop Abbilds aktualisiert hat.</span><span class="sxs-lookup"><span data-stu-id="e05ff-116">[**IDXGIOutputDuplication::GetFrameDirtyRects**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframedirtyrects) returns dirty regions, which are non-overlapping rectangles that indicate the areas of the desktop image that the operating system updated since you processed the previous desktop image.</span></span>
-   <span data-ttu-id="e05ff-117">[**Idxgioutputduplizierung:: getframemoverects**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframemoverects) gibt Verschiebungs Bereiche zurück, bei denen es sich um Rechtecke im Desktop Bild handelt, die das Betriebssystem an einen anderen Speicherort innerhalb desselben Bilds verschoben hat.</span><span class="sxs-lookup"><span data-stu-id="e05ff-117">[**IDXGIOutputDuplication::GetFrameMoveRects**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframemoverects) returns move regions, which are rectangles of pixels in the desktop image that the operating system moved to another location within the same image.</span></span> <span data-ttu-id="e05ff-118">Jeder Verschiebungs Bereich besteht aus einem Ziel Rechteck und einem Quellpunkt.</span><span class="sxs-lookup"><span data-stu-id="e05ff-118">Each move region consists of a destination rectangle and a source point.</span></span> <span data-ttu-id="e05ff-119">Der Quellpunkt gibt den Speicherort an, von dem aus das Betriebssystem den Bereich kopiert hat, und das Ziel Rechteck gibt an, wohin das Betriebssystem diese Region verschoben hat.</span><span class="sxs-lookup"><span data-stu-id="e05ff-119">The source point specifies the location from where the operating system copied the region and the destination rectangle specifies to where the operating system moved that region.</span></span> <span data-ttu-id="e05ff-120">Verschiebungs Bereiche sind immer nicht gestreckte Bereiche, sodass die Quelle immer dieselbe Größe wie das Ziel hat.</span><span class="sxs-lookup"><span data-stu-id="e05ff-120">Move regions are always non-stretched regions so the source is always the same size as the destination.</span></span>

<span data-ttu-id="e05ff-121">Angenommen, das Desktop Image wurde über eine langsame Verbindung mit der Remote Client-App übertragen.</span><span class="sxs-lookup"><span data-stu-id="e05ff-121">Suppose the desktop image was transmitted over a slow connection to your remote client app.</span></span> <span data-ttu-id="e05ff-122">Die Menge der Daten, die über die Verbindung gesendet wird, wird verringert, indem nur Daten darüber empfangen werden, wie die Client-App Bereiche von Pixeln und nicht die eigentlichen Pixeldaten verschieben muss.</span><span class="sxs-lookup"><span data-stu-id="e05ff-122">The amount of data that is sent over the connection is reduced by receiving only data about how your client app must move regions of pixels rather than actual pixel data.</span></span> <span data-ttu-id="e05ff-123">Zum Verarbeiten der Verschiebungen muss Ihre Client-App das gesamte letzte Abbild gespeichert haben.</span><span class="sxs-lookup"><span data-stu-id="e05ff-123">To process the moves, your client app must have stored the complete last image.</span></span>

<span data-ttu-id="e05ff-124">Wenngleich das Betriebssystem nicht verarbeitete Desktop Abbild Aktualisierungen akkumuliert, kann es nicht mehr genügend Speicherplatz für die genaue Speicherung der Update Regionen gibt.</span><span class="sxs-lookup"><span data-stu-id="e05ff-124">While the operating system accumulates unprocessed desktop image updates, it might run out of space to accurately store the update regions.</span></span> <span data-ttu-id="e05ff-125">In dieser Situation nimmt das Betriebssystem an, die Updates zu sammeln, indem Sie Sie mit vorhandenen Update Regionen zusammenfügen, um alle neuen Updates abzudecken.</span><span class="sxs-lookup"><span data-stu-id="e05ff-125">In this situation, the operating system starts to accumulate the updates by coalescing them with existing update regions to cover all new updates.</span></span> <span data-ttu-id="e05ff-126">Folglich deckt das Betriebssystem Pixel ab, die in diesem Frame noch nicht aktualisiert wurden.</span><span class="sxs-lookup"><span data-stu-id="e05ff-126">As a result, the operating system covers pixels that it has not actually updated in that frame yet.</span></span> <span data-ttu-id="e05ff-127">Diese Situation erzeugt jedoch keine visuellen Probleme in Ihrer Client-App, da Sie das gesamte Desktop Image und nicht nur die aktualisierten Pixel erhalten.</span><span class="sxs-lookup"><span data-stu-id="e05ff-127">But this situation doesn’t produce visual issues on your client app because you receive the entire desktop image and not just the updated pixels.</span></span>

<span data-ttu-id="e05ff-128">Um das korrekte Desktop Abbild zu rekonstruieren, muss Ihre Client-App zunächst alle Verschiebungs Regionen verarbeiten und dann alle geänderten Regionen verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="e05ff-128">To reconstruct the correct desktop image, your client app must first process all the move regions and then process all the dirty regions.</span></span> <span data-ttu-id="e05ff-129">Diese Listen mit den geänderten und verschiebenden Regionen können vollständig leer sein.</span><span class="sxs-lookup"><span data-stu-id="e05ff-129">Either of these lists of dirty and move regions can be completely empty.</span></span> <span data-ttu-id="e05ff-130">Der Beispielcode aus dem Beispiel für eine [Desktop Duplizierung](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/DXGI%20desktop%20duplication%20sample) zeigt, wie die Änderungs-und Verschiebungs Bereiche in einem einzelnen Frame verarbeitet werden:</span><span class="sxs-lookup"><span data-stu-id="e05ff-130">The example code from the [Desktop Duplication Sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/DXGI%20desktop%20duplication%20sample) shows how to process both the dirty and move regions in a single frame:</span></span>


```C++
//
// Get next frame and write it into Data
//
HRESULT DUPLICATIONMANAGER::GetFrame(_Out_ FRAME_DATA* Data)
{
    HRESULT hr = S_OK;

    IDXGIResource* DesktopResource = NULL;
    DXGI_OUTDUPL_FRAME_INFO FrameInfo;

    //Get new frame
    hr = DeskDupl->AcquireNextFrame(500, &FrameInfo, &DesktopResource);
    if (FAILED(hr))
    {
        if ((hr != DXGI_ERROR_ACCESS_LOST) && (hr != DXGI_ERROR_WAIT_TIMEOUT))
        {
            DisplayErr(L"Failed to acquire next frame in DUPLICATIONMANAGER", L"Error", hr);
        }
        return hr;
    }

    // If still holding old frame, destroy it
    if (AcquiredDesktopImage)
    {
        AcquiredDesktopImage->Release();
        AcquiredDesktopImage = NULL;
    }

    // QI for IDXGIResource
    hr = DesktopResource->QueryInterface(__uuidof(ID3D11Texture2D), reinterpret_cast<void **>(&AcquiredDesktopImage));
    DesktopResource->Release();
    DesktopResource = NULL;
    if (FAILED(hr))
    {
        DisplayErr(L"Failed to QI for ID3D11Texture2D from acquired IDXGIResource in DUPLICATIONMANAGER", L"Error", hr);
        return hr;
    }

    // Get metadata
    if (FrameInfo.TotalMetadataBufferSize)
    {
        // Old buffer too small
        if (FrameInfo.TotalMetadataBufferSize > MetaDataSize)
        {
            if (MetaDataBuffer)
            {
                delete [] MetaDataBuffer;
                MetaDataBuffer = NULL;
            }
            MetaDataBuffer = new (std::nothrow) BYTE[FrameInfo.TotalMetadataBufferSize];
            if (!MetaDataBuffer)
            {
                DisplayErr(L"Failed to allocate memory for metadata in DUPLICATIONMANAGER", L"Error", E_OUTOFMEMORY);
                MetaDataSize = 0;
                Data->MoveCount = 0;
                Data->DirtyCount = 0;
                return E_OUTOFMEMORY;
            }
            MetaDataSize = FrameInfo.TotalMetadataBufferSize;
        }

        UINT BufSize = FrameInfo.TotalMetadataBufferSize;

        // Get move rectangles
        hr = DeskDupl->GetFrameMoveRects(BufSize, reinterpret_cast<DXGI_OUTDUPL_MOVE_RECT*>(MetaDataBuffer), &BufSize);
        if (FAILED(hr))
        {
            if (hr != DXGI_ERROR_ACCESS_LOST)
            {
                DisplayErr(L"Failed to get frame move rects in DUPLICATIONMANAGER", L"Error", hr);
            }
            Data->MoveCount = 0;
            Data->DirtyCount = 0;
            return hr;
        }
        Data->MoveCount = BufSize / sizeof(DXGI_OUTDUPL_MOVE_RECT);

        BYTE* DirtyRects = MetaDataBuffer + BufSize;
        BufSize = FrameInfo.TotalMetadataBufferSize - BufSize;

        // Get dirty rectangles
        hr = DeskDupl->GetFrameDirtyRects(BufSize, reinterpret_cast<RECT*>(DirtyRects), &BufSize);
        if (FAILED(hr))
        {
            if (hr != DXGI_ERROR_ACCESS_LOST)
            {
                DisplayErr(L"Failed to get frame dirty rects in DUPLICATIONMANAGER", L"Error", hr);
            }
            Data->MoveCount = 0;
            Data->DirtyCount = 0;
            return hr;
        }
        Data->DirtyCount = BufSize / sizeof(RECT);

        Data->MetaData = MetaDataBuffer;
    }

    Data->Frame = AcquiredDesktopImage;
    Data->FrameInfo = FrameInfo;

    return hr;
}

//
// Release frame
//
HRESULT DUPLICATIONMANAGER::DoneWithFrame()
{
    HRESULT hr = S_OK;

    hr = DeskDupl->ReleaseFrame();
    if (FAILED(hr))
    {
        DisplayErr(L"Failed to release frame in DUPLICATIONMANAGER", L"Error", hr);
        return hr;
    }

    if (AcquiredDesktopImage)
    {
        AcquiredDesktopImage->Release();
        AcquiredDesktopImage = NULL;
    }

    return hr;
}
```



## <a name="rotating-the-desktop-image"></a><span data-ttu-id="e05ff-131">Drehen des Desktop Bilds</span><span class="sxs-lookup"><span data-stu-id="e05ff-131">Rotating the desktop image</span></span>

<span data-ttu-id="e05ff-132">Sie müssen Ihrer Client-App zur Desktop Duplizierung expliziten Code hinzufügen, um gedrehte Modi zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="e05ff-132">You must add explicit code to your desktop duplication client app to support rotated modes.</span></span> <span data-ttu-id="e05ff-133">In einem gedrehten Modus befindet sich die Oberfläche, die Sie von [**idxgioutputdupli:: acquunenextframe**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) erhalten, immer in der nicht gedrehten Ausrichtung, und das Desktop Bild wird innerhalb der Oberfläche gedreht.</span><span class="sxs-lookup"><span data-stu-id="e05ff-133">In a rotated mode, the surface that you receive from [**IDXGIOutputDuplication::AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) is always in the un-rotated orientation, and the desktop image is rotated within the surface.</span></span> <span data-ttu-id="e05ff-134">Wenn der Desktop z. b. auf 768x1024 bei 90 °-Drehung festgelegt ist, gibt **acquunenextframe** eine 1024 x 768-Oberfläche zurück, wobei das Desktop Bild darin gedreht wird.</span><span class="sxs-lookup"><span data-stu-id="e05ff-134">For example, if the desktop is set to 768x1024 at 90 degrees rotation, **AcquireNextFrame** returns a 1024x768 surface with the desktop image rotated within it.</span></span> <span data-ttu-id="e05ff-135">Hier finden Sie einige Beispiele für die Rotation.</span><span class="sxs-lookup"><span data-stu-id="e05ff-135">Here are some rotation examples.</span></span>



| <span data-ttu-id="e05ff-136">Anzeigemodus in der Anzeige-Systemsteuerung festgelegt</span><span class="sxs-lookup"><span data-stu-id="e05ff-136">Display mode set from display control panel</span></span> | <span data-ttu-id="e05ff-137">Von GDI oder DXGI zurückgegebener Anzeigemodus</span><span class="sxs-lookup"><span data-stu-id="e05ff-137">Display mode returned by GDI or DXGI</span></span> | <span data-ttu-id="e05ff-138">Von " [ **acquunesextframe** " zurückgegebene Oberfläche](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe)</span><span class="sxs-lookup"><span data-stu-id="e05ff-138">Surface returned from [**AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe)</span></span>                |
|---------------------------------------------|--------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e05ff-139">1024 x 768-Querformat</span><span class="sxs-lookup"><span data-stu-id="e05ff-139">1024x768 landscape</span></span>                          | <span data-ttu-id="e05ff-140">-Drehung mit 1024 x 768 0 Grad</span><span class="sxs-lookup"><span data-stu-id="e05ff-140">1024x768 0 degree rotation</span></span>           | <span data-ttu-id="e05ff-141">1024 x 768 Zeilen \[ zeiligen Zeilen\]</span><span class="sxs-lookup"><span data-stu-id="e05ff-141">1024x768\[newline\]</span></span> ![nicht gedrehter Remote Desktop](images/dxgi-outdupl-0-rotate.png)<br/>            |
| <span data-ttu-id="e05ff-143">1024 x 768-Hochformat</span><span class="sxs-lookup"><span data-stu-id="e05ff-143">1024x768 portrait</span></span>                           | <span data-ttu-id="e05ff-144">768x 1024 90 Grad Drehung</span><span class="sxs-lookup"><span data-stu-id="e05ff-144">768x1024 90 degree rotation</span></span>          | <span data-ttu-id="e05ff-145">1024 x 768 Zeilen \[ zeiligen Zeilen\]</span><span class="sxs-lookup"><span data-stu-id="e05ff-145">1024x768\[newline\]</span></span> ![90-Grad-Remote Desktop gedreht](images/dxgi-outdupl-90-rotate.png)<br/>   |
| <span data-ttu-id="e05ff-147">1024 x 768-Querformat (gekippt)</span><span class="sxs-lookup"><span data-stu-id="e05ff-147">1024x768 landscape (flipped)</span></span>                | <span data-ttu-id="e05ff-148">1024 x 768 180 Grad Drehung</span><span class="sxs-lookup"><span data-stu-id="e05ff-148">1024x768 180 degree rotation</span></span>         | <span data-ttu-id="e05ff-149">1024 x 768 Zeilen \[ zeiligen Zeilen\]</span><span class="sxs-lookup"><span data-stu-id="e05ff-149">1024x768\[newline\]</span></span> ![180-Grad-Remote Desktop gedreht](images/dxgi-outdupl-180-rotate.png)<br/> |
| <span data-ttu-id="e05ff-151">1024 x 768-Hochformat (gekippt)</span><span class="sxs-lookup"><span data-stu-id="e05ff-151">1024x768 portrait (flipped)</span></span>                 | <span data-ttu-id="e05ff-152">768x 1024 270 Grad Drehung</span><span class="sxs-lookup"><span data-stu-id="e05ff-152">768x1024 270 degree rotation</span></span>         | <span data-ttu-id="e05ff-153">1024 x 768 Zeilen \[ zeiligen Zeilen\]</span><span class="sxs-lookup"><span data-stu-id="e05ff-153">1024x768\[newline\]</span></span> ![270-Grad-Remote Desktop gedreht](images/dxgi-outdupl-270-rotate.png)<br/> |



 

<span data-ttu-id="e05ff-155">Der Code in der Client-App für die Desktop Duplizierung muss das Desktop Image entsprechend drehen, bevor Sie das Desktop Bild anzeigen.</span><span class="sxs-lookup"><span data-stu-id="e05ff-155">The code in your desktop duplication client app must rotate the desktop image appropriately before you display the desktop image.</span></span>

> [!Note]  
> <span data-ttu-id="e05ff-156">In Szenarios mit mehreren Monitoren können Sie das Desktop Abbild für jeden Monitor unabhängig voneinander drehen.</span><span class="sxs-lookup"><span data-stu-id="e05ff-156">In multi-monitor scenarios, you can rotate the desktop image for each monitor independently.</span></span>

 

## <a name="updating-the-desktop-pointer"></a><span data-ttu-id="e05ff-157">Aktualisieren des Desktop Zeigers</span><span class="sxs-lookup"><span data-stu-id="e05ff-157">Updating the desktop pointer</span></span>

<span data-ttu-id="e05ff-158">Sie müssen die Desktop Duplizierungs-API verwenden, um zu bestimmen, ob Ihre Client-App die Mauszeiger Form auf das Desktop Bild zeichnen muss.</span><span class="sxs-lookup"><span data-stu-id="e05ff-158">You need to use the desktop duplication API to determine if your client app must draw the mouse pointer shape onto the desktop image.</span></span> <span data-ttu-id="e05ff-159">Entweder ist der Mauszeiger bereits auf dem Desktop Bild gezeichnet, das [**idxgioutputdupliziert:: acquirren-extframe**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) bereitstellt, oder der Mauszeiger ist vom Desktop Bild getrennt.</span><span class="sxs-lookup"><span data-stu-id="e05ff-159">Either the mouse pointer is already drawn onto the desktop image that [**IDXGIOutputDuplication::AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) provides or the mouse pointer is separate from the desktop image.</span></span> <span data-ttu-id="e05ff-160">Wenn der Mauszeiger auf das Desktop Bild gezeichnet wird, zeigt der Zeiger Positionsdaten an, die von **acquunenextframe** (im **pointerposition** -Member der [**DXGI \_ outdupl- \_ Frame \_ Info**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_outdupl_frame_info) , auf die der *pframeinfo* -Parameter verweist) gemeldet wird, um anzuzeigen, dass ein separater Zeiger nicht sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="e05ff-160">If the mouse pointer is drawn onto the desktop image, the pointer position data that is reported by **AcquireNextFrame** (in the **PointerPosition** member of [**DXGI\_OUTDUPL\_FRAME\_INFO**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_outdupl_frame_info) that the *pFrameInfo* parameter points to) indicates that a separate pointer isn’t visible.</span></span> <span data-ttu-id="e05ff-161">Wenn der Grafikadapter den Mauszeiger oberhalb des Desktop Bilds überlagert, meldet " **acquiriesextframe** ", dass ein separater Zeiger sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="e05ff-161">If the graphics adapter overlays the mouse pointer on top of the desktop image, **AcquireNextFrame** reports that a separate pointer is visible.</span></span> <span data-ttu-id="e05ff-162">Daher muss Ihre Client-App die Mauszeiger Form auf das Desktop Bild zeichnen, um genau darzustellen, was dem aktuellen Benutzer auf dem Monitor angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="e05ff-162">So, your client app must draw the mouse pointer shape onto the desktop image to accurately represent what the current user will see on their monitor.</span></span>

<span data-ttu-id="e05ff-163">Um den Mauszeiger des Desktops zu zeichnen, verwenden Sie den **pointerposition** -Member der [**DXGI \_ outdupl- \_ Frame \_ Info**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_outdupl_frame_info) aus dem *pframeinfo* -Parameter von [**acquunenextframe**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) , um zu bestimmen, wo die linke obere Ecke des Mauszeigers auf dem Desktop Bild zu finden ist.</span><span class="sxs-lookup"><span data-stu-id="e05ff-163">To draw the desktop’s mouse pointer, use the **PointerPosition** member of [**DXGI\_OUTDUPL\_FRAME\_INFO**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_outdupl_frame_info) from the *pFrameInfo* parameter of [**AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) to determine where to locate the top left hand corner of the mouse pointer on the desktop image.</span></span> <span data-ttu-id="e05ff-164">Wenn Sie den ersten Frame zeichnen, müssen Sie die [**idxgioutputdupli:: getframepointershape**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframepointershape) -Methode verwenden, um Informationen über die Form des Mauszeigers abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e05ff-164">When you draw the first frame, you must use the [**IDXGIOutputDuplication::GetFramePointerShape**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframepointershape) method to obtain info about the shape of the mouse pointer.</span></span> <span data-ttu-id="e05ff-165">Jeder aufzurufende aufzurufende **Befehl zum Abrufen** des nächsten Frames liefert auch die aktuelle Zeigerposition für diesen Frame.</span><span class="sxs-lookup"><span data-stu-id="e05ff-165">Each call to **AcquireNextFrame** to get the next frame also provides the current pointer position for that frame.</span></span> <span data-ttu-id="e05ff-166">Andererseits müssen Sie **getframepointershape** nur dann erneut verwenden, wenn sich die Form ändert.</span><span class="sxs-lookup"><span data-stu-id="e05ff-166">On the other hand, you need to use **GetFramePointerShape** again only if the shape changes.</span></span> <span data-ttu-id="e05ff-167">Behalten Sie also eine Kopie des letzten Zeiger Bilds bei, und verwenden Sie diese zum Zeichnen auf dem Desktop, es sei denn, die Form des Mauszeigers ändert sich.</span><span class="sxs-lookup"><span data-stu-id="e05ff-167">So, keep a copy of the last pointer image and use it to draw on the desktop unless the shape of the mouse pointer changes.</span></span>

> [!Note]  
> <span data-ttu-id="e05ff-168">Zusammen mit dem Zeiger Form Bild gibt [**getframepointershape**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframepointershape) die Größe der Hotspot Position an.</span><span class="sxs-lookup"><span data-stu-id="e05ff-168">Together with the pointer shape image, [**GetFramePointerShape**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframepointershape) provides the size of the hot spot location.</span></span> <span data-ttu-id="e05ff-169">Der Hotspot wird nur zu Informationszwecken angegeben.</span><span class="sxs-lookup"><span data-stu-id="e05ff-169">The hot spot is given for informational purposes only.</span></span> <span data-ttu-id="e05ff-170">Der Speicherort, an dem das Zeiger Bild gezeichnet werden soll, ist unabhängig vom Hotspot.</span><span class="sxs-lookup"><span data-stu-id="e05ff-170">The location of where to draw the pointer image is independent to the hotspot.</span></span>

 

<span data-ttu-id="e05ff-171">Dieser Beispielcode aus dem Beispiel für eine [Desktop Duplizierung](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/DXGI%20desktop%20duplication%20sample) zeigt, wie die Form des Mauszeigers angezeigt wird:</span><span class="sxs-lookup"><span data-stu-id="e05ff-171">This example code from the [Desktop Duplication Sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/DXGI%20desktop%20duplication%20sample) shows how to get the mouse pointer shape:</span></span>


```C++
//
// Retrieves mouse info and write it into PtrInfo
//
HRESULT DUPLICATIONMANAGER::GetMouse(_Out_ PTR_INFO* PtrInfo, _In_ DXGI_OUTDUPL_FRAME_INFO* FrameInfo, INT OffsetX, INT OffsetY)
{
    HRESULT hr = S_OK;

    // A non-zero mouse update timestamp indicates that there is a mouse position update and optionally a shape change
    if (FrameInfo->LastMouseUpdateTime.QuadPart == 0)
    {
        return hr;
    }

    bool UpdatePosition = true;

    // Make sure we don't update pointer position wrongly
    // If pointer is invisible, make sure we did not get an update from another output that the last time that said pointer
    // was visible, if so, don't set it to invisible or update.
    if (!FrameInfo->PointerPosition.Visible && (PtrInfo->WhoUpdatedPositionLast != OutputNumber))
    {
        UpdatePosition = false;
    }

    // If two outputs both say they have a visible, only update if new update has newer timestamp
    if (FrameInfo->PointerPosition.Visible && PtrInfo->Visible && (PtrInfo->WhoUpdatedPositionLast != OutputNumber) && (PtrInfo->LastTimeStamp.QuadPart > FrameInfo->LastMouseUpdateTime.QuadPart))
    {
        UpdatePosition = false;
    }

    // Update position
    if (UpdatePosition)
    {
        PtrInfo->Position.x = FrameInfo->PointerPosition.Position.x + OutputDesc.DesktopCoordinates.left - OffsetX;
        PtrInfo->Position.y = FrameInfo->PointerPosition.Position.y + OutputDesc.DesktopCoordinates.top - OffsetY;
        PtrInfo->WhoUpdatedPositionLast = OutputNumber;
        PtrInfo->LastTimeStamp = FrameInfo->LastMouseUpdateTime;
        PtrInfo->Visible = FrameInfo->PointerPosition.Visible != 0;
    }

    // No new shape
    if (FrameInfo->PointerShapeBufferSize == 0)
    {
        return hr;
    }

    // Old buffer too small
    if (FrameInfo->PointerShapeBufferSize > PtrInfo->BufferSize)
    {
        if (PtrInfo->PtrShapeBuffer)
        {
            delete [] PtrInfo->PtrShapeBuffer;
            PtrInfo->PtrShapeBuffer = NULL;
        }
        PtrInfo->PtrShapeBuffer = new (std::nothrow) BYTE[FrameInfo->PointerShapeBufferSize];
        if (!PtrInfo->PtrShapeBuffer)
        {
            DisplayErr(L"Failed to allocate memory for pointer shape in DUPLICATIONMANAGER", L"Error", E_OUTOFMEMORY);
            PtrInfo->BufferSize = 0;
            return E_OUTOFMEMORY;
        }

        // Update buffer size
        PtrInfo->BufferSize = FrameInfo->PointerShapeBufferSize;
    }

    UINT BufferSizeRequired;
    // Get shape
    hr = DeskDupl->GetFramePointerShape(FrameInfo->PointerShapeBufferSize, reinterpret_cast<VOID*>(PtrInfo->PtrShapeBuffer), &BufferSizeRequired, &(PtrInfo->ShapeInfo));
    if (FAILED(hr))
    {
        if (hr != DXGI_ERROR_ACCESS_LOST)
        {
            DisplayErr(L"Failed to get frame pointer shape in DUPLICATIONMANAGER", L"Error", hr);
        }
        delete [] PtrInfo->PtrShapeBuffer;
        PtrInfo->PtrShapeBuffer = NULL;
        PtrInfo->BufferSize = 0;
        return hr;
    }

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="e05ff-172">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e05ff-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e05ff-173">DXGI 1,2-Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="e05ff-173">DXGI 1.2 Improvements</span></span>](dxgi-1-2-improvements.md)
</dt> </dl>

 

 
