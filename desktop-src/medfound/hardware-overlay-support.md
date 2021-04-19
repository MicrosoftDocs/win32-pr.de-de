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
# <a name="hardware-overlay-support"></a><span data-ttu-id="549a5-103">Hardware-Overlay</span><span class="sxs-lookup"><span data-stu-id="549a5-103">Hardware Overlay Support</span></span>

<span data-ttu-id="549a5-104">Eine Hardware Überlagerung ist ein dedizierter Bereich von Videospeicher, der auf der primären Oberfläche überlastet werden kann.</span><span class="sxs-lookup"><span data-stu-id="549a5-104">A hardware overlay is a dedicated area of video memory that can be overlayed on the primary surface.</span></span> <span data-ttu-id="549a5-105">Wenn das Overlay angezeigt wird, wird kein Kopiervorgang durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="549a5-105">No copy is performed when the overlay is displayed.</span></span> <span data-ttu-id="549a5-106">Der Überlagerungs Vorgang wird in Hardware ausgeführt, ohne die Daten auf der primären Oberfläche zu ändern.</span><span class="sxs-lookup"><span data-stu-id="549a5-106">The overlay operation is performed in hardware, without modifying the data in the primary surface.</span></span>

<span data-ttu-id="549a5-107">Die Verwendung von Hardware Überlagerungen für die Videowiedergabe war in früheren Versionen von Windows üblich, da die Überlagerungen für Videoinhalte mit einer hohen Framerate effizient sind.</span><span class="sxs-lookup"><span data-stu-id="549a5-107">The use of hardware overlays for video playback was common in earlier versions of Windows, because overlays are efficient for video content with a high frame rate.</span></span> <span data-ttu-id="549a5-108">Ab Windows 7 unterstützt Direct3D 9 Hardware Überlagerungen.</span><span class="sxs-lookup"><span data-stu-id="549a5-108">Starting in Windows 7, Direct3D 9 supports hardware overlays.</span></span> <span data-ttu-id="549a5-109">Diese Unterstützung ist in erster Linie für die Videowiedergabe gedacht und unterscheidet sich in gewisser Hinsicht von früheren DirectDraw-APIs:</span><span class="sxs-lookup"><span data-stu-id="549a5-109">This support is intended primarily for video playback, and differs in some respects from earlier DirectDraw APIs:</span></span>

-   <span data-ttu-id="549a5-110">Das Overlay kann nicht verkleinert, gespiegelt oder Deinterlacing werden.</span><span class="sxs-lookup"><span data-stu-id="549a5-110">The overlay cannot be shrunk, mirrored, or deinterlaced.</span></span>
-   <span data-ttu-id="549a5-111">Quell Farben und Alpha Blending werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="549a5-111">Source color keys and alpha blending are not supported.</span></span>
-   <span data-ttu-id="549a5-112">Überlagerungen können gestreckt werden, wenn die Überlagerungs Hardware diese unterstützt.</span><span class="sxs-lookup"><span data-stu-id="549a5-112">Overlays can be stretched if the overlay hardware supports it.</span></span> <span data-ttu-id="549a5-113">Andernfalls wird die Streckung nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="549a5-113">Otherwise, stretching is not supported.</span></span> <span data-ttu-id="549a5-114">In der Praxis unterstützen nicht alle Grafiktreiber das Stretching.</span><span class="sxs-lookup"><span data-stu-id="549a5-114">In practice, not all graphics drivers support stretching.</span></span>
-   <span data-ttu-id="549a5-115">Jedes Gerät unterstützt höchstens ein Overlay.</span><span class="sxs-lookup"><span data-stu-id="549a5-115">Each device supports at most one overlay.</span></span>
-   <span data-ttu-id="549a5-116">Die Überlagerung wird mithilfe eines Ziel Farb Schlüssels ausgeführt, aber die Direct3D-Laufzeit wählt automatisch die Farbe aus und zeichnet das Ziel Rechteck.</span><span class="sxs-lookup"><span data-stu-id="549a5-116">Overlay is performed using a destination color key, but the Direct3D runtime automatically selects the color and draws the destination rectangle.</span></span> <span data-ttu-id="549a5-117">Direct3D verfolgt automatisch die Position des Fensters und aktualisiert die Überlagerungs Position, wenn der **presentex** aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="549a5-117">Direct3D automatically tracks the position of the window and updates the overlay position whenever the **PresentEx** is called.</span></span>

