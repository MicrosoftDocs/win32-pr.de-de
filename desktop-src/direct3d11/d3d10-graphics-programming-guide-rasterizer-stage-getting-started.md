---
title: Einstieg in die Rasterizer-Phase
description: In diesem Abschnitt wird das Festlegen des Viewports, des Scheren Rechtecks, des Status des Rasterizers und der mehrfach Stichproben Erstellung beschrieben.
ms.assetid: d78c3845-76fd-4bd7-a603-bb1d8c66ac49
keywords:
- Multisampling, Status des Rasterizers (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac95a15221f6fd4bd422e96c0686816afb35d4e8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315213"
---
# <a name="getting-started-with-the-rasterizer-stage"></a><span data-ttu-id="080a8-104">Einstieg in die Rasterizer-Phase</span><span class="sxs-lookup"><span data-stu-id="080a8-104">Getting Started with the Rasterizer Stage</span></span>

<span data-ttu-id="080a8-105">In diesem Abschnitt wird das Festlegen des Viewports, des Scheren Rechtecks, des Status des Rasterizers und der mehrfach Stichproben Erstellung beschrieben.</span><span class="sxs-lookup"><span data-stu-id="080a8-105">This section describes setting the viewport, the scissors rectangle, the rasterizer state, and multi-sampling.</span></span>

## <a name="set-the-viewport"></a><span data-ttu-id="080a8-106">Festlegen des Viewports</span><span class="sxs-lookup"><span data-stu-id="080a8-106">Set the Viewport</span></span>

<span data-ttu-id="080a8-107">Ein Viewport ordnet Scheitelpunkt Positionen (im Clip Bereich) den renderzielpositionen zu.</span><span class="sxs-lookup"><span data-stu-id="080a8-107">A viewport maps vertex positions (in clip space) into render target positions.</span></span> <span data-ttu-id="080a8-108">In diesem Schritt werden die 3D-Positionen in 2D-Raum skaliert.</span><span class="sxs-lookup"><span data-stu-id="080a8-108">This step scales the 3D positions into 2D space.</span></span> <span data-ttu-id="080a8-109">Ein Renderziel ist mit den Y-Achsen ausgerichtet, die nach unten zeigen. Dies erfordert, dass die Y-Koordinaten während der viewportskala gekippt werden.</span><span class="sxs-lookup"><span data-stu-id="080a8-109">A render target is oriented with the Y axes pointing down; this requires that the Y coordinates get flipped during the viewport scale.</span></span> <span data-ttu-id="080a8-110">Außerdem werden die x-und y-Blöcke (Bereich der x-und y-Werte) skaliert, sodass Sie der Viewportgröße entsprechend den folgenden Formeln entsprechen:</span><span class="sxs-lookup"><span data-stu-id="080a8-110">In addition, the x and y extents (range of the x and y values) are scaled to fit the viewport size according to the following formulas:</span></span>


```
X = (X + 1) * Viewport.Width * 0.5 + Viewport.TopLeftX
Y = (1 - Y) * Viewport.Height * 0.5 + Viewport.TopLeftY
Z = Viewport.MinDepth + Z * (Viewport.MaxDepth - Viewport.MinDepth) 
```



<span data-ttu-id="080a8-111">In Tutorial 1 wird ein 640 × 480-Viewport mithilfe von [**D3D11 \_ Viewport**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_viewport) und durch Aufrufen von [**Verknüpfung id3d11devicecontext aus:: rssetviewports**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports)erstellt.</span><span class="sxs-lookup"><span data-stu-id="080a8-111">Tutorial 1 creates a 640 × 480 viewport using [**D3D11\_VIEWPORT**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_viewport) and by calling [**ID3D11DeviceContext::RSSetViewports**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports).</span></span>


```
    D3D11_VIEWPORT vp[1];
    vp[0].Width = 640.0f;
    vp[0].Height = 480.0f;
    vp[0].MinDepth = 0;
    vp[0].MaxDepth = 1;
    vp[0].TopLeftX = 0;
    vp[0].TopLeftY = 0;
    g_pd3dDevice->RSSetViewports( 1, vp );
```



<span data-ttu-id="080a8-112">Die viewportbeschreibung gibt die Größe des Viewports, den Bereich, dem die Tiefe zugeordnet werden soll (mit *mintiefe* und *maxtiefe*) und die Platzierung der oberen linken Ecke des Viewports an.</span><span class="sxs-lookup"><span data-stu-id="080a8-112">The viewport description specifies the size of the viewport, the range to map depth to (using *MinDepth* and *MaxDepth*), and the placement of the top left of the viewport.</span></span> <span data-ttu-id="080a8-113">*Mintiefe* muss kleiner oder gleich *maxtiefe* sein. der Bereich für *mintiefe* und *maxtiefe* liegt zwischen 0,0 und 1,0 (einschließlich).</span><span class="sxs-lookup"><span data-stu-id="080a8-113">*MinDepth* must be less than or equal to *MaxDepth*; the range for both *MinDepth* and *MaxDepth* is between 0.0 and 1.0, inclusive.</span></span> <span data-ttu-id="080a8-114">Es ist üblich, dass der Viewport einem Renderziel zugeordnet wird, dies ist jedoch nicht erforderlich. Außerdem muss der Viewport nicht dieselbe Größe oder Position aufweisen wie das Renderziel.</span><span class="sxs-lookup"><span data-stu-id="080a8-114">It is common for the viewport to map to a render target but it is not necessary; additionally, the viewport does not have to have the same size or position as the render target.</span></span>

<span data-ttu-id="080a8-115">Sie können ein Array von Viewports erstellen, aber nur eines kann auf eine primitive Ausgabe vom Geometry-Shader angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="080a8-115">You can create an array of viewports, but only one can be applied to a primitive output from the geometry shader.</span></span> <span data-ttu-id="080a8-116">Es kann jeweils nur ein Viewport aktiv festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="080a8-116">Only one viewport can be set active at a time.</span></span> <span data-ttu-id="080a8-117">Die Pipeline verwendet während der rasterisierung einen standardviewport (und das im nächsten Abschnitt erörterte Scheren-Rechteck).</span><span class="sxs-lookup"><span data-stu-id="080a8-117">The pipeline uses a default viewport (and scissor rectangle, discussed in the next section) during rasterization.</span></span> <span data-ttu-id="080a8-118">Der Standardwert ist immer das erste Viewport (oder Scheren Rechteck) im Array.</span><span class="sxs-lookup"><span data-stu-id="080a8-118">The default is always the first viewport (or scissor rectangle) in the array.</span></span> <span data-ttu-id="080a8-119">Um eine einzelne Auswahl des Viewports im Geometry-Shader auszuführen, geben Sie die "viewportarrayindex"-Semantik in der entsprechenden GS-Ausgabe Komponente in der GS-Ausgabe Signatur Deklaration an.</span><span class="sxs-lookup"><span data-stu-id="080a8-119">To perform a per-primitive selection of the viewport in the geometry shader, specify the ViewportArrayIndex semantic on the appropriate GS output component in the GS output signature declaration.</span></span>

<span data-ttu-id="080a8-120">Die maximale Anzahl von Viewports (und Scheren Rechtecke), die zu einem beliebigen Zeitpunkt an die Raster-Stufe gebunden werden können, ist 16 (angegeben durch **D3D11 \_ Viewport \_ und \_ scissorrect- \_ Objekt \_ Anzahl \_ pro \_ Pipeline**).</span><span class="sxs-lookup"><span data-stu-id="080a8-120">The maximum number of viewports (and scissor rectangles) that can be bound to the rasterizer stage at any one time is 16 (specified by **D3D11\_VIEWPORT\_AND\_SCISSORRECT\_OBJECT\_COUNT\_PER\_PIPELINE**).</span></span>

## <a name="set-the-scissor-rectangle"></a><span data-ttu-id="080a8-121">Festlegen des Scheren Rechtecks</span><span class="sxs-lookup"><span data-stu-id="080a8-121">Set the Scissor Rectangle</span></span>

<span data-ttu-id="080a8-122">Mit einem Scheren Rechteck haben Sie weitere Möglichkeiten, die Anzahl der Pixel zu verringern, die an die Ausgabe Zusammenführungs Phase gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="080a8-122">A scissor rectangle gives you another opportunity to reduce the number of pixels that will be sent to the output merger stage.</span></span> <span data-ttu-id="080a8-123">Pixel außerhalb des Scheren Rechtecks werden verworfen.</span><span class="sxs-lookup"><span data-stu-id="080a8-123">Pixels outside of the scissor rectangle are discarded.</span></span> <span data-ttu-id="080a8-124">Die Größe des Scheren Rechtecks wird in ganzen Zahlen angegeben.</span><span class="sxs-lookup"><span data-stu-id="080a8-124">The size of the scissor rectangle is specified in integers.</span></span> <span data-ttu-id="080a8-125">Auf ein Dreieck kann während der rasterisierung nur ein Scheren-Rechteck (auf der Grundlage von *viewportarrayindex* in der [Semantik des System Werts](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)) angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="080a8-125">Only one scissor rectangle (based on *ViewportArrayIndex* in [system value semantics](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)) can be applied to a triangle during rasterization.</span></span>

<span data-ttu-id="080a8-126">Um das Scheren-Rechteck zu aktivieren, verwenden Sie den *scissorenable* -Member (in [**D3D11 \_ Rasterizer \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)).</span><span class="sxs-lookup"><span data-stu-id="080a8-126">To enable the scissor rectangle, use the *ScissorEnable* member (in [**D3D11\_RASTERIZER\_DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)).</span></span> <span data-ttu-id="080a8-127">Das standardmäßige Scheren-Rechteck ist ein leeres Rechteck. Das heißt, alle Rect-Werte sind 0 (null).</span><span class="sxs-lookup"><span data-stu-id="080a8-127">The default scissor rectangle is an empty rectangle; that is, all rect values are 0.</span></span> <span data-ttu-id="080a8-128">Anders ausgedrückt: Wenn Sie das Scheren-Rechteck nicht einrichten und Scheren aktiviert ist, senden Sie keine Pixel an die Ausgabe-Fusion-Phase.</span><span class="sxs-lookup"><span data-stu-id="080a8-128">In other words, if you do not set up the scissor rectangle and scissor is enabled, you will not send any pixels to the output-merger stage.</span></span> <span data-ttu-id="080a8-129">Das gängigste Setup ist das Initialisieren des Scheren Rechtecks mit der Größe des Viewports.</span><span class="sxs-lookup"><span data-stu-id="080a8-129">The most common setup is to initialize the scissor rectangle to the size of the viewport.</span></span>

<span data-ttu-id="080a8-130">Um ein Array von Scheren Rechtecke auf das Gerät festzulegen, müssen Sie [**Verknüpfung id3d11devicecontext aus:: rssetcissorrects**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetscissorrects) mit [**D3D11 \_ Rect**](d3d11-rect.md)abrufen.</span><span class="sxs-lookup"><span data-stu-id="080a8-130">To set an array of scissor rectangles to the device, call [**ID3D11DeviceContext::RSSetScissorRects**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetscissorrects) with [**D3D11\_RECT**](d3d11-rect.md).</span></span>


```
D3D11_RECT rects[1];
  rects[0].left = 0;
  rects[0].right = 640;
  rects[0].top = 0;
  rects[0].bottom = 480;

  D3DDevice->RSSetScissorRects( 1, rects );
```



<span data-ttu-id="080a8-131">Diese Methode nimmt zwei Parameter an: (1) die Anzahl der Rechtecke im Array und (2) ein Array von Rechtecke.</span><span class="sxs-lookup"><span data-stu-id="080a8-131">This method takes two parameters: (1) the number of rectangles in the array and (2) an array of rectangles.</span></span>

<span data-ttu-id="080a8-132">Die Pipeline verwendet einen standardmäßigen Scheren-Rechteck Index während der rasterisierung (der Standardwert ist ein Rechteck der Größe 0 (null), bei dem Clipping deaktiviert ist).</span><span class="sxs-lookup"><span data-stu-id="080a8-132">The pipeline uses a default scissor rectangle index during rasterization (the default is a zero-size rectangle with clipping disabled).</span></span> <span data-ttu-id="080a8-133">Um dies zu überschreiben, geben \_ Sie die Semantik von SV viewportarrayindex zu einer GS-Ausgabe Komponente in der GS-Ausgabe Signatur Deklaration an.</span><span class="sxs-lookup"><span data-stu-id="080a8-133">To override this, specify the SV\_ViewportArrayIndex semantic to a GS output component in the GS output signature declaration.</span></span> <span data-ttu-id="080a8-134">Dies bewirkt, dass die GS-Phase diese GS-Ausgabe Komponente als vom systemgenerierte Komponente mit dieser Semantik markiert.</span><span class="sxs-lookup"><span data-stu-id="080a8-134">This will cause the GS stage to mark this GS output component as a system-generated component with this semantic.</span></span> <span data-ttu-id="080a8-135">Diese Semantik wird von der Raster-Stufe erkannt, und der Parameter, an den Sie angefügt ist, wird als Scheren Rechtecks Index verwendet, um auf das Array von Scheren Rechtecke zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="080a8-135">The rasterizer stage recognizes this semantic and will use the parameter it is attached to as the scissor rectangle index to access the array of scissor rectangles.</span></span> <span data-ttu-id="080a8-136">Vergessen Sie nicht, die Raster-Phase anzuweisen, das von Ihnen definierte Scheren-Rechteck zu verwenden, indem Sie den *scissorenable* -Wert in der Beschreibung des Rasterizers aktivieren, bevor Sie das Raster-Objekt erstellen.</span><span class="sxs-lookup"><span data-stu-id="080a8-136">Don't forget to tell the rasterizer stage to use the scissor rectangle that you define by enabling the *ScissorEnable* value in the rasterizer description before creating the rasterizer object.</span></span>

## <a name="set-rasterizer-state"></a><span data-ttu-id="080a8-137">Status des Rasterizers festlegen</span><span class="sxs-lookup"><span data-stu-id="080a8-137">Set Rasterizer State</span></span>

<span data-ttu-id="080a8-138">Beginnend mit Direct3D 10 ist der Raster State in einem Raster State-Objekt gekapselt.</span><span class="sxs-lookup"><span data-stu-id="080a8-138">Beginning with Direct3D 10, rasterizer state is encapsulated in a rasterizer state object.</span></span> <span data-ttu-id="080a8-139">Sie können bis zu 4096 Raster State-Objekte erstellen, die dann auf das Gerät festgelegt werden können, indem Sie ein Handle an das State-Objekt übergeben.</span><span class="sxs-lookup"><span data-stu-id="080a8-139">You may create up to 4096 rasterizer state objects which can then be set to the device by passing a handle to the state object.</span></span>

<span data-ttu-id="080a8-140">Verwenden Sie [**ID3D11Device1:: CreateRasterizerState1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createrasterizerstate1) , um ein Raster State-Objekt aus einer Beschreibung des Rasterizers zu erstellen (siehe [**D3D11 \_ Raster \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)).</span><span class="sxs-lookup"><span data-stu-id="080a8-140">Use [**ID3D11Device1::CreateRasterizerState1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createrasterizerstate1) to create a rasterizer state object from a rasterizer description (see [**D3D11\_RASTERIZER\_DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)).</span></span>


```
    ID3D11RasterizerState1 * g_pRasterState;

    D3D11_RASTERIZER_DESC1 rasterizerState;
    rasterizerState.FillMode = D3D11_FILL_SOLID;
    rasterizerState.CullMode = D3D11_CULL_FRONT;
    rasterizerState.FrontCounterClockwise = true;
    rasterizerState.DepthBias = false;
    rasterizerState.DepthBiasClamp = 0;
    rasterizerState.SlopeScaledDepthBias = 0;
    rasterizerState.DepthClipEnable = true;
    rasterizerState.ScissorEnable = true;
    rasterizerState.MultisampleEnable = false;
    rasterizerState.AntialiasedLineEnable = false;
    rasterizerState.ForcedSampleCount = 0;
    pd3dDevice->CreateRasterizerState1( &rasterizerState, &g_pRasterState );
```



<span data-ttu-id="080a8-141">Dieser Beispielsatz von Zuständen ist möglicherweise die einfachste Einrichtung des Rasterizers:</span><span class="sxs-lookup"><span data-stu-id="080a8-141">This example set of state accomplishes perhaps the most basic rasterizer setup:</span></span>

-   <span data-ttu-id="080a8-142">Vollfüll Modus</span><span class="sxs-lookup"><span data-stu-id="080a8-142">Solid fill mode</span></span>
-   <span data-ttu-id="080a8-143">Entfernen oder Entfernen von Hinterflächen gegen den Uhrzeigersinn ausgewickelte Reihenfolge für primitive annehmen</span><span class="sxs-lookup"><span data-stu-id="080a8-143">Cull out or remove back faces; assume counter-clockwise winding order for primitives</span></span>
-   <span data-ttu-id="080a8-144">Deaktivieren der tiefen Verschiebung, Aktivieren der tiefen Pufferung und Aktivieren des Scheren Rechtecks</span><span class="sxs-lookup"><span data-stu-id="080a8-144">Turn off depth bias but enable depth buffering and enable the scissor rectangle</span></span>
-   <span data-ttu-id="080a8-145">Deaktivieren von multisamplinggrad und Zeilen-Antialiasing</span><span class="sxs-lookup"><span data-stu-id="080a8-145">Turn off multisampling and line anti-aliasing</span></span>

<span data-ttu-id="080a8-146">Außerdem enthalten die grundlegenden Raster-Vorgänge immer Folgendes: Clipping (in der Ansicht "Frustum"), Perspektiven Teilung und viewportskala.</span><span class="sxs-lookup"><span data-stu-id="080a8-146">In addition, basic rasterizer operations, always include the following: clipping (to the view frustum), perspective divide, and the viewport scale.</span></span> <span data-ttu-id="080a8-147">Nachdem das Raster State-Objekt erfolgreich erstellt wurde, legen Sie es wie folgt auf das Gerät fest:</span><span class="sxs-lookup"><span data-stu-id="080a8-147">After successfully creating the rasterizer state object, set it to the device like this:</span></span>


```
    pd3dDevice->RSSetState(g_pRasterState);
```



### <a name="multisampling"></a><span data-ttu-id="080a8-148">Multisampling</span><span class="sxs-lookup"><span data-stu-id="080a8-148">Multisampling</span></span>

<span data-ttu-id="080a8-149">Bei der Multisampling-Funktion werden einige oder alle Komponenten eines Bilds mit einer höheren Auflösung (gefolgt von einer Herabstufung der ursprünglichen Auflösung) als Stichprobe angezeigt, um die am häufigsten sichtbare Form von Aliasing durch das Zeichnen von Polygon Kanten zu verringern.</span><span class="sxs-lookup"><span data-stu-id="080a8-149">Multisampling samples some or all of the components of an image at a higher resolution (followed by downsampling to the original resolution) to reduce the most visible form of aliasing caused by drawing polygon edges.</span></span> <span data-ttu-id="080a8-150">Obwohl multisamplinggrad subpixelbeispiele erfordert, implementieren moderne GPU multisamplinggrad, sodass ein Pixelshader einmal pro Pixel ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="080a8-150">Even though multisampling requires sub-pixel samples, modern GPU's implement multisampling so that a pixel shader runs once per pixel.</span></span> <span data-ttu-id="080a8-151">Dies bietet einen akzeptablen Kompromiss zwischen Leistung (insbesondere in einer GPU-gebundenen Anwendung) und Antialiasing des endgültigen Bilds.</span><span class="sxs-lookup"><span data-stu-id="080a8-151">This provides an acceptable tradeoff between performance (especially in a GPU bound application) and anti-aliasing the final image.</span></span>

<span data-ttu-id="080a8-152">Wenn Sie Multisampling verwenden möchten, legen Sie das Feld aktivieren in der [**Beschreibung der rasterisierung**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)fest, erstellen Sie ein Multisampling-Renderziel, und lesen Sie entweder das Renderziel mit einem Shader, um die Beispiele in eine einzelne Pixelfarbe aufzulösen oder [**Verknüpfung id3d11devicecontext aus:: resolvesbresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-resolvesubresource) aufzurufen, um die Beispiele mithilfe der Grafikkarte aufzulösen.</span><span class="sxs-lookup"><span data-stu-id="080a8-152">To use multisampling, set the enable field in the [**rasterization description**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1), create a multisampled render target, and either read the render target with a shader to resolve the samples into a single pixel color or call [**ID3D11DeviceContext::ResolveSubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-resolvesubresource) to resolve the samples using the video card.</span></span> <span data-ttu-id="080a8-153">Das häufigste Szenario ist das Zeichnen eines oder mehrerer Multisampling-Renderziele.</span><span class="sxs-lookup"><span data-stu-id="080a8-153">The most common scenario is to draw to one or more multisampled render targets.</span></span>

<span data-ttu-id="080a8-154">Multisampling ist unabhängig davon, ob eine Beispiel Maske verwendet wird, ob [die Alpha-zu-Abdeckung-](d3d10-graphics-programming-guide-blend-state.md) Funktion aktiviert ist, oder ob es sich um Schablonen Vorgänge handelt (die immer pro Stichprobe ausgeführt werden).</span><span class="sxs-lookup"><span data-stu-id="080a8-154">Multisampling is independent of whether or not a sample mask is used, [alpha-to-coverage](d3d10-graphics-programming-guide-blend-state.md) is enabled, or stencil operations (which are always performed per-sample).</span></span>

<span data-ttu-id="080a8-155">Die tiefen Tests sind von Multisampling betroffen:</span><span class="sxs-lookup"><span data-stu-id="080a8-155">Depth testing is affected by multisampling:</span></span>

-   <span data-ttu-id="080a8-156">Wenn multisamplinggrad aktiviert ist, wird die Tiefe pro Stichprobe interpoliert, und der tiefen-/Schablone-Test erfolgt pro Beispiel. die Pixel-Shader-Ausgabe Farbe wird für alle bestandenen Beispiele dupliziert.</span><span class="sxs-lookup"><span data-stu-id="080a8-156">When multisampling is enabled, depth is interpolated per sample and the depth/stencil test is done per sample; the pixel shader output color is duplicated for all passing samples.</span></span> <span data-ttu-id="080a8-157">Wenn der Pixelshader eine Tiefe ausgibt, wird der tiefen Wert für alle Stichproben dupliziert (obwohl dieses Szenario den Vorteil von Multisampling verliert).</span><span class="sxs-lookup"><span data-stu-id="080a8-157">If the pixel shader outputs depth, the depth value is duplicated for all samples (although this scenario loses the benefit of multisampling).</span></span>
-   <span data-ttu-id="080a8-158">Wenn die multisamplinggrad-Funktion deaktiviert ist, werden tiefen/Schablone-Tests immer noch pro Stichprobe ausgeführt, aber die Tiefe wird nicht pro Stichprobe interpoliert.</span><span class="sxs-lookup"><span data-stu-id="080a8-158">When multisampling is disabled, depth/stencil testing is still done per-sample, but depth is not interpolated per-sample.</span></span>

<span data-ttu-id="080a8-159">Es gibt keine Einschränkungen für das Mischen von Multisampling-und nicht-Multisampling-Rendering innerhalb eines einzelnen Renderziels.</span><span class="sxs-lookup"><span data-stu-id="080a8-159">There are no restrictions for mixing multisampled and non-multisampled rendering within a single render target.</span></span> <span data-ttu-id="080a8-160">Wenn Sie multisamplinggrad aktivieren und zu einem Renderziel ohne multisamplinggrad ziehen, führen Sie das gleiche Ergebnis wie bei aktivierter multisamplinggrad-Funktion aus. die Stichprobenentnahme erfolgt mit einem einzelnen Beispiel pro Pixel.</span><span class="sxs-lookup"><span data-stu-id="080a8-160">If you enable multisampling and draw to a non-multisampled render target, you produce the same result as if multisampling were not enabled; sampling is done with a single sample per-pixel.</span></span>

## <a name="related-topics"></a><span data-ttu-id="080a8-161">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="080a8-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="080a8-162">Stufe des Rasterizers</span><span class="sxs-lookup"><span data-stu-id="080a8-162">Rasterizer Stage</span></span>](d3d10-graphics-programming-guide-rasterizer-stage.md)
</dt> </dl>

 

 