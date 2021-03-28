---
title: Reihen folgen Ansichten für Rasterizer
description: Mithilfe geordneter Ansichten von Rasterizer (ROVs) kann der Pixel-Shader-Code UAV-Bindungen mit einer Deklaration markieren, die die normalen Anforderungen für die Reihenfolge der Ergebnisse der Grafik Pipeline für UAVs ändert.
ms.assetid: 7FCFCD28-E68D-4594-8879-937F57245507
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d891701aeaadd6f4474aeed8303d9b0046d1b656
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102082"
---
# <a name="rasterizer-order-views"></a><span data-ttu-id="50d69-103">Reihen folgen Ansichten für Rasterizer</span><span class="sxs-lookup"><span data-stu-id="50d69-103">Rasterizer Order Views</span></span>

<span data-ttu-id="50d69-104">Mithilfe geordneter Ansichten von Rasterizer (ROVs) kann der Pixel-Shader-Code UAV-Bindungen mit einer Deklaration markieren, die die normalen Anforderungen für die Reihenfolge der Ergebnisse der Grafik Pipeline für UAVs ändert.</span><span class="sxs-lookup"><span data-stu-id="50d69-104">Rasterizer ordered views (ROVs) allow pixel shader code to mark UAV bindings with a declaration that alters the normal requirements for the order of graphics pipeline results for UAVs.</span></span> <span data-ttu-id="50d69-105">Dadurch können OIT-Algorithmen (Order Independent Transparenz) funktionieren, die deutlich bessere renderingergebnisse bieten, wenn mehrere transparente Objekte in einer Ansicht aufeinander zueinander stehen.</span><span class="sxs-lookup"><span data-stu-id="50d69-105">This enables Order Independent Transparency (OIT) algorithms to work, which give much better rendering results when multiple transparent objects are in line with each other in a view.</span></span>

