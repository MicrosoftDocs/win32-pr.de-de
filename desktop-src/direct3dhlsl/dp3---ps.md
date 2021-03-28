---
title: DP3-PS
description: Berechnet das 3-Komponenten-Punktprodukt der Quell Register. | DP3-PS
ms.assetid: a365acd1-89c0-4340-8f51-8e478f84ddc0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 09e4178f6aedbfb5242f4c545d624f1d07796008
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981408"
---
# <a name="dp3---ps"></a><span data-ttu-id="5df89-104">DP3-PS</span><span class="sxs-lookup"><span data-stu-id="5df89-104">dp3 - ps</span></span>

<span data-ttu-id="5df89-105">Berechnet das 3-Komponenten-Punktprodukt der Quell Register.</span><span class="sxs-lookup"><span data-stu-id="5df89-105">Computes the three-component dot product of the source registers.</span></span>

## <a name="syntax"></a><span data-ttu-id="5df89-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="5df89-106">Syntax</span></span>



| <span data-ttu-id="5df89-107">DP3 DST, src0, Quelle1</span><span class="sxs-lookup"><span data-stu-id="5df89-107">dp3 dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="5df89-108">where</span><span class="sxs-lookup"><span data-stu-id="5df89-108">where</span></span>

-   <span data-ttu-id="5df89-109">DST ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="5df89-109">dst is the destination register.</span></span>
-   <span data-ttu-id="5df89-110">src0 ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="5df89-110">src0 is a source register.</span></span>
-   <span data-ttu-id="5df89-111">Quelle1 ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="5df89-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="5df89-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5df89-112">Remarks</span></span>



| <span data-ttu-id="5df89-113">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="5df89-113">Pixel shader versions</span></span> | <span data-ttu-id="5df89-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="5df89-114">1\_1</span></span> | <span data-ttu-id="5df89-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="5df89-115">1\_2</span></span> | <span data-ttu-id="5df89-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="5df89-116">1\_3</span></span> | <span data-ttu-id="5df89-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="5df89-117">1\_4</span></span> | <span data-ttu-id="5df89-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5df89-118">2\_0</span></span> | <span data-ttu-id="5df89-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="5df89-119">2\_x</span></span> | <span data-ttu-id="5df89-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="5df89-120">2\_sw</span></span> | <span data-ttu-id="5df89-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5df89-121">3\_0</span></span> | <span data-ttu-id="5df89-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="5df89-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="5df89-123">dp3</span><span class="sxs-lookup"><span data-stu-id="5df89-123">dp3</span></span>                   | <span data-ttu-id="5df89-124">x</span><span class="sxs-lookup"><span data-stu-id="5df89-124">x</span></span>    | <span data-ttu-id="5df89-125">x</span><span class="sxs-lookup"><span data-stu-id="5df89-125">x</span></span>    | <span data-ttu-id="5df89-126">x</span><span class="sxs-lookup"><span data-stu-id="5df89-126">x</span></span>    | <span data-ttu-id="5df89-127">x</span><span class="sxs-lookup"><span data-stu-id="5df89-127">x</span></span>    | <span data-ttu-id="5df89-128">x</span><span class="sxs-lookup"><span data-stu-id="5df89-128">x</span></span>    | <span data-ttu-id="5df89-129">x</span><span class="sxs-lookup"><span data-stu-id="5df89-129">x</span></span>    | <span data-ttu-id="5df89-130">x</span><span class="sxs-lookup"><span data-stu-id="5df89-130">x</span></span>     | <span data-ttu-id="5df89-131">x</span><span class="sxs-lookup"><span data-stu-id="5df89-131">x</span></span>    | <span data-ttu-id="5df89-132">x</span><span class="sxs-lookup"><span data-stu-id="5df89-132">x</span></span>     |



 

<span data-ttu-id="5df89-133">Der folgende Code Ausschnitt zeigt die Vorgänge, die ausgeführt werden:</span><span class="sxs-lookup"><span data-stu-id="5df89-133">The following code snippet shows the operations performed:</span></span>


```
dest.x = dest.y = dest.z = dest.w = 
  (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z);
```



<span data-ttu-id="5df89-134">Diese Anweisung wird in der Vektor Pipeline ausgeführt und schreibt immer in die Farbkanäle.</span><span class="sxs-lookup"><span data-stu-id="5df89-134">This instruction runs in the vector pipeline, always writing out to the color channels.</span></span> <span data-ttu-id="5df89-135">Bei Version 1 \_ 4 verwendet diese Anweisung weiterhin die Vektor Pipeline, kann jedoch in beliebige Kanäle schreiben.</span><span class="sxs-lookup"><span data-stu-id="5df89-135">For version 1\_4, this instruction still uses the vector pipeline but may write to any channel.</span></span>

<span data-ttu-id="5df89-136">Eine Anweisung mit einer Ziel Register. RGB-Schreib Maske (. XYZ) kann mit DP3, wie unten gezeigt, zusammengestellt werden.</span><span class="sxs-lookup"><span data-stu-id="5df89-136">An instruction with a destination register .rgb (.xyz) write mask may be co-issued with dp3 As shown below.</span></span>


```
dp3 r0.rgb, t0, v0            // Copy scalar result to color components
+mov r2.a, t0                 // Copy alpha component from t0 in parallel 
```



<span data-ttu-id="5df89-137">Die DP3-Anweisung kann mithilfe des Quell Registrierungs-Modifizierers für [signierte Skalierung](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md) ( \_ bx2) geändert werden, wenn Sie nicht bereits in einen dynamischen Bereich mit Vorzeichen erweitert wurden.</span><span class="sxs-lookup"><span data-stu-id="5df89-137">The dp3 instruction can be modified using the [Source Register Signed Scaling](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md) input argument modifier (\_bx2) applied to its input arguments if they are not already expanded to signed dynamic range.</span></span> <span data-ttu-id="5df89-138">Bei einem Beleuchtungs-Shader wird der Bezeichner für die bearbeitungsanweisungsmodifizierer ( \_ Sat) häufig verwendet, um die negativen Werte an schwarz zu binden, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="5df89-138">For a lighting shader, the saturate instruction modifier (\_sat) is often used to clamp the negative values to black, as shown in the following example.</span></span>


```
dp3_sat r0, t0_bx2, v0_bx2    // t0 is a bump map, v0 contains the light direction
```



## <a name="related-topics"></a><span data-ttu-id="5df89-139">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5df89-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5df89-140">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="5df89-140">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




