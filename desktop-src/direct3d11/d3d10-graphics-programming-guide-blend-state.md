---
title: Konfigurieren von Mischungs Funktionen
description: Mischungs Vorgänge werden für jede Pixel-Shader-Ausgabe (RGBA-Wert) ausgeführt, bevor der Ausgabewert in ein Renderziel geschrieben wird. Wenn die multisamplinggrad-Funktion aktiviert ist, erfolgt die Mischung in jedem Multisample. Andernfalls wird für jedes Pixel ein Mischungs Vorgang durchgeführt.
ms.assetid: f5c79baf-7bd3-4f58-abe7-8e96cd6be9d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08acf1ea286b29a1cb96873bbfe170c6f38699f7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993391"
---
# <a name="configuring-blending-functionality"></a><span data-ttu-id="49be6-104">Konfigurieren von Mischungs Funktionen</span><span class="sxs-lookup"><span data-stu-id="49be6-104">Configuring Blending Functionality</span></span>

<span data-ttu-id="49be6-105">Mischungs Vorgänge werden für jede Pixel-Shader-Ausgabe (RGBA-Wert) ausgeführt, bevor der Ausgabewert in ein Renderziel geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="49be6-105">Blending operations are performed on every pixel shader output (RGBA value) before the output value is written to a render target.</span></span> <span data-ttu-id="49be6-106">Wenn die multisamplinggrad-Funktion aktiviert ist, erfolgt die Mischung in jedem Multisample. Andernfalls wird für jedes Pixel ein Mischungs Vorgang durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="49be6-106">If multisampling is enabled, blending is done on each multisample; otherwise, blending is performed on each pixel.</span></span>

