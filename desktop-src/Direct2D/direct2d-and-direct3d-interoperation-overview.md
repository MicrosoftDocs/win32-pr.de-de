---
title: Übersicht über die Interoperabilität von Direct2D und Direct3D
description: Übersicht über die Interoperabilität von Direct2D und Direct3D
ms.assetid: 27680714-dc68-44eb-ab16-2cae3529b352
keywords:
- Direct2D,Direct3D-Interoperation
- Direct2D, Interoperabilität
- Interoperabilität,Direct2D
- Interoperabilität,Direct3D
- Direct3D, Interoperabilität
- Direct3D,Direct2D-Interoperation
- Direct2D, DXGI
- DXGI
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: cf7cfa41c3decc964492258dad9c6a3a497f504b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089188"
---
# <a name="direct2d-and-direct3d-interoperability-overview"></a><span data-ttu-id="41019-111">Übersicht über die Interoperabilität von Direct2D und Direct3D</span><span class="sxs-lookup"><span data-stu-id="41019-111">Direct2D and Direct3D Interoperability Overview</span></span>

<span data-ttu-id="41019-112">Hardwarebeschleunigte 2D- und 3D-Grafiken werden zunehmend zu einem Teil von Nicht-Gaminganwendungen, und die meisten Gaminganwendungen verwenden 2D-Grafiken in Form von Menüs und Heads-Up Displays (HUDs).</span><span class="sxs-lookup"><span data-stu-id="41019-112">Hardware accelerated 2-D and 3-D graphics are increasingly becoming a part of non-gaming applications, and most gaming applications use 2-D graphics in the form of menus and Heads-Up Displays (HUDs).</span></span> <span data-ttu-id="41019-113">Es gibt viele Werte, die hinzugefügt werden können, indem herkömmliches 2D-Rendering auf effiziente Weise mit Direct3D-Rendering gemischt werden kann.</span><span class="sxs-lookup"><span data-stu-id="41019-113">There is lots of value that can be added by enabling traditional 2-D rendering to be mixed with Direct3D rendering in an efficient manner.</span></span>

<span data-ttu-id="41019-114">In diesem Thema wird beschrieben, wie 2D- und 3D-Grafiken mit direct2D und [Direct3D integriert werden.](../graphics-and-multimedia.md)</span><span class="sxs-lookup"><span data-stu-id="41019-114">This topic describes how to integrate 2-D and 3-D graphics by using Direct2D and [Direct3D](../graphics-and-multimedia.md).</span></span>

<span data-ttu-id="41019-115">Der Abschnitt ist wie folgt gegliedert.</span><span class="sxs-lookup"><span data-stu-id="41019-115">It contains the following sections.</span></span>

