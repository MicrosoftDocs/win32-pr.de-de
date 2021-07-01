---
title: bem - ps
description: Wenden Sie eine Fake-Bump-Umgebungszuordnungstransformation an.
ms.assetid: b41009d4-a2bb-4397-ad23-c95ef2620a66
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1adae07e3e2ebbca085981ca03a3b6449e2ffd9d
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129929"
---
# <a name="bem---ps"></a><span data-ttu-id="4236e-103">bem - ps</span><span class="sxs-lookup"><span data-stu-id="4236e-103">bem - ps</span></span>

<span data-ttu-id="4236e-104">Wenden Sie eine Fake-Bump-Umgebungszuordnungstransformation an.</span><span class="sxs-lookup"><span data-stu-id="4236e-104">Apply a fake bump environment-map transform.</span></span>

## <a name="syntax"></a><span data-ttu-id="4236e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4236e-105">Syntax</span></span>



| <span data-ttu-id="4236e-106">bem dst.rg, src0, src1</span><span class="sxs-lookup"><span data-stu-id="4236e-106">bem dst.rg, src0, src1</span></span> |
|------------------------|



 

<span data-ttu-id="4236e-107">where</span><span class="sxs-lookup"><span data-stu-id="4236e-107">where</span></span>

-   <span data-ttu-id="4236e-108">dst.rg dst ist das Zielregister.</span><span class="sxs-lookup"><span data-stu-id="4236e-108">dst.rg dst is the destination register.</span></span> <span data-ttu-id="4236e-109">Die Schreibmaske der roten und grünen Komponente muss verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4236e-109">The red and green component write mask must be used.</span></span>
-   <span data-ttu-id="4236e-110">src0 ist ein Quellregister.</span><span class="sxs-lookup"><span data-stu-id="4236e-110">src0 is a source register.</span></span>
-   <span data-ttu-id="4236e-111">src1 ist ein Quellregister.</span><span class="sxs-lookup"><span data-stu-id="4236e-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="4236e-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4236e-112">Remarks</span></span>



| <span data-ttu-id="4236e-113">Pixel-Shaderversionen</span><span class="sxs-lookup"><span data-stu-id="4236e-113">Pixel shader versions</span></span> | <span data-ttu-id="4236e-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="4236e-114">1\_1</span></span> | <span data-ttu-id="4236e-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="4236e-115">1\_2</span></span> | <span data-ttu-id="4236e-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="4236e-116">1\_3</span></span> | <span data-ttu-id="4236e-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="4236e-117">1\_4</span></span> | <span data-ttu-id="4236e-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4236e-118">2\_0</span></span> | <span data-ttu-id="4236e-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="4236e-119">2\_x</span></span> | <span data-ttu-id="4236e-120">2 \_ sw</span><span class="sxs-lookup"><span data-stu-id="4236e-120">2\_sw</span></span> | <span data-ttu-id="4236e-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4236e-121">3\_0</span></span> | <span data-ttu-id="4236e-122">3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="4236e-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="4236e-123">Bem</span><span class="sxs-lookup"><span data-stu-id="4236e-123">bem</span></span>                   |      |      |      | <span data-ttu-id="4236e-124">x</span><span class="sxs-lookup"><span data-stu-id="4236e-124">x</span></span>    |      |      |       |      |       |



 

<span data-ttu-id="4236e-125">Diese Anweisung führt die folgende Berechnung aus.</span><span class="sxs-lookup"><span data-stu-id="4236e-125">This instruction performs the following calculation.</span></span>


```
(Given n == dest register #)
dest.r = src0.r + D3DTSS_BUMPENVMAT00(stage n) * src1.r 
                + D3DTSS_BUMPENVMAT10(stage n) * src1.g

dest.g = src0.g + D3DTSS_BUMPENVMAT01(stage n) * src1.r
                + D3DTSS_BUMPENVMAT11(stage n) * src1.g
```



<span data-ttu-id="4236e-126">Regeln für die Verwendung von bem:</span><span class="sxs-lookup"><span data-stu-id="4236e-126">Rules for using bem:</span></span>

1.  <span data-ttu-id="4236e-127">bem muss in der ersten Phase eines Shaders (d. h. vor einem Phasenmarker) angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="4236e-127">bem must appear in the first phase of a shader (that is, before a phase marker).</span></span>
2.  <span data-ttu-id="4236e-128">bem verwendet zwei arithmetische Anweisungsslots.</span><span class="sxs-lookup"><span data-stu-id="4236e-128">bem consumes two arithmetic instruction slots.</span></span>
3.  <span data-ttu-id="4236e-129">Pro Shader ist nur eine Verwendung dieser Anweisung zulässig.</span><span class="sxs-lookup"><span data-stu-id="4236e-129">Only one use of this instruction is allowed per shader.</span></span>
4.  <span data-ttu-id="4236e-130">Die Ziel-Schreibmaske muss .rg /.xy sein.</span><span class="sxs-lookup"><span data-stu-id="4236e-130">Destination writemask must be .rg /.xy.</span></span>
5.  <span data-ttu-id="4236e-131">Diese Anweisung kann nicht gemeinsam ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4236e-131">This instruction cannot be co-issued.</span></span>
6.  <span data-ttu-id="4236e-132">Abgesehen von der Einschränkung, dass die Ziel-Schreibmaske .rg ist, sind Modifizierer für die Quellmodifizierer src0, src1 und anweisungsmodifizierer uneingeschränkt.</span><span class="sxs-lookup"><span data-stu-id="4236e-132">Aside from the restriction that destination write mask be .rg, modifiers on source src0, src1, and instruction modifiers are unconstrained.</span></span>

## <a name="instruction-information"></a><span data-ttu-id="4236e-133">Anweisungsinformationen</span><span class="sxs-lookup"><span data-stu-id="4236e-133">Instruction Information</span></span>



| <span data-ttu-id="4236e-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4236e-134">Requirement</span></span>                         | <span data-ttu-id="4236e-135">Wert</span><span class="sxs-lookup"><span data-stu-id="4236e-135">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="4236e-136">Mindestbetriebssystem</span><span class="sxs-lookup"><span data-stu-id="4236e-136">Minimum operating system</span></span> | <span data-ttu-id="4236e-137">Windows 98</span><span class="sxs-lookup"><span data-stu-id="4236e-137">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="4236e-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4236e-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4236e-139">Anweisungen für Pixel-Shader</span><span class="sxs-lookup"><span data-stu-id="4236e-139">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




