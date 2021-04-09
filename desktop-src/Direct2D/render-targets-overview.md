---
title: Übersicht über Renderziele
description: Beschreibt die verschiedenen Typen von Direct2D-Renderingzielen und deren Verwendung.
ms.assetid: 8a67babd-20c7-47f4-8dd3-8c0320d89ad6
keywords:
- Direct2D, Renderziele
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 1770447d1468d7a09990696f8d523458bd2d0e46
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948868"
---
# <a name="render-targets-overview"></a><span data-ttu-id="d3a10-104">Übersicht über Renderziele</span><span class="sxs-lookup"><span data-stu-id="d3a10-104">Render Targets Overview</span></span>

<span data-ttu-id="d3a10-105">Ein Renderziel ist eine Ressource, die von der [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) -Schnittstelle erbt.</span><span class="sxs-lookup"><span data-stu-id="d3a10-105">A render target is a resource that inherits from the [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) interface.</span></span> <span data-ttu-id="d3a10-106">Ein Renderziel erstellt Ressourcen zum Zeichnen und ausführen tatsächlicher Zeichnungsvorgänge.</span><span class="sxs-lookup"><span data-stu-id="d3a10-106">A render target creates resources for drawing and performs actual drawing operations.</span></span> <span data-ttu-id="d3a10-107">In diesem Thema werden die verschiedenen Typen von Direct2D-Renderingzielen und deren Verwendung beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d3a10-107">This topic describes the different types of Direct2D render targets and how to use them.</span></span>

