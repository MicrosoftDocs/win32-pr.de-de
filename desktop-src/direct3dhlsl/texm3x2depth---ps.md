---
title: texm3x2depth-PS
description: Berechnen Sie den Tiefen Wert, der für den tiefen Test für dieses Pixel verwendet werden soll.
ms.assetid: bacdd471-a6ee-4998-badd-93ffd4fd61d4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 26d2c3efd1a31681520828b18d606d618d8c900a
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104976385"
---
# <a name="texm3x2depth---ps"></a><span data-ttu-id="8e4d6-103">texm3x2depth-PS</span><span class="sxs-lookup"><span data-stu-id="8e4d6-103">texm3x2depth - ps</span></span>

<span data-ttu-id="8e4d6-104">Berechnen Sie den Tiefen Wert, der für den tiefen Test für dieses Pixel verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8e4d6-104">Calculate the depth value to be used in depth testing for this pixel.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e4d6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8e4d6-105">Syntax</span></span>



| <span data-ttu-id="8e4d6-106">texm3x2depth DST, src</span><span class="sxs-lookup"><span data-stu-id="8e4d6-106">texm3x2depth dst, src</span></span> |
|-----------------------|



 

<span data-ttu-id="8e4d6-107">where</span><span class="sxs-lookup"><span data-stu-id="8e4d6-107">where</span></span>

-   <span data-ttu-id="8e4d6-108">DST ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="8e4d6-108">dst is the destination register.</span></span>
-   <span data-ttu-id="8e4d6-109">src ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="8e4d6-109">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e4d6-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8e4d6-110">Remarks</span></span>



| <span data-ttu-id="8e4d6-111">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="8e4d6-111">Pixel shader versions</span></span> | <span data-ttu-id="8e4d6-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="8e4d6-112">1\_1</span></span> | <span data-ttu-id="8e4d6-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="8e4d6-113">1\_2</span></span> | <span data-ttu-id="8e4d6-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="8e4d6-114">1\_3</span></span> | <span data-ttu-id="8e4d6-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="8e4d6-115">1\_4</span></span> | <span data-ttu-id="8e4d6-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8e4d6-116">2\_0</span></span> | <span data-ttu-id="8e4d6-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="8e4d6-117">2\_x</span></span> | <span data-ttu-id="8e4d6-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="8e4d6-118">2\_sw</span></span> | <span data-ttu-id="8e4d6-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8e4d6-119">3\_0</span></span> | <span data-ttu-id="8e4d6-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="8e4d6-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="8e4d6-121">texm3x2depth</span><span class="sxs-lookup"><span data-stu-id="8e4d6-121">texm3x2depth</span></span>          |      |      | <span data-ttu-id="8e4d6-122">x</span><span class="sxs-lookup"><span data-stu-id="8e4d6-122">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="8e4d6-123">Diese Anweisung muss mit der [texm3x2pad-PS-](texm3x2pad---ps.md) Anweisung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8e4d6-123">This instruction must be used with the [texm3x2pad - ps](texm3x2pad---ps.md) instruction.</span></span>

<span data-ttu-id="8e4d6-124">Bei Verwendung dieser beiden Anweisungen müssen Textur Register die folgende Sequenz verwenden.</span><span class="sxs-lookup"><span data-stu-id="8e4d6-124">When using these two instructions, texture registers must use the following sequence.</span></span>


```
 
tex t(n)                     // Define tn as a standard 3-vector.(tn must be 
                             // defined in some way before it is used
texm3x2pad   t(m),   t(n)    // Where m > n
                             // Calculate z value
texm3x2depth t(m+1), t(n)    // Calculate w value; use both z and w to
                             // find depth
```



<span data-ttu-id="8e4d6-125">Die tiefen Berechnung erfolgt nach dem Verwenden eines Punktprodukt Vorgangs, um z und w zu suchen.</span><span class="sxs-lookup"><span data-stu-id="8e4d6-125">The depth calculation is done after using a dot product operation to find z and w.</span></span> <span data-ttu-id="8e4d6-126">Im folgenden finden Sie weitere Details dazu, wie die tiefen Berechnung durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8e4d6-126">Here is more detail about how the depth calculation is accomplished.</span></span>

<span data-ttu-id="8e4d6-127">Die texm3x2pad-Anweisung berechnet z.</span><span class="sxs-lookup"><span data-stu-id="8e4d6-127">The texm3x2pad instruction calculates z.</span></span>

<span data-ttu-id="8e4d6-128">z = TextureCoordinates (Stufe m)<sub>UVW</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="8e4d6-128">z = TextureCoordinates(stage m)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="8e4d6-129">Die texm3x2depth-Anweisung berechnet w.</span><span class="sxs-lookup"><span data-stu-id="8e4d6-129">The texm3x2depth instruction calculates w.</span></span>

<span data-ttu-id="8e4d6-130">w = TextureCoordinates (Phase m + 1)<sub>UVW</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="8e4d6-130">w = TextureCoordinates(stage m+1)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="8e4d6-131">Berechnen Sie die Tiefe, und speichern Sie das Ergebnis in t (m + 1).</span><span class="sxs-lookup"><span data-stu-id="8e4d6-131">Calculate depth and store the result in t(m+1).</span></span>


```
 
if (w == 0)
  t(m+1) = 1.0
else
  t(m+1) = z/w
```



<span data-ttu-id="8e4d6-132">Die berechnete Tiefe wird so gekennzeichnet, dass Sie im tiefen Test für das Pixel verwendet wird, wobei der vorhandene tiefen Testwert für das Pixel ersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="8e4d6-132">The calculated depth is tagged to be used in the depth test for the pixel, replacing the existing depth test value for the pixel.</span></span>

<span data-ttu-id="8e4d6-133">Stellen Sie sicher, dass z/w im Bereich von (0-1) liegt.</span><span class="sxs-lookup"><span data-stu-id="8e4d6-133">Be sure to clamp z/w to be in the range of (0-1).</span></span> <span data-ttu-id="8e4d6-134">Wenn z/w außerhalb dieses Bereichs liegt, wird das im tiefen Puffer gespeicherte Ergebnis nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="8e4d6-134">If z/w is outside this range, the result stored in the depth buffer will be undefined.</span></span>

<span data-ttu-id="8e4d6-135">Nach dem Ausführen von texm3x2depth steht Register t (m + 1) nicht mehr zur Verwendung im Shader zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="8e4d6-135">After running texm3x2depth, register t(m+1) is no longer available for use in the shader.</span></span>

<span data-ttu-id="8e4d6-136">Wenn Sie mit dieser Anweisung eine Multisampling-Anweisung verwenden, entfällt der größte Vorteil des tiefen Puffers höherer Auflösung.</span><span class="sxs-lookup"><span data-stu-id="8e4d6-136">When multisampling, using this instruction eliminates most of the benefit of the higher resolution depth buffer.</span></span> <span data-ttu-id="8e4d6-137">Da der Pixelshader einmal pro Pixel ausgeführt wird, wird der einzelne tiefen Wert, der von texm3x2depth oder [textiefe-PS](texdepth---ps.md) ausgegeben wird, für jeden Vergleichstest des Subpixels-tiefen Werts verwendet.</span><span class="sxs-lookup"><span data-stu-id="8e4d6-137">Because the pixel shader runs once per pixel, the single depth value output by texm3x2depth or [texdepth - ps](texdepth---ps.md) will be used for each of the subpixel depth comparison tests.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8e4d6-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8e4d6-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e4d6-139">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="8e4d6-139">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