### <a name="creating-a-hardware-overlay-surface"></a><span data-ttu-id="549a5-118">Erstellen einer Hardware Überlagerungs Oberfläche</span><span class="sxs-lookup"><span data-stu-id="549a5-118">Creating a Hardware Overlay Surface</span></span>

<span data-ttu-id="549a5-119">Um die Überlagerungs Unterstützung abzufragen, nennen Sie **IDirect3D9:: GetDeviceCaps**.</span><span class="sxs-lookup"><span data-stu-id="549a5-119">To query for overlay support, call **IDirect3D9::GetDeviceCaps**.</span></span> <span data-ttu-id="549a5-120">Wenn der Treiber die Hardware Überlagerung unterstützt, wird das **D3DCAPS \_ Overlay** -Flag in D3DCAPS9 festgelegt **. Caps** -Member.</span><span class="sxs-lookup"><span data-stu-id="549a5-120">If the driver supports hardware overlay, the **D3DCAPS\_OVERLAY** flag is set in the **D3DCAPS9.Caps** member.</span></span>

<span data-ttu-id="549a5-121">Um herauszufinden, ob ein bestimmtes Überlagerungs Format für einen bestimmten Anzeigemodus unterstützt wird, müssen Sie [**IDirect3D9ExOverlayExtension:: checkdeviceoverlaytype**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9exoverlayextension-checkdeviceoverlaytype)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="549a5-121">To find out whether a specific overlay format is supported for a given display mode, call [**IDirect3D9ExOverlayExtension::CheckDeviceOverlayType**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9exoverlayextension-checkdeviceoverlaytype).</span></span>

<span data-ttu-id="549a5-122">Um das Overlay zu erstellen, rufen Sie **IDirect3D9Ex:: kreatedeviceex** auf, und geben Sie den **D3DSWAPEFFECT \_ Overlay** -Swap-Effekt an.</span><span class="sxs-lookup"><span data-stu-id="549a5-122">To create the overlay, call **IDirect3D9Ex::CreateDeviceEx** and specify the **D3DSWAPEFFECT\_OVERLAY** swap effect.</span></span> <span data-ttu-id="549a5-123">Der Hintergrund Puffer kann ein nicht-RGB-Format verwenden, wenn es von der Hardware unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="549a5-123">The back buffer can use a non-RGB format if the hardware supports it.</span></span>

<span data-ttu-id="549a5-124">Überlagerungs Oberflächen weisen die folgenden Einschränkungen auf:</span><span class="sxs-lookup"><span data-stu-id="549a5-124">Overlay surfaces have the following limitations:</span></span>

-   <span data-ttu-id="549a5-125">Die Anwendung kann nicht mehr als eine Überlagerungs Austausch Kette erstellen.</span><span class="sxs-lookup"><span data-stu-id="549a5-125">The application cannot create more than one overlay swap chain.</span></span>
-   <span data-ttu-id="549a5-126">Das Overlay muss im Fenstermodus verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="549a5-126">The overlay must be used in windowed mode.</span></span> <span data-ttu-id="549a5-127">Sie kann nicht im Vollbildmodus verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="549a5-127">It cannot be used in fullscreen mode.</span></span>
-   <span data-ttu-id="549a5-128">Der Überlagerungs Swap-Effekt muss mit der **IDirect3DDevice9Ex** -Schnittstelle verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="549a5-128">The overlay swap effect must be used with the **IDirect3DDevice9Ex** interface.</span></span> <span data-ttu-id="549a5-129">Sie wird für **IDirect3DDevice9** nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="549a5-129">It is not supported for **IDirect3DDevice9**.</span></span>
-   <span data-ttu-id="549a5-130">Multisampling kann nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="549a5-130">Multisampling cannot be used.</span></span>
-   <span data-ttu-id="549a5-131">Die **D3DPRESENT \_ donotflip** -und **D3DPRESENT \_ fliprestart** -Flags werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="549a5-131">The **D3DPRESENT\_DONOTFLIP** and **D3DPRESENT\_FLIPRESTART** flags are not supported.</span></span>
-   <span data-ttu-id="549a5-132">Die Präsentations Statistik ist für die Überlagerungs Oberfläche nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="549a5-132">Presentation statistics are not available for the overlay surface.</span></span>

