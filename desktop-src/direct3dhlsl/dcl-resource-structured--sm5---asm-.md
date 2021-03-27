---
title: dcl_resource strukturiert (SM5-ASM)
description: Deklarieren Sie eine shaderressourceneingabe, und weisen Sie Sie einem t \-a-Platzhalter Register für die Ressource zu. | dcl_resource strukturiert (SM5-ASM)
ms.assetid: 87FC8A56-9DB2-424B-889C-2AB59885DA13
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ab993e0cb260529c3419210c33f5d735a625bce
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104219181"
---
# <a name="dcl_resource-structured-sm5---asm"></a><span data-ttu-id="33aa9-104">strukturierte DCL \_ -Ressource (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="33aa9-104">dcl\_resource structured (sm5 - asm)</span></span>

<span data-ttu-id="33aa9-105">Deklarieren Sie eine shaderressourceneingabe, und weisen Sie Sie einem t \# -a-Platzhalter Register für die Ressource zu.</span><span class="sxs-lookup"><span data-stu-id="33aa9-105">Declare a shader resource input and assign it to a t\# - a placeholder register for the resource.</span></span>



| <span data-ttu-id="33aa9-106">DCL- \_ Ressource \_ strukturiert dstsrv, structbytestride</span><span class="sxs-lookup"><span data-stu-id="33aa9-106">dcl\_resource\_structured dstSRV, structByteStride</span></span> |
|----------------------------------------------------|



 



| <span data-ttu-id="33aa9-107">Element</span><span class="sxs-lookup"><span data-stu-id="33aa9-107">Item</span></span>                                                                                                                                   | <span data-ttu-id="33aa9-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="33aa9-108">Description</span></span>                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33aa9-109"><span id="dstSRV"></span><span id="dstsrv"></span><span id="DSTSRV"></span>*dstsrv*</span><span class="sxs-lookup"><span data-stu-id="33aa9-109"><span id="dstSRV"></span><span id="dstsrv"></span><span id="DSTSRV"></span>*dstSRV*</span></span><br/>                                         | <span data-ttu-id="33aa9-110">\[in \] einem t-Register, das \# als Verweis auf einen shaderresourceview eines strukturierten Puffers mit dem angegebenen Schritt deklariert wurde, der an den SRV-Slot \# an der API gebunden werden muss.</span><span class="sxs-lookup"><span data-stu-id="33aa9-110">\[in\] A t\# register declared as a reference to a ShaderResourceView of a structured buffer with the specified stride that must be bound to SRV slot \# at the API.</span></span> <br/> |
| <span data-ttu-id="33aa9-111"><span id="structByteStride"></span><span id="structbytestride"></span><span id="STRUCTBYTESTRIDE"></span>*structbytestride*</span><span class="sxs-lookup"><span data-stu-id="33aa9-111"><span id="structByteStride"></span><span id="structbytestride"></span><span id="STRUCTBYTESTRIDE"></span>*structByteStride*</span></span><br/> | <span data-ttu-id="33aa9-112">\[in \] einem uint, das die Größe der-Struktur in Bytes in dem deklarierten Puffer angibt.</span><span class="sxs-lookup"><span data-stu-id="33aa9-112">\[in\] A uint that specifies the size of the structure in bytes in the buffer being declared.</span></span> <span data-ttu-id="33aa9-113">Dieser Wert muss größer als 0 sein.</span><span class="sxs-lookup"><span data-stu-id="33aa9-113">This value must be greater than zero.</span></span><br/>                                   |



 

## <a name="remarks"></a><span data-ttu-id="33aa9-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="33aa9-114">Remarks</span></span>

<span data-ttu-id="33aa9-115">Der Inhalt der-Struktur hat keinen Typ. für den Arbeitsspeicher ausgeführte Vorgänge können die Daten implizit als Typ interpretieren.</span><span class="sxs-lookup"><span data-stu-id="33aa9-115">The contents of the structure have no type; operations performed on the memory may implicitly interpret the data as having a type.</span></span>

