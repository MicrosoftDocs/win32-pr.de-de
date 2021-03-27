---
title: dcl_resource RAW (SM5-ASM)
description: Deklarieren Sie eine shaderressourceneingabe, und weisen Sie Sie einem t \-a-Platzhalter Register für die Ressource zu. | dcl_resource RAW (SM5-ASM)
ms.assetid: ECBA9DAB-F217-47FB-9588-F35866004E72
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dd6ccc5990e34990772a072086d9e080cde67b4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104219244"
---
# <a name="dcl_resource-raw-sm5---asm"></a><span data-ttu-id="15727-104">DCL \_ -Ressource RAW (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="15727-104">dcl\_resource raw (sm5 - asm)</span></span>

<span data-ttu-id="15727-105">Deklarieren Sie eine shaderressourceneingabe, und weisen Sie Sie einem t \# -a-Platzhalter Register für die Ressource zu.</span><span class="sxs-lookup"><span data-stu-id="15727-105">Declare a shader resource input and assign it to a t\# - a placeholder register for the resource.</span></span>



| <span data-ttu-id="15727-106">DCL- \_ Ressource \_ RAW dstsrv</span><span class="sxs-lookup"><span data-stu-id="15727-106">dcl\_resource\_raw dstSRV</span></span> |
|---------------------------|



 



| <span data-ttu-id="15727-107">Element</span><span class="sxs-lookup"><span data-stu-id="15727-107">Item</span></span>                                                                                           | <span data-ttu-id="15727-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="15727-108">Description</span></span>                                                                                       |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15727-109"><span id="dstSRV"></span><span id="dstsrv"></span><span id="DSTSRV"></span>*dstsrv*</span><span class="sxs-lookup"><span data-stu-id="15727-109"><span id="dstSRV"></span><span id="dstsrv"></span><span id="DSTSRV"></span>*dstSRV*</span></span><br/> | <span data-ttu-id="15727-110">\[in \] einem t- \# Register, das als Verweis auf einen shaderresourceview eines RAW-Puffers deklariert ist.</span><span class="sxs-lookup"><span data-stu-id="15727-110">\[in\] A t\# register declared as a reference to a ShaderResourceView of a raw buffer.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="15727-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="15727-111">Remarks</span></span>

<span data-ttu-id="15727-112">Der Inhalt der-Struktur hat keinen Typ. für den Arbeitsspeicher ausgeführte Vorgänge können die Daten implizit als Typ interpretieren.</span><span class="sxs-lookup"><span data-stu-id="15727-112">The contents of the structure have no type; operations performed on the memory may implicitly interpret the data as having a type.</span></span>

<span data-ttu-id="15727-113">Anweisungen, die \# auf ein unformatiertes t verweisen, benötigen eine 1D-Adresse, einen 32-Bit-Wert ohne Vorzeichen, der den Byte Offset an eine 32-Bit-ausgerichtete Position im Puffer angibt.</span><span class="sxs-lookup"><span data-stu-id="15727-113">Instructions that reference a raw t\# take a 1D address, an unsigned 32-bit value specifying the byte offset to a 32-bit aligned location in the Buffer.</span></span> <span data-ttu-id="15727-114">Die Adresse muss ein Vielfaches von 4 (Bytes) sein.</span><span class="sxs-lookup"><span data-stu-id="15727-114">The address must be a multiple of 4 (bytes).</span></span>

<span data-ttu-id="15727-115">Für Sichten, die \# als RAW deklariert sind, muss RAW bei der Erstellung angegeben werden. andernfalls ist das Verhalten beim Zugriff über einen Shader nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="15727-115">Views bound to t\# declared as raw must have RAW specified on their creation; otherwise behavior when accessed from a shader is undefined.</span></span>

<span data-ttu-id="15727-116">CS \_ 4 \_ 0 und CS \_ 4 \_ 1 unterstützen diese Anweisung.</span><span class="sxs-lookup"><span data-stu-id="15727-116">cs\_4\_0 and cs\_4\_1 support this instruction.</span></span>

<span data-ttu-id="15727-117">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="15727-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="15727-118">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="15727-118">Vertex</span></span> | <span data-ttu-id="15727-119">Hülle</span><span class="sxs-lookup"><span data-stu-id="15727-119">Hull</span></span> | <span data-ttu-id="15727-120">Domain</span><span class="sxs-lookup"><span data-stu-id="15727-120">Domain</span></span> | <span data-ttu-id="15727-121">Geometrie</span><span class="sxs-lookup"><span data-stu-id="15727-121">Geometry</span></span> | <span data-ttu-id="15727-122">Pixel</span><span class="sxs-lookup"><span data-stu-id="15727-122">Pixel</span></span> | <span data-ttu-id="15727-123">Compute</span><span class="sxs-lookup"><span data-stu-id="15727-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="15727-124">X</span><span class="sxs-lookup"><span data-stu-id="15727-124">X</span></span>      | <span data-ttu-id="15727-125">X</span><span class="sxs-lookup"><span data-stu-id="15727-125">X</span></span>    | <span data-ttu-id="15727-126">X</span><span class="sxs-lookup"><span data-stu-id="15727-126">X</span></span>      | <span data-ttu-id="15727-127">X</span><span class="sxs-lookup"><span data-stu-id="15727-127">X</span></span>        | <span data-ttu-id="15727-128">X</span><span class="sxs-lookup"><span data-stu-id="15727-128">X</span></span>     | <span data-ttu-id="15727-129">X</span><span class="sxs-lookup"><span data-stu-id="15727-129">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="15727-130">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="15727-130">Minimum Shader Model</span></span>

<span data-ttu-id="15727-131">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="15727-131">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="15727-132">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="15727-132">Shader Model</span></span>                                              | <span data-ttu-id="15727-133">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="15727-133">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="15727-134">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="15727-134">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="15727-135">ja</span><span class="sxs-lookup"><span data-stu-id="15727-135">yes</span></span>       |
| [<span data-ttu-id="15727-136">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="15727-136">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="15727-137">nein</span><span class="sxs-lookup"><span data-stu-id="15727-137">no</span></span>        |
| [<span data-ttu-id="15727-138">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="15727-138">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="15727-139">nein</span><span class="sxs-lookup"><span data-stu-id="15727-139">no</span></span>        |
| [<span data-ttu-id="15727-140">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="15727-140">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="15727-141">nein</span><span class="sxs-lookup"><span data-stu-id="15727-141">no</span></span>        |
| [<span data-ttu-id="15727-142">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="15727-142">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="15727-143">nein</span><span class="sxs-lookup"><span data-stu-id="15727-143">no</span></span>        |
| [<span data-ttu-id="15727-144">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="15727-144">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="15727-145">nein</span><span class="sxs-lookup"><span data-stu-id="15727-145">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="15727-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="15727-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15727-147">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="15727-147">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





