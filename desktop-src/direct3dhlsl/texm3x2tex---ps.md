---
title: texm3x2tex-PS
description: Führt die letzte Zeile einer 3 x 2-Matrix multiplizieren aus und verwendet das Ergebnis, um eine Textur Suche durchzuführen. texm3x2tex muss in Verbindung mit der texm3x2pad-PS-Anweisung verwendet werden.
ms.assetid: c6cfbf75-4a63-4c82-9fb6-286b51b7f883
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 62206bc4ef1e1b64ec760a240a087ec13526d896
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993094"
---
# <a name="texm3x2tex---ps"></a><span data-ttu-id="fa38c-104">texm3x2tex-PS</span><span class="sxs-lookup"><span data-stu-id="fa38c-104">texm3x2tex - ps</span></span>

<span data-ttu-id="fa38c-105">Führt die letzte Zeile einer 3 x 2-Matrix multiplizieren aus und verwendet das Ergebnis, um eine Textur Suche durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="fa38c-105">Performs the final row of a 3x2 matrix multiply and uses the result to do a texture lookup.</span></span> <span data-ttu-id="fa38c-106">texm3x2tex muss in Verbindung mit der [texm3x2pad-PS-](texm3x2pad---ps.md) Anweisung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fa38c-106">texm3x2tex must be used in conjunction with the [texm3x2pad - ps](texm3x2pad---ps.md) instruction.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa38c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="fa38c-107">Syntax</span></span>



| <span data-ttu-id="fa38c-108">texm3x2tex DST, src</span><span class="sxs-lookup"><span data-stu-id="fa38c-108">texm3x2tex dst, src</span></span> |
|---------------------|



 

<span data-ttu-id="fa38c-109">where</span><span class="sxs-lookup"><span data-stu-id="fa38c-109">where</span></span>

-   <span data-ttu-id="fa38c-110">DST ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="fa38c-110">dst is the destination register.</span></span>
-   <span data-ttu-id="fa38c-111">src ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="fa38c-111">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa38c-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fa38c-112">Remarks</span></span>



| <span data-ttu-id="fa38c-113">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="fa38c-113">Pixel shader versions</span></span> | <span data-ttu-id="fa38c-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="fa38c-114">1\_1</span></span> | <span data-ttu-id="fa38c-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="fa38c-115">1\_2</span></span> | <span data-ttu-id="fa38c-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="fa38c-116">1\_3</span></span> | <span data-ttu-id="fa38c-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="fa38c-117">1\_4</span></span> | <span data-ttu-id="fa38c-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="fa38c-118">2\_0</span></span> | <span data-ttu-id="fa38c-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="fa38c-119">2\_x</span></span> | <span data-ttu-id="fa38c-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="fa38c-120">2\_sw</span></span> | <span data-ttu-id="fa38c-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="fa38c-121">3\_0</span></span> | <span data-ttu-id="fa38c-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="fa38c-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="fa38c-123">texm3x2tex</span><span class="sxs-lookup"><span data-stu-id="fa38c-123">texm3x2tex</span></span>            | <span data-ttu-id="fa38c-124">x</span><span class="sxs-lookup"><span data-stu-id="fa38c-124">x</span></span>    | <span data-ttu-id="fa38c-125">x</span><span class="sxs-lookup"><span data-stu-id="fa38c-125">x</span></span>    | <span data-ttu-id="fa38c-126">x</span><span class="sxs-lookup"><span data-stu-id="fa38c-126">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="fa38c-127">Die-Anweisung wird als eine von zwei Anweisungen verwendet, die einen 3 x 2-Matrix Multiplikations Vorgang darstellen.</span><span class="sxs-lookup"><span data-stu-id="fa38c-127">The instruction is used as one of two instructions representing a 3x2 matrix multiply operation.</span></span> <span data-ttu-id="fa38c-128">Diese Anweisung muss mit der [texm3x2pad-PS-](texm3x2pad---ps.md) Anweisung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fa38c-128">This instruction must be used with the [texm3x2pad - ps](texm3x2pad---ps.md) instruction.</span></span>

<span data-ttu-id="fa38c-129">Bei Verwendung dieser beiden Anweisungen müssen Textur Register die folgende Sequenz verwenden.</span><span class="sxs-lookup"><span data-stu-id="fa38c-129">When using these two instructions, texture registers must use the following sequence.</span></span>


```
 
tex t(n)                      // Define tn as a standard 3-vector (tn must 
                              // be defined in some way before it is used)
texm3x2pad  t(m),   t(n)      // where m > n
                              // Perform first row of matrix multiply
texm3x2tex  t(m+1), t(n)      // Perform second row of matrix multiply 
                              // to get (u,v) to sample texture 
                              // associated with stage m+1
```