<span data-ttu-id="549a5-133">Wenn die Hardware keine Streckung unterstützt, wird empfohlen, eine SwapChain so groß wie den Anzeigemodus zu erstellen, damit die Größe des Fensters in beliebige Dimensionen geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="549a5-133">If the hardware does not support stretching, it is recommended to create a swap chain as large as the display mode, so that the window can be resized to any dimensions.</span></span> <span data-ttu-id="549a5-134">Das Neuerstellen der SwapChain ist nicht optimal geeignet, um die Größe des Fensters zu ändern, da es schwerwiegende Renderingartefakte verursachen kann.</span><span class="sxs-lookup"><span data-stu-id="549a5-134">Recreating the swap chain is not an optimal way to handle resizing the window, because it can cause severe rendering artifacts.</span></span> <span data-ttu-id="549a5-135">Aufgrund der Art und Weise, wie die GPU den Überlagerungs Speicher verwaltet, kann das Neuerstellen der Swapkette möglicherweise dazu führen, dass eine Anwendung nicht mehr über den Videospeicher verfügt.</span><span class="sxs-lookup"><span data-stu-id="549a5-135">Also, because of the way the GPU manages the overlay memory, recreating the swap chain can potentially cause an application to run out of video memory.</span></span>

### <a name="new-d3dpresent_parameters-flags"></a><span data-ttu-id="549a5-136">Neue D3DPRESENT \_ Parameter-Flags</span><span class="sxs-lookup"><span data-stu-id="549a5-136">New D3DPRESENT\_PARAMETERS Flags</span></span>

<span data-ttu-id="549a5-137">Die folgenden **D3DPRESENT \_ Parameter** -Flags werden zum Erstellen von Überlagerungen definiert.</span><span class="sxs-lookup"><span data-stu-id="549a5-137">The following **D3DPRESENT\_PARAMETERS** flags are defined for creating overlays.</span></span>



