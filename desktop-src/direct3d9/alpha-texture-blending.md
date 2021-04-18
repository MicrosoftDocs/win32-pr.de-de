---
description: Die Beleuchtungs-Engine kombiniert Material Farbe, Vertexfarbe und Beleuchtungs Informationen, um eine pro-Vertex-Farbe zu generieren.
ms.assetid: 1e7c31cb-dc63-4f4a-9ddc-d1d1d0b69085
title: Alpha Textur Mischung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ad394b70b96e17b2ce858f871fb869afde0d122
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106339697"
---
# <a name="alpha-texture-blending-direct3d-9"></a><span data-ttu-id="a6b1a-103">Alpha Textur Mischung (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="a6b1a-103">Alpha Texture Blending (Direct3D 9)</span></span>

<span data-ttu-id="a6b1a-104">Die Beleuchtungs-Engine kombiniert Material Farbe, Vertexfarbe und Beleuchtungs Informationen, um eine pro-Vertex-Farbe zu generieren.</span><span class="sxs-lookup"><span data-stu-id="a6b1a-104">The lighting engine combines material color, vertex color, and lighting information to generate a per-vertex color.</span></span> <span data-ttu-id="a6b1a-105">Nach der Interpolation wird dadurch eine pro-Pixel-Farbe generiert, die in den Frame Puffer geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="a6b1a-105">Once interpolated, this generates a per-pixel color that is written to the frame buffer.</span></span> <span data-ttu-id="a6b1a-106">Wenn eine Anwendung Textur blending ermöglicht, wird die Pixelfarbe zu einer Kombination des aktuellen Pixels im Frame Puffer und einer Textur Farbe.</span><span class="sxs-lookup"><span data-stu-id="a6b1a-106">If an application enables texture blending, the pixel color will become a combination of the current pixel in the frame buffer and a texture color.</span></span>

<span data-ttu-id="a6b1a-107">Diese Formel bestimmt die endgültige gemischte Pixelfarbe:</span><span class="sxs-lookup"><span data-stu-id="a6b1a-107">This formula determines the final blended pixel color:</span></span>


```
Color = TexelColor x SourceBlend + CurrentPixelColor x DestBlend
```



<span data-ttu-id="a6b1a-108">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="a6b1a-108">Where:</span></span>

-   <span data-ttu-id="a6b1a-109">Color ist die Ausgabe Pixelfarbe.</span><span class="sxs-lookup"><span data-stu-id="a6b1a-109">Color is the output pixel color.</span></span>
-   <span data-ttu-id="a6b1a-110">Texelcolor ist die Eingabe Farbe nach der Textur Filterung.</span><span class="sxs-lookup"><span data-stu-id="a6b1a-110">TexelColor is the input color after texture filtering.</span></span>
-   <span data-ttu-id="a6b1a-111">Sourceblend ist der Prozentsatz der endgültigen Pixelfarbe, die aus der texessource-Quellfarbe besteht.</span><span class="sxs-lookup"><span data-stu-id="a6b1a-111">SourceBlend is the percentage of the final pixel color that is made up of the source texel color.</span></span>
-   <span data-ttu-id="a6b1a-112">Currentpixelcolor ist die Farbe des aktuellen Pixels.</span><span class="sxs-lookup"><span data-stu-id="a6b1a-112">CurrentPixelColor is the color of the current pixel.</span></span>
-   <span data-ttu-id="a6b1a-113">Destblend ist der Prozentsatz der endgültigen Pixelfarbe, die aus der aktuellen Pixelfarbe besteht.</span><span class="sxs-lookup"><span data-stu-id="a6b1a-113">DestBlend is the percentage of the final pixel color that is made up of the current pixel color.</span></span>

<span data-ttu-id="a6b1a-114">Die abschließende Mischungs Gleichung wird festgelegt, indem [**IDirect3DDevice9:: setrenderstate**](/windows/desktop/api) aufgerufen und der Blend-renderzustand (D3DRS \_ blendxxx) mit einem entsprechenden Mischungs Faktor ([**D3DBLEND**](./d3dblend.md)) angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a6b1a-114">The final blending equation is set by calling [**IDirect3DDevice9::SetRenderState**](/windows/desktop/api) and specifying the blend render state (D3DRS\_BLENDXXX) with a corresponding blending factor ([**D3DBLEND**](./d3dblend.md)).</span></span> <span data-ttu-id="a6b1a-115">Die Werte von sourceblend und destblend reichen von 0,0 (transparent) bis 1,0 (nicht transparent) einschließlich.</span><span class="sxs-lookup"><span data-stu-id="a6b1a-115">The values of SourceBlend and DestBlend range from 0.0 (transparent) to 1.0 (opaque) inclusive.</span></span> <span data-ttu-id="a6b1a-116">Außerdem kann eine Anwendung die Transparenz eines Pixels steuern, indem der Alpha-Wert in einer Textur festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="a6b1a-116">In addition, an application can control the transparency of a pixel by setting the alpha value in a texture.</span></span> <span data-ttu-id="a6b1a-117">Verwenden Sie in diesem Fall Folgendes:</span><span class="sxs-lookup"><span data-stu-id="a6b1a-117">In this case, use the following:</span></span>


```
SourceBlend = D3DBLEND_ZERO 
DestBlend = D3DBLEND_ONE
```



<span data-ttu-id="a6b1a-118">Die Mischungs Gleichung bewirkt, dass das gerenderte Pixel transparent ist.</span><span class="sxs-lookup"><span data-stu-id="a6b1a-118">The blending equation will cause the rendered pixel to be transparent.</span></span> <span data-ttu-id="a6b1a-119">Die Standardwerte lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="a6b1a-119">The default values are:</span></span>


```
SourceBlend = D3DBLEND_SRCALPHA 
DestBlend = D3DBLEND_INVSRCALPHA
```



## <a name="related-topics"></a><span data-ttu-id="a6b1a-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a6b1a-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6b1a-121">Textur Mischung</span><span class="sxs-lookup"><span data-stu-id="a6b1a-121">Texture Blending</span></span>](texture-blending.md)
</dt> <dt>

[<span data-ttu-id="a6b1a-122">Textur Filterung (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="a6b1a-122">Texture Filtering (Direct3D 9)</span></span>](texture-filtering.md)
</dt> <dt>

[<span data-ttu-id="a6b1a-123">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="a6b1a-123">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 
