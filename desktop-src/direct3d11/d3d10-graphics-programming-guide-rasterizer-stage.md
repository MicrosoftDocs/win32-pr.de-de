---
title: Stufe des Rasterizers
description: Die Rasterung-Phase konvertiert Vektor Informationen (bestehend aus Formen oder primitiven) in ein Rasterbild (bestehend aus Pixeln), um Echt Zeit 3D-Grafiken anzuzeigen.
ms.assetid: efd3f819-7c63-4e1a-9923-8e7198354ec6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e746c5ace3512f36f9b9ad34d34a3ea578e1de36
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "103949248"
---
# <a name="rasterizer-stage"></a><span data-ttu-id="ea9d6-103">Stufe des Rasterizers</span><span class="sxs-lookup"><span data-stu-id="ea9d6-103">Rasterizer Stage</span></span>

<span data-ttu-id="ea9d6-104">Die Rasterung-Phase konvertiert Vektor Informationen (bestehend aus Formen oder primitiven) in ein Rasterbild (bestehend aus Pixeln), um Echt Zeit 3D-Grafiken anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="ea9d6-104">The rasterization stage converts vector information (composed of shapes or primitives) into a raster image (composed of pixels) for the purpose of displaying real-time 3D graphics.</span></span>

<span data-ttu-id="ea9d6-105">Während der rasterisierung wird jedes primitive in Pixel konvertiert, während pro-Scheitelpunkt Werte zwischen den einzelnen primitiven interpolieren werden.</span><span class="sxs-lookup"><span data-stu-id="ea9d6-105">During rasterization, each primitive is converted into pixels, while interpolating per-vertex values across each primitive.</span></span> <span data-ttu-id="ea9d6-106">Die rasterisierung umfasst Clipping-Scheitel Punkte für die Ansicht "Frustum", eine Division durch z, um Perspektiven bereitzustellen, primitive einem 2D-Viewport zuzuordnen und zu bestimmen, wie der Pixelshader aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="ea9d6-106">Rasterization includes clipping vertices to the view frustum, performing a divide by z to provide perspective, mapping primitives to a 2D viewport, and determining how to invoke the pixel shader.</span></span> <span data-ttu-id="ea9d6-107">Die Verwendung eines Pixelshaders ist optional, aber die Raster-Stufe führt immer Clipping aus, eine perspektivische Teilung zum Transformieren der Punkte in homogenen Raum und ordnet die Scheitel Punkte dem Viewport zu.</span><span class="sxs-lookup"><span data-stu-id="ea9d6-107">While using a pixel shader is optional, the rasterizer stage always performs clipping, a perspective divide to transform the points into homogeneous space, and maps the vertices to the viewport.</span></span>

<span data-ttu-id="ea9d6-108">Bei Scheitel Punkten (x, y, z, w), die sich in der Raster-Phase befinden, wird davon ausgegangen, dass es sich um einen homogenen Clip Bereich handelt.</span><span class="sxs-lookup"><span data-stu-id="ea9d6-108">Vertices (x,y,z,w), coming into the rasterizer stage are assumed to be in homogeneous clip-space.</span></span> <span data-ttu-id="ea9d6-109">In diesem Koordinaten Bereich zeigt die X-Achse nach rechts, Y zeigt nach oben und Z Punkte von der Kamera.</span><span class="sxs-lookup"><span data-stu-id="ea9d6-109">In this coordinate space the X axis points right, Y points up and Z points away from camera.</span></span>

