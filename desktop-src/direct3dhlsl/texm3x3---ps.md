---
title: texm3x3-PS
description: Führt eine 3X3-Matrix Multiplikation aus, wenn Sie in Verbindung mit zwei texm3x3pad-PS-Anweisungen verwendet wird.
ms.assetid: d0b14c87-3507-4237-9f2c-1eb94a6df71c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6238a4b148de67275af1b288d57686cc4d381ee9
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104976353"
---
# <a name="texm3x3---ps"></a><span data-ttu-id="7947c-103">texm3x3-PS</span><span class="sxs-lookup"><span data-stu-id="7947c-103">texm3x3 - ps</span></span>

<span data-ttu-id="7947c-104">Führt eine 3X3-Matrix Multiplikation aus, wenn Sie in Verbindung mit zwei [texm3x3pad-PS-](texm3x3pad---ps.md) Anweisungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7947c-104">Performs a 3x3 matrix multiply when used in conjunction with two [texm3x3pad - ps](texm3x3pad---ps.md) instructions.</span></span>

## <a name="syntax"></a><span data-ttu-id="7947c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7947c-105">Syntax</span></span>



| <span data-ttu-id="7947c-106">texm3x3 DST, src</span><span class="sxs-lookup"><span data-stu-id="7947c-106">texm3x3 dst, src</span></span> |
|------------------|



 

<span data-ttu-id="7947c-107">where</span><span class="sxs-lookup"><span data-stu-id="7947c-107">where</span></span>

-   <span data-ttu-id="7947c-108">DST ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="7947c-108">dst is the destination register.</span></span>
-   <span data-ttu-id="7947c-109">src ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="7947c-109">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="7947c-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7947c-110">Remarks</span></span>



| <span data-ttu-id="7947c-111">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="7947c-111">Pixel shader versions</span></span> | <span data-ttu-id="7947c-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="7947c-112">1\_1</span></span> | <span data-ttu-id="7947c-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="7947c-113">1\_2</span></span> | <span data-ttu-id="7947c-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="7947c-114">1\_3</span></span> | <span data-ttu-id="7947c-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="7947c-115">1\_4</span></span> | <span data-ttu-id="7947c-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7947c-116">2\_0</span></span> | <span data-ttu-id="7947c-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="7947c-117">2\_x</span></span> | <span data-ttu-id="7947c-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7947c-118">2\_sw</span></span> | <span data-ttu-id="7947c-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7947c-119">3\_0</span></span> | <span data-ttu-id="7947c-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7947c-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="7947c-121">texm3x3</span><span class="sxs-lookup"><span data-stu-id="7947c-121">texm3x3</span></span>               |      | <span data-ttu-id="7947c-122">x</span><span class="sxs-lookup"><span data-stu-id="7947c-122">x</span></span>    | <span data-ttu-id="7947c-123">x</span><span class="sxs-lookup"><span data-stu-id="7947c-123">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="7947c-124">Diese Anweisung ist mit der [texm3x3tex-PS-](texm3x3tex---ps.md) Anweisung ohne die Textur Suche identisch.</span><span class="sxs-lookup"><span data-stu-id="7947c-124">This instruction is the same as the [texm3x3tex - ps](texm3x3tex---ps.md) instruction, without the texture lookup.</span></span>

<span data-ttu-id="7947c-125">Diese Anweisung wird als letzte von drei Anweisungen verwendet, die einen 3X3-Matrix Multiplikations Vorgang darstellen.</span><span class="sxs-lookup"><span data-stu-id="7947c-125">This instruction is used as the final of three instructions representing a 3x3 matrix multiply operation.</span></span> <span data-ttu-id="7947c-126">Die 3X3-Matrix besteht aus den Texturkoordinaten der dritten Textur Phase und den beiden vorangehenden Textur Stufen.</span><span class="sxs-lookup"><span data-stu-id="7947c-126">The 3x3 matrix is comprised of the texture coordinates of the third texture stage, and by the two preceding texture stages.</span></span> <span data-ttu-id="7947c-127">Jede Textur, die einer der drei Textur Stufen zugewiesen ist, wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="7947c-127">Any texture assigned to any of the three texture stages is ignored.</span></span>

<span data-ttu-id="7947c-128">Diese Anweisung muss mit zwei texm3x3pad-Anweisungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7947c-128">This instruction must be used with two texm3x3pad instructions.</span></span> <span data-ttu-id="7947c-129">Textur Register müssen der folgenden Reihenfolge folgen.</span><span class="sxs-lookup"><span data-stu-id="7947c-129">Texture registers must follow the following sequence.</span></span>


```
 
tex t(n)                 // Define tn as a standard 3-vector (tn must
                         // be defined in some way before it is used)
texm3x3pad t(m),   t(n)  // where m > n
                         // Perform first row of matrix multiply
texm3x3pad t(m+1), t(n)  // Perform second row of matrix multiply
texm3x3    t(m+2), t(n)  // Perform third row of matrix multiply to get a
                         // 3-vector result
```



<span data-ttu-id="7947c-130">Hier finden Sie weitere Details dazu, wie die 3X3-Multiplikation durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7947c-130">Here is more detail about how the 3x3 multiply is accomplished.</span></span>

<span data-ttu-id="7947c-131">Die erste texm3x3pad-Anweisung führt die erste Zeile der Multiplikation durch, um u<sup>'</sup>zu suchen.</span><span class="sxs-lookup"><span data-stu-id="7947c-131">The first texm3x3pad instruction performs the first row of the multiply to find u<sup>'</sup>.</span></span>

<span data-ttu-id="7947c-132">u<sup>'</sup> = TextureCoordinates (Stufe m)<sub>UVW</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="7947c-132">u<sup>'</sup> = TextureCoordinates(stage m)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="7947c-133">Die zweite texm3x3pad-Anweisung führt die zweite Zeile der Multiplikation durch,<sup>um v zu</sup>suchen.</span><span class="sxs-lookup"><span data-stu-id="7947c-133">The second texm3x3pad instruction performs the second row of the multiply to find v<sup>'</sup>.</span></span>

<span data-ttu-id="7947c-134">v<sup>'</sup> = TextureCoordinates (Stufe m + 1)<sub>UVW</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="7947c-134">v<sup>'</sup> = TextureCoordinates(stage m+1)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="7947c-135">Die texm3x3tex-Anweisung führt die dritte Zeile der Multiplikation aus, um w<sup>'</sup>zu suchen.</span><span class="sxs-lookup"><span data-stu-id="7947c-135">The texm3x3tex instruction performs the third row of the multiply to find w<sup>'</sup>.</span></span>

<span data-ttu-id="7947c-136">w<sup>'</sup> = TextureCoordinates (Stufe m + 2)<sub>UVW</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="7947c-136">w<sup>'</sup> = TextureCoordinates(stage m+2)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="7947c-137">Platzieren Sie das Ergebnis der Matrix Multiplikation im Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="7947c-137">Place the result of the matrix multiply in the destination register.</span></span>

<span data-ttu-id="7947c-138">t (m + 2)<sub>RGBA</sub> = (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> , 1)</span><span class="sxs-lookup"><span data-stu-id="7947c-138">t(m+2)<sub>RGBA</sub> = (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> , 1)</span></span>

## <a name="related-topics"></a><span data-ttu-id="7947c-139">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7947c-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7947c-140">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="7947c-140">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




