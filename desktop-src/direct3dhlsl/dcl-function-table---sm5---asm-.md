---
title: dcl_function_table (SM5-ASM)
description: Deklarieren Sie eine Funktions Tabelle.
ms.assetid: 3693A03F-5E4B-40E8-B436-2FE3462C8DB8
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0710f53171ad2a86097dca96afb2756b1b067fef
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993254"
---
# <a name="dcl_function_table-sm5---asm"></a><span data-ttu-id="c0a16-103">DCL \_ \_ -Funktions Tabelle (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="c0a16-103">dcl\_function\_table (sm5 - asm)</span></span>

<span data-ttu-id="c0a16-104">Deklarieren Sie eine Funktions Tabelle.</span><span class="sxs-lookup"><span data-stu-id="c0a16-104">Declare a function table.</span></span>



| <span data-ttu-id="c0a16-105">DCL- \_ Funktions \_ Tabelle ft \# = {FB \# , FB \# ,...}</span><span class="sxs-lookup"><span data-stu-id="c0a16-105">dcl\_function\_table ft\# = {fb\#, fb\#, ...}</span></span> |
|-----------------------------------------------|



 



| <span data-ttu-id="c0a16-106">Element</span><span class="sxs-lookup"><span data-stu-id="c0a16-106">Item</span></span>                                                      | <span data-ttu-id="c0a16-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c0a16-107">Description</span></span>                                   |
|-----------------------------------------------------------|-----------------------------------------------|
| <span data-ttu-id="c0a16-108"><span id="ft"></span><span id="FT"></span>*GRA*</span><span class="sxs-lookup"><span data-stu-id="c0a16-108"><span id="ft"></span><span id="FT"></span>*ft*</span></span><br/> | <span data-ttu-id="c0a16-109">\[in \] den Funktionstabellen Einträgen.</span><span class="sxs-lookup"><span data-stu-id="c0a16-109">\[in\] The function table entries.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c0a16-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c0a16-110">Remarks</span></span>

<span data-ttu-id="c0a16-111">Diese Funktion deklariert eine Funktions Tabelle als Satz von Funktions Texten, die zuvor deklariert wurden.</span><span class="sxs-lookup"><span data-stu-id="c0a16-111">This function declares a function table as a set of function bodies that have been declared earlier.</span></span>

<span data-ttu-id="c0a16-112">Dies entspricht einer C++ Vtable, es sei denn, es gibt einen Eintrag pro CallSite für eine Schnittstelle anstelle von pro Methode.</span><span class="sxs-lookup"><span data-stu-id="c0a16-112">This is like a C++ vtable except there is an entry per call site for an interface instead of per method.</span></span>

<span data-ttu-id="c0a16-113">Es gibt keine Beschränkung für die Anzahl der Funktions Texte, die in einer Funktions Tabelle aufgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="c0a16-113">There is no limit to how many function bodies can be listed in a function table.</span></span>

<span data-ttu-id="c0a16-114">Es ist zulässig, dass ein angegebener Funktions Text-FB \# mehrmals in einer oder mehreren Funktionstabellen referenziert wird, um gemeinsamen Code freizugeben.</span><span class="sxs-lookup"><span data-stu-id="c0a16-114">It is valid for a given function body fb\# to be referenced multiple times in one or more function tables, as a way of sharing common code.</span></span>

<span data-ttu-id="c0a16-115">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="c0a16-115">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="c0a16-116">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="c0a16-116">Vertex</span></span> | <span data-ttu-id="c0a16-117">Hülle</span><span class="sxs-lookup"><span data-stu-id="c0a16-117">Hull</span></span> | <span data-ttu-id="c0a16-118">Domain</span><span class="sxs-lookup"><span data-stu-id="c0a16-118">Domain</span></span> | <span data-ttu-id="c0a16-119">Geometrie</span><span class="sxs-lookup"><span data-stu-id="c0a16-119">Geometry</span></span> | <span data-ttu-id="c0a16-120">Pixel</span><span class="sxs-lookup"><span data-stu-id="c0a16-120">Pixel</span></span> | <span data-ttu-id="c0a16-121">Compute</span><span class="sxs-lookup"><span data-stu-id="c0a16-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="c0a16-122">X</span><span class="sxs-lookup"><span data-stu-id="c0a16-122">X</span></span>      | <span data-ttu-id="c0a16-123">X</span><span class="sxs-lookup"><span data-stu-id="c0a16-123">X</span></span>    | <span data-ttu-id="c0a16-124">X</span><span class="sxs-lookup"><span data-stu-id="c0a16-124">X</span></span>      | <span data-ttu-id="c0a16-125">X</span><span class="sxs-lookup"><span data-stu-id="c0a16-125">X</span></span>        | <span data-ttu-id="c0a16-126">X</span><span class="sxs-lookup"><span data-stu-id="c0a16-126">X</span></span>     | <span data-ttu-id="c0a16-127">X</span><span class="sxs-lookup"><span data-stu-id="c0a16-127">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="c0a16-128">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="c0a16-128">Minimum Shader Model</span></span>

<span data-ttu-id="c0a16-129">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="c0a16-129">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="c0a16-130">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="c0a16-130">Shader Model</span></span>                                              | <span data-ttu-id="c0a16-131">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="c0a16-131">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="c0a16-132">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="c0a16-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="c0a16-133">ja</span><span class="sxs-lookup"><span data-stu-id="c0a16-133">yes</span></span>       |
| [<span data-ttu-id="c0a16-134">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="c0a16-134">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="c0a16-135">nein</span><span class="sxs-lookup"><span data-stu-id="c0a16-135">no</span></span>        |
| [<span data-ttu-id="c0a16-136">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="c0a16-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="c0a16-137">nein</span><span class="sxs-lookup"><span data-stu-id="c0a16-137">no</span></span>        |
| [<span data-ttu-id="c0a16-138">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c0a16-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="c0a16-139">nein</span><span class="sxs-lookup"><span data-stu-id="c0a16-139">no</span></span>        |
| [<span data-ttu-id="c0a16-140">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c0a16-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="c0a16-141">nein</span><span class="sxs-lookup"><span data-stu-id="c0a16-141">no</span></span>        |
| [<span data-ttu-id="c0a16-142">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c0a16-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="c0a16-143">nein</span><span class="sxs-lookup"><span data-stu-id="c0a16-143">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="c0a16-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c0a16-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c0a16-145">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c0a16-145">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