<span data-ttu-id="ea9d6-110">Sie können die rasterisierung deaktivieren, indem Sie der Pipeline mitteilen, dass kein Pixelshader vorhanden ist (legen Sie die Pixel-Shader-Phase mit [**Verknüpfung id3d11devicecontext aus::P ssetshader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshader)auf **null** fest), und deaktivieren Sie Tiefe und Schablonen Tests (legen Sie **depthenable** und **stencilenable** auf **false** in der [**D3D11- \_ tiefen \_ Schablone \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)) fest.</span><span class="sxs-lookup"><span data-stu-id="ea9d6-110">You may disable rasterization by telling the pipeline there is no pixel shader (set the pixel shader stage to **NULL** with [**ID3D11DeviceContext::PSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshader)), and disabling depth and stencil testing (set **DepthEnable** and **StencilEnable** to **FALSE** in [**D3D11\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)).</span></span> <span data-ttu-id="ea9d6-111">Wenn die Rasterung deaktiviert ist, werden damit zusammenhängende Pipelinezähler nicht aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="ea9d6-111">While disabled, rasterization-related pipeline counters will not update.</span></span> <span data-ttu-id="ea9d6-112">Außerdem gibt es eine umfassende Beschreibung der [rasterisierungsregeln](d3d10-graphics-programming-guide-rasterizer-stage-rules.md).</span><span class="sxs-lookup"><span data-stu-id="ea9d6-112">There is also a complete description of the [rasterization rules](d3d10-graphics-programming-guide-rasterizer-stage-rules.md).</span></span>

<span data-ttu-id="ea9d6-113">Auf Hardware, die hierarchische Z-Puffer Optimierungen implementiert, können Sie das vorab Laden des z-Puffers aktivieren, indem Sie die Pixel-Shader-Stufe auf **null** festlegen, während Sie Tiefe und Schablonen Tests aktivieren.</span><span class="sxs-lookup"><span data-stu-id="ea9d6-113">On hardware that implements hierarchical Z-buffer optimizations, you may enable preloading the z-buffer by setting the pixel shader stage to **NULL** while enabling depth and stencil testing.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="ea9d6-114">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="ea9d6-114">In this section</span></span>



| <span data-ttu-id="ea9d6-115">Thema</span><span class="sxs-lookup"><span data-stu-id="ea9d6-115">Topic</span></span>                                                                                                                         | <span data-ttu-id="ea9d6-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ea9d6-116">Description</span></span>                                                                                                                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ea9d6-117">Einstieg in die Rasterizer-Phase</span><span class="sxs-lookup"><span data-stu-id="ea9d6-117">Getting Started with the Rasterizer Stage</span></span>](d3d10-graphics-programming-guide-rasterizer-stage-getting-started.md)<br/> | <span data-ttu-id="ea9d6-118">In diesem Abschnitt wird das Festlegen des Viewports, des Scheren Rechtecks, des Status des Rasterizers und der mehrfach Stichproben Erstellung beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ea9d6-118">This section describes setting the viewport, the scissors rectangle, the rasterizer state, and multi-sampling.</span></span><br/>                                                                                                                                                                                                |
| [<span data-ttu-id="ea9d6-119">Rasterisierungsregeln</span><span class="sxs-lookup"><span data-stu-id="ea9d6-119">Rasterization Rules</span></span>](d3d10-graphics-programming-guide-rasterizer-stage-rules.md)<br/>                                 | <span data-ttu-id="ea9d6-120">Rasterisierungsregeln definieren, wie Vektordaten in Rasterdaten zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="ea9d6-120">Rasterization rules define how vector data is mapped into raster data.</span></span> <span data-ttu-id="ea9d6-121">Die Rasterdaten werden an ganzzahlige Speicherorte angedockt, die dann durch ein-und abgeschnitten werden (um die Mindestanzahl von Pixeln zu zeichnen), und pro Pixel-Attribute werden interpoliert (von pro-Vertex-Attributen), bevor Sie an einen PixelShader übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="ea9d6-121">The raster data is snapped to integer locations that are then culled and clipped (to draw the minimum number of pixels), and per-pixel attributes are interpolated (from per-vertex attributes) before being passed to a pixel shader.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="ea9d6-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ea9d6-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea9d6-123">Grafik Pipeline</span><span class="sxs-lookup"><span data-stu-id="ea9d6-123">Graphics Pipeline</span></span>](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[<span data-ttu-id="ea9d6-124">Pipeline Stufen (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="ea9d6-124">Pipeline Stages (Direct3D 10)</span></span>](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

