---
title: Bem-PS
description: Anwenden einer gefälschten Bump Environment-Map-Transformation.
ms.assetid: b41009d4-a2bb-4397-ad23-c95ef2620a66
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7c591555e2cbd2c6eaebf6e392bb94d6ec50e748
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389560"
---
# <a name="bem---ps"></a><span data-ttu-id="e5020-103">Bem-PS</span><span class="sxs-lookup"><span data-stu-id="e5020-103">bem - ps</span></span>

<span data-ttu-id="e5020-104">Anwenden einer gefälschten Bump Environment-Map-Transformation.</span><span class="sxs-lookup"><span data-stu-id="e5020-104">Apply a fake bump environment-map transform.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5020-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e5020-105">Syntax</span></span>



| <span data-ttu-id="e5020-106">Bem DST. RG, src0, Quelle1</span><span class="sxs-lookup"><span data-stu-id="e5020-106">bem dst.rg, src0, src1</span></span> |
|------------------------|



 

<span data-ttu-id="e5020-107">where</span><span class="sxs-lookup"><span data-stu-id="e5020-107">where</span></span>

-   <span data-ttu-id="e5020-108">DST. RG DST ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="e5020-108">dst.rg dst is the destination register.</span></span> <span data-ttu-id="e5020-109">Die rote und grüne Komponenten Schreib Maske muss verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e5020-109">The red and green component write mask must be used.</span></span>
-   <span data-ttu-id="e5020-110">src0 ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="e5020-110">src0 is a source register.</span></span>
-   <span data-ttu-id="e5020-111">Quelle1 ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="e5020-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5020-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e5020-112">Remarks</span></span>



| <span data-ttu-id="e5020-113">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="e5020-113">Pixel shader versions</span></span> | <span data-ttu-id="e5020-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="e5020-114">1\_1</span></span> | <span data-ttu-id="e5020-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="e5020-115">1\_2</span></span> | <span data-ttu-id="e5020-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="e5020-116">1\_3</span></span> | <span data-ttu-id="e5020-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="e5020-117">1\_4</span></span> | <span data-ttu-id="e5020-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e5020-118">2\_0</span></span> | <span data-ttu-id="e5020-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="e5020-119">2\_x</span></span> | <span data-ttu-id="e5020-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="e5020-120">2\_sw</span></span> | <span data-ttu-id="e5020-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e5020-121">3\_0</span></span> | <span data-ttu-id="e5020-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="e5020-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="e5020-123">Bem</span><span class="sxs-lookup"><span data-stu-id="e5020-123">bem</span></span>                   |      |      |      | <span data-ttu-id="e5020-124">x</span><span class="sxs-lookup"><span data-stu-id="e5020-124">x</span></span>    |      |      |       |      |       |



 

<span data-ttu-id="e5020-125">Diese Anweisung führt die folgende Berechnung aus.</span><span class="sxs-lookup"><span data-stu-id="e5020-125">This instruction performs the following calculation.</span></span>


```
(Given n == dest register #)
dest.r = src0.r + D3DTSS_BUMPENVMAT00(stage n) * src1.r 
                + D3DTSS_BUMPENVMAT10(stage n) * src1.g

dest.g = src0.g + D3DTSS_BUMPENVMAT01(stage n) * src1.r
                + D3DTSS_BUMPENVMAT11(stage n) * src1.g
```



<span data-ttu-id="e5020-126">Regeln für die Verwendung von Bem:</span><span class="sxs-lookup"><span data-stu-id="e5020-126">Rules for using bem:</span></span>

1.  <span data-ttu-id="e5020-127">Bem muss in der ersten Phase eines Shaders (d. h. vor einem Phasen Marker) angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="e5020-127">bem must appear in the first phase of a shader (that is, before a phase marker).</span></span>
2.  <span data-ttu-id="e5020-128">Bem verwendet zwei arithmetische Anweisungs Slots.</span><span class="sxs-lookup"><span data-stu-id="e5020-128">bem consumes two arithmetic instruction slots.</span></span>
3.  <span data-ttu-id="e5020-129">Nur eine Verwendung dieser Anweisung ist pro Shader zulässig.</span><span class="sxs-lookup"><span data-stu-id="e5020-129">Only one use of this instruction is allowed per shader.</span></span>
4.  <span data-ttu-id="e5020-130">Die Ziel-schreibfrage muss ". RG/.XY." lauten.</span><span class="sxs-lookup"><span data-stu-id="e5020-130">Destination writemask must be .rg /.xy.</span></span>
5.  <span data-ttu-id="e5020-131">Diese Anweisung kann nicht gemeinsam ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e5020-131">This instruction cannot be co-issued.</span></span>
6.  <span data-ttu-id="e5020-132">Abgesehen von der Einschränkung, dass die Ziel Schreib Maske. RG ist, sind Modifizierer für die Quell-src0-, Quelle1-und Anweisungs Modifizierer nicht eingeschränkt.</span><span class="sxs-lookup"><span data-stu-id="e5020-132">Aside from the restriction that destination write mask be .rg, modifiers on source src0, src1, and instruction modifiers are unconstrained.</span></span>

## <a name="instruction-information"></a><span data-ttu-id="e5020-133">Anweisungs Informationen</span><span class="sxs-lookup"><span data-stu-id="e5020-133">Instruction Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="e5020-134">Mindestens Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="e5020-134">Minimum operating system</span></span> | <span data-ttu-id="e5020-135">Windows 98</span><span class="sxs-lookup"><span data-stu-id="e5020-135">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="e5020-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e5020-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5020-137">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="e5020-137">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