-   [<span data-ttu-id="49be6-107">Erstellen des Blend-Status</span><span class="sxs-lookup"><span data-stu-id="49be6-107">Create the Blend State</span></span>](#create-the-blend-state)
-   [<span data-ttu-id="49be6-108">Binden des Blend-Status</span><span class="sxs-lookup"><span data-stu-id="49be6-108">Bind the Blend State</span></span>](#bind-the-blend-state)
-   [<span data-ttu-id="49be6-109">Erweiterte Mischungs Themen</span><span class="sxs-lookup"><span data-stu-id="49be6-109">Advanced Blending Topics</span></span>](#advanced-blending-topics)
    -   [<span data-ttu-id="49be6-110">Alpha-zu-Abdeckung</span><span class="sxs-lookup"><span data-stu-id="49be6-110">Alpha-To-Coverage</span></span>](#alpha-to-coverage)
    -   [<span data-ttu-id="49be6-111">Mischen von Pixel-Shader-Ausgaben</span><span class="sxs-lookup"><span data-stu-id="49be6-111">Blending Pixel Shader Outputs</span></span>](#blending-pixel-shader-outputs)
-   [<span data-ttu-id="49be6-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="49be6-112">Related topics</span></span>](#related-topics)

## <a name="create-the-blend-state"></a><span data-ttu-id="49be6-113">Erstellen des Blend-Status</span><span class="sxs-lookup"><span data-stu-id="49be6-113">Create the Blend State</span></span>

<span data-ttu-id="49be6-114">Der Blend-Status ist eine Auflistung von Zuständen, die zum Steuern von Mischungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="49be6-114">The blend state is a collection of states used to control blending.</span></span> <span data-ttu-id="49be6-115">Diese Zustände (definiert in [**D3D11 \_ Blend \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_blend_desc1)) werden zum Erstellen des Blend-Zustands Objekts durch Aufrufen von [**ID3D11Device1:: CreateBlendState1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createblendstate1)verwendet.</span><span class="sxs-lookup"><span data-stu-id="49be6-115">These states (defined in [**D3D11\_BLEND\_DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_blend_desc1)) are used to create the blend state object by calling [**ID3D11Device1::CreateBlendState1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createblendstate1).</span></span>

<span data-ttu-id="49be6-116">Im folgenden finden Sie ein sehr einfaches Beispiel für die Erstellung von Blend-Zuständen, mit dem Alpha Blending deaktiviert und keine Pixel Maskierung pro Komponente verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="49be6-116">For instance, here is a very simple example of blend-state creation that disables alpha blending and uses no per-component pixel masking.</span></span>


```
ID3D11BlendState1* g_pBlendStateNoBlend = NULL;

D3D11_BLEND_DESC1 BlendState;
ZeroMemory(&BlendState, sizeof(D3D11_BLEND_DESC1));
BlendState.RenderTarget[0].BlendEnable = FALSE;
BlendState.RenderTarget[0].RenderTargetWriteMask = D3D11_COLOR_WRITE_ENABLE_ALL;
pd3dDevice->CreateBlendState1(&BlendState, &g_pBlendStateNoBlend);
```



<span data-ttu-id="49be6-117">Dieses Beispiel ähnelt dem [HLSLWithoutFX10](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx)-Beispiel.</span><span class="sxs-lookup"><span data-stu-id="49be6-117">This example is similar to the [HLSLWithoutFX10 Sample](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx).</span></span>

## <a name="bind-the-blend-state"></a><span data-ttu-id="49be6-118">Binden des Blend-Status</span><span class="sxs-lookup"><span data-stu-id="49be6-118">Bind the Blend State</span></span>

<span data-ttu-id="49be6-119">Nachdem Sie das Blend-State-Objekt erstellt haben, binden Sie das Blend-State-Objekt an die Output-Merger-Phase durch Aufrufen von [**Verknüpfung id3d11devicecontext aus:: omsetblendstate**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetblendstate).</span><span class="sxs-lookup"><span data-stu-id="49be6-119">After you create the blend-state object, bind the blend-state object to the output-merger stage by calling [**ID3D11DeviceContext::OMSetBlendState**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetblendstate).</span></span>


```
float blendFactor[4] = { 0.0f, 0.0f, 0.0f, 0.0f };
UINT sampleMask   = 0xffffffff;

pd3dDevice->OMSetBlendState(g_pBlendStateNoBlend, blendFactor, sampleMask);
```



<span data-ttu-id="49be6-120">Diese API übernimmt drei Parameter: das Blend-State-Objekt, einen Kombination aus vier Komponenten und eine Beispiel Maske.</span><span class="sxs-lookup"><span data-stu-id="49be6-120">This API takes three parameters: the blend-state object, a four-component blend factor, and a sample mask.</span></span> <span data-ttu-id="49be6-121">Sie können **null** für das Blend-State-Objekt übergeben, um den standardmäßigen Blend-Status anzugeben, oder übergeben Sie ein Blend-State-Objekt.</span><span class="sxs-lookup"><span data-stu-id="49be6-121">You can pass in **NULL** for the blend-state object to specify the default blend state or pass in a blend-state object.</span></span> <span data-ttu-id="49be6-122">Wenn Sie das Blend-State-Objekt mit [**D3D11 \_ Blend \_ Blend \_ Factor**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_blend) oder [**D3D11 \_ Blend \_ Inv \_ Blend \_ Factor**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_blend)erstellt haben, können Sie einen Blend-Faktor übergeben, um Werte für den Pixelshader, das Renderziel oder beides zu modulieren.</span><span class="sxs-lookup"><span data-stu-id="49be6-122">If you created the blend-state object with [**D3D11\_BLEND\_BLEND\_FACTOR**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_blend) or [**D3D11\_BLEND\_INV\_BLEND\_FACTOR**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_blend), you can pass a blend factor to modulate values for the pixel shader, render target, or both.</span></span> <span data-ttu-id="49be6-123">Wenn Sie das Blend-State-Objekt nicht mit dem **D3D11 \_ Blend- \_ \_ Faktor** oder **D3D11 Blend- \_ \_ Inv- \_ Blend \_**-Faktor erstellt haben, können Sie trotzdem einen nicht-NULL-Blend-Faktor übergeben, aber die Mischungs Phase verwendet nicht den Blend-Faktor. die Laufzeit speichert den Blend-Faktor, und Sie können später [**Verknüpfung id3d11devicecontext aus:**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omgetblendstate)</span><span class="sxs-lookup"><span data-stu-id="49be6-123">If you didn't create the blend-state object with **D3D11\_BLEND\_BLEND\_FACTOR** or **D3D11\_BLEND\_INV\_BLEND\_FACTOR**, you can still pass a non-NULL blend factor, but the blending stage does not use the blend factor; the runtime stores the blend factor, and you can later call [**ID3D11DeviceContext::OMGetBlendState**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omgetblendstate) to retrieve the blend factor.</span></span> <span data-ttu-id="49be6-124">Wenn Sie **null** übergeben, verwendet die Common Language Runtime einen Blend-Faktor, der gleich {1, 1, 1, 1} ist, oder speichert diesen.</span><span class="sxs-lookup"><span data-stu-id="49be6-124">If you pass **NULL**, the runtime uses or stores a blend factor equal to { 1, 1, 1, 1 }.</span></span> <span data-ttu-id="49be6-125">Bei der Sample Mask handelt es sich um eine benutzerdefinierte Maske, die bestimmt, wie das vorhandene Renderziel vor dem Aktualisieren Stichproben wird.</span><span class="sxs-lookup"><span data-stu-id="49be6-125">The sample mask is a user-defined mask that determines how to sample the existing render target before updating it.</span></span> <span data-ttu-id="49be6-126">Die standardmäßige Samplings-Maske ist 0xFFFFFFFF und legt die Punkt Stichproben Entnahme fest.</span><span class="sxs-lookup"><span data-stu-id="49be6-126">The default sampling mask is 0xffffffff which designates point sampling.</span></span>

<span data-ttu-id="49be6-127">In den meisten tiefen Puffer Schemas ist das Pixel, das der Kamera am nächsten ist, das, das gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="49be6-127">In most depth buffering schemes, the pixel closest to the camera is the one that gets drawn.</span></span> <span data-ttu-id="49be6-128">Beim [Einrichten des Status der tiefen Schablone](d3d10-graphics-programming-guide-depth-stencil.md)kann es sich bei dem **depthfunc** -Member der [**D3D11- \_ tiefen \_ Schablone \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc) um einen beliebigen [**D3D11- \_ Vergleichs \_ Func**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_comparison_func)handeln.</span><span class="sxs-lookup"><span data-stu-id="49be6-128">When [setting up the depth stencil state](d3d10-graphics-programming-guide-depth-stencil.md), the **DepthFunc** member of [**D3D11\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc) can be any [**D3D11\_COMPARISON\_FUNC**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_comparison_func).</span></span> <span data-ttu-id="49be6-129">Normalerweise sollte **depthfunc** den **D3D11- \_ Vergleich \_ weniger** betragen, sodass die Pixel, die der Kamera am nächsten sind, die dahinter liegenden Pixel überschreiben werden.</span><span class="sxs-lookup"><span data-stu-id="49be6-129">Normally, you would want **DepthFunc** to be **D3D11\_COMPARISON\_LESS**, so that the pixels closest to the camera will overwrite the pixels behind them.</span></span> <span data-ttu-id="49be6-130">Abhängig von den Anforderungen Ihrer Anwendung können jedoch alle anderen Vergleichsfunktionen für den tiefen Test verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="49be6-130">However, depending on the needs of your application, any of the other comparison functions may be used to do the depth test.</span></span>

## <a name="advanced-blending-topics"></a><span data-ttu-id="49be6-131">Erweiterte Mischungs Themen</span><span class="sxs-lookup"><span data-stu-id="49be6-131">Advanced Blending Topics</span></span>

-   [<span data-ttu-id="49be6-132">Alpha-zu-Abdeckung</span><span class="sxs-lookup"><span data-stu-id="49be6-132">Alpha-To-Coverage</span></span>](#alpha-to-coverage)
-   [<span data-ttu-id="49be6-133">Mischen von Pixel-Shader-Ausgaben</span><span class="sxs-lookup"><span data-stu-id="49be6-133">Blending Pixel Shader Outputs</span></span>](#blending-pixel-shader-outputs)

### <a name="alpha-to-coverage"></a><span data-ttu-id="49be6-134">Alpha-zu-Abdeckung</span><span class="sxs-lookup"><span data-stu-id="49be6-134">Alpha-To-Coverage</span></span>

<span data-ttu-id="49be6-135">Alpha-zu-Abdeckung ist eine multisamplinggrad-Technik, die besonders nützlich für Situationen wie z. b. ein dichtes Laub ist, bei dem mehrere überlappende Polygone verwendet werden, um die Ränder innerhalb der Oberfläche zu definieren.</span><span class="sxs-lookup"><span data-stu-id="49be6-135">Alpha-to-coverage is a multisampling technique that is most useful for situations such as dense foliage where there are several overlapping polygons that use alpha transparency to define edges within the surface.</span></span>

<span data-ttu-id="49be6-136">Sie können den **Alpha atocoverageenable** -Member von [**D3D11 \_ Blend \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_blend_desc1) oder [**D3D11 \_ Blend \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc) verwenden, um zu wechseln, ob die Common Language Runtime die. a-Komponente (Alpha) des Ausgabe Registers [SV \_ target](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)0 aus dem Pixel-Shader in eine n-Sample-Abdeckungs Maske (bei einem n-Sample- **renderTarget**) konvertiert.</span><span class="sxs-lookup"><span data-stu-id="49be6-136">You can use the **AlphaToCoverageEnable** member of [**D3D11\_BLEND\_DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_blend_desc1) or [**D3D11\_BLEND\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc) to toggle whether the runtime converts the .a component (alpha) of output register [SV\_Target](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)0 from the pixel shader to an n-step coverage mask (given an n-sample **RenderTarget**).</span></span> <span data-ttu-id="49be6-137">Die Laufzeit führt eine **and-** Operation dieser Maske mit der typischen Beispiel Abdeckung für das Pixel im primitiven (zusätzlich zur Beispiel Maske) aus, um zu bestimmen, welche Beispiele in allen aktiven **renderTarget** s aktualisiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="49be6-137">The runtime performs an **AND** operation of this mask with the typical sample coverage for the pixel in the primitive (in addition to the sample mask) to determine which samples to update in all the active **RenderTarget** s.</span></span>

<span data-ttu-id="49be6-138">Wenn der Pixelshader die [SV- \_ Abdeckung](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)ausgibt, deaktiviert die Runtime die Alpha-zu-Abdeckung.</span><span class="sxs-lookup"><span data-stu-id="49be6-138">If the pixel shader outputs [SV\_Coverage](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics), the runtime disables alpha-to-coverage.</span></span>

> [!Note]  
> <span data-ttu-id="49be6-139">Bei Multisampling gibt die Laufzeit nur eine Abdeckung für alle **renderTarget** s frei.</span><span class="sxs-lookup"><span data-stu-id="49be6-139">In multisampling, the runtime shares only one coverage for all **RenderTarget** s.</span></span> <span data-ttu-id="49be6-140">Die Tatsache, dass die Laufzeit liest und konvertiert. ein von der Ausgabe [SV \_ target](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)0 in die Abdeckung, wenn **Alpha atocoverageenable** den Wert true hat, ändert sich nicht. ein Wert, der an den Blender bei **renderTarget** 0 übergeht (wenn ein **renderTarget** festgelegt wird).</span><span class="sxs-lookup"><span data-stu-id="49be6-140">The fact that the runtime reads and converts .a from output [SV\_Target](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)0 to coverage when **AlphaToCoverageEnable** is TRUE does not change the .a value that goes to the blender at **RenderTarget** 0 (if a **RenderTarget** happens to be set there).</span></span> <span data-ttu-id="49be6-141">Im Allgemeinen haben Sie, wenn Sie Alpha-zu-Abdeckung aktivieren, nicht Einfluss darauf, wie alle Farb Ausgaben von Pixel-Shadern mit **renderTarget** s über die [Ausgabe-Fusion-Phase](d3d10-graphics-programming-guide-output-merger-stage.md) interagieren, mit der Ausnahme, dass die Laufzeit eine **and** -Operation der Abdeckungs Maske mit der Alpha-zu-Coverage-Maske ausführt.</span><span class="sxs-lookup"><span data-stu-id="49be6-141">In general, if you enable alpha-to-coverage, you don't affect how all color outputs from pixel shaders interact with **RenderTarget** s through the [output-merger stage](d3d10-graphics-programming-guide-output-merger-stage.md) except that the runtime performs an **AND** operation of the coverage mask with the alpha-to-coverage mask.</span></span> <span data-ttu-id="49be6-142">Die Alpha-zu-Abdeckung funktioniert unabhängig davon, ob die Laufzeit **renderTarget** mischen kann oder ob Sie Blending auf **renderTarget** verwenden.</span><span class="sxs-lookup"><span data-stu-id="49be6-142">Alpha-to-coverage works independently to whether the runtime can blend **RenderTarget** or whether you use blending on **RenderTarget**.</span></span>

 

<span data-ttu-id="49be6-143">Die Grafikhardware gibt nicht genau an, wie der Pixelshader [SV \_ target](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)0. a (Alpha) in eine Abdeckungs Maske konvertiert wird, mit dem Unterschied, dass Alpha von 0 (oder weniger) keiner Abdeckung zugeordnet werden muss und Alpha von 1 (oder höher) der vollständigen Abdeckung zugeordnet werden muss (bevor die Laufzeit eine **and-** Operation mit tatsächlicher primitiver Abdeckung ausführt).</span><span class="sxs-lookup"><span data-stu-id="49be6-143">Graphics hardware doesn't precisely specify exactly how it converts pixel shader [SV\_Target](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)0.a (alpha) to a coverage mask, except that alpha of 0 (or less) must map to no coverage and alpha of 1 (or greater) must map to full coverage (before the runtime performs an **AND** operation with actual primitive coverage).</span></span> <span data-ttu-id="49be6-144">Da Alpha zwischen 0 und 1 wechselt, sollte sich die resultierende Abdeckung in der Regel monoton steigern.</span><span class="sxs-lookup"><span data-stu-id="49be6-144">As alpha goes from 0 to 1, the resulting coverage should generally increase monotonically.</span></span> <span data-ttu-id="49be6-145">Allerdings kann die Hardware eine Bereichs Auflösung durchführen, um eine bessere Quantisierung von Alpha Werten zu ermöglichen, die sich aus räumlichen Lösungen und Geräuschen zusammenbringt.</span><span class="sxs-lookup"><span data-stu-id="49be6-145">However, hardware might perform area dithering to provide some better quantization of alpha values at the cost of spatial resolution and noise.</span></span> <span data-ttu-id="49be6-146">Der Alpha-Wert NaN (keine Zahl) führt zu einer nichtabdeckung (null) Maske.</span><span class="sxs-lookup"><span data-stu-id="49be6-146">An alpha value of NaN (Not a Number) results in a no coverage (zero) mask.</span></span>

<span data-ttu-id="49be6-147">Die Alpha-zu-Abdeckung wird auch normalerweise für die Bildschirm-und türtransparenz verwendet, oder es werden ausführliche Silhouetten für anderweitig nicht transparente Sprites definiert.</span><span class="sxs-lookup"><span data-stu-id="49be6-147">Alpha-to-coverage is also traditionally used for screen-door transparency or defining detailed silhouettes for otherwise opaque sprites.</span></span>

### <a name="blending-pixel-shader-outputs"></a><span data-ttu-id="49be6-148">Mischen von Pixel-Shader-Ausgaben</span><span class="sxs-lookup"><span data-stu-id="49be6-148">Blending Pixel Shader Outputs</span></span>

<span data-ttu-id="49be6-149">Diese Funktion ermöglicht der Ausgabe Zusammenführung, beide Pixel-Shader-Ausgaben gleichzeitig als Eingabe Quellen für einen Mischungs Vorgang mit dem einzelnen Renderziel an Slot 0 zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="49be6-149">This feature enables the output merger to use both the pixel shader outputs simultaneously as input sources to a blending operation with the single render target at slot 0.</span></span>

<span data-ttu-id="49be6-150">In diesem Beispiel werden zwei Ergebnisse angenommen und in einem einzigen Durchlauf kombiniert. dabei wird ein Array mit einer Multiplikation und der andere mit einem Add-in das Ziel gemischt:</span><span class="sxs-lookup"><span data-stu-id="49be6-150">This example takes two results and combines them in a single pass, blending one into the destination with a multiply and the other with an add:</span></span>


```
SrcBlend = D3D11_BLEND_ONE;
DestBlend = D3D11_BLEND_SRC1_COLOR;
```



<span data-ttu-id="49be6-151">In diesem Beispiel wird die erste Pixel-Shader-Ausgabe als Quellfarbe und die zweite Ausgabe als Farbkomponenten-Blend Faktor pro Farbe konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="49be6-151">This example configures the first pixel shader output as the source color and the second output as a per-color component blend factor.</span></span>


```
SrcBlend = D3D11_BLEND_SRC1_COLOR;
DestBlend = D3D11_BLEND_INV_SRC1_COLOR;
```



<span data-ttu-id="49be6-152">In diesem Beispiel wird veranschaulicht, wie die Blend-Faktoren den Shader-wischen entsprechen müssen:</span><span class="sxs-lookup"><span data-stu-id="49be6-152">This example illustrates how the blend factors must match the shader swizzles:</span></span>


```
SrcFactor = D3D11_BLEND_SRC1_ALPHA;
DestFactor = D3D11_BLEND_SRC_COLOR;
OutputWriteMask[0] = .ra; // pseudocode for setting the mask at
                          // RenderTarget slot 0 to .ra
```



<span data-ttu-id="49be6-153">Die Blend-Faktoren und der Shader-Code implizieren miteinander, dass der Pixelshader mindestens o0. r und o1. a ausgeben muss.</span><span class="sxs-lookup"><span data-stu-id="49be6-153">Together, the blend factors and the shader code imply that the pixel shader is required to output at least o0.r and o1.a.</span></span> <span data-ttu-id="49be6-154">Zusätzliche Ausgabe Komponenten können vom Shader ausgegeben werden, werden jedoch ignoriert, aber weniger Komponenten würden nicht definierte Ergebnisse verursachen.</span><span class="sxs-lookup"><span data-stu-id="49be6-154">Extra output components can be output by the shader but would be ignored, fewer components would produce undefined results.</span></span>

## <a name="related-topics"></a><span data-ttu-id="49be6-155">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="49be6-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49be6-156">Ausgabe-Fusion-Phase</span><span class="sxs-lookup"><span data-stu-id="49be6-156">Output-Merger Stage</span></span>](d3d10-graphics-programming-guide-output-merger-stage.md)
</dt> <dt>

[<span data-ttu-id="49be6-157">Pipeline Stufen (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="49be6-157">Pipeline Stages (Direct3D 10)</span></span>](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

 