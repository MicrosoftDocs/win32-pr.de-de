---
description: Der Frame Puffer Blender kann nun Alphakanäle unabhängig von der Farb Kanal Mischung bei renderzielen vermischen. Dieses Steuerelement wird mit einem neuen Rendering-Zustand aktiviert, D3DRS \_ separatealphablendenable.
ms.assetid: 6d30b13e-f4c6-4bc4-8735-15c398c099f1
title: Renderziel Alpha (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b70f395406559782172448b5555daff056ffd54c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520475"
---
# <a name="render-target-alpha-direct3d-9"></a><span data-ttu-id="cd067-104">Renderziel Alpha (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="cd067-104">Render Target Alpha (Direct3D 9)</span></span>

<span data-ttu-id="cd067-105">Der Frame Puffer Blender kann nun Alphakanäle unabhängig von der Farb Kanal Mischung bei renderzielen vermischen.</span><span class="sxs-lookup"><span data-stu-id="cd067-105">The frame buffer blender can now blend alpha channels independent from color-channel blending on render targets.</span></span> <span data-ttu-id="cd067-106">Dieses Steuerelement wird mit einem neuen Rendering-Zustand aktiviert, D3DRS \_ separatealphablendenable.</span><span class="sxs-lookup"><span data-stu-id="cd067-106">This control is enabled with a new render state, D3DRS\_SEPARATEALPHABLENDENABLE.</span></span>

<span data-ttu-id="cd067-107">Wenn D3DRS \_ separatealphablendenable auf **false** festgelegt ist (Dies ist die Standard Bedingung), sind die auf Alpha angewendeten Mischungs Ziel Faktoren und-Vorgänge identisch mit denen, die für das Mischen von Farbkanälen definiert sind.</span><span class="sxs-lookup"><span data-stu-id="cd067-107">When D3DRS\_SEPARATEALPHABLENDENABLE is set to **FALSE** (which is the default condition), the render-target blending factors and operations applied to alpha are the same as those defined for blending color channels.</span></span> <span data-ttu-id="cd067-108">Ein Treiber muss das Limit von D3DPMISCCAPS \_ separatealphablend festlegen, um anzugeben, dass es das Mischen von renderzielalpha unterstützen kann.</span><span class="sxs-lookup"><span data-stu-id="cd067-108">A driver needs to set the D3DPMISCCAPS\_SEPARATEALPHABLEND cap to indicate that it can support render-target alpha blending.</span></span> <span data-ttu-id="cd067-109">Stellen Sie sicher, dass Sie D3DRS \_ AlphaBlend aktivieren, um der Pipeline mitzuteilen, dass Alpha Blending benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="cd067-109">Be sure to enable D3DRS\_ALPHABLEND to tell the pipeline that alpha blending is needed.</span></span>

<span data-ttu-id="cd067-110">Um die Faktoren im Alphakanal der Renderer des Renderziels zu steuern, werden zwei neue renderzustände wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="cd067-110">To control the factors in the alpha channel of the render-target blenders, two new render states are defined as follows:</span></span>


```
D3DRS_SRCBLENDALPHA 
D3DRS_DESTBLENDALPHA 
```



<span data-ttu-id="cd067-111">Wie D3DRS \_ srcblend und D3DRS \_ destblend können diese auf einen der Werte in der [**D3DBLEND**](./d3dblend.md) -Enumeration festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="cd067-111">Like the D3DRS\_SRCBLEND and D3DRS\_DESTBLEND, these can be set to one of the values in the [**D3DBLEND**](./d3dblend.md) enumeration.</span></span> <span data-ttu-id="cd067-112">Die Blend-Einstellungen für Quelle und Ziel können auf verschiedene Arten kombiniert werden, abhängig von den Einstellungen in den srcblendcaps-und destblendcaps-Membern von [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="cd067-112">The source and destination blend settings can be combined in several ways, depending on the settings in the SrcBlendCaps and DestBlendCaps members of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

<span data-ttu-id="cd067-113">Die Alpha Mischung erfolgt wie folgt:</span><span class="sxs-lookup"><span data-stu-id="cd067-113">The alpha blending is done as follows:</span></span>

<span data-ttu-id="cd067-114">rendertargetalpha = (Alpha<sub>in</sub> \* srcblendop) blendop (Alpha<sub>RT</sub> \* destblendop)</span><span class="sxs-lookup"><span data-stu-id="cd067-114">renderTargetAlpha = (alpha<sub>in</sub> \* srcBlendOp) BlendOp (alpha<sub>rt</sub> \* destBlendOp)</span></span>

<span data-ttu-id="cd067-115">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="cd067-115">Where:</span></span>

-   <span data-ttu-id="cd067-116">Alpha<sub>in</sub> ist der eingabealphawert.</span><span class="sxs-lookup"><span data-stu-id="cd067-116">alpha<sub>in</sub> is the input alpha value.</span></span>
-   <span data-ttu-id="cd067-117">srcblendop ist einer der Blend-Faktoren in [**D3DBLEND**](./d3dblend.md).</span><span class="sxs-lookup"><span data-stu-id="cd067-117">srcBlendOp is one of the blend factors in [**D3DBLEND**](./d3dblend.md).</span></span>
-   <span data-ttu-id="cd067-118">Blendop ist einer der Blend-Faktoren in [**D3DBLENDOP**](./d3dblendop.md).</span><span class="sxs-lookup"><span data-stu-id="cd067-118">BlendOp is one of the blend factors in [**D3DBLENDOP**](./d3dblendop.md).</span></span>
-   <span data-ttu-id="cd067-119">Alpha<sub>RT</sub> ist der Wert für den Renderziel-Alpha Wert.</span><span class="sxs-lookup"><span data-stu-id="cd067-119">alpha<sub>rt</sub> is the render-target alpha value.</span></span>
-   <span data-ttu-id="cd067-120">destblendop ist einer der Blend-Faktoren in [**D3DBLEND**](./d3dblend.md).</span><span class="sxs-lookup"><span data-stu-id="cd067-120">destBlendOp is one of the blend factors in [**D3DBLEND**](./d3dblend.md).</span></span>
-   <span data-ttu-id="cd067-121">rendertargetalpha ist der abschließende gemischte Alpha-Wert.</span><span class="sxs-lookup"><span data-stu-id="cd067-121">renderTargetAlpha is the final blended alpha value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cd067-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cd067-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cd067-123">Alpha Blending</span><span class="sxs-lookup"><span data-stu-id="cd067-123">Alpha Blending</span></span>](alpha-blending.md)
</dt> </dl>

 

 