<span data-ttu-id="fa38c-130">Hier finden Sie weitere Details dazu, wie die 3 x 2-Multiplikation durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fa38c-130">Here is more detail about how the 3x2 multiply is accomplished.</span></span>

<span data-ttu-id="fa38c-131">Die texm3x2pad-Anweisung führt die erste Zeile der Multiplikation durch, um u<sup>'</sup>zu suchen.</span><span class="sxs-lookup"><span data-stu-id="fa38c-131">The texm3x2pad instruction performs the first row of the multiply to find u<sup>'</sup>.</span></span>

<span data-ttu-id="fa38c-132">u<sup>'</sup> = t (n)<sub>RGB</sub> \* TextureCoordinates (Stufe m)<sub>UVW</sub></span><span class="sxs-lookup"><span data-stu-id="fa38c-132">u<sup>'</sup> = t(n)<sub>RGB</sub> \* TextureCoordinates(stage m)<sub>UVW</sub></span></span>

<span data-ttu-id="fa38c-133">Die texm3x2tex-Anweisung führt die zweite Zeile der Multiplikation durch,<sup>um v zu</sup>suchen.</span><span class="sxs-lookup"><span data-stu-id="fa38c-133">The texm3x2tex instruction performs the second row of the multiply to find v<sup>'</sup>.</span></span>

<span data-ttu-id="fa38c-134">v<sup>'</sup> = t (n)<sub>RGB</sub> \* TextureCoordinates (Stufe m + 1)<sub>UVW</sub></span><span class="sxs-lookup"><span data-stu-id="fa38c-134">v<sup>'</sup> = t(n)<sub>RGB</sub> \* TextureCoordinates(stage m+1)<sub>UVW</sub></span></span>

<span data-ttu-id="fa38c-135">Die texm3x2tex-Anweisung Stichproben die Textur auf der Stufe (m + 1) mit (u<sup>'</sup>, v<sup>'</sup>) und speichert das Ergebnis in t (m + 1).</span><span class="sxs-lookup"><span data-stu-id="fa38c-135">The texm3x2tex instruction samples the texture on stage (m+1) with (u<sup>'</sup>,v<sup>'</sup>) and stores the result in t(m+1).</span></span>

<span data-ttu-id="fa38c-136">t (m + 1)<sub>RGB</sub> = texturesample (Phase m + 1)<sub>RGB</sub> mithilfe von (u<sup>'</sup>, v<sup>'</sup> ) als Koordinaten</span><span class="sxs-lookup"><span data-stu-id="fa38c-136">t(m+1)<sub>RGB</sub> = TextureSample(stage m+1)<sub>RGB</sub> using (u<sup>'</sup>, v<sup>'</sup> ) as coordinates</span></span>

## <a name="examples"></a><span data-ttu-id="fa38c-137">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fa38c-137">Examples</span></span>

<span data-ttu-id="fa38c-138">Hier ist ein Beispiel-Shader mit den Textur Maps und den identifizierten Textur Stufen.</span><span class="sxs-lookup"><span data-stu-id="fa38c-138">Here is an example shader with the texture maps and the texture stages identified.</span></span>


```
ps_1_1
tex t0                // Bind texture in stage 0 to register t0
texm3x2pad  t1,  t0   // First row of matrix multiply
texm3x2tex  t2,  t0   // Second row of matrix multiply to get (u,v)
                      // with which to sample texture in stage 2
mov r0, t2            // Output result
```



<span data-ttu-id="fa38c-139">Für dieses Beispiel sind die folgenden Texturen in den folgenden Textur Phasen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="fa38c-139">This example requires the following textures in the following texture stages.</span></span>

-   <span data-ttu-id="fa38c-140">Phase 0 nimmt eine Zuordnung mit (x, y, z) perturingdaten vor.</span><span class="sxs-lookup"><span data-stu-id="fa38c-140">Stage 0 takes a map with (x,y,z) perturbation data.</span></span>
-   <span data-ttu-id="fa38c-141">Phase 1 enthält Texturkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="fa38c-141">Stage 1 holds texture coordinates.</span></span> <span data-ttu-id="fa38c-142">In der Textur Phase ist keine Textur erforderlich.</span><span class="sxs-lookup"><span data-stu-id="fa38c-142">No texture is required in the texture stage.</span></span>
-   <span data-ttu-id="fa38c-143">Phase 2 enthält sowohl Texturkoordinaten als auch eine 2D-Textur, die in dieser Textur Phase festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="fa38c-143">Stage 2 holds both texture coordinates as well as a 2D texture set at that texture stage.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fa38c-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fa38c-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa38c-145">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="fa38c-145">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