-   [<span data-ttu-id="d3a10-108">Renderziele</span><span class="sxs-lookup"><span data-stu-id="d3a10-108">Render Targets</span></span>](#render-targets-overview)
    -   [<span data-ttu-id="d3a10-109">Renderzielfeatures</span><span class="sxs-lookup"><span data-stu-id="d3a10-109">Render Target Features</span></span>](#render-target-features)
    -   [<span data-ttu-id="d3a10-110">Renderziel Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d3a10-110">Render Target Resources</span></span>](#render-target-resources)
    -   [<span data-ttu-id="d3a10-111">Zeichnen von Befehlen</span><span class="sxs-lookup"><span data-stu-id="d3a10-111">Drawing Commands</span></span>](#drawing-commands)
    -   [<span data-ttu-id="d3a10-112">Fehlerbehandlung</span><span class="sxs-lookup"><span data-stu-id="d3a10-112">Error Handling</span></span>](#error-handling)
-   [<span data-ttu-id="d3a10-113">Beispiel: Rendering von Inhalt in einem Fenster</span><span class="sxs-lookup"><span data-stu-id="d3a10-113">Example: Render Content to a Window</span></span>](#example-render-content-to-a-window)

## <a name="render-targets"></a><span data-ttu-id="d3a10-114">Renderziele</span><span class="sxs-lookup"><span data-stu-id="d3a10-114">Render Targets</span></span>

<span data-ttu-id="d3a10-115">Ein Renderziel ist eine Ressource, die von der [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) -Schnittstelle erbt.</span><span class="sxs-lookup"><span data-stu-id="d3a10-115">A render target is a resource that inherits from the [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) interface.</span></span> <span data-ttu-id="d3a10-116">Ein Renderziel erstellt Ressourcen zum Zeichnen und ausführen tatsächlicher Zeichnungsvorgänge.</span><span class="sxs-lookup"><span data-stu-id="d3a10-116">A render target creates resources for drawing and performs actual drawing operations.</span></span> <span data-ttu-id="d3a10-117">Es gibt verschiedene Arten von renderzielen, die zum renderinggrafiken auf folgende Weise verwendet werden können:</span><span class="sxs-lookup"><span data-stu-id="d3a10-117">There are several kinds of render targets that can be used to render graphics in the following ways:</span></span>

-   <span data-ttu-id="d3a10-118">[**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) -Objekte erzeugen Inhalt in einem Fenster.</span><span class="sxs-lookup"><span data-stu-id="d3a10-118">[**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) objects render content to a window.</span></span>
-   <span data-ttu-id="d3a10-119">[**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) -Objekte werden in einen GDI-Gerätekontext gerendering.</span><span class="sxs-lookup"><span data-stu-id="d3a10-119">[**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) objects render to a GDI device context.</span></span>
-   <span data-ttu-id="d3a10-120">Bitmap-renderzielobjekte renderinginhalte Inhalt zu einer Offscreen-Bitmap.</span><span class="sxs-lookup"><span data-stu-id="d3a10-120">Bitmap render target objects render content to an off-screen bitmap.</span></span>
-   <span data-ttu-id="d3a10-121">DXGI Renderziel Objekte werden zu einer DXGI-Oberfläche für die Verwendung mit Direct3D.</span><span class="sxs-lookup"><span data-stu-id="d3a10-121">DXGI render target objects render to a DXGI surface for use with Direct3D.</span></span>

<span data-ttu-id="d3a10-122">Da ein Renderziel mit einem bestimmten renderinggerät verknüpft ist, ist es eine Geräte abhängige Ressource und funktioniert nicht mehr, wenn das Gerät entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="d3a10-122">Because a render target is associated with a particular rendering device, it is a device-dependent resource and ceases to function if the device is removed.</span></span>

### <a name="render-target-features"></a><span data-ttu-id="d3a10-123">Renderzielfeatures</span><span class="sxs-lookup"><span data-stu-id="d3a10-123">Render Target Features</span></span>

<span data-ttu-id="d3a10-124">Sie können angeben, ob ein Renderziel eine Hardwarebeschleunigung verwendet und ob die Remote Anzeige von einem lokalen oder einem Remote Computer gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="d3a10-124">You can specify whether a render target uses hardware acceleration and whether remote display is rendered by a local or a remote computer.</span></span> <span data-ttu-id="d3a10-125">Renderziele können für Alias-oder Antialiasing-Rendering eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="d3a10-125">Render targets can be set up for aliased or antialiased rendering.</span></span> <span data-ttu-id="d3a10-126">Für renderingszenen mit einer großen Anzahl von primitiven kann ein Entwickler auch 2D-Grafiken im Alias Modus Rendern und D3D Multisampling Antialiasing verwenden, um eine höhere Skalierbarkeit zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="d3a10-126">For rendering scenes with a large number of primitives, a developer can also render 2-D graphics in aliased mode and use D3D multisample antialiasing to achieve greater scalability.</span></span>

<span data-ttu-id="d3a10-127">Renderziele können auch Zeichnungsvorgänge in Ebenen gruppieren, die durch die [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) -Schnittstelle dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="d3a10-127">Render targets can also group drawing operations into layers represented by the [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) interface.</span></span> <span data-ttu-id="d3a10-128">Ebenen sind nützlich, um Zeichnungsvorgänge zu erfassen, die zusammen zusammengeführt werden, wenn ein Frame gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="d3a10-128">Layers are useful for collecting drawing operations to be composited together when rendering a frame.</span></span> <span data-ttu-id="d3a10-129">In einigen Szenarien kann dies eine nützliche Alternative zum Rendern in ein Bitmap-Renderziel sein und dann den Bitmapinhalt wieder verwenden, da die Zuordnungs Kosten für die Schichten niedriger sind als bei einem [**ID2D1BitmapRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget).</span><span class="sxs-lookup"><span data-stu-id="d3a10-129">For some scenarios, this can be a useful alternative to rendering to a bitmap render target, and then reusing the bitmap contents, as allocation costs for layering are lower than for an [**ID2D1BitmapRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget).</span></span>

<span data-ttu-id="d3a10-130">Renderziele können neue Renderziele erstellen, die mit sich selbst kompatibel sind. Dies ist für das zwischengeschaltete debuggerrendering nützlich, während die verschiedenen renderzieleigenschaften beibehalten werden, die für den ursprünglichen festgelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="d3a10-130">Render targets can create new render targets that are compatible with themselves, which is useful for intermediate off-screen rendering while retaining the various render-target properties that were set on the original.</span></span>

<span data-ttu-id="d3a10-131">Es ist auch möglich, die Verwendung von GDI für ein Direct2D-Renderziel durch Aufrufen von [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für ein Renderziel für [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget)zu renderzielen, das über [**GetDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-getdc) -und [**ReleaseDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-releasedc) -Methoden verfügt, die zum Abrufen eines GDI-Geräte Kontexts verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="d3a10-131">It is also possible to render using GDI on a Direct2D render target by calling [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on a render target for [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget), which has [**GetDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-getdc) and [**ReleaseDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-releasedc) methods on it that can be used to retrieve a GDI device context.</span></span> <span data-ttu-id="d3a10-132">Das Rendering über GDI ist nur möglich, wenn das Renderziel mit dem festgelegten [**GDI-kompatiblen Flag "D2D1 \_ \_ Renderziel \_ \_ \_ Verwendung**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_usage) " erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="d3a10-132">Rendering via GDI is possible only if the render target was created with the [**D2D1\_RENDER\_TARGET\_USAGE\_GDI\_COMPATIBLE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_usage) flag set.</span></span> <span data-ttu-id="d3a10-133">Dies ist nützlich für Anwendungen, die in erster Linie mit Direct2D rendern, aber über ein Erweiterbarkeits Modell oder andere Legacy Inhalte verfügen, die die Fähigkeit zum Rendern mit GDI erfordern.</span><span class="sxs-lookup"><span data-stu-id="d3a10-133">This is useful for applications that are primarily rendering with Direct2D but have an extensibility model or other legacy content that requires the ability to render with GDI.</span></span> <span data-ttu-id="d3a10-134">Weitere Informationen finden Sie unter [Übersicht über die Zusammenarbeit zwischen Direct2D und GDI](direct2d-and-gdi-interoperation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d3a10-134">For more information, see the [Direct2D and GDI Interoperation Overview](direct2d-and-gdi-interoperation-overview.md).</span></span>

### <a name="render-target-resources"></a><span data-ttu-id="d3a10-135">Renderziel Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d3a10-135">Render Target Resources</span></span>

<span data-ttu-id="d3a10-136">Wie eine Factory kann ein Renderziel Zeichnungs Ressourcen erstellen.</span><span class="sxs-lookup"><span data-stu-id="d3a10-136">Like a factory, a render target can create drawing resources.</span></span> <span data-ttu-id="d3a10-137">Alle von einem Renderziel erstellten Ressourcen sind Geräte abhängige Ressourcen (genau wie das Renderziel).</span><span class="sxs-lookup"><span data-stu-id="d3a10-137">Any resources created by a render target are device-dependent resources (just like the render target).</span></span> <span data-ttu-id="d3a10-138">Mit einem Renderziel können die folgenden Ressourcentypen erstellt werden:</span><span class="sxs-lookup"><span data-stu-id="d3a10-138">A render target can create the following types of resources:</span></span>

-   <span data-ttu-id="d3a10-139">Bitmaps</span><span class="sxs-lookup"><span data-stu-id="d3a10-139">Bitmaps</span></span>
-   <span data-ttu-id="d3a10-140">Pinsel</span><span class="sxs-lookup"><span data-stu-id="d3a10-140">Brushes</span></span>
-   <span data-ttu-id="d3a10-141">Ebenen</span><span class="sxs-lookup"><span data-stu-id="d3a10-141">Layers</span></span>
-   <span data-ttu-id="d3a10-142">Gittermodelle</span><span class="sxs-lookup"><span data-stu-id="d3a10-142">Meshes</span></span>

### <a name="drawing-commands"></a><span data-ttu-id="d3a10-143">Zeichnen von Befehlen</span><span class="sxs-lookup"><span data-stu-id="d3a10-143">Drawing Commands</span></span>

<span data-ttu-id="d3a10-144">Zum Renderinginhalt verwenden Sie die Zeichnungs Methoden des Renderziels.</span><span class="sxs-lookup"><span data-stu-id="d3a10-144">To render content, you use the render target drawing methods.</span></span> <span data-ttu-id="d3a10-145">Bevor Sie mit dem Zeichnen beginnen, wird die [**ID2D1RenderTarget:: beginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) -Methode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="d3a10-145">Before you begin drawing, you call the [**ID2D1RenderTarget::BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) method.</span></span> <span data-ttu-id="d3a10-146">Nachdem Sie das Zeichnen abgeschlossen haben, können Sie die [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="d3a10-146">After you finished drawing, you call the [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method.</span></span> <span data-ttu-id="d3a10-147">Zwischen diesen Aufrufen verwenden Sie Draw-und Fill-Methoden zum Rendering von Zeichnungs Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="d3a10-147">Between these calls, you use Draw and Fill methods to render drawing resources.</span></span> <span data-ttu-id="d3a10-148">Die meisten Draw-und Fill-Methoden übernehmen eine Form (entweder eine primitive oder eine Geometrie) und einen Pinsel zum ausfüllen oder gliedern der Form.</span><span class="sxs-lookup"><span data-stu-id="d3a10-148">Most Draw and Fill methods take a shape (either a primitive or a geometry) and a brush for filling or outlining the shape.</span></span>

<span data-ttu-id="d3a10-149">Renderziele stellen Methoden für das Abschneiden, das Anwenden von Deck Kraft Masken und das Transformieren des Koordinaten Raums bereit.</span><span class="sxs-lookup"><span data-stu-id="d3a10-149">Render targets provide methods for clipping, applying opacity masks, and transforming the coordinate space.</span></span>

<span data-ttu-id="d3a10-150">Direct2D verwendet ein Links händiges Koordinatensystem: positive Werte der x-Achse werden nach rechts fortgesetzt, und die positiven y-Achsen Werte werden nach unten fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="d3a10-150">Direct2D uses a left-handed coordinate system: positive x-axis values proceed to the right and positive y-axis values proceed downward.</span></span>

### <a name="error-handling"></a><span data-ttu-id="d3a10-151">Fehlerbehandlung</span><span class="sxs-lookup"><span data-stu-id="d3a10-151">Error Handling</span></span>

<span data-ttu-id="d3a10-152">Zeichnungs Befehle des Renderziels geben nicht an, ob der angeforderte Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="d3a10-152">Render target drawing commands do not indicate whether the requested operation was successful.</span></span> <span data-ttu-id="d3a10-153">Um herauszufinden, ob Zeichnungs Fehler vorliegen, rufen Sie die Renderziel-Löschmethode oder die [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) [**-Methode auf**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) , um ein **HRESULT** zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d3a10-153">To find out whether there are drawing errors, call the render target [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) method or [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method to obtain an **HRESULT**.</span></span>

## <a name="example-render-content-to-a-window"></a><span data-ttu-id="d3a10-154">Beispiel: Rendering von Inhalt in einem Fenster</span><span class="sxs-lookup"><span data-stu-id="d3a10-154">Example: Render Content to a Window</span></span>

<span data-ttu-id="d3a10-155">Im folgenden Beispiel wird die Methode " [**kreatehwndrendertarget**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createhwndrendertarget(constd2d1_render_target_properties__constd2d1_hwnd_render_target_properties__id2d1hwndrendertarget)) " verwendet, um eine [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget)zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d3a10-155">The following example uses the [**CreateHwndRenderTarget**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createhwndrendertarget(constd2d1_render_target_properties__constd2d1_hwnd_render_target_properties__id2d1hwndrendertarget)) method to create an [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget).</span></span>


```C++
RECT rc;
GetClientRect(m_hwnd, &rc);

D2D1_SIZE_U size = D2D1::SizeU(
    rc.right - rc.left,
    rc.bottom - rc.top
    );

// Create a Direct2D render target.
hr = m_pD2DFactory->CreateHwndRenderTarget(
    D2D1::RenderTargetProperties(),
    D2D1::HwndRenderTargetProperties(m_hwnd, size),
    &m_pRenderTarget
    );
```



<span data-ttu-id="d3a10-156">Im nächsten Beispiel wird [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) verwendet, um Text in das Fenster zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="d3a10-156">The next example uses the [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) to draw text to the window.</span></span>


```C++
//  Called whenever the application needs to display the client
//  window. This method writes "Hello, World"
//
//  Note that this function will automatically discard device-specific
//  resources if the Direct3D device disappears during function
//  invocation, and will recreate the resources the next time it's
//  invoked.
//
HRESULT DemoApp::OnRender()
{
    HRESULT hr;

    hr = CreateDeviceResources();

    if (SUCCEEDED(hr))
    {
        static const WCHAR sc_helloWorld[] = L"Hello, World!";

        // Retrieve the size of the render target.
        D2D1_SIZE_F renderTargetSize = m_pRenderTarget->GetSize();

        m_pRenderTarget->BeginDraw();

        m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

        m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::White));

        m_pRenderTarget->DrawText(
            sc_helloWorld,
            ARRAYSIZE(sc_helloWorld) - 1,
            m_pTextFormat,
            D2D1::RectF(0, 0, renderTargetSize.width, renderTargetSize.height),
            m_pBlackBrush
            );

        hr = m_pRenderTarget->EndDraw();

        if (hr == D2DERR_RECREATE_TARGET)
        {
            hr = S_OK;
            DiscardDeviceResources();
        }
    }

    return hr;
}
```



<span data-ttu-id="d3a10-157">Code wurde in diesem Beispiel ausgelassen.</span><span class="sxs-lookup"><span data-stu-id="d3a10-157">Code has been omitted from this example.</span></span>

 

 