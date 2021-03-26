---
title: bufinfo (SM5-ASM)
description: Abfragen der Element Anzahl in einem Puffer (aber nicht im Konstanten Puffer).
ms.assetid: 3A5C28F3-FE59-4C67-92AC-66B10E1D9692
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff8dd33871aa5bd56db6e7375979c6d49f374b74
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993078"
---
# <a name="bufinfo-sm5---asm"></a><span data-ttu-id="f6337-103">bufinfo (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="f6337-103">bufinfo (sm5 - asm)</span></span>

<span data-ttu-id="f6337-104">Abfragen der Element Anzahl in einem Puffer (aber nicht im Konstanten Puffer).</span><span class="sxs-lookup"><span data-stu-id="f6337-104">Query the element count on a buffer (but not the constant buffer).</span></span>



| <span data-ttu-id="f6337-105">bufinfo dest \[ . mask \] , srkresource</span><span class="sxs-lookup"><span data-stu-id="f6337-105">bufinfo dest\[.mask\], srcResource</span></span> |
|------------------------------------|



 



| <span data-ttu-id="f6337-106">Element</span><span class="sxs-lookup"><span data-stu-id="f6337-106">Item</span></span>                                                                                                               | <span data-ttu-id="f6337-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f6337-107">Description</span></span>                                                                           |
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f6337-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="f6337-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="f6337-109">\[in \] der Adresse der Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="f6337-109">\[in\] The address of the results.</span></span><br/>                                         |
| <span data-ttu-id="f6337-110"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srkresource*</span><span class="sxs-lookup"><span data-stu-id="f6337-110"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="f6337-111">\[in \] einem Puffer, bei dem es sich nicht um einen konstanten Puffer handelt, in einem SRV (t \# ) oder UAV (u \# ).</span><span class="sxs-lookup"><span data-stu-id="f6337-111">\[in\] Buffer, other than a constant Buffer, in an SRV (t\#) or UAV (u\#).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f6337-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f6337-112">Remarks</span></span>

<span data-ttu-id="f6337-113">Alle-Komponenten in *dest* empfangen die ganzzahlige Anzahl von Elementen in der Shader-Ressourcen Ansicht des Puffers.</span><span class="sxs-lookup"><span data-stu-id="f6337-113">All components in *dest* receive the integer number of elements in the buffer s shader resource view.</span></span> <span data-ttu-id="f6337-114">Die Anzahl der Elemente hängt von den Sicht Parametern (z. b. dem Speicherformat) ab.</span><span class="sxs-lookup"><span data-stu-id="f6337-114">The number of elements depends on the view parameters such as memory format.</span></span>

<span data-ttu-id="f6337-115">Bei einem typisierten Puffer SRV oder UAV ist der Rückgabewert die Anzahl der Elemente in der Sicht (wobei ein Element eine Einheit des typisierten Formats ist).</span><span class="sxs-lookup"><span data-stu-id="f6337-115">For a typed buffer SRV or UAV, the return value is the number of elements in the view (where an element is one unit of the typed format).</span></span>

<span data-ttu-id="f6337-116">Bei einem rohpuffer-SRV oder UAV ist der Rückgabewert die Anzahl der Bytes in der Sicht.</span><span class="sxs-lookup"><span data-stu-id="f6337-116">For a raw buffer SRV or UAV, the return value is the number of bytes in the view.</span></span>

<span data-ttu-id="f6337-117">Bei einem strukturierten Puffer SRV oder UAV ist der Rückgabewert die Anzahl der Strukturen in der Sicht.</span><span class="sxs-lookup"><span data-stu-id="f6337-117">For a structured buffer SRV or UAV, the return value is the number of structures in the view.</span></span>

<span data-ttu-id="f6337-118">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="f6337-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="f6337-119">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="f6337-119">Vertex</span></span> | <span data-ttu-id="f6337-120">Hülle</span><span class="sxs-lookup"><span data-stu-id="f6337-120">Hull</span></span> | <span data-ttu-id="f6337-121">Domain</span><span class="sxs-lookup"><span data-stu-id="f6337-121">Domain</span></span> | <span data-ttu-id="f6337-122">Geometrie</span><span class="sxs-lookup"><span data-stu-id="f6337-122">Geometry</span></span> | <span data-ttu-id="f6337-123">Pixel</span><span class="sxs-lookup"><span data-stu-id="f6337-123">Pixel</span></span> | <span data-ttu-id="f6337-124">Compute</span><span class="sxs-lookup"><span data-stu-id="f6337-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="f6337-125">X</span><span class="sxs-lookup"><span data-stu-id="f6337-125">X</span></span>      | <span data-ttu-id="f6337-126">X</span><span class="sxs-lookup"><span data-stu-id="f6337-126">X</span></span>    | <span data-ttu-id="f6337-127">X</span><span class="sxs-lookup"><span data-stu-id="f6337-127">X</span></span>      | <span data-ttu-id="f6337-128">X</span><span class="sxs-lookup"><span data-stu-id="f6337-128">X</span></span>        | <span data-ttu-id="f6337-129">X</span><span class="sxs-lookup"><span data-stu-id="f6337-129">X</span></span>     | <span data-ttu-id="f6337-130">X</span><span class="sxs-lookup"><span data-stu-id="f6337-130">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="f6337-131">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="f6337-131">Minimum Shader Model</span></span>

<span data-ttu-id="f6337-132">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="f6337-132">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="f6337-133">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="f6337-133">Shader Model</span></span>                                              | <span data-ttu-id="f6337-134">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="f6337-134">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="f6337-135">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="f6337-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="f6337-136">ja</span><span class="sxs-lookup"><span data-stu-id="f6337-136">yes</span></span>       |
| [<span data-ttu-id="f6337-137">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="f6337-137">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="f6337-138">nein</span><span class="sxs-lookup"><span data-stu-id="f6337-138">no</span></span>        |
| [<span data-ttu-id="f6337-139">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="f6337-139">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="f6337-140">nein</span><span class="sxs-lookup"><span data-stu-id="f6337-140">no</span></span>        |
| [<span data-ttu-id="f6337-141">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f6337-141">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="f6337-142">nein</span><span class="sxs-lookup"><span data-stu-id="f6337-142">no</span></span>        |
| [<span data-ttu-id="f6337-143">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f6337-143">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="f6337-144">nein</span><span class="sxs-lookup"><span data-stu-id="f6337-144">no</span></span>        |
| [<span data-ttu-id="f6337-145">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f6337-145">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="f6337-146">nein</span><span class="sxs-lookup"><span data-stu-id="f6337-146">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="f6337-147">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f6337-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6337-148">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f6337-148">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