<span data-ttu-id="33aa9-116">Anweisungen, die auf eine strukturierte t verweisen \# , benötigen eine 2D-Adresse, bei der die erste Komponente \[ struct \] auswählt und die zweite Komponente \[ Offset innerhalb von Struktur, mehrere von 32 Bits, auswählt \] .</span><span class="sxs-lookup"><span data-stu-id="33aa9-116">Instructions that reference a structured t\# take a 2D address, where the first component picks \[struct\], and the second component picks \[offset within struct, multiple of 32-bits\].</span></span>

<span data-ttu-id="33aa9-117">CS \_ 4 \_ 0 und CS \_ 4 \_ 1 unterstützen diese Anweisung.</span><span class="sxs-lookup"><span data-stu-id="33aa9-117">cs\_4\_0 and cs\_4\_1 support this instruction.</span></span>

<span data-ttu-id="33aa9-118">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="33aa9-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="33aa9-119">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="33aa9-119">Vertex</span></span> | <span data-ttu-id="33aa9-120">Hülle</span><span class="sxs-lookup"><span data-stu-id="33aa9-120">Hull</span></span> | <span data-ttu-id="33aa9-121">Domain</span><span class="sxs-lookup"><span data-stu-id="33aa9-121">Domain</span></span> | <span data-ttu-id="33aa9-122">Geometrie</span><span class="sxs-lookup"><span data-stu-id="33aa9-122">Geometry</span></span> | <span data-ttu-id="33aa9-123">Pixel</span><span class="sxs-lookup"><span data-stu-id="33aa9-123">Pixel</span></span> | <span data-ttu-id="33aa9-124">Compute</span><span class="sxs-lookup"><span data-stu-id="33aa9-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="33aa9-125">X</span><span class="sxs-lookup"><span data-stu-id="33aa9-125">X</span></span>      | <span data-ttu-id="33aa9-126">X</span><span class="sxs-lookup"><span data-stu-id="33aa9-126">X</span></span>    | <span data-ttu-id="33aa9-127">X</span><span class="sxs-lookup"><span data-stu-id="33aa9-127">X</span></span>      | <span data-ttu-id="33aa9-128">X</span><span class="sxs-lookup"><span data-stu-id="33aa9-128">X</span></span>        | <span data-ttu-id="33aa9-129">X</span><span class="sxs-lookup"><span data-stu-id="33aa9-129">X</span></span>     | <span data-ttu-id="33aa9-130">X</span><span class="sxs-lookup"><span data-stu-id="33aa9-130">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="33aa9-131">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="33aa9-131">Minimum Shader Model</span></span>

<span data-ttu-id="33aa9-132">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="33aa9-132">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="33aa9-133">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="33aa9-133">Shader Model</span></span>                                              | <span data-ttu-id="33aa9-134">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="33aa9-134">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="33aa9-135">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="33aa9-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="33aa9-136">ja</span><span class="sxs-lookup"><span data-stu-id="33aa9-136">yes</span></span>       |
| [<span data-ttu-id="33aa9-137">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="33aa9-137">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="33aa9-138">nein</span><span class="sxs-lookup"><span data-stu-id="33aa9-138">no</span></span>        |
| [<span data-ttu-id="33aa9-139">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="33aa9-139">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="33aa9-140">nein</span><span class="sxs-lookup"><span data-stu-id="33aa9-140">no</span></span>        |
| [<span data-ttu-id="33aa9-141">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="33aa9-141">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="33aa9-142">nein</span><span class="sxs-lookup"><span data-stu-id="33aa9-142">no</span></span>        |
| [<span data-ttu-id="33aa9-143">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="33aa9-143">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="33aa9-144">nein</span><span class="sxs-lookup"><span data-stu-id="33aa9-144">no</span></span>        |
| [<span data-ttu-id="33aa9-145">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="33aa9-145">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="33aa9-146">nein</span><span class="sxs-lookup"><span data-stu-id="33aa9-146">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="33aa9-147">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="33aa9-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33aa9-148">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="33aa9-148">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





