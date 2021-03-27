---
title: textiefe-PS
description: Berechnen von tiefen Werten, die im tiefen Puffer Vergleichstest für dieses Pixel verwendet werden sollen.
ms.assetid: f7128dbb-a5f3-4e95-b53b-7432439ae0c4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3eb5cd337108d08efee465c136adf1afb4921123
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "103857755"
---
# <a name="texdepth---ps"></a><span data-ttu-id="de6b9-103">textiefe-PS</span><span class="sxs-lookup"><span data-stu-id="de6b9-103">texdepth - ps</span></span>

<span data-ttu-id="de6b9-104">Berechnen von tiefen Werten, die im tiefen Puffer Vergleichstest für dieses Pixel verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="de6b9-104">Calculate depth values to be used in the depth buffer comparison test for this pixel.</span></span>

## <a name="syntax"></a><span data-ttu-id="de6b9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="de6b9-105">Syntax</span></span>



| <span data-ttu-id="de6b9-106">textiefe DST</span><span class="sxs-lookup"><span data-stu-id="de6b9-106">texdepth dst</span></span> |
|--------------|



 

<span data-ttu-id="de6b9-107">where</span><span class="sxs-lookup"><span data-stu-id="de6b9-107">where</span></span>

-   <span data-ttu-id="de6b9-108">DST ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="de6b9-108">dst is the destination register.</span></span>

## <a name="remarks"></a><span data-ttu-id="de6b9-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="de6b9-109">Remarks</span></span>



| <span data-ttu-id="de6b9-110">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="de6b9-110">Pixel shader versions</span></span> | <span data-ttu-id="de6b9-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="de6b9-111">1\_1</span></span> | <span data-ttu-id="de6b9-112">1\_2</span><span class="sxs-lookup"><span data-stu-id="de6b9-112">1\_2</span></span> | <span data-ttu-id="de6b9-113">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="de6b9-113">1\_3</span></span> | <span data-ttu-id="de6b9-114">1\_4</span><span class="sxs-lookup"><span data-stu-id="de6b9-114">1\_4</span></span> | <span data-ttu-id="de6b9-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="de6b9-115">2\_0</span></span> | <span data-ttu-id="de6b9-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="de6b9-116">2\_x</span></span> | <span data-ttu-id="de6b9-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="de6b9-117">2\_sw</span></span> | <span data-ttu-id="de6b9-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="de6b9-118">3\_0</span></span> | <span data-ttu-id="de6b9-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="de6b9-119">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="de6b9-120">textiefe</span><span class="sxs-lookup"><span data-stu-id="de6b9-120">texdepth</span></span>              |      |      |      | <span data-ttu-id="de6b9-121">x</span><span class="sxs-lookup"><span data-stu-id="de6b9-121">x</span></span>    |      |      |       |      |       |



 

<span data-ttu-id="de6b9-122">Diese Anweisung verwendet "R5. r/R5. g" im tiefen Puffer Vergleichstest für dieses Pixel.</span><span class="sxs-lookup"><span data-stu-id="de6b9-122">This instruction uses r5.r / r5.g in the depth buffer comparison test for this pixel.</span></span> <span data-ttu-id="de6b9-123">Die Daten in den blauen und Alpha Kanälen werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="de6b9-123">The data in the blue and alpha channels is ignored.</span></span> <span data-ttu-id="de6b9-124">Wenn R5. g = 0, das Ergebnis von R5. r/R5. g = 1,0.</span><span class="sxs-lookup"><span data-stu-id="de6b9-124">If r5.g = 0, the result of r5.r / r5.g = 1.0.</span></span>

<span data-ttu-id="de6b9-125">Temporäres Register R5 ist das einzige Register, das von dieser Anweisung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="de6b9-125">Temporary register r5 is the only register that this instruction can use.</span></span>

<span data-ttu-id="de6b9-126">Nach dem Ausführen dieser Anweisung ist das temporäre Register "R5" für zusätzliche Verwendung im Shader nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="de6b9-126">After executing this instruction, temporary register r5 is unavailable for additional use in the shader.</span></span>

<span data-ttu-id="de6b9-127">Wenn Sie mit dieser Anweisung eine Multisampling-Anweisung verwenden, entfällt der größte Vorteil des tiefen Puffers höherer Auflösung.</span><span class="sxs-lookup"><span data-stu-id="de6b9-127">When multisampling, using this instruction eliminates most of the benefit of the higher resolution depth buffer.</span></span> <span data-ttu-id="de6b9-128">Da der Pixelshader einmal pro Pixel ausgeführt wird, wird der einzelne tiefen Wert, der von [texm3x2depth-PS](texm3x2depth---ps.md) oder textiefe ausgegeben wird, für jeden Vergleichstest des Subpixels-tiefen Werts verwendet.</span><span class="sxs-lookup"><span data-stu-id="de6b9-128">Because the pixel shader runs once per pixel, the single depth value output by [texm3x2depth - ps](texm3x2depth---ps.md) or texdepth will be used for each of the subpixel depth comparison tests.</span></span>

## <a name="examples"></a><span data-ttu-id="de6b9-129">Beispiele</span><span class="sxs-lookup"><span data-stu-id="de6b9-129">Examples</span></span>

<span data-ttu-id="de6b9-130">Hier finden Sie ein Beispiel für die Verwendung von textiefe.</span><span class="sxs-lookup"><span data-stu-id="de6b9-130">Here is an example using texdepth.</span></span>


```
ps_1_4              
texld  r0, t0        // Sample texture from texture stage 0 (dest 
                     //   register number) into r0
                     // Use texture coordinate data from t0
texcrd r1.rgb, t1    // Load a second set of texture coordinate data into r1
add    r5.rg, r0, r1 // Add the two sets of texture coordinate data
phase                // Phase marker, required when using texdepth instruction
texdepth  r5         // Calculate pixel depth as r5.r / r5.g
                     // Do other color calculations with shader output r0
```



## <a name="related-topics"></a><span data-ttu-id="de6b9-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="de6b9-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="de6b9-132">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="de6b9-132">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