| <span data-ttu-id="549a5-138">Flag</span><span class="sxs-lookup"><span data-stu-id="549a5-138">Flag</span></span>                                      | <span data-ttu-id="549a5-139">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="549a5-139">Description</span></span>                                                                                                                                                                        |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="549a5-140">**D3DPRESENTFLAG \_ Overlay \_ limitedrgb**</span><span class="sxs-lookup"><span data-stu-id="549a5-140">**D3DPRESENTFLAG\_OVERLAY\_LIMITEDRGB**</span></span>   | <span data-ttu-id="549a5-141">Der RGB-Bereich ist 16 – 235.</span><span class="sxs-lookup"><span data-stu-id="549a5-141">The RGB range is 16–235.</span></span> <span data-ttu-id="549a5-142">Der Standardwert ist 0 – 255.</span><span class="sxs-lookup"><span data-stu-id="549a5-142">The default is 0–255.</span></span> <br/> <span data-ttu-id="549a5-143">Erfordert die **D3DOVERLAYCAPS \_ limitedranger GB** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="549a5-143">Requires the **D3DOVERLAYCAPS\_LIMITEDRANGERGB** capability.</span></span><br/>                                                 |
| <span data-ttu-id="549a5-144">**D3DPRESENTFLAG \_ Overlay \_ YCbCr \_ BT709**</span><span class="sxs-lookup"><span data-stu-id="549a5-144">**D3DPRESENTFLAG\_OVERLAY\_YCbCr\_BT709**</span></span> | <span data-ttu-id="549a5-145">YUV-Farben verwenden die BT. 709-Definition.</span><span class="sxs-lookup"><span data-stu-id="549a5-145">YUV colors use the BT.709 definition.</span></span> <span data-ttu-id="549a5-146">Der Standardwert ist "BT. 601".</span><span class="sxs-lookup"><span data-stu-id="549a5-146">The default is BT.601.</span></span> <br/> <span data-ttu-id="549a5-147">Erfordert die **D3DOVERLAYCAPS \_ YCbCr \_ BT709** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="549a5-147">Requires the **D3DOVERLAYCAPS\_YCbCr\_BT709** capability.</span></span><br/>                                      |
| <span data-ttu-id="549a5-148">**D3DPRESENTFLAG \_ Overlay \_ YCbCr \_ xwycc**</span><span class="sxs-lookup"><span data-stu-id="549a5-148">**D3DPRESENTFLAG\_OVERLAY\_YCbCr\_xvYCC**</span></span> | <span data-ttu-id="549a5-149">Geben Sie die Daten mithilfe von Extended YCbCr (xwycc) aus.</span><span class="sxs-lookup"><span data-stu-id="549a5-149">Output the data by using extended YCbCr (xvYCC).</span></span><br/> <span data-ttu-id="549a5-150">Erfordert die **D3DOVERLAYCAPS \_ YCbCr \_ BT601 \_ xvYCC** -oder **D3DOVERLAYCAPS \_ YCbCr \_ BT709 \_ xwycc** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="549a5-150">Requires the **D3DOVERLAYCAPS\_YCbCr\_BT601\_xvYCC** or **D3DOVERLAYCAPS\_YCbCr\_BT709\_xvYCC** capability.</span></span><br/> |



 

### <a name="using-hardware-overlays"></a><span data-ttu-id="549a5-151">Verwenden von Hardware Überlagerungen</span><span class="sxs-lookup"><span data-stu-id="549a5-151">Using Hardware Overlays</span></span>

<span data-ttu-id="549a5-152">Um die Überlagerungs Oberfläche anzuzeigen, ruft die Anwendung **IDirect3DDevice9Ex::P resentex** auf.</span><span class="sxs-lookup"><span data-stu-id="549a5-152">To display the overlay surface, the application calls **IDirect3DDevice9Ex::PresentEx**.</span></span> <span data-ttu-id="549a5-153">Die Direct3D-Laufzeit zeichnet automatisch den Ziel Farbschlüssel.</span><span class="sxs-lookup"><span data-stu-id="549a5-153">The Direct3D runtime automatically draws the destination color key.</span></span>

<span data-ttu-id="549a5-154">Die folgenden **presentex** -Flags werden für Überlagerungen definiert.</span><span class="sxs-lookup"><span data-stu-id="549a5-154">The following **PresentEx** flags are defined for overlays.</span></span>