-   [<span data-ttu-id="50d69-106">Übersicht</span><span class="sxs-lookup"><span data-stu-id="50d69-106">Overview</span></span>](#overview)
-   [<span data-ttu-id="50d69-107">Implementierungsdetails</span><span class="sxs-lookup"><span data-stu-id="50d69-107">Implementation details</span></span>](#implementation-details)
-   [<span data-ttu-id="50d69-108">API-Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="50d69-108">API summary</span></span>](#api-summary)
-   [<span data-ttu-id="50d69-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="50d69-109">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="50d69-110">Übersicht</span><span class="sxs-lookup"><span data-stu-id="50d69-110">Overview</span></span>

<span data-ttu-id="50d69-111">Standard Grafik Pipelines haben möglicherweise Probleme mit der ordnungsgemäßen Zusammensetzung mehrerer Texturen, die Transparenz enthalten.</span><span class="sxs-lookup"><span data-stu-id="50d69-111">Standard graphics pipelines may have trouble correctly compositing together multiple textures that contain transparency.</span></span> <span data-ttu-id="50d69-112">Objekte wie z. b. Drahtzäune, Rauch, Feuer, Vegetation und farbige Glas verwenden Transparenz, um den gewünschten Effekt zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="50d69-112">Objects such as wire fences, smoke, fire, vegetation, and colored glass use transparency to get the desired effect.</span></span> <span data-ttu-id="50d69-113">Es treten Probleme auf, wenn mehrere Texturen, die Transparenz enthalten, aufeinander zueinander stehen (Feuer vor einem Fence vor einem Glasgebäude, das eine Vegetations enthält).</span><span class="sxs-lookup"><span data-stu-id="50d69-113">Problems arise when multiple textures that contain transparency are in line with each other (smoke in front of a fence in front of a glass building containing vegetation, as an example).</span></span> <span data-ttu-id="50d69-114">Mithilfe geordneter Ansichten (ROVs) für Rasterizer können die zugrunde liegenden OIT-Algorithmen die Features der Hardware verwenden, um die Transparenz Reihenfolge ordnungsgemäß aufzulösen.</span><span class="sxs-lookup"><span data-stu-id="50d69-114">Rasterizer ordered views (ROVs) enable the underlying OIT algorithms to use features of the hardware to try to resolve the transparency order correctly.</span></span> <span data-ttu-id="50d69-115">Transparenz wird vom Pixelshader behandelt.</span><span class="sxs-lookup"><span data-stu-id="50d69-115">Transparency is handled by the pixel shader.</span></span>

<span data-ttu-id="50d69-116">Mithilfe geordneter Ansichten von Rasterizer (ROVs) kann der Pixel-Shader-Code UAV-Bindungen mit einer Deklaration markieren, die die normalen Anforderungen für die Reihenfolge der Ergebnisse der Grafik Pipeline für UAVs ändert.</span><span class="sxs-lookup"><span data-stu-id="50d69-116">Rasterizer ordered views (ROVs) allow pixel shader code to mark UAV bindings with a declaration that alters the normal requirements for the order of graphics pipeline results for UAVs.</span></span>

<span data-ttu-id="50d69-117">ROVs garantieren die Reihenfolge von UAV-Zugriffen für beliebige Paare von überlappenden Pixelshader-aufrufen.</span><span class="sxs-lookup"><span data-stu-id="50d69-117">ROVs guarantee the order of UAV accesses for any pair of overlapping pixel shader invocations.</span></span> <span data-ttu-id="50d69-118">In diesem Fall bedeutet "überlappende", dass die Aufrufe von denselben zeichnen-aufrufen generiert werden und die gleiche Pixel Koordinate gemeinsam verwenden, wenn der Ausführungs Modus für die Pixelfrequenz und das gleiche Pixel und die gleiche Stichproben Koordinate im Modus für die Stichproben Häufigkeit ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="50d69-118">In this case “overlapping” means that the invocations are generated by the same draw calls and share the same pixel coordinate when in pixel-frequency execution mode, and the same pixel and sample coordinate in sample-frequency mode.</span></span>

<span data-ttu-id="50d69-119">Die Reihenfolge, in der sich überlappende Rows-Zugriffe von pixelshaderaufrufen ausführen, ist mit der Reihenfolge identisch, in der die Geometrie übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="50d69-119">The order in which overlapping ROV accesses of pixel shader invocations are executed is identical to the order in which the geometry is submitted.</span></span> <span data-ttu-id="50d69-120">Dies bedeutet, dass bei überlappenden Pixelshader-aufrufen die von einem Pixelshader-Aufruf ausgeführten Rows-Schreibvorgänge verfügbar sein müssen, um von einem nachfolgenden Aufruf gelesen zu werden, und keine Auswirkungen auf Lesevorgänge durch einen vorherigen Aufruf haben dürfen.</span><span class="sxs-lookup"><span data-stu-id="50d69-120">This means that, for overlapping pixel shader invocations, ROV writes performed by a pixel shader invocation must be available to be read by a subsequent invocation and must not affect reads by a previous invocation.</span></span> <span data-ttu-id="50d69-121">Von einem Pixelshader-Aufruf ausgeführte Row-Lesevorgänge müssen Schreibvorgänge durch einen vorherigen Aufruf widerspiegeln und dürfen keine Schreibvorgänge durch einen nachfolgenden Aufruf widerspiegeln.</span><span class="sxs-lookup"><span data-stu-id="50d69-121">ROV reads performed by a pixel shader invocation must reflect writes by a previous invocation and must not reflect writes by a subsequent invocation.</span></span> <span data-ttu-id="50d69-122">Dies ist für UAVs wichtig, da Sie explizit aus den in der Ausgabe Invarianz Garantie ausgelassenen Garantien weggelassen werden, die normalerweise durch die festgelegte Reihenfolge der Ergebnisse der Grafik Pipeline</span><span class="sxs-lookup"><span data-stu-id="50d69-122">This is important for UAVs because they are explicitly omitted from the output-invariance guarantees normally set by the fixed order of graphics pipeline results.</span></span>

## <a name="implementation-details"></a><span data-ttu-id="50d69-123">Details zur Implementierung</span><span class="sxs-lookup"><span data-stu-id="50d69-123">Implementation details</span></span>

<span data-ttu-id="50d69-124">Rasterizer-geordnete Sichten (ROVs) werden mit den folgenden neuen HLSL-Objekten (High Level Shader Language) deklariert und sind nur für den Pixelshader verfügbar:</span><span class="sxs-lookup"><span data-stu-id="50d69-124">Rasterizer ordered views (ROVs) are declared with the following new High Level Shader Language (HLSL) objects, and are only available to the pixel shader:</span></span>

-   `RasterizerOrderedBuffer`
-   `RasterizerOrderedByteAddressBuffer`
-   `RasterizerOrderedStructuredBuffer`
-   `RasterizerOrderedTexture1D`
-   `RasterizerOrderedTexture1DArray`
-   `RasterizerOrderedTexture2D`
-   `RasterizerOrderedTexture2DArray`
-   `RasterizerOrderedTexture3D`

<span data-ttu-id="50d69-125">Verwenden Sie diese Objekte auf die gleiche Weise wie andere UAV-Objekte (z. b `RWBuffer` . usw.).</span><span class="sxs-lookup"><span data-stu-id="50d69-125">Use these objects in the same manner as other UAV objects (such as `RWBuffer` etc.).</span></span>

## <a name="api-summary"></a><span data-ttu-id="50d69-126">API-Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="50d69-126">API summary</span></span>

<span data-ttu-id="50d69-127">ROVs sind ein nur-HLSL-Konstrukt, das unterschiedliche Verhaltens Semantik auf UAVs anwendet.</span><span class="sxs-lookup"><span data-stu-id="50d69-127">ROVs are an HLSL-only construct that applies different behavior semantics to UAVs.</span></span> <span data-ttu-id="50d69-128">Alle für UAVs relevanten APIs sind auch für ROVs relevant.</span><span class="sxs-lookup"><span data-stu-id="50d69-128">All APIs relevant to UAVs are also relevant to ROVs.</span></span> <span data-ttu-id="50d69-129">Beachten Sie, dass die folgende Methode, Struktur und Hilfsklasse auf den Rasterizer verweisen:</span><span class="sxs-lookup"><span data-stu-id="50d69-129">Note that the following method, structures, and helper class reference the rasterizer:</span></span>

-   <span data-ttu-id="50d69-130">[**D3D11 \_ Raster \_ DESC2**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_rasterizer_desc2) : Struktur mit der Beschreibung des Rasterizers. Beachten Sie die CD3D12 \_ Raster \_ DESC2 Helper-Klasse zum Erstellen von Raster-Beschreibungen.</span><span class="sxs-lookup"><span data-stu-id="50d69-130">[**D3D11\_RASTERIZER\_DESC2**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_rasterizer_desc2) : structure holding the rasterizer description, noting the CD3D12\_RASTERIZER\_DESC2 helper class for creating rasterizer descriptions.</span></span>
-   <span data-ttu-id="50d69-131">[**D3D11 \_ Feature \_ Data \_ D3D11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) : Struktur mit dem booleschen Wert `ROVsSupported` , der die Unterstützung angibt.</span><span class="sxs-lookup"><span data-stu-id="50d69-131">[**D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) : structure holding the boolean `ROVsSupported`, indicating the support.</span></span>
-   <span data-ttu-id="50d69-132">[**ID3D11Device:: checkfeaturesupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) : Methode für den Zugriff auf die unterstützten Funktionen.</span><span class="sxs-lookup"><span data-stu-id="50d69-132">[**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) : method to access the supported features.</span></span>

## <a name="related-topics"></a><span data-ttu-id="50d69-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="50d69-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50d69-134">Direct3D 11,3-Features</span><span class="sxs-lookup"><span data-stu-id="50d69-134">Direct3D 11.3 Features</span></span>](direct3d-11-3-features.md)
</dt> <dt>

[<span data-ttu-id="50d69-135">Shadermodell 5,1</span><span class="sxs-lookup"><span data-stu-id="50d69-135">Shader Model 5.1</span></span>](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> </dl>

 

 