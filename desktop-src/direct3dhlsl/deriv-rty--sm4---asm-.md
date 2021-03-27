---
title: deriv_rty (SM4-ASM)
description: Renderziel-y-Entsprechung von DERIV \_ RTX.
ms.assetid: F78F2DBD-9428-4F34-85AD-276DF54C52D1
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2e4517782c687473b4789229334b4cafc94b989
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "103857751"
---
# <a name="deriv_rty-sm4---asm"></a><span data-ttu-id="28069-103">DERIV \_ Eigenschaft (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="28069-103">deriv\_rty (sm4 - asm)</span></span>

<span data-ttu-id="28069-104">Renderziel-y-Entsprechung von [DERIV \_ RTX](deriv-rtx--sm4---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="28069-104">Render-target y equivalent of [deriv\_rtx](deriv-rtx--sm4---asm-.md).</span></span>



| <span data-ttu-id="28069-105">DERIV \_ Eigenschaft \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="28069-105">deriv\_rty\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\],</span></span> |
|--------------------------------------------------------------------|



 



| <span data-ttu-id="28069-106">Element</span><span class="sxs-lookup"><span data-stu-id="28069-106">Item</span></span>                                                            | <span data-ttu-id="28069-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="28069-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="28069-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="28069-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="28069-109">\[in \] der Adresse des Vorgangs Ergebnisses.</span><span class="sxs-lookup"><span data-stu-id="28069-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="28069-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="28069-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="28069-111">\[in \] der-Komponente im-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="28069-111">\[in\] The component in the operation.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="28069-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="28069-112">Remarks</span></span>

<span data-ttu-id="28069-113">Nur ein einzelnes x-, y-abgeleitetes Paar wird für jeden 2 x 2-Stempel von Pixel berechnet.</span><span class="sxs-lookup"><span data-stu-id="28069-113">Only a single x,y derivative pair is computed for each 2x2 stamp of pixels.</span></span>

<span data-ttu-id="28069-114">Dieser Vorgang ist Hardware abhängig.</span><span class="sxs-lookup"><span data-stu-id="28069-114">This operation is hardware dependent.</span></span>

<span data-ttu-id="28069-115">Implementierung des verweisrasterizers für Dreiecke:</span><span class="sxs-lookup"><span data-stu-id="28069-115">Reference rasterizer implementation for triangles:</span></span>

-   <span data-ttu-id="28069-116">Der Pixelshader führt den Shader immer über 2 x 2 Quad von Pixeln in Gleichschritt aus (sogar Durchfluss Steuerung, Maskierungs deaktivierte Pixel).</span><span class="sxs-lookup"><span data-stu-id="28069-116">Pixel Shader always runs Shader over 2x2 quad of pixels in lockstep (even through flow control, masking disabled pixels).</span></span>
-   <span data-ttu-id="28069-117">Bei den Quads sind immer sogar nummerierte Pixelkoordinaten (x und y) für das linke obere Pixel vorhanden.</span><span class="sxs-lookup"><span data-stu-id="28069-117">Quads always have even numbered pixel coordinates (both x and y) for top-left pixel.</span></span>
-   <span data-ttu-id="28069-118">Dummypixel werden primitiv, wenn primitiv zu klein ist, um ein 2 x 2 Quad zu füllen.</span><span class="sxs-lookup"><span data-stu-id="28069-118">Dummy pixels run off primitive if primitive is too small to fill a 2x2 quad.</span></span>
-   <span data-ttu-id="28069-119">[DERIV \_ RTX](deriv-rtx--sm4---asm-.md) wird berechnet, indem zuerst 2 Pixel ausgewählt werden: das aktuelle Pixel und das andere Pixel mit derselben y-Koordinate aus dem Quad.</span><span class="sxs-lookup"><span data-stu-id="28069-119">[deriv\_rtx](deriv-rtx--sm4---asm-.md) is computed by first choosing 2 pixels: the current pixel and the other pixel with the same y coordinate from the quad.</span></span> <span data-ttu-id="28069-120">Das Ergebnis wird dann wie folgt berechnet: *src0*(ungerade x Pixel)- *src0*(sogar x Pixel) \[ pro Komponente\]</span><span class="sxs-lookup"><span data-stu-id="28069-120">Then, the result is calculated as: *src0*(odd x pixel) - *src0*(even x pixel) \[per-component\]</span></span>
-   <span data-ttu-id="28069-121">**DERIV \_ Eigenschaft** wird berechnet, indem zuerst 2 Pixel ausgewählt werden: das aktuelle Pixel und das andere Pixel mit derselben x-Koordinate aus dem Quad.</span><span class="sxs-lookup"><span data-stu-id="28069-121">**deriv\_rty** is computed by first choosing 2 pixels: the current pixel and the other pixel with the same x coordinate from the quad.</span></span> <span data-ttu-id="28069-122">Das Ergebnis wird dann wie folgt berechnet: *src0*(ungerader y Pixel)- *src0*(sogar y Pixel) \[ pro Komponente\]</span><span class="sxs-lookup"><span data-stu-id="28069-122">Then, the result is calculated as: *src0*(odd y pixel) - *src0*(even y pixel) \[per-component\]</span></span>

<span data-ttu-id="28069-123">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="28069-123">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="28069-124">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="28069-124">Vertex Shader</span></span> | <span data-ttu-id="28069-125">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="28069-125">Geometry Shader</span></span> | <span data-ttu-id="28069-126">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="28069-126">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               |                 | <span data-ttu-id="28069-127">x</span><span class="sxs-lookup"><span data-stu-id="28069-127">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="28069-128">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="28069-128">Minimum Shader Model</span></span>

<span data-ttu-id="28069-129">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="28069-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="28069-130">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="28069-130">Shader Model</span></span>                                              | <span data-ttu-id="28069-131">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="28069-131">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="28069-132">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="28069-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="28069-133">ja</span><span class="sxs-lookup"><span data-stu-id="28069-133">yes</span></span>       |
| [<span data-ttu-id="28069-134">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="28069-134">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="28069-135">ja</span><span class="sxs-lookup"><span data-stu-id="28069-135">yes</span></span>       |
| [<span data-ttu-id="28069-136">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="28069-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="28069-137">ja</span><span class="sxs-lookup"><span data-stu-id="28069-137">yes</span></span>       |
| [<span data-ttu-id="28069-138">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="28069-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="28069-139">nein</span><span class="sxs-lookup"><span data-stu-id="28069-139">no</span></span>        |
| [<span data-ttu-id="28069-140">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="28069-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="28069-141">nein</span><span class="sxs-lookup"><span data-stu-id="28069-141">no</span></span>        |
| [<span data-ttu-id="28069-142">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="28069-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="28069-143">nein</span><span class="sxs-lookup"><span data-stu-id="28069-143">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="28069-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="28069-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28069-145">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="28069-145">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