| <span data-ttu-id="549a5-155">Flag</span><span class="sxs-lookup"><span data-stu-id="549a5-155">Flag</span></span>                              | <span data-ttu-id="549a5-156">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="549a5-156">Description</span></span>                                                                                                                                                                                                                                                                           |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="549a5-157">**D3DPRESENT \_ updatecolorkey**</span><span class="sxs-lookup"><span data-stu-id="549a5-157">**D3DPRESENT\_UPDATECOLORKEY**</span></span>    | <span data-ttu-id="549a5-158">Legen Sie dieses Flag fest, wenn die Komposition von Desktopfenster-Manager (DWM) deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="549a5-158">Set this flag if Desktop Window Manager (DWM) composition is disabled.</span></span> <span data-ttu-id="549a5-159">Dieses Flag bewirkt, dass Direct3D den Farbschlüssel neu zeichnet.</span><span class="sxs-lookup"><span data-stu-id="549a5-159">This flag causes Direct3D to redraw the color key.</span></span><br/> <span data-ttu-id="549a5-160">Wenn DWM aktiviert ist, ist dieses Flag nicht erforderlich, da Direct3D den Farbschlüssel einmal auf der Oberfläche zeichnet, die DWM für die Umleitung verwendet.</span><span class="sxs-lookup"><span data-stu-id="549a5-160">If DWM is enabled, this flag is not required, because Direct3D draws the color key once on the surface that DWM uses for redirection.</span></span><br/> |
| <span data-ttu-id="549a5-161">**D3DPRESENT \_ hideoverlay**</span><span class="sxs-lookup"><span data-stu-id="549a5-161">**D3DPRESENT\_HIDEOVERLAY**</span></span>       | <span data-ttu-id="549a5-162">Blendet die Überlagerung aus.</span><span class="sxs-lookup"><span data-stu-id="549a5-162">Hides the overlay.</span></span>                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="549a5-163">**D3DPRESENT \_ updateoverlayonly**</span><span class="sxs-lookup"><span data-stu-id="549a5-163">**D3DPRESENT\_UPDATEOVERLAYONLY**</span></span> | <span data-ttu-id="549a5-164">Aktualisiert das Overlay, ohne den Inhalt zu ändern.</span><span class="sxs-lookup"><span data-stu-id="549a5-164">Updates the overlay without changing the contents.</span></span><br/> <span data-ttu-id="549a5-165">Dieses Flag ist nützlich, wenn das Fenster verschoben wird, während das Video angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="549a5-165">This flag is useful if the window moves while the video is paused.</span></span><br/>                                                                                                                                           |



 

<span data-ttu-id="549a5-166">Eine Anwendung sollte darauf vorbereitet sein, die folgenden Fälle zu behandeln:</span><span class="sxs-lookup"><span data-stu-id="549a5-166">An application should be prepared to handle the following cases:</span></span>

-   <span data-ttu-id="549a5-167">Wenn eine andere Anwendung das Overlay verwendet, gibt **presentex** **D3DERR \_ NotAvailable** zurück.</span><span class="sxs-lookup"><span data-stu-id="549a5-167">If another application is using the overlay, **PresentEx** returns **D3DERR\_NOTAVAILABLE**.</span></span>
-   <span data-ttu-id="549a5-168">Wenn das Fenster auf einen anderen Monitor verschoben wird, muss die SwapChain von der Anwendung neu erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="549a5-168">If the window is moved to another monitor, the application must recreate the swap chain.</span></span> <span data-ttu-id="549a5-169">Andernfalls gibt **presentex** **D3DERR \_ invaliddevice** zurück, wenn die Anwendung einen **presentex** aufruft, um die Überlagerung auf einem anderen Monitor anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="549a5-169">Otherwise, if the application calls **PresentEx** to display the overlay on a different monitor, **PresentEx** returns **D3DERR\_INVALIDDEVICE**.</span></span>
-   <span data-ttu-id="549a5-170">Wenn sich der Anzeigemodus ändert, versucht Direct3D, die Überlagerung wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="549a5-170">If the display mode changes, Direct3D attempts to restore the overlay.</span></span> <span data-ttu-id="549a5-171">Wenn der neue Modus das Overlay nicht unterstützt, gibt **presentex** **D3DERR \_ unsupportedoverlay** zurück.</span><span class="sxs-lookup"><span data-stu-id="549a5-171">If the new mode does not support the overlay, **PresentEx** returns **D3DERR\_UNSUPPORTEDOVERLAY**.</span></span>

### <a name="example-code"></a><span data-ttu-id="549a5-172">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="549a5-172">Example Code</span></span>

<span data-ttu-id="549a5-173">Im folgenden Beispiel wird gezeigt, wie eine Überlagerungs Oberfläche erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="549a5-173">The following example shows how to create an overlay surface.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="549a5-174">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="549a5-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="549a5-175">Direct3D-Video-APIs</span><span class="sxs-lookup"><span data-stu-id="549a5-175">Direct3D Video APIs</span></span>](direct3d-video-apis.md)
</dt> </dl>

 

 




