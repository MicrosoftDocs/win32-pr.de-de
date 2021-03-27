---
title: Konfigurieren von Depth-Stencil Funktionen
description: In diesem Abschnitt werden die Schritte zum Einrichten des tiefen Schablone-Puffers und der Status der tiefen Schablone für die Ausgabe-Fusion-Phase behandelt.
ms.assetid: e8f52d5f-266f-4e2c-b38d-d7fd9e27fe1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65bf48b0ba9a782be25568ac3fc0569314dae76e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728744"
---
# <a name="configuring-depth-stencil-functionality"></a><span data-ttu-id="4fe0f-103">Konfigurieren von Depth-Stencil Funktionen</span><span class="sxs-lookup"><span data-stu-id="4fe0f-103">Configuring Depth-Stencil Functionality</span></span>

<span data-ttu-id="4fe0f-104">In diesem Abschnitt werden die Schritte zum Einrichten des tiefen Schablone-Puffers und der Status der tiefen Schablone für die Ausgabe-Fusion-Phase behandelt.</span><span class="sxs-lookup"><span data-stu-id="4fe0f-104">This section covers the steps for setting up the depth-stencil buffer, and depth-stencil state for the output-merger stage.</span></span>

-   [<span data-ttu-id="4fe0f-105">Erstellen einer Depth-Stencil Ressource</span><span class="sxs-lookup"><span data-stu-id="4fe0f-105">Create a Depth-Stencil Resource</span></span>](#create-a-depth-stencil-resource)
-   [<span data-ttu-id="4fe0f-106">Depth-Stencil Zustand erstellen</span><span class="sxs-lookup"><span data-stu-id="4fe0f-106">Create Depth-Stencil State</span></span>](#create-depth-stencil-state)
-   [<span data-ttu-id="4fe0f-107">Binden von Depth-Stencil Daten an die OM-Phase</span><span class="sxs-lookup"><span data-stu-id="4fe0f-107">Bind Depth-Stencil Data to the OM Stage</span></span>](#bind-depth-stencil-data-to-the-om-stage)

<span data-ttu-id="4fe0f-108">Wenn Sie wissen, wie Sie den tiefen Schablone-Puffer und den entsprechenden Status der tiefen Schablone verwenden, finden Sie weitere Informationen unter [Advanced-Stencil-Techniken](#advanced-stencil-techniques).</span><span class="sxs-lookup"><span data-stu-id="4fe0f-108">Once you know how to use the depth-stencil buffer and the corresponding depth-stencil state, refer to [advanced-stencil techniques](#advanced-stencil-techniques).</span></span>

## <a name="create-a-depth-stencil-resource"></a><span data-ttu-id="4fe0f-109">Erstellen einer Depth-Stencil Ressource</span><span class="sxs-lookup"><span data-stu-id="4fe0f-109">Create a Depth-Stencil Resource</span></span>

<span data-ttu-id="4fe0f-110">Erstellen Sie den tiefen Schablonen Puffer mithilfe einer Textur Ressource.</span><span class="sxs-lookup"><span data-stu-id="4fe0f-110">Create the depth-stencil buffer using a texture resource.</span></span>


```
ID3D11Texture2D* pDepthStencil = NULL;
D3D11_TEXTURE2D_DESC descDepth;
descDepth.Width = backBufferSurfaceDesc.Width;
descDepth.Height = backBufferSurfaceDesc.Height;
descDepth.MipLevels = 1;
descDepth.ArraySize = 1;
descDepth.Format = pDeviceSettings->d3d11.AutoDepthStencilFormat;
descDepth.SampleDesc.Count = 1;
descDepth.SampleDesc.Quality = 0;
descDepth.Usage = D3D11_USAGE_DEFAULT;
descDepth.BindFlags = D3D11_BIND_DEPTH_STENCIL;
descDepth.CPUAccessFlags = 0;
descDepth.MiscFlags = 0;
hr = pd3dDevice->CreateTexture2D( &descDepth, NULL, &pDepthStencil );
```



## <a name="create-depth-stencil-state"></a><span data-ttu-id="4fe0f-111">Depth-Stencil Zustand erstellen</span><span class="sxs-lookup"><span data-stu-id="4fe0f-111">Create Depth-Stencil State</span></span>

<span data-ttu-id="4fe0f-112">Der Status der tiefen Schablone teilt der Ausgabe-Fusion-Phase mit, wie der [tiefen Schablonen Test](d3d10-graphics-programming-guide-output-merger-stage.md)durchgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4fe0f-112">The depth-stencil state tells the output-merger stage how to perform the [depth-stencil test](d3d10-graphics-programming-guide-output-merger-stage.md).</span></span> <span data-ttu-id="4fe0f-113">Der tiefen Schablone-Test bestimmt, ob ein bestimmtes Pixel gezeichnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4fe0f-113">The depth-stencil test determines whether or not a given pixel should be drawn.</span></span>


```
D3D11_DEPTH_STENCIL_DESC dsDesc;

// Depth test parameters
dsDesc.DepthEnable = true;
dsDesc.DepthWriteMask = D3D11_DEPTH_WRITE_MASK_ALL;
dsDesc.DepthFunc = D3D11_COMPARISON_LESS;

// Stencil test parameters
dsDesc.StencilEnable = true;
dsDesc.StencilReadMask = 0xFF;
dsDesc.StencilWriteMask = 0xFF;

// Stencil operations if pixel is front-facing
dsDesc.FrontFace.StencilFailOp = D3D11_STENCIL_OP_KEEP;
dsDesc.FrontFace.StencilDepthFailOp = D3D11_STENCIL_OP_INCR;
dsDesc.FrontFace.StencilPassOp = D3D11_STENCIL_OP_KEEP;
dsDesc.FrontFace.StencilFunc = D3D11_COMPARISON_ALWAYS;

// Stencil operations if pixel is back-facing
dsDesc.BackFace.StencilFailOp = D3D11_STENCIL_OP_KEEP;
dsDesc.BackFace.StencilDepthFailOp = D3D11_STENCIL_OP_DECR;
dsDesc.BackFace.StencilPassOp = D3D11_STENCIL_OP_KEEP;
dsDesc.BackFace.StencilFunc = D3D11_COMPARISON_ALWAYS;

// Create depth stencil state
ID3D11DepthStencilState * pDSState;
pd3dDevice->CreateDepthStencilState(&dsDesc, &pDSState);
```



<span data-ttu-id="4fe0f-114">Depthenable und stencilenable aktivieren (und deaktivieren) tiefen-und Schablonen Tests.</span><span class="sxs-lookup"><span data-stu-id="4fe0f-114">DepthEnable and StencilEnable enable (and disable) depth and stencil testing.</span></span> <span data-ttu-id="4fe0f-115">Legen Sie depthenable auf **false** fest, um tiefen Tests zu deaktivieren und das Schreiben in den tiefen Puffer zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="4fe0f-115">Set DepthEnable to **FALSE** to disable depth testing and prevent writing to the depth buffer.</span></span> <span data-ttu-id="4fe0f-116">Legen Sie "Schablone" auf " **false** " fest, um Schablonen Tests zu deaktivieren und das Schreiben in den Schablonen Puffer zu verhindern (wenn "depthenable" den Wert " **false** " hat und "stencilenable" den Wert " **true**" hat, wird der tiefen Test immer in der Schablone</span><span class="sxs-lookup"><span data-stu-id="4fe0f-116">Set StencilEnable to **FALSE** to disable stencil testing and prevent writing to the stencil buffer (when DepthEnable is **FALSE** and StencilEnable is **TRUE**, the depth test always passes in the stencil operation).</span></span>

<span data-ttu-id="4fe0f-117">Depthenable wirkt sich nur auf die Ausgabe-Fusion-Phase aus. es wirkt sich nicht auf das Abschneiden, die tiefen Verschiebung oder das Festlegen von Werten aus, bevor die Daten in einen PixelShader eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4fe0f-117">DepthEnable only affects the output-merger stage - it does not affect clipping, depth bias, or clamping of values before the data is input to a pixel shader.</span></span>

## <a name="bind-depth-stencil-data-to-the-om-stage"></a><span data-ttu-id="4fe0f-118">Binden von Depth-Stencil Daten an die OM-Phase</span><span class="sxs-lookup"><span data-stu-id="4fe0f-118">Bind Depth-Stencil Data to the OM Stage</span></span>

<span data-ttu-id="4fe0f-119">Binden Sie den Status der tiefen Schablone.</span><span class="sxs-lookup"><span data-stu-id="4fe0f-119">Bind the depth-stencil state.</span></span>


```
// Bind depth stencil state
pDevice->OMSetDepthStencilState(pDSState, 1);
```



<span data-ttu-id="4fe0f-120">Binden Sie die Tiefe der tiefen Schablone mithilfe einer Ansicht.</span><span class="sxs-lookup"><span data-stu-id="4fe0f-120">Bind the depth-stencil resource using a view.</span></span>


```
D3D11_DEPTH_STENCIL_VIEW_DESC descDSV;
descDSV.Format = DXGI_FORMAT_D32_FLOAT_S8X24_UINT;
descDSV.ViewDimension = D3D11_DSV_DIMENSION_TEXTURE2D;
descDSV.Texture2D.MipSlice = 0;

// Create the depth stencil view
ID3D11DepthStencilView* pDSV;
hr = pd3dDevice->CreateDepthStencilView( pDepthStencil, // Depth stencil texture
                                         &descDSV, // Depth stencil desc
                                         &pDSV );  // [out] Depth stencil view

// Bind the depth stencil view
pd3dDeviceContext->OMSetRenderTargets( 1,          // One rendertarget view
                                &pRTV,      // Render target view, created earlier
                                pDSV );     // Depth stencil view for the render target
```



<span data-ttu-id="4fe0f-121">Ein Array von renderzielsichten kann an [**Verknüpfung id3d11devicecontext aus:: omantrendertargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargets)übermittelt werden. alle renderzielsichten entsprechen jedoch einer einzelnen Ansicht der tiefen Schablone.</span><span class="sxs-lookup"><span data-stu-id="4fe0f-121">An array of render-target views may be passed into [**ID3D11DeviceContext::OMSetRenderTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargets), however all of those render-target views will correspond to a single depth stencil view.</span></span> <span data-ttu-id="4fe0f-122">Das renderzielarray in Direct3D 11 ist eine Funktion, die es einer Anwendung ermöglicht, auf mehreren Renderingzielen gleichzeitig auf primitiver Ebene zu renderzielen.</span><span class="sxs-lookup"><span data-stu-id="4fe0f-122">The render target array in Direct3D 11 is a feature that enables an application to render onto multiple render targets simultaneously at the primitive level.</span></span> <span data-ttu-id="4fe0f-123">Renderzielarrays bieten eine bessere Leistung im Vergleich zur individuellen Festlegung von renderzielen mit mehreren Aufrufen von **Verknüpfung id3d11devicecontext aus:: omsetrendertargets** (im Wesentlichen die Methode, die in Direct3D 9 verwendet wird).</span><span class="sxs-lookup"><span data-stu-id="4fe0f-123">Render target arrays offer increased performance over individually setting render targets with multiple calls to **ID3D11DeviceContext::OMSetRenderTargets** (essentially the method employed in Direct3D 9).</span></span>

<span data-ttu-id="4fe0f-124">Renderziele müssen alle den gleichen Ressourcentyp aufweisen.</span><span class="sxs-lookup"><span data-stu-id="4fe0f-124">Render targets must all be the same type of resource.</span></span> <span data-ttu-id="4fe0f-125">Wenn Multisampling-Antialiasing verwendet wird, müssen alle gebundenen Renderingziele und tiefen Puffer dieselbe Stichproben Anzahl aufweisen.</span><span class="sxs-lookup"><span data-stu-id="4fe0f-125">If multisample antialiasing is used, all bound render targets and depth buffers must have the same sample counts.</span></span>

<span data-ttu-id="4fe0f-126">Wenn ein Puffer als Renderziel verwendet wird, werden tiefen Schablonen Tests und mehrere Renderingziele nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4fe0f-126">When a buffer is used as a render target, depth-stencil testing and multiple render targets are not supported.</span></span>

-   <span data-ttu-id="4fe0f-127">Bis zu 8 Renderziele können gleichzeitig gebunden werden.</span><span class="sxs-lookup"><span data-stu-id="4fe0f-127">As many as 8 render targets can be bound simultaneously.</span></span>
-   <span data-ttu-id="4fe0f-128">Alle Renderziele müssen in allen Dimensionen (Breite und Höhe) und Tiefe für die 3D-oder Array Größe für Array Typen die gleiche Größe aufweisen \* .</span><span class="sxs-lookup"><span data-stu-id="4fe0f-128">All render targets must have the same size in all dimensions (width and height, and depth for 3D or array size for \*Array types).</span></span>
-   <span data-ttu-id="4fe0f-129">Jedes Renderziel weist möglicherweise ein anderes Datenformat auf.</span><span class="sxs-lookup"><span data-stu-id="4fe0f-129">Each render target may have a different data format.</span></span>
-   <span data-ttu-id="4fe0f-130">Schreib Masken steuern, welche Daten in ein Renderziel geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="4fe0f-130">Write masks control what data gets written to a render target.</span></span> <span data-ttu-id="4fe0f-131">Mit dem Ausgabe Schreibvorgang werden Masken Steuerelemente für ein pro-Renderziel und jede Komponentenebene geschrieben, welche Daten in die Renderziele geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="4fe0f-131">The output write masks control on a per-render target, per-component level what data gets written to the render target(s).</span></span>

## <a name="advanced-stencil-techniques"></a><span data-ttu-id="4fe0f-132">Erweiterte Schablonen Techniken</span><span class="sxs-lookup"><span data-stu-id="4fe0f-132">Advanced Stencil Techniques</span></span>

<span data-ttu-id="4fe0f-133">Der Schablone-Teil des tiefen Schablonen Puffers kann zum Erstellen von renderingeffekten wie zusammensetzen, herabstufen und Gliederung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4fe0f-133">The stencil portion of the depth-stencil buffer can be used for creating rendering effects such as compositing, decaling, and outlining.</span></span>

-   [<span data-ttu-id="4fe0f-134">Zusammensetzung</span><span class="sxs-lookup"><span data-stu-id="4fe0f-134">Compositing</span></span>](#compositing)
-   [<span data-ttu-id="4fe0f-135">Wird abgebrochen</span><span class="sxs-lookup"><span data-stu-id="4fe0f-135">Decaling</span></span>](#decaling)
-   [<span data-ttu-id="4fe0f-136">Kontur und Silhouetten</span><span class="sxs-lookup"><span data-stu-id="4fe0f-136">Outlines and Silhouettes</span></span>](#outlines-and-silhouettes)
-   [<span data-ttu-id="4fe0f-137">Zweiseitige Schablone</span><span class="sxs-lookup"><span data-stu-id="4fe0f-137">Two-Sided Stencil</span></span>](#two-sided-stencil)
-   [<span data-ttu-id="4fe0f-138">Lesen des Depth-Stencil Puffers als Textur</span><span class="sxs-lookup"><span data-stu-id="4fe0f-138">Reading the Depth-Stencil Buffer as a Texture</span></span>](#reading-the-depth-stencil-buffer-as-a-texture)

### <a name="compositing"></a><span data-ttu-id="4fe0f-139">Zusammensetzung</span><span class="sxs-lookup"><span data-stu-id="4fe0f-139">Compositing</span></span>

<span data-ttu-id="4fe0f-140">Die Anwendung kann mit dem Schablonen Puffer 2D-oder 3D-Bilder in eine 3D-Szene zusammensetzen.</span><span class="sxs-lookup"><span data-stu-id="4fe0f-140">Your application can use the stencil buffer to composite 2D or 3D images onto a 3D scene.</span></span> <span data-ttu-id="4fe0f-141">Eine Maske im Schablone-Puffer wird verwendet, um einen Bereich der Renderingzieloberfläche zu okzieren.</span><span class="sxs-lookup"><span data-stu-id="4fe0f-141">A mask in the stencil buffer is used to occlude an area of the rendering target surface.</span></span> <span data-ttu-id="4fe0f-142">Gespeicherte 2D-Informationen, wie z. b. Text oder Bitmaps, können dann in den Bereich "okded" geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="4fe0f-142">Stored 2D information, such as text or bitmaps, can then be written to the occluded area.</span></span> <span data-ttu-id="4fe0f-143">Alternativ kann die Anwendung zusätzliche 3D-primitive in den mit der Schablone maskierten Bereich der Renderingzieloberfläche rendern.</span><span class="sxs-lookup"><span data-stu-id="4fe0f-143">Alternately, your application can render additional 3D primitives to the stencil-masked region of the rendering target surface.</span></span> <span data-ttu-id="4fe0f-144">Sie kann sogar eine ganze Szene darstellen.</span><span class="sxs-lookup"><span data-stu-id="4fe0f-144">It can even render an entire scene.</span></span>

<span data-ttu-id="4fe0f-145">Spiele sind häufig mehrere 3D-Szenen zusammengesetzt.</span><span class="sxs-lookup"><span data-stu-id="4fe0f-145">Games often composite multiple 3D scenes together.</span></span> <span data-ttu-id="4fe0f-146">Beispielsweise wird bei Fahr spielen in der Regel eine Spiegelung der Rückseite angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4fe0f-146">For instance, driving games typically display a rear-view mirror.</span></span> <span data-ttu-id="4fe0f-147">Die Spiegel Datenbank enthält die Ansicht der 3D-Szene hinter dem Treiber.</span><span class="sxs-lookup"><span data-stu-id="4fe0f-147">The mirror contains the view of the 3D scene behind the driver.</span></span> <span data-ttu-id="4fe0f-148">Es handelt sich im Wesentlichen um eine zweite 3D-Szene, die mit der vorwärts Ansicht des Treibers zusammengesetzt wird</span><span class="sxs-lookup"><span data-stu-id="4fe0f-148">It is essentially a second 3D scene composited with the driver's forward view.</span></span>

### <a name="decaling"></a><span data-ttu-id="4fe0f-149">Wird abgebrochen</span><span class="sxs-lookup"><span data-stu-id="4fe0f-149">Decaling</span></span>

<span data-ttu-id="4fe0f-150">Direct3D-Anwendungen verwenden die-Verwendung, um zu steuern, welche Pixel von einem bestimmten primitiven Bild auf die Renderingzieloberfläche gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="4fe0f-150">Direct3D applications use decaling to control which pixels from a particular primitive image are drawn to the rendering target surface.</span></span> <span data-ttu-id="4fe0f-151">Anwendungen wenden die Abbilder von primitiven an, damit Coplanar-Polygone ordnungsgemäß wieder hergestellt werden können.</span><span class="sxs-lookup"><span data-stu-id="4fe0f-151">Applications apply decals to the images of primitives to enable coplanar polygons to render correctly.</span></span>

<span data-ttu-id="4fe0f-152">Wenn beispielsweise Reifen Markierungen und gelbe Linien auf eine Straßenebene angewendet werden, sollten die Markierungen direkt auf der Straße angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="4fe0f-152">For instance, when applying tire marks and yellow lines to a roadway, the markings should appear directly on top of the road.</span></span> <span data-ttu-id="4fe0f-153">Die z-Werte der Markierungen und der Straße sind jedoch identisch.</span><span class="sxs-lookup"><span data-stu-id="4fe0f-153">However, the z values of the markings and the road are the same.</span></span> <span data-ttu-id="4fe0f-154">Daher erzeugt der tiefen Puffer möglicherweise keine saubere Trennung zwischen den beiden.</span><span class="sxs-lookup"><span data-stu-id="4fe0f-154">Therefore, the depth buffer might not produce a clean separation between the two.</span></span> <span data-ttu-id="4fe0f-155">Einige Pixel im Hintergrundtyp können über dem Front-primitiv und umgekehrt gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="4fe0f-155">Some pixels in the back primitive may be rendered on top of the front primitive and vice versa.</span></span> <span data-ttu-id="4fe0f-156">Das resultierende Bild wird angezeigt, um von Frame zu Rahmen zu vershicheln.</span><span class="sxs-lookup"><span data-stu-id="4fe0f-156">The resulting image appears to shimmer from frame to frame.</span></span> <span data-ttu-id="4fe0f-157">Dieser Effekt heißt z-Fighting oder Flimmern.</span><span class="sxs-lookup"><span data-stu-id="4fe0f-157">This effect is called z-fighting or flimmering.</span></span>

<span data-ttu-id="4fe0f-158">Um dieses Problem zu beheben, verwenden Sie eine Schablone, um den Abschnitt des hintergrundprimitivs zu maskieren, in dem die Client Zugriffslizenz angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="4fe0f-158">To solve this problem, use a stencil to mask the section of the back primitive where the decal will appear.</span></span> <span data-ttu-id="4fe0f-159">Deaktivieren Sie die z-Pufferung, und Renderern Sie das Bild des Front-Primitivs in den maskierten Bereich der Renderziel-Oberfläche.</span><span class="sxs-lookup"><span data-stu-id="4fe0f-159">Turn off z-buffering and render the image of the front primitive into the masked-off area of the render-target surface.</span></span>

<span data-ttu-id="4fe0f-160">Zum lösen dieses Problems können mehrere Textur Mischungs Möglichkeiten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4fe0f-160">Multiple texture blending can be used to solve this problem.</span></span>

### <a name="outlines-and-silhouettes"></a><span data-ttu-id="4fe0f-161">Kontur und Silhouetten</span><span class="sxs-lookup"><span data-stu-id="4fe0f-161">Outlines and Silhouettes</span></span>

<span data-ttu-id="4fe0f-162">Sie können den Schablonen Puffer für abstraktere Effekte verwenden, z. b. Gliederung und Silhouette.</span><span class="sxs-lookup"><span data-stu-id="4fe0f-162">You can use the stencil buffer for more abstract effects, such as outlining and silhouetting.</span></span>

<span data-ttu-id="4fe0f-163">Wenn die Anwendung zwei Renderungs Ergebnisse übergibt: eine zum Generieren der Schablonen Maske und eine zweite, um die Schablonen Maske auf das Bild anzuwenden, aber mit den primitiven, die im zweiten Durchlauf etwas kleiner sind, enthält das resultierende Bild nur den Umriss des primitiven.</span><span class="sxs-lookup"><span data-stu-id="4fe0f-163">If your application does two render passes - one to generate the stencil mask and second to apply the stencil mask to the image, but with the primitives slightly smaller on the second pass - the resulting image will contain only the primitive's outline.</span></span> <span data-ttu-id="4fe0f-164">Die Anwendung kann dann den Bereich der Schablone maskiert mit einer voll Tonfarbe ausfüllen, wodurch dem primitiven ein geprägte Bild angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="4fe0f-164">The application can then fill the stencil-masked area of the image with a solid color, giving the primitive an embossed look.</span></span>

<span data-ttu-id="4fe0f-165">Wenn die Schablone-Maske dieselbe Größe und Form wie das primitive-Format aufweist, das Sie rendern, enthält das resultierende Bild eine Lücke, in der der primitive entsprechen sollte.</span><span class="sxs-lookup"><span data-stu-id="4fe0f-165">If the stencil mask is the same size and shape as the primitive you are rendering, the resulting image contains a hole where the primitive should be.</span></span> <span data-ttu-id="4fe0f-166">Die Anwendung kann dann das Loch mit Black auffüllen, um eine Silhouette des primitiven zu schaffen.</span><span class="sxs-lookup"><span data-stu-id="4fe0f-166">Your application can then fill the hole with black to produce a silhouette of the primitive.</span></span>

### <a name="two-sided-stencil"></a><span data-ttu-id="4fe0f-167">Two-Sided Schablone</span><span class="sxs-lookup"><span data-stu-id="4fe0f-167">Two-Sided Stencil</span></span>

<span data-ttu-id="4fe0f-168">Schattenvolumes werden zum Zeichnen von Schatten mit dem Schablonen Puffer verwendet.</span><span class="sxs-lookup"><span data-stu-id="4fe0f-168">Shadow Volumes are used for drawing shadows with the stencil buffer.</span></span> <span data-ttu-id="4fe0f-169">Die Anwendung berechnet die schattenvolumes, die durch die Schattierung von Geometrie umgewandelt werden, indem die Silhouette-Kanten berechnet und vom Licht in eine Gruppe von 3D-Volumes aufgeteilt werden.</span><span class="sxs-lookup"><span data-stu-id="4fe0f-169">The application computes the shadow volumes cast by occluding geometry, by computing the silhouette edges and extruding them away from the light into a set of 3D volumes.</span></span> <span data-ttu-id="4fe0f-170">Diese Volumes werden dann zweimal im Schablonen Puffer gerendert.</span><span class="sxs-lookup"><span data-stu-id="4fe0f-170">These volumes are then rendered twice into the stencil buffer.</span></span>

<span data-ttu-id="4fe0f-171">Das erste Rendering zeichnet nach vorne gerichtete Polygone und erhöht die Schablonen Puffer Werte.</span><span class="sxs-lookup"><span data-stu-id="4fe0f-171">The first render draws forward-facing polygons, and increments the stencil-buffer values.</span></span> <span data-ttu-id="4fe0f-172">Das zweite Rendering zeichnet die rückwärts gerichteten Polygone des Schatten Volumens und Dekremente die Schablonen Puffer Werte.</span><span class="sxs-lookup"><span data-stu-id="4fe0f-172">The second render draws the back-facing polygons of the shadow volume, and decrements the stencil buffer values.</span></span> <span data-ttu-id="4fe0f-173">Normalerweise brechen alle inkrementierten und dekrementierten Werte einander ab. Die Szene wurde jedoch bereits mit normaler Geometrie gerendert, sodass einige Pixel den z-Puffer-Test nicht bestanden haben, während das Schatten Volume gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="4fe0f-173">Normally, all incremented and decremented values cancel each other out. However, the scene was already rendered with normal geometry causing some pixels to fail the z-buffer test as the shadow volume is rendered.</span></span> <span data-ttu-id="4fe0f-174">Werte, die im Schablonen Puffer verbleiben, entsprechen den im Schatten entsprechenden Pixeln.</span><span class="sxs-lookup"><span data-stu-id="4fe0f-174">Values left in the stencil buffer correspond to pixels that are in the shadow.</span></span> <span data-ttu-id="4fe0f-175">Diese verbleibenden Schablone-Puffer Inhalte werden als Maske verwendet, um einen großen, umfassenden, vier Vierfache in die Szene zu mischen.</span><span class="sxs-lookup"><span data-stu-id="4fe0f-175">These remaining stencil-buffer contents are used as a mask, to alpha-blend a large, all-encompassing black quad into the scene.</span></span> <span data-ttu-id="4fe0f-176">Wenn der Schablone-Puffer als Maske fungiert, besteht das Ergebnis darin, die Pixel in den Schatten zu verbergen.</span><span class="sxs-lookup"><span data-stu-id="4fe0f-176">With the stencil buffer acting as a mask, the result is to darken pixels that are in the shadows.</span></span>

<span data-ttu-id="4fe0f-177">Dies bedeutet, dass die Schatten Geometrie zweimal pro Lichtquelle gezeichnet wird und somit den Scheitelpunkt Durchsatz der GPU erhöht.</span><span class="sxs-lookup"><span data-stu-id="4fe0f-177">This means that the shadow geometry is drawn twice per light source, hence putting pressure on the vertex throughput of the GPU.</span></span> <span data-ttu-id="4fe0f-178">Das zweiseitige Schablonen Feature wurde entwickelt, um diese Situation zu mindern.</span><span class="sxs-lookup"><span data-stu-id="4fe0f-178">The two-sided stencil feature has been designed to mitigate this situation.</span></span> <span data-ttu-id="4fe0f-179">Bei dieser Vorgehensweise gibt es zwei Sätze von Schablone State (unten genannt), jeweils eine Menge für die Vorder-und die andere für die mit der Rückseite gerichteten Dreiecke.</span><span class="sxs-lookup"><span data-stu-id="4fe0f-179">In this approach, there are two sets of stencil state (named below), one set each for the front-facing triangles and the other for the back-facing triangles.</span></span> <span data-ttu-id="4fe0f-180">Auf diese Weise wird nur ein einzelner Durchlauf pro Schatten Volume pro Licht gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="4fe0f-180">This way, only a single pass is drawn per shadow volume, per light.</span></span>

<span data-ttu-id="4fe0f-181">Ein Beispiel für die zweiseitige Schablonen Implementierung finden Sie im [ShadowVolume10](https://msdn.microsoft.com/library/Ee416427(v=VS.85).aspx)-Beispiel.</span><span class="sxs-lookup"><span data-stu-id="4fe0f-181">An example of two-sided stencil implementation can be found in the [ShadowVolume10 Sample](https://msdn.microsoft.com/library/Ee416427(v=VS.85).aspx).</span></span>

### <a name="reading-the-depth-stencil-buffer-as-a-texture"></a><span data-ttu-id="4fe0f-182">Lesen des Depth-Stencil Puffers als Textur</span><span class="sxs-lookup"><span data-stu-id="4fe0f-182">Reading the Depth-Stencil Buffer as a Texture</span></span>

<span data-ttu-id="4fe0f-183">Ein inaktiver tiefen Schablone-Puffer kann von einem Shader als Textur gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="4fe0f-183">An inactive depth-stencil buffer can be read by a shader as a texture.</span></span> <span data-ttu-id="4fe0f-184">Eine Anwendung, die einen tiefen Schablone-Puffer liest, wenn eine Textur in zwei Durchläufen gerendert wird, wird der erste Pass in den tiefen Schablone-Puffer geschrieben, und der zweite Durchlauf liest aus dem Puffer.</span><span class="sxs-lookup"><span data-stu-id="4fe0f-184">An application that reads a depth-stencil buffer as a texture renders in two passes, the first pass writes to the depth-stencil buffer and the second pass reads from the buffer.</span></span> <span data-ttu-id="4fe0f-185">Dadurch kann ein Shader Tiefe-oder Schablonen Werte, die zuvor in den Puffer geschrieben wurden, mit dem Wert für das Pixel vergleichen, das in der Vergangenheit gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="4fe0f-185">This allows a shader to compare depth or stencil values previously written to the buffer against the value for the pixel currrently being rendered.</span></span> <span data-ttu-id="4fe0f-186">Das Ergebnis des Vergleichs kann verwendet werden, um Effekte wie z. b. eine Schatten Zuordnung oder weiche Partikel in einem Partikelsystem zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4fe0f-186">The result of the comparison can be used to create effects such as shadow mapping or soft particles in a particle system.</span></span>

<span data-ttu-id="4fe0f-187">Zum Erstellen eines tiefen Schablone-Puffers, der sowohl als tiefen Schablone als auch als Shaderressource verwendet werden kann, müssen einige Änderungen am Beispielcode im Abschnitt [Erstellen einer Depth-Stencil Ressource](#create-a-depth-stencil-resource) vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="4fe0f-187">To create a depth-stencil buffer that can be used as both a depth-stencil resource and a shader resource a few changes need to be made to sample code in the [Create a Depth-Stencil Resource](#create-a-depth-stencil-resource) section.</span></span>

-   <span data-ttu-id="4fe0f-188">Die tiefen Schablone-Ressource muss ein typloses Format aufweisen, wie z. b. das DXGI- \_ Format \_ R32 \_ typlose.</span><span class="sxs-lookup"><span data-stu-id="4fe0f-188">The depth-stencil resource must have a typeless format such as DXGI\_FORMAT\_R32\_TYPELESS.</span></span>
    ```
    descDepth.Format = DXGI_FORMAT_R32_TYPELESS;
    ```

    

-   <span data-ttu-id="4fe0f-189">Die tiefen Schablone-Ressource muss sowohl die d3d10 Bind- \_ \_ \_ und d3d10 \_ Bind- \_ Shader- \_ ressourcenbindungsflags verwenden.</span><span class="sxs-lookup"><span data-stu-id="4fe0f-189">The depth-stencil resource must use both the D3D10\_BIND\_DEPTH\_STENCIL and D3D10\_BIND\_SHADER\_RESOURCE bind flags.</span></span>
    ```
    descDepth.BindFlags = D3D10_BIND_DEPTH_STENCIL | D3D10_BIND_SHADER_RESOURCE;
    ```

    

<span data-ttu-id="4fe0f-190">Außerdem muss für den tiefen Puffer eine shaderressourcenansicht erstellt werden, die eine [**D3D11 \_ Shader- \_ Ressourcen \_ Ansicht \_**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc) (Debug-Struktur) und " [**ID3D11Device:: | ateshaderresourceview**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createshaderresourceview)" verwendet.</span><span class="sxs-lookup"><span data-stu-id="4fe0f-190">In addition a shader resource view needs to be created for the depth buffer using a [**D3D11\_SHADER\_RESOURCE\_VIEW\_DESC**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc) structure and [**ID3D11Device::CreateShaderResourceView**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createshaderresourceview).</span></span> <span data-ttu-id="4fe0f-191">Die Shader-Ressourcen Ansicht verwendet ein typisiertes Format, z. b. das **DXGI- \_ Format \_ R32 \_ float** , das dem typlosen Format entspricht, das beim Erstellen der tiefen Schablone-Ressource angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="4fe0f-191">The shader resource view will use a typed format such as **DXGI\_FORMAT\_R32\_FLOAT** that is the equivalent to the typeless format specified when the depth-stencil resource was created.</span></span>

<span data-ttu-id="4fe0f-192">Im ersten renderdurchlauf wird der tiefen Puffer gebunden, wie im Abschnitt [Binden von Depth-Stencil Daten an den OM-Stufen](#bind-depth-stencil-data-to-the-om-stage) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="4fe0f-192">In the first render pass the depth buffer is bound as described in the [Bind Depth-Stencil Data to the OM Stage](#bind-depth-stencil-data-to-the-om-stage) section.</span></span> <span data-ttu-id="4fe0f-193">Beachten Sie, dass das Format an die [**D3D11- \_ tiefen \_ Schablone \_ ansichtsansicht \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_view_desc). Das Format verwendet ein typisiertes Format, z. b. **DXGI- \_ Format \_ d32 \_ float**.</span><span class="sxs-lookup"><span data-stu-id="4fe0f-193">Note that the format passed to [**D3D11\_DEPTH\_STENCIL\_VIEW\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_view_desc).Format will use a typed format such as **DXGI\_FORMAT\_D32\_FLOAT**.</span></span> <span data-ttu-id="4fe0f-194">Nach dem ersten renderdurchlauf enthält der tiefen Puffer die tiefen Werte für die Szene.</span><span class="sxs-lookup"><span data-stu-id="4fe0f-194">After the first render pass the depth buffer will contain the depth values for the scene.</span></span>

<span data-ttu-id="4fe0f-195">Im zweiten Renderpass wird die [**Verknüpfung id3d11devicecontext aus:: omsetrendertargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargets) -Funktion verwendet, um die Ansicht der tiefen Schablone auf **null** oder eine andere Tiefe der tiefen Schablone festzulegen, und die Shader-Ressourcen Ansicht wird mithilfe von [**ID3D11EffectShaderResourceVariable:: setresource**](id3dx11effectshaderresourcevariable-setresource.md)an den Shader übergeben.</span><span class="sxs-lookup"><span data-stu-id="4fe0f-195">In the second render pass the [**ID3D11DeviceContext::OMSetRenderTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargets) function is used to set the depth-stencil view to **NULL** or a different depth-stencil resource and the shader resource view is passed to the shader using [**ID3D11EffectShaderResourceVariable::SetResource**](id3dx11effectshaderresourcevariable-setresource.md).</span></span> <span data-ttu-id="4fe0f-196">Dies ermöglicht es dem Shader, die tiefen Werte zu suchen, die im ersten Renderingdurchlauf berechnet wurden.</span><span class="sxs-lookup"><span data-stu-id="4fe0f-196">This allows the shader to look up the depth values calculated in the first rendering pass.</span></span> <span data-ttu-id="4fe0f-197">Beachten Sie, dass eine Transformation zum Abrufen von tiefen Werten angewendet werden muss, wenn sich die Sicht des ersten Renderpass von dem zweiten renderdurchlauf unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="4fe0f-197">Note that a transformation will need to be applied to retrieve depth values if the point of view of the first render pass is different from the second render pass.</span></span> <span data-ttu-id="4fe0f-198">Wenn z. b. eine schattenmappenmethode verwendet wird, wird der erste renderdurchlauf aus der Perspektive einer Lichtquelle geleitet, während der zweite renderdurchlauf aus der Perspektive des Viewers erfolgt.</span><span class="sxs-lookup"><span data-stu-id="4fe0f-198">For example, if a shadow mapping technique is being used the first render pass will be from the perspective of a light source while the second render pass will from the viewer's perspective.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4fe0f-199">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4fe0f-199">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4fe0f-200">Ausgabe-Fusion-Phase</span><span class="sxs-lookup"><span data-stu-id="4fe0f-200">Output-Merger Stage</span></span>](d3d10-graphics-programming-guide-output-merger-stage.md)
</dt> <dt>

[<span data-ttu-id="4fe0f-201">Pipeline Stufen (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="4fe0f-201">Pipeline Stages (Direct3D 10)</span></span>](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

 