-   [<span data-ttu-id="41019-116">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="41019-116">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="41019-117">Unterstützte Direct3D-Versionen</span><span class="sxs-lookup"><span data-stu-id="41019-117">Supported Direct3D Versions</span></span>](#supported-direct3d-versions)
-   [<span data-ttu-id="41019-118">Interoperabilität durch DXGI</span><span class="sxs-lookup"><span data-stu-id="41019-118">Interoperability Through DXGI</span></span>](#interoperability-through-dxgi)
-   [<span data-ttu-id="41019-119">Schreiben auf eine Direct3D-Oberfläche mit einem DXGI-Oberflächenrenderingziel</span><span class="sxs-lookup"><span data-stu-id="41019-119">Writing to a Direct3D Surface with a DXGI Surface Render Target</span></span>](#writing-to-a-direct3d-surface-with-a-dxgi-surface-render-target)
    -   [<span data-ttu-id="41019-120">Erstellen einer DXGI-Oberfläche</span><span class="sxs-lookup"><span data-stu-id="41019-120">Creating a DXGI Surface</span></span>](#creating-a-dxgi-surface)
-   [<span data-ttu-id="41019-121">Schreiben von Direct2D-Inhalt in einen Swap Chain-Puffer</span><span class="sxs-lookup"><span data-stu-id="41019-121">Writing Direct2D Content to a Swap Chain Buffer</span></span>](#writing-direct2d-content-to-a-swap-chain-buffer)
    -   [<span data-ttu-id="41019-122">Beispiel: Zeichnen eines 2D-Hintergrunds</span><span class="sxs-lookup"><span data-stu-id="41019-122">Example: Draw a 2-D Background</span></span>](#example-draw-a-2-d-background)
-   [<span data-ttu-id="41019-123">Verwenden von Direct2D-Inhalt als Textur</span><span class="sxs-lookup"><span data-stu-id="41019-123">Using Direct2D Content as a Texture</span></span>](#using-direct2d-content-as-a-texture)
    -   [<span data-ttu-id="41019-124">Beispiel: Verwenden von Direct2D-Inhalt als Textur</span><span class="sxs-lookup"><span data-stu-id="41019-124">Example: Use Direct2D Content as a Texture</span></span>](#example-use-direct2d-content-as-a-texture)
-   [<span data-ttu-id="41019-125">Ändern der Größe eines DXGI-Oberflächenrenderingziels</span><span class="sxs-lookup"><span data-stu-id="41019-125">Resizing a DXGI Surface Render Target</span></span>](#resizing-a-dxgi-surface-render-target)
-   [<span data-ttu-id="41019-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="41019-126">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="41019-127">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="41019-127">Prerequisites</span></span>

<span data-ttu-id="41019-128">In dieser Übersicht wird davon ausgegangen, dass Sie mit grundlegenden Direct2D-Zeichnungsvorgängen vertraut sind.</span><span class="sxs-lookup"><span data-stu-id="41019-128">This overview assumes that you are familiar with basic Direct2D drawing operations.</span></span> <span data-ttu-id="41019-129">Ein Tutorial finden Sie im [Direct2D-Schnellstart.](direct2d-quickstart.md)</span><span class="sxs-lookup"><span data-stu-id="41019-129">For a tutorial, see the [Direct2D QuickStart](direct2d-quickstart.md).</span></span> <span data-ttu-id="41019-130">Außerdem wird davon ausgegangen, dass Sie mit [Direct3D 10.1](/windows/desktop/direct3d10/d3d10-graphics)programmieren können.</span><span class="sxs-lookup"><span data-stu-id="41019-130">It also assumes that you can program by using [Direct3D 10.1](/windows/desktop/direct3d10/d3d10-graphics).</span></span>

## <a name="supported-direct3d-versions"></a><span data-ttu-id="41019-131">Unterstützte Direct3D-Versionen</span><span class="sxs-lookup"><span data-stu-id="41019-131">Supported Direct3D Versions</span></span>

<span data-ttu-id="41019-132">Mit DirectX 11.0 unterstützt Direct2D nur die Interoperabilität mit Direct3D 10.1-Geräten.</span><span class="sxs-lookup"><span data-stu-id="41019-132">With DirectX 11.0, Direct2D supports interoperability with Direct3D 10.1 devices only.</span></span> <span data-ttu-id="41019-133">Mit DirectX 11.1 oder höher unterstützt Direct2D auch die Interoperabilität mit Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="41019-133">With DirectX 11.1 or later, Direct2D supports interoperability with Direct3D 11 as well.</span></span>

## <a name="interoperability-through-dxgi"></a><span data-ttu-id="41019-134">Interoperabilität durch DXGI</span><span class="sxs-lookup"><span data-stu-id="41019-134">Interoperability Through DXGI</span></span>

<span data-ttu-id="41019-135">Ab Direct3D 10 verwendet die Direct3D-Runtime [DXGI](/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi) für die Ressourcenverwaltung.</span><span class="sxs-lookup"><span data-stu-id="41019-135">As of Direct3D 10, the Direct3D runtime uses [DXGI](/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi) for resource management.</span></span> <span data-ttu-id="41019-136">Die DXGI-Laufzeitebene ermöglicht die prozessübergreifende Freigabe von Videospeicheroberflächen und dient als Grundlage für andere videospeicherbasierte Laufzeitplattformen.</span><span class="sxs-lookup"><span data-stu-id="41019-136">The DXGI runtime layer provides cross-process sharing of video memory surfaces and serves as the foundation for other video memory-based runtime platforms.</span></span> <span data-ttu-id="41019-137">Direct2D verwendet DXGI für die Zusammenarbeit mit Direct3D.</span><span class="sxs-lookup"><span data-stu-id="41019-137">Direct2D uses DXGI to interoperate with Direct3D.</span></span>

<span data-ttu-id="41019-138">Es gibt zwei Primäre Möglichkeiten, Direct2D und Direct3D zusammen zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="41019-138">There are two primary ways to use Direct2D and Direct3D together:</span></span>

-   <span data-ttu-id="41019-139">Sie können Direct2D-Inhalt in eine Direct3D-Oberfläche schreiben, indem Sie eine [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface) abrufen und mit [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) verwenden, um eine [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="41019-139">You can write Direct2D content to a Direct3D surface by obtaining an [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface) and using it with the [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) to create an [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget).</span></span> <span data-ttu-id="41019-140">Sie können dann das Renderziel verwenden, um dreidimensionalen Grafiken eine zweidimensionale Schnittstelle oder einen Hintergrund hinzuzufügen, oder eine Direct2D-Zeichnung als Textur für ein dreidimensionales Objekt verwenden.</span><span class="sxs-lookup"><span data-stu-id="41019-140">You can then use the render target to add a two-dimensional interface or background to three-dimensional graphics, or use a Direct2D drawing as a texture for a three dimensional object.</span></span>
-   <span data-ttu-id="41019-141">Indem [**Sie CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) verwenden, um eine [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) aus einer [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface)zu erstellen, können Sie eine Direct3D-Szene in eine Bitmap schreiben und mit Direct2D rendern.</span><span class="sxs-lookup"><span data-stu-id="41019-141">By using [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) to create an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) from an [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface), you can write a Direct3D scene to a bitmap and render it with Direct2D.</span></span>

## <a name="writing-to-a-direct3d-surface-with-a-dxgi-surface-render-target"></a><span data-ttu-id="41019-142">Schreiben in eine Direct3D-Oberfläche mit einem DXGI Surface-Renderziel</span><span class="sxs-lookup"><span data-stu-id="41019-142">Writing to a Direct3D Surface with a DXGI Surface Render Target</span></span>

<span data-ttu-id="41019-143">Um in eine Direct3D-Oberfläche zu schreiben, rufen Sie eine [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface) ab und übergeben sie an die [**CreateDxgiSurfaceRenderTarget-Methode,**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) um ein DXGI-Oberflächenrenderziel zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="41019-143">To write to a Direct3D surface, you obtain an [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface) and pass it to the [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) method to create a DXGI surface render target.</span></span> <span data-ttu-id="41019-144">Anschließend können Sie das DXGI-Oberflächenrenderingziel verwenden, um 2D-Inhalte auf die DXGI-Oberfläche zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="41019-144">You can then use the DXGI surface render target to draw 2-D content to the DXGI surface.</span></span>

<span data-ttu-id="41019-145">Ein DXGI-Oberflächenrenderziel ist eine Art von [**ID2D1RenderTarget.**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)</span><span class="sxs-lookup"><span data-stu-id="41019-145">A DXGI surface render target is a kind of [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget).</span></span> <span data-ttu-id="41019-146">Wie andere Direct2D-Renderziele können Sie damit Ressourcen erstellen und Zeichnungsbefehle ausführen.</span><span class="sxs-lookup"><span data-stu-id="41019-146">Like other Direct2D render targets, you can use it to create resources and issue drawing commands.</span></span>

<span data-ttu-id="41019-147">Das DXGI-Oberflächenrenderziel und die DXGI-Oberfläche müssen dasselbe DXGI-Format verwenden.</span><span class="sxs-lookup"><span data-stu-id="41019-147">The DXGI surface render target and the DXGI surface must use the same DXGI format.</span></span> <span data-ttu-id="41019-148">Wenn Sie beim Erstellen des Renderziels das [**\_ DXGI FORMAT \_ UNMARKEN-Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) angeben, wird automatisch das Format der Oberfläche verwendet.</span><span class="sxs-lookup"><span data-stu-id="41019-148">If you specify the [**DXGI\_FORMAT\_UNKOWN**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) format when you create the render target, it will automatically use the surface's format.</span></span>

<span data-ttu-id="41019-149">Das DXGI-Oberflächenrenderziel führt keine DXGI-Oberflächensynchronisierung durch.</span><span class="sxs-lookup"><span data-stu-id="41019-149">The DXGI surface render target does not perform DXGI surface synchronization.</span></span>

### <a name="creating-a-dxgi-surface"></a><span data-ttu-id="41019-150">Erstellen einer DXGI-Oberfläche</span><span class="sxs-lookup"><span data-stu-id="41019-150">Creating a DXGI Surface</span></span>

<span data-ttu-id="41019-151">Mit Direct3D 10 gibt es mehrere Möglichkeiten, eine DXGI-Oberfläche zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="41019-151">With Direct3D 10, there are several ways to obtain a DXGI surface.</span></span> <span data-ttu-id="41019-152">Sie können eine [**IDXGISwapChain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) für ein Gerät erstellen und dann die [**GetBuffer-Methode**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) der Swapkette verwenden, um eine DXGI-Oberfläche abzurufen.</span><span class="sxs-lookup"><span data-stu-id="41019-152">You can create an [**IDXGISwapChain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) for a device, then use the swap chain's [**GetBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) method to obtain a DXGI surface.</span></span> <span data-ttu-id="41019-153">Alternativ können Sie ein Gerät verwenden, um eine Textur zu erstellen, und dann diese Textur als DXGI-Oberfläche verwenden.</span><span class="sxs-lookup"><span data-stu-id="41019-153">Or, you can use a device to create a texture, then use that texture as a DXGI surface.</span></span>

<span data-ttu-id="41019-154">Unabhängig davon, wie Sie die DXGI-Oberfläche erstellen, muss die Oberfläche eines der DXGI-Formate verwenden, die von DXGI-Oberflächenrenderingzielen unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="41019-154">Regardless of how you create the DXGI surface, the surface must use one of the DXGI formats supported by DXGI surface render targets.</span></span> <span data-ttu-id="41019-155">Eine Liste finden Sie unter [Unterstützte Pixelformate und Alphamodi.](supported-pixel-formats-and-alpha-modes.md)</span><span class="sxs-lookup"><span data-stu-id="41019-155">For a list, see [Supported Pixel Formats and Alpha Modes](supported-pixel-formats-and-alpha-modes.md).</span></span>

<span data-ttu-id="41019-156">Darüber hinaus muss die [**ID3D10Device1,**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1) die der DXGI-Oberfläche zugeordnet ist, BGRA DXGI-Formate unterstützen, damit die Oberfläche mit Direct2D funktioniert.</span><span class="sxs-lookup"><span data-stu-id="41019-156">Additionally, the [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1) associated with the DXGI surface must support BGRA DXGI formats for the surface to work with Direct2D.</span></span> <span data-ttu-id="41019-157">Um diese Unterstützung sicherzustellen, verwenden Sie das [**\_ \_ \_ BGRA \_ SUPPORT-Flag D3D10 CREATE DEVICE,**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_create_device_flag) wenn Sie die [**D3D10CreateDevice1-Methode**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdevice1) aufrufen, um das Gerät zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="41019-157">To ensure this support, use the [**D3D10\_CREATE\_DEVICE\_BGRA\_SUPPORT**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_create_device_flag) flag when you call the [**D3D10CreateDevice1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdevice1) method to create the device.</span></span>

<span data-ttu-id="41019-158">Der folgende Code definiert eine Methode, die eine [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1)erstellt.</span><span class="sxs-lookup"><span data-stu-id="41019-158">The following code defines a method that creates an [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1).</span></span> <span data-ttu-id="41019-159">Er wählt die beste verfügbare Featureebene aus und greift auf [Windows Advanced Rasterization Platform (WARP)](./installing-the-direct2d-debug-layer.md) zurück, wenn kein Hardwarerendering verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="41019-159">It selects the best feature level available and falls back to [Windows Advanced Rasterization Platform (WARP)](./installing-the-direct2d-debug-layer.md) when hardware rendering is not available.</span></span>


```C++
HRESULT DXGISampleApp::CreateD3DDevice(
    IDXGIAdapter *pAdapter,
    D3D10_DRIVER_TYPE driverType,
    UINT flags,
    ID3D10Device1 **ppDevice
    )
{
    HRESULT hr = S_OK;

    static const D3D10_FEATURE_LEVEL1 levelAttempts[] =
    {
        D3D10_FEATURE_LEVEL_10_0,
        D3D10_FEATURE_LEVEL_9_3,
        D3D10_FEATURE_LEVEL_9_2,
        D3D10_FEATURE_LEVEL_9_1,
    };

    for (UINT level = 0; level < ARRAYSIZE(levelAttempts); level++)
    {
        ID3D10Device1 *pDevice = NULL;
        hr = D3D10CreateDevice1(
            pAdapter,
            driverType,
            NULL,
            flags,
            levelAttempts[level],
            D3D10_1_SDK_VERSION,
            &pDevice
            );

        if (SUCCEEDED(hr))
        {
            // transfer reference
            *ppDevice = pDevice;
            pDevice = NULL;
            break;
        }

    }

    return hr;
}
```



<span data-ttu-id="41019-160">Im nächsten Codebeispiel wird die `CreateD3DDevice` im vorherigen Beispiel gezeigte Methode verwendet, um ein Direct3D-Gerät zu erstellen, das DXGI-Oberflächen für die Verwendung mit Direct2D erstellen kann.</span><span class="sxs-lookup"><span data-stu-id="41019-160">The next code example uses the `CreateD3DDevice` method shown in the previous example to create a Direct3D device that can create DXGI surfaces for use with Direct2D.</span></span>


```C++
// Create device
hr = CreateD3DDevice(
    NULL,
    D3D10_DRIVER_TYPE_HARDWARE,
    nDeviceFlags,
    &pDevice
    );

if (FAILED(hr))
{
    hr = CreateD3DDevice(
        NULL,
        D3D10_DRIVER_TYPE_WARP,
        nDeviceFlags,
        &pDevice
        );
}
```



## <a name="writing-direct2d-content-to-a-swap-chain-buffer"></a><span data-ttu-id="41019-161">Schreiben von Direct2D-Inhalten in einen Austauschkettenpuffer</span><span class="sxs-lookup"><span data-stu-id="41019-161">Writing Direct2D Content to a Swap Chain Buffer</span></span>

<span data-ttu-id="41019-162">Die einfachste Möglichkeit zum Hinzufügen von Direct2D-Inhalten zu einer Direct3D-Szene besteht darin, die [**GetBuffer-Methode**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) einer [**IDXGISwapChain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) zu verwenden, um eine DXGI-Oberfläche abzurufen, und dann die Oberfläche mit der [**CreateDxgiSurfaceRenderTarget-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) zu verwenden, um eine [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) zu erstellen, mit der Sie Ihren 2D-Inhalt zeichnen können.</span><span class="sxs-lookup"><span data-stu-id="41019-162">The simplest way to add Direct2D content to a Direct3D scene is to use the [**GetBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) method of an [**IDXGISwapChain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) to obtain a DXGI surface, then use the surface with the [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) method to create an [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) with which to draw your 2-D content.</span></span>

<span data-ttu-id="41019-163">Bei diesem Ansatz werden Ihre Inhalte nicht in drei Dimensionen gerendert. sie hat keine Perspektive oder Tiefe.</span><span class="sxs-lookup"><span data-stu-id="41019-163">This approach does not render your content in three dimensions; it will not have perspective or depth.</span></span> <span data-ttu-id="41019-164">Dies ist jedoch für mehrere allgemeine Aufgaben nützlich:</span><span class="sxs-lookup"><span data-stu-id="41019-164">However, it is useful for several common tasks:</span></span>

-   <span data-ttu-id="41019-165">Erstellen eines 2D-Hintergrunds für eine 3D-Szene.</span><span class="sxs-lookup"><span data-stu-id="41019-165">Creating a 2-D background for a 3-D scene.</span></span>
-   <span data-ttu-id="41019-166">Erstellen einer 2D-Schnittstelle vor einer 3D-Szene.</span><span class="sxs-lookup"><span data-stu-id="41019-166">Creating a 2-D interface in front of a 3-D scene.</span></span>
-   <span data-ttu-id="41019-167">Verwenden von Direct3D-Multisampling beim Rendern von Direct2D-Inhalt.</span><span class="sxs-lookup"><span data-stu-id="41019-167">Using Direct3D multisampling when rendering Direct2D content.</span></span>

<span data-ttu-id="41019-168">Im nächsten Abschnitt wird gezeigt, wie Sie einen 2D-Hintergrund für eine 3D-Szene erstellen.</span><span class="sxs-lookup"><span data-stu-id="41019-168">The next section shows how to create a 2-D background for a 3-D scene.</span></span>

### <a name="example-draw-a-2-d-background"></a><span data-ttu-id="41019-169">Beispiel: Zeichnen eines 2D-Hintergrunds</span><span class="sxs-lookup"><span data-stu-id="41019-169">Example: Draw a 2-D Background</span></span>

<span data-ttu-id="41019-170">In den folgenden Schritten wird beschrieben, wie Ein DXGI-Oberflächenrenderingziel erstellt und zum Zeichnen eines Farbverlaufshintergrunds verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="41019-170">The following steps describe how to create a DXGI surface render target and use it to draw a gradient background.</span></span>

1.  <span data-ttu-id="41019-171">Verwenden Sie [**die CreateSwapChain-Methode,**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain) um eine Swapkette für [**eine ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1) *(die m \_ pDevice-Variable) zu* erstellen.</span><span class="sxs-lookup"><span data-stu-id="41019-171">Use the [**CreateSwapChain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain) method to create a swap chain for an [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1) (the *m\_pDevice* variable).</span></span> <span data-ttu-id="41019-172">Die Swapkette verwendet das [**DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) DXGI-Format, eines der DXGI-Formate, die von Direct2D unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="41019-172">The swap chain uses the [**DXGI\_FORMAT\_B8G8R8A8\_UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) DXGI format, one of the DXGI formats supported by Direct2D.</span></span>

```C++
    if (SUCCEEDED(hr))
    {
        hr = pDevice->QueryInterface(&m_pDevice);
    }
    if (SUCCEEDED(hr))
    {
        hr = pDevice->QueryInterface(&pDXGIDevice);
    }
    if (SUCCEEDED(hr))
    {
        hr = pDXGIDevice->GetAdapter(&pAdapter);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAdapter->GetParent(IID_PPV_ARGS(&pDXGIFactory));
    }
    if (SUCCEEDED(hr))
    {
        DXGI_SWAP_CHAIN_DESC swapDesc;
        ::ZeroMemory(&swapDesc, sizeof(swapDesc));

        swapDesc.BufferDesc.Width = nWidth;
        swapDesc.BufferDesc.Height = nHeight;
        swapDesc.BufferDesc.Format = DXGI_FORMAT_B8G8R8A8_UNORM;
        swapDesc.BufferDesc.RefreshRate.Numerator = 60;
        swapDesc.BufferDesc.RefreshRate.Denominator = 1;
        swapDesc.SampleDesc.Count = 1;
        swapDesc.SampleDesc.Quality = 0;
        swapDesc.BufferUsage = DXGI_USAGE_RENDER_TARGET_OUTPUT;
        swapDesc.BufferCount = 1;
        swapDesc.OutputWindow = m_hwnd;
        swapDesc.Windowed = TRUE;

        hr = pDXGIFactory->CreateSwapChain(m_pDevice, &swapDesc, &m_pSwapChain);
    }
```

    

2.  <span data-ttu-id="41019-173">Verwenden Sie die [**GetBuffer-Methode**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) der Austauschkette, um eine DXGI-Oberfläche zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="41019-173">Use the swap chain's [**GetBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) method to obtain a DXGI surface.</span></span>

```C++
    // Get a surface in the swap chain
    hr = m_pSwapChain->GetBuffer(
        0,
        IID_PPV_ARGS(&pBackBuffer)
        );
```

    

3.  <span data-ttu-id="41019-174">Verwenden Sie die DXGI-Oberfläche, um ein DXGI-Renderziel zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="41019-174">Use the DXGI surface to create a DXGI render target.</span></span>
```C++
    // Create the DXGI Surface Render Target.
    FLOAT dpiX;
    FLOAT dpiY;
    m_pD2DFactory->GetDesktopDpi(&dpiX, &dpiY);

    D2D1_RENDER_TARGET_PROPERTIES props =
        D2D1::RenderTargetProperties(
            D2D1_RENDER_TARGET_TYPE_DEFAULT,
            D2D1::PixelFormat(DXGI_FORMAT_UNKNOWN, D2D1_ALPHA_MODE_PREMULTIPLIED),
            dpiX,
            dpiY
            );

    // Create a Direct2D render target which can draw into the surface in the swap chain

    
hr = m_pD2DFactory->CreateDxgiSurfaceRenderTarget(
        pBackBuffer,
        &props,
        &m_pBackBufferRT
        );
    
```



    

4.  <span data-ttu-id="41019-175">Verwenden Sie das Renderziel, um einen Farbverlaufshintergrund zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="41019-175">Use the render target to draw a gradient background.</span></span>

```C++
    // Swap chain will tell us how big the back buffer is
    DXGI_SWAP_CHAIN_DESC swapDesc;
    hr = m_pSwapChain->GetDesc(&swapDesc);

    if (SUCCEEDED(hr))
    {

    
// Draw a gradient background.
    if (m_pBackBufferRT)
    {
        D2D1_SIZE_F targetSize = m_pBackBufferRT->GetSize();

        m_pBackBufferRT->BeginDraw();

        m_pBackBufferGradientBrush->SetTransform(
            D2D1::Matrix3x2F::Scale(targetSize)
            );

        D2D1_RECT_F rect = D2D1::RectF(
            0.0f,
            0.0f,
            targetSize.width,
            targetSize.height
            );

        m_pBackBufferRT->FillRectangle(&rect, m_pBackBufferGradientBrush);

        hr = m_pBackBufferRT->EndDraw();
    }
```



    

<span data-ttu-id="41019-176">Code wird in diesem Beispiel ausgelassen.</span><span class="sxs-lookup"><span data-stu-id="41019-176">Code is omitted from this sample.</span></span>

## <a name="using-direct2d-content-as-a-texture"></a><span data-ttu-id="41019-177">Verwenden von Direct2D-Inhalt als Textur</span><span class="sxs-lookup"><span data-stu-id="41019-177">Using Direct2D Content as a Texture</span></span>

<span data-ttu-id="41019-178">Eine weitere Möglichkeit, Direct2D-Inhalt mit Direct3D zu verwenden, ist die Verwendung von Direct2D zum Generieren einer 2D-Textur und das anschließende Anwenden dieser Textur auf ein 3D-Modell.</span><span class="sxs-lookup"><span data-stu-id="41019-178">Another way to use Direct2D content with Direct3D is to use Direct2D to generate a 2-D texture and then apply that texture to a 3-D model.</span></span> <span data-ttu-id="41019-179">Hierzu erstellen Sie eine [**ID3D10Texture2D,**](/windows/desktop/api/d3d10/nn-d3d10-id3d10texture2d)erhalten eine DXGI-Oberfläche aus der Textur und verwenden dann die Oberfläche, um ein DXGI-Oberflächenrenderingziel zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="41019-179">You do this by creating an [**ID3D10Texture2D**](/windows/desktop/api/d3d10/nn-d3d10-id3d10texture2d), obtaining a DXGI surface from the texture, and then using the surface to create a DXGI surface render target.</span></span> <span data-ttu-id="41019-180">Die **ID3D10Texture2D-Oberfläche** muss das Bindungsflag [**D3D10 \_ BIND RENDER \_ \_ TARGET**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_bind_flag) und ein DXGI-Format verwenden, das von DXGI-Oberflächenrenderingzielen unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="41019-180">The **ID3D10Texture2D** surface must use the [**D3D10\_BIND\_RENDER\_TARGET**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_bind_flag) bind flag and use a DXGI format supported by DXGI surface render targets.</span></span> <span data-ttu-id="41019-181">Eine Liste der unterstützten DXGI-Formate finden Sie unter [Unterstützte Pixelformate und Alphamodi.](supported-pixel-formats-and-alpha-modes.md)</span><span class="sxs-lookup"><span data-stu-id="41019-181">For a list of supported DXGI formats, see [Supported Pixel Formats and Alpha Modes](supported-pixel-formats-and-alpha-modes.md).</span></span>

### <a name="example-use-direct2d-content-as-a-texture"></a><span data-ttu-id="41019-182">Beispiel: Verwenden von Direct2D-Inhalt als Textur</span><span class="sxs-lookup"><span data-stu-id="41019-182">Example: Use Direct2D Content as a Texture</span></span>

<span data-ttu-id="41019-183">Die folgenden Beispiele zeigen, wie Sie ein DXGI-Oberflächenrenderingziel erstellen, das in einer 2D-Textur gerendert wird (dargestellt durch [**id3D10Texture2D**](/windows/desktop/api/d3d10/nn-d3d10-id3d10texture2d)).</span><span class="sxs-lookup"><span data-stu-id="41019-183">The following examples show how to create a DXGI surface render target that renders to a 2-D texture (represented by an [**ID3D10Texture2D**](/windows/desktop/api/d3d10/nn-d3d10-id3d10texture2d)).</span></span>

1.  <span data-ttu-id="41019-184">Verwenden Sie zunächst ein Direct3D-Gerät, um eine 2D-Textur zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="41019-184">First, use a Direct3D device to create a 2-D texture.</span></span> <span data-ttu-id="41019-185">Die Textur verwendet die Bindungsflags [**D3D10 \_ BIND \_ RENDER \_ TARGET**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_bind_flag) und **D3D10 \_ BIND \_ SHADER \_ RESOURCE** und verwendet das [**\_ DXGI FORMAT \_ B8G8R8A8 \_ UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) DXGI-Format, eines der von Direct2D unterstützten DXGI-Formate.</span><span class="sxs-lookup"><span data-stu-id="41019-185">The texture uses the [**D3D10\_BIND\_RENDER\_TARGET**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_bind_flag) and **D3D10\_BIND\_SHADER\_RESOURCE** bind flags, and it uses the [**DXGI\_FORMAT\_B8G8R8A8\_UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) DXGI format, one of the DXGI formats supported by Direct2D.</span></span>

```C++
    // Allocate a offscreen D3D surface for D2D to render our 2D content into
    D3D10_TEXTURE2D_DESC texDesc;
    texDesc.ArraySize = 1;
    texDesc.BindFlags = D3D10_BIND_RENDER_TARGET | D3D10_BIND_SHADER_RESOURCE;
    texDesc.CPUAccessFlags = 0;
    texDesc.Format = DXGI_FORMAT_B8G8R8A8_UNORM;
    texDesc.Height = 512;
    texDesc.Width = 512;
    texDesc.MipLevels = 1;
    texDesc.MiscFlags = 0;
    texDesc.SampleDesc.Count = 1;
    texDesc.SampleDesc.Quality = 0;
    texDesc.Usage = D3D10_USAGE_DEFAULT;

    hr = m_pDevice->CreateTexture2D(&texDesc, NULL, &m_pOffscreenTexture);
```

    

2.  <span data-ttu-id="41019-186">Verwenden Sie die Textur, um eine DXGI-Oberfläche zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="41019-186">Use the texture to obtain a DXGI surface.</span></span>

```C++
    IDXGISurface *pDxgiSurface = NULL;

    
hr = m_pOffscreenTexture->QueryInterface(&pDxgiSurface);
```



    

3.  <span data-ttu-id="41019-187">Verwenden Sie die Oberfläche mit der [**CreateDxgiSurfaceRenderTarget-Methode,**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) um ein Direct2D-Renderziel abzurufen.</span><span class="sxs-lookup"><span data-stu-id="41019-187">Use the surface with the [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) method to obtain a Direct2D render target.</span></span>

```C++
    if (SUCCEEDED(hr))
    {
        // Create a D2D render target which can draw into our offscreen D3D
        // surface. Given that we use a constant size for the texture, we
        // fix the DPI at 96.
        D2D1_RENDER_TARGET_PROPERTIES props =
            D2D1::RenderTargetProperties(
                D2D1_RENDER_TARGET_TYPE_DEFAULT,
                D2D1::PixelFormat(DXGI_FORMAT_UNKNOWN, D2D1_ALPHA_MODE_PREMULTIPLIED),
                96,
                96
                );

    
    hr = m_pD2DFactory->CreateDxgiSurfaceRenderTarget(
            pDxgiSurface,
            &props,
            &m_pRenderTarget
            );
    }
```



    

<span data-ttu-id="41019-188">Nachdem Sie nun ein Direct2D-Renderziel erhalten und es einer Direct3D-Textur zugeordnet haben, können Sie das Renderziel verwenden, um Direct2D-Inhalt auf diese Textur zu zeichnen, und Sie können diese Textur auf Direct3D-Primitive anwenden.</span><span class="sxs-lookup"><span data-stu-id="41019-188">Now that you have obtained a Direct2D render target and associated it with a Direct3D texture, you can use the render target to draw Direct2D content to that texture, and you can apply that texture to Direct3D primitives.</span></span>

<span data-ttu-id="41019-189">Code wird in diesem Beispiel ausgelassen.</span><span class="sxs-lookup"><span data-stu-id="41019-189">Code is omitted from this sample.</span></span>

## <a name="resizing-a-dxgi-surface-render-target"></a><span data-ttu-id="41019-190">Ändern der Größe eines DXGI-Oberflächenrenderziels</span><span class="sxs-lookup"><span data-stu-id="41019-190">Resizing a DXGI Surface Render Target</span></span>

<span data-ttu-id="41019-191">DXGI-Oberflächenrenderziele unterstützen die [**ID2D1RenderTarget::Resize-Methode**](/windows/desktop/api/d2d1/nf-d2d1-id2d1hwndrendertarget-resize(constd2d1_size_u)) nicht.</span><span class="sxs-lookup"><span data-stu-id="41019-191">DXGI surface render targets do not support the [**ID2D1RenderTarget::Resize**](/windows/desktop/api/d2d1/nf-d2d1-id2d1hwndrendertarget-resize(constd2d1_size_u)) method.</span></span> <span data-ttu-id="41019-192">Um die Größe eines DXGI-Oberflächenrenderziels zu ändern, muss die Anwendung es freigeben und neu erstellen.</span><span class="sxs-lookup"><span data-stu-id="41019-192">To resize a DXGI surface render target, the application must release and re-create it.</span></span>

<span data-ttu-id="41019-193">Dieser Vorgang kann zu Leistungsproblemen führen.</span><span class="sxs-lookup"><span data-stu-id="41019-193">This operation can potentially create performance issues.</span></span> <span data-ttu-id="41019-194">Das Renderziel ist möglicherweise die letzte aktive Direct2D-Ressource, die einen Verweis auf die [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1) beibehält, die der DXGI-Oberfläche des Renderziels zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="41019-194">The render target might be the last active Direct2D resource that keeps a reference to the [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1) associated with the render target's DXGI surface.</span></span> <span data-ttu-id="41019-195">Wenn die Anwendung das Renderziel freigibt und der **ID3D10Device1-Verweis** zerstört wird, muss ein neues neu erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="41019-195">If the application releases the render target and the **ID3D10Device1** reference is destroyed, a new one must be recreated.</span></span>

<span data-ttu-id="41019-196">Sie können diesen potenziell kostspieligen Vorgang vermeiden, indem Sie mindestens eine Direct2D-Ressource behalten, die vom Renderziel erstellt wurde, während Sie dieses Renderziel neu erstellen.</span><span class="sxs-lookup"><span data-stu-id="41019-196">You can avoid this potentially expensive operation by keeping at least one Direct2D resource that was created by the render target while you re-create that render target.</span></span> <span data-ttu-id="41019-197">Es folgen einige Direct2D-Ressourcen, die für diesen Ansatz geeignet sind:</span><span class="sxs-lookup"><span data-stu-id="41019-197">The following are some Direct2D resources that work for this approach:</span></span>

-   <span data-ttu-id="41019-198">[**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) (die indirekt von einem [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush)gehalten werden kann)</span><span class="sxs-lookup"><span data-stu-id="41019-198">[**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) (which may be held indirectly by an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush))</span></span>
-   [<span data-ttu-id="41019-199">**ID2D1Layer**</span><span class="sxs-lookup"><span data-stu-id="41019-199">**ID2D1Layer**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1layer)
-   [<span data-ttu-id="41019-200">**ID2D1Mesh**</span><span class="sxs-lookup"><span data-stu-id="41019-200">**ID2D1Mesh**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1mesh)

<span data-ttu-id="41019-201">Um diesem Ansatz gerecht zu werden, sollte Ihre Größenänderungsmethode testen, ob das Direct3D-Gerät verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="41019-201">To accommodate this approach, your resize method should test to see whether the Direct3D device is available.</span></span> <span data-ttu-id="41019-202">Falls verfügbar, geben Sie Ihre DXGI-Oberflächenrenderziele frei, und erstellen Sie sie neu. Behalten Sie jedoch alle zuvor erstellten Ressourcen bei, und verwenden Sie sie wieder.</span><span class="sxs-lookup"><span data-stu-id="41019-202">If it is available, release and re-create your DXGI surface render targets, but keep all the resources that they created previously and reuse them.</span></span> <span data-ttu-id="41019-203">Dies funktioniert, da, wie in der Übersicht über Ressourcen [beschrieben,](resources-and-resource-domains.md)Ressourcen, die von zwei Renderzielen erstellt werden, kompatibel sind, wenn beide Renderziele demselben Direct3D-Gerät zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="41019-203">This works because, as described in the [Resources Overview](resources-and-resource-domains.md), resources created by two render targets are compatible when both render targets are associated with the same Direct3D device.</span></span>

## <a name="related-topics"></a><span data-ttu-id="41019-204">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="41019-204">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41019-205">Unterstützte Pixelformate und Alpha-Modi</span><span class="sxs-lookup"><span data-stu-id="41019-205">Supported Pixel Formats and Alpha Modes</span></span>](supported-pixel-formats-and-alpha-modes.md)
</dt> <dt>

<span data-ttu-id="41019-206">[**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget))</span><span class="sxs-lookup"><span data-stu-id="41019-206">[**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget))</span></span>
</dt> <dt>

[<span data-ttu-id="41019-207">Windows DirectX-Grafiken</span><span class="sxs-lookup"><span data-stu-id="41019-207">Windows DirectX Graphics</span></span>](../graphics-and-multimedia.md)
</dt> </dl>

 

 
