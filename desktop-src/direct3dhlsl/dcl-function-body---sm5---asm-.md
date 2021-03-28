---
title: dcl_function_body (SM5-ASM)
description: Deklarieren Sie einen Funktions Text.
ms.assetid: 3A651107-BEA6-4D79-938F-8E0243C874C3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33f020748ecff270311fbbc89798d82b223b1f34
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104101114"
---
# <a name="dcl_function_body-sm5---asm"></a><span data-ttu-id="e0e3e-103">DCL \_ \_ -Funktions Text (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="e0e3e-103">dcl\_function\_body (sm5 - asm)</span></span>

<span data-ttu-id="e0e3e-104">Deklarieren Sie einen Funktions Text.</span><span class="sxs-lookup"><span data-stu-id="e0e3e-104">Declare a function body.</span></span>



| <span data-ttu-id="e0e3e-105">DCL- \_ Funktions \_ Text FB\#</span><span class="sxs-lookup"><span data-stu-id="e0e3e-105">dcl\_function\_body fb\#</span></span> |
|--------------------------|



 



| <span data-ttu-id="e0e3e-106">Element</span><span class="sxs-lookup"><span data-stu-id="e0e3e-106">Item</span></span>                                                          | <span data-ttu-id="e0e3e-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e0e3e-107">Description</span></span>                                                              |
|---------------------------------------------------------------|--------------------------------------------------------------------------|
| <span data-ttu-id="e0e3e-108"><span id="fb_"></span><span id="FB_"></span>*ÖFB\#*</span><span class="sxs-lookup"><span data-stu-id="e0e3e-108"><span id="fb_"></span><span id="FB_"></span>*fb\#*</span></span><br/> | <span data-ttu-id="e0e3e-109">\[in \] der Bezeichnung des Speicher Orts, an dem die Funktion angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="e0e3e-109">\[in\] The label of the place where the function will appear.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e0e3e-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e0e3e-110">Remarks</span></span>

<span data-ttu-id="e0e3e-111">Diese Anweisung deklariert einen eindeutigen Funktions Text, dessen Code später im Programm bei der Bezeichnung FB angezeigt wird \# .</span><span class="sxs-lookup"><span data-stu-id="e0e3e-111">This instruction declares a unique function body whose code will appear later in the program at label fb\#.</span></span>

<span data-ttu-id="e0e3e-112">Funktions Texte werden in Funktionstabellen Deklarationen verwendet.</span><span class="sxs-lookup"><span data-stu-id="e0e3e-112">Function bodies are used in function table declarations.</span></span> <span data-ttu-id="e0e3e-113">Weitere Informationen finden Sie unter [DCL \_ Function \_ Table](dcl-function-table---sm5---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="e0e3e-113">For more info, see [dcl\_function\_table](dcl-function-table---sm5---asm-.md).</span></span>

<span data-ttu-id="e0e3e-114">Im Rumpf-Shader und im Domänen-Shader, in dem mehrere Phasen vorhanden sind (Steuerungspunkt Phase, Verzweigungs Phase und joinphase), werden alle Funktions Texte (Bezeichnung FB \# ) nach allen Phasen angezeigt, anstatt nach Phasen gruppiert zu werden.</span><span class="sxs-lookup"><span data-stu-id="e0e3e-114">In the hull shader and domain shader, where there are multiple phases (control point phase, fork phase, and join phase), all function bodies (label fb\#) appear after all the phases, rather than being grouped by phase.</span></span>

<span data-ttu-id="e0e3e-115">Es gibt keine Beschränkung, wie viele funktionskörper vorhanden sein können.</span><span class="sxs-lookup"><span data-stu-id="e0e3e-115">There is no limit to how many function bodies can be present.</span></span>

<span data-ttu-id="e0e3e-116">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="e0e3e-116">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="e0e3e-117">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="e0e3e-117">Vertex</span></span> | <span data-ttu-id="e0e3e-118">Hülle</span><span class="sxs-lookup"><span data-stu-id="e0e3e-118">Hull</span></span> | <span data-ttu-id="e0e3e-119">Domain</span><span class="sxs-lookup"><span data-stu-id="e0e3e-119">Domain</span></span> | <span data-ttu-id="e0e3e-120">Geometrie</span><span class="sxs-lookup"><span data-stu-id="e0e3e-120">Geometry</span></span> | <span data-ttu-id="e0e3e-121">Pixel</span><span class="sxs-lookup"><span data-stu-id="e0e3e-121">Pixel</span></span> | <span data-ttu-id="e0e3e-122">Compute</span><span class="sxs-lookup"><span data-stu-id="e0e3e-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="e0e3e-123">X</span><span class="sxs-lookup"><span data-stu-id="e0e3e-123">X</span></span>      | <span data-ttu-id="e0e3e-124">X</span><span class="sxs-lookup"><span data-stu-id="e0e3e-124">X</span></span>    | <span data-ttu-id="e0e3e-125">X</span><span class="sxs-lookup"><span data-stu-id="e0e3e-125">X</span></span>      | <span data-ttu-id="e0e3e-126">X</span><span class="sxs-lookup"><span data-stu-id="e0e3e-126">X</span></span>        | <span data-ttu-id="e0e3e-127">X</span><span class="sxs-lookup"><span data-stu-id="e0e3e-127">X</span></span>     | <span data-ttu-id="e0e3e-128">X</span><span class="sxs-lookup"><span data-stu-id="e0e3e-128">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="e0e3e-129">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="e0e3e-129">Minimum Shader Model</span></span>

<span data-ttu-id="e0e3e-130">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="e0e3e-130">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="e0e3e-131">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="e0e3e-131">Shader Model</span></span>                                              | <span data-ttu-id="e0e3e-132">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="e0e3e-132">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="e0e3e-133">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="e0e3e-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="e0e3e-134">ja</span><span class="sxs-lookup"><span data-stu-id="e0e3e-134">yes</span></span>       |
| [<span data-ttu-id="e0e3e-135">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="e0e3e-135">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="e0e3e-136">nein</span><span class="sxs-lookup"><span data-stu-id="e0e3e-136">no</span></span>        |
| [<span data-ttu-id="e0e3e-137">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="e0e3e-137">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="e0e3e-138">nein</span><span class="sxs-lookup"><span data-stu-id="e0e3e-138">no</span></span>        |
| [<span data-ttu-id="e0e3e-139">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e0e3e-139">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="e0e3e-140">nein</span><span class="sxs-lookup"><span data-stu-id="e0e3e-140">no</span></span>        |
| [<span data-ttu-id="e0e3e-141">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e0e3e-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="e0e3e-142">nein</span><span class="sxs-lookup"><span data-stu-id="e0e3e-142">no</span></span>        |
| [<span data-ttu-id="e0e3e-143">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e0e3e-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="e0e3e-144">nein</span><span class="sxs-lookup"><span data-stu-id="e0e3e-144">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="e0e3e-145">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e0e3e-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0e3e-146">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e0e3e-146">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





