---
title: Phase-PS
description: Die Phasen Anweisung markiert den Übergang Zwischenphase 1 und Phase 2. Wenn keine Phasen Anweisung vorhanden ist, wird der gesamte Shader so ausgeführt, als handele es sich um einen Shader der Phase 2.
ms.assetid: e0e89425-dc8e-489f-a0d1-3eefbfd09178
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e9a16b01e186de5645ffe65e003ebbe6defca2d5
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104038361"
---
# <a name="phase---ps"></a><span data-ttu-id="318a6-104">Phase-PS</span><span class="sxs-lookup"><span data-stu-id="318a6-104">phase - ps</span></span>

<span data-ttu-id="318a6-105">Die Phasen Anweisung markiert den Übergang Zwischenphase 1 und Phase 2.</span><span class="sxs-lookup"><span data-stu-id="318a6-105">The phase instruction marks the transition between phase 1 and phase 2.</span></span> <span data-ttu-id="318a6-106">Wenn keine Phasen Anweisung vorhanden ist, wird der gesamte Shader so ausgeführt, als handele es sich um einen Shader der Phase 2.</span><span class="sxs-lookup"><span data-stu-id="318a6-106">If no phase instruction is present, the entire shader runs as if it is a phase 2 shader.</span></span>

<span data-ttu-id="318a6-107">Diese Anweisung gilt nur für Version 1 \_ 4.</span><span class="sxs-lookup"><span data-stu-id="318a6-107">This instruction applies to version 1\_4 only.</span></span>

## <a name="syntax"></a><span data-ttu-id="318a6-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="318a6-108">Syntax</span></span>


```
phase
```



## <a name="remarks"></a><span data-ttu-id="318a6-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="318a6-109">Remarks</span></span>



| <span data-ttu-id="318a6-110">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="318a6-110">Pixel shader versions</span></span> | <span data-ttu-id="318a6-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="318a6-111">1\_1</span></span> | <span data-ttu-id="318a6-112">1\_2</span><span class="sxs-lookup"><span data-stu-id="318a6-112">1\_2</span></span> | <span data-ttu-id="318a6-113">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="318a6-113">1\_3</span></span> | <span data-ttu-id="318a6-114">1\_4</span><span class="sxs-lookup"><span data-stu-id="318a6-114">1\_4</span></span> | <span data-ttu-id="318a6-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="318a6-115">2\_0</span></span> | <span data-ttu-id="318a6-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="318a6-116">2\_x</span></span> | <span data-ttu-id="318a6-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="318a6-117">2\_sw</span></span> | <span data-ttu-id="318a6-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="318a6-118">3\_0</span></span> | <span data-ttu-id="318a6-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="318a6-119">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="318a6-120">phase</span><span class="sxs-lookup"><span data-stu-id="318a6-120">phase</span></span>                 |      |      |      | <span data-ttu-id="318a6-121">x</span><span class="sxs-lookup"><span data-stu-id="318a6-121">x</span></span>    |      |      |       |      |       |



 

<span data-ttu-id="318a6-122">Shaderanweisungen, die vor der Phasen Anweisung erfolgen, sind Anweisungen der Phase 1.</span><span class="sxs-lookup"><span data-stu-id="318a6-122">Shader instructions that occur before the phase instruction are phase 1 instructions.</span></span> <span data-ttu-id="318a6-123">Alle anderen Anweisungen sind Anweisungen der Phase 2.</span><span class="sxs-lookup"><span data-stu-id="318a6-123">All other instructions are phase 2 instructions.</span></span> <span data-ttu-id="318a6-124">Wenn Sie zwei Phasen für Anweisungen haben, wird die maximale Anzahl von Anweisungen pro Shader angehoben.</span><span class="sxs-lookup"><span data-stu-id="318a6-124">By having two phases for instructions, the maximum number of instructions per shader is increased.</span></span>

<span data-ttu-id="318a6-125">Der unglückliche Nebeneffekt des Phasenübergangs besteht darin, dass die Alpha Komponente von [temporären Registern](dx9-graphics-reference-asm-ps-registers-ps-1-x.md) nicht über den Übergang hinweg beibehalten wird.</span><span class="sxs-lookup"><span data-stu-id="318a6-125">The unfortunate side-effect of the phase transition is that the alpha component of [temporary registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md) do not persist across the transition.</span></span> <span data-ttu-id="318a6-126">Das heißt, die Alpha Komponente muss nach der Phasen Anweisung erneut initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="318a6-126">In other words, the alpha component must be reinitialized after the phase instruction.</span></span>

## <a name="example"></a><span data-ttu-id="318a6-127">Beispiel</span><span class="sxs-lookup"><span data-stu-id="318a6-127">Example</span></span>

<span data-ttu-id="318a6-128">In diesem Beispiel wird gezeigt, wie Sie Anweisungen in Phase 1 oder in Phase 2 in einem Shader gruppieren.</span><span class="sxs-lookup"><span data-stu-id="318a6-128">This example shows how to group instructions as phase 1 or phase 2 instructions within a shader.</span></span>

<span data-ttu-id="318a6-129">Die Phasen Anweisung wird auch als Phasen Marker bezeichnet, da Sie den Übergang zwischen den Anweisungen in Phase 1 und 2 markiert.</span><span class="sxs-lookup"><span data-stu-id="318a6-129">The phase instruction is also commonly called the phase marker because it marks the transition between phase 1 and 2 instructions.</span></span> <span data-ttu-id="318a6-130">Wenn in einem \_ Pixelshader der Version 1 4 der Phasen Marker nicht vorhanden ist, wird der Shader so ausgeführt, als ob er in Phase 2 ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="318a6-130">In a version 1\_4 pixel shader, if the phase marker is not present, the shader is run as if it is running in phase 2.</span></span> <span data-ttu-id="318a6-131">Dies ist wichtig, da es Unterschiede zwischen den Anweisungen in Phase 1 und 2 gibt und die Verfügbarkeit registriert ist.</span><span class="sxs-lookup"><span data-stu-id="318a6-131">This is important because there are differences between phase 1 and 2 instructions and register availability.</span></span> <span data-ttu-id="318a6-132">Die Unterschiede werden im gesamten Referenz Abschnitt vermerkt.</span><span class="sxs-lookup"><span data-stu-id="318a6-132">The differences are noted throughout the reference section.</span></span>


```
ps_1_4
  // Add phase 1 instructions here

phase
  // Add phase 2 instructions here
```



## <a name="related-topics"></a><span data-ttu-id="318a6-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="318a6-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="318a6-134">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="318a6-134">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




