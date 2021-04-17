---
title: deriv_rtx (SM4-ASM)
description: Rate der Inhalts Änderungen jeder float32-Komponente von src0 (Post-Swizzle), hinsichtlich renderTarget x Direction (RTX) oder renderTarget y Direction.
ms.assetid: 2438DB36-C348-4854-AE1B-EC3C890B0B42
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21d4543805c02cf70d9c6b7856461c427788f616
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389502"
---
# <a name="deriv_rtx-sm4---asm"></a><span data-ttu-id="9e33f-103">DERIV \_ RTX (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="9e33f-103">deriv\_rtx (sm4 - asm)</span></span>

<span data-ttu-id="9e33f-104">Rate der Inhalts Änderungen jeder float32-Komponente von *src0* (Post-Swizzle), hinsichtlich renderTarget x Direction (RTX) oder renderTarget y Direction.</span><span class="sxs-lookup"><span data-stu-id="9e33f-104">Rate of change of contents of each float32 component of *src0* (post-swizzle), with regard to RenderTarget x direction (rtx) or RenderTarget y direction.</span></span>



| <span data-ttu-id="9e33f-105">DERIV \_ RTX \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="9e33f-105">deriv\_rtx\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\],</span></span> |
|--------------------------------------------------------------------|



 



| <span data-ttu-id="9e33f-106">Element</span><span class="sxs-lookup"><span data-stu-id="9e33f-106">Item</span></span>                                                            | <span data-ttu-id="9e33f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9e33f-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="9e33f-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="9e33f-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="9e33f-109">\[in \] der Adresse des Vorgangs Ergebnisses.</span><span class="sxs-lookup"><span data-stu-id="9e33f-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="9e33f-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="9e33f-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="9e33f-111">\[in \] der-Komponente im-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="9e33f-111">\[in\] The component in the operation.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="9e33f-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9e33f-112">Remarks</span></span>

<span data-ttu-id="9e33f-113">Nur ein einzelnes x-, y-abgeleitetes Paar wird für jeden 2 x 2-Stempel von Pixel berechnet.</span><span class="sxs-lookup"><span data-stu-id="9e33f-113">Only a single x,y derivative pair is computed for each 2x2 stamp of pixels.</span></span>

<span data-ttu-id="9e33f-114">Dieser Vorgang ist Hardware abhängig.</span><span class="sxs-lookup"><span data-stu-id="9e33f-114">This operation is hardware dependent.</span></span>

<span data-ttu-id="9e33f-115">Implementierung des verweisrasterizers für Dreiecke:</span><span class="sxs-lookup"><span data-stu-id="9e33f-115">Reference rasterizer implementation for triangles:</span></span>

-   <span data-ttu-id="9e33f-116">Der Pixelshader führt den Shader immer über 2 x 2 Quad von Pixeln in Gleichschritt aus (sogar Durchfluss Steuerung, Maskierungs deaktivierte Pixel).</span><span class="sxs-lookup"><span data-stu-id="9e33f-116">Pixel Shader always runs Shader over 2x2 quad of pixels in lockstep (even through flow control, masking disabled pixels).</span></span>
-   <span data-ttu-id="9e33f-117">Bei den Quads sind immer sogar nummerierte Pixelkoordinaten (x und y) für das linke obere Pixel vorhanden.</span><span class="sxs-lookup"><span data-stu-id="9e33f-117">Quads always have even numbered pixel coordinates (both x and y) for top-left pixel.</span></span>
-   <span data-ttu-id="9e33f-118">Dummypixel werden primitiv, wenn primitiv zu klein ist, um ein 2 x 2 Quad zu füllen.</span><span class="sxs-lookup"><span data-stu-id="9e33f-118">Dummy pixels run off primitive if primitive is too small to fill a 2x2 quad.</span></span>
-   <span data-ttu-id="9e33f-119">**DERIV \_ RTX** wird berechnet, indem zuerst 2 Pixel ausgewählt werden: das aktuelle Pixel und das andere Pixel mit derselben y-Koordinate aus dem Quad.</span><span class="sxs-lookup"><span data-stu-id="9e33f-119">**deriv\_rtx** is computed by first choosing 2 pixels: the current pixel and the other pixel with the same y coordinate from the quad.</span></span> <span data-ttu-id="9e33f-120">Das Ergebnis wird dann wie folgt berechnet: *src0*(ungerade x Pixel)- *src0*(sogar x Pixel) \[ pro Komponente\]</span><span class="sxs-lookup"><span data-stu-id="9e33f-120">Then, the result is calculated as: *src0*(odd x pixel) - *src0*(even x pixel) \[per-component\]</span></span>
-   <span data-ttu-id="9e33f-121">[DERIV \_ Eigenschaft](deriv-rty--sm4---asm-.md) wird berechnet, indem zuerst 2 Pixel ausgewählt werden: das aktuelle Pixel und das andere Pixel mit derselben x-Koordinate aus dem Quad.</span><span class="sxs-lookup"><span data-stu-id="9e33f-121">[deriv\_rty](deriv-rty--sm4---asm-.md) is computed by first choosing 2 pixels: the current pixel and the other pixel with the same x coordinate from the quad.</span></span> <span data-ttu-id="9e33f-122">Das Ergebnis wird dann wie folgt berechnet: *src0*(ungerader y Pixel)- *src0*(sogar y Pixel) \[ pro Komponente\]</span><span class="sxs-lookup"><span data-stu-id="9e33f-122">Then, the result is calculated as: *src0*(odd y pixel) - *src0*(even y pixel) \[per-component\]</span></span>

<span data-ttu-id="9e33f-123">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="9e33f-123">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="9e33f-124">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="9e33f-124">Vertex Shader</span></span> | <span data-ttu-id="9e33f-125">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="9e33f-125">Geometry Shader</span></span> | <span data-ttu-id="9e33f-126">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="9e33f-126">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               |                 | <span data-ttu-id="9e33f-127">x</span><span class="sxs-lookup"><span data-stu-id="9e33f-127">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="9e33f-128">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="9e33f-128">Minimum Shader Model</span></span>

<span data-ttu-id="9e33f-129">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9e33f-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="9e33f-130">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="9e33f-130">Shader Model</span></span>                                              | <span data-ttu-id="9e33f-131">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="9e33f-131">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="9e33f-132">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="9e33f-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="9e33f-133">ja</span><span class="sxs-lookup"><span data-stu-id="9e33f-133">yes</span></span>       |
| [<span data-ttu-id="9e33f-134">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="9e33f-134">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="9e33f-135">ja</span><span class="sxs-lookup"><span data-stu-id="9e33f-135">yes</span></span>       |
| [<span data-ttu-id="9e33f-136">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="9e33f-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="9e33f-137">ja</span><span class="sxs-lookup"><span data-stu-id="9e33f-137">yes</span></span>       |
| [<span data-ttu-id="9e33f-138">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9e33f-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="9e33f-139">nein</span><span class="sxs-lookup"><span data-stu-id="9e33f-139">no</span></span>        |
| [<span data-ttu-id="9e33f-140">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9e33f-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="9e33f-141">nein</span><span class="sxs-lookup"><span data-stu-id="9e33f-141">no</span></span>        |
| [<span data-ttu-id="9e33f-142">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9e33f-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="9e33f-143">nein</span><span class="sxs-lookup"><span data-stu-id="9e33f-143">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="9e33f-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9e33f-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9e33f-145">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9e33f-145">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





