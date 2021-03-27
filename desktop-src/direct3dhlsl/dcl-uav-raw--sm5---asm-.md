---
title: dcl_uav_raw (SM5-ASM)
description: Deklarieren Sie eine ungeordnete Zugriffs Ansicht (UAV) für die Verwendung durch einen Shader. | dcl_uav_raw (SM5-ASM)
ms.assetid: D0F43FF8-FF1C-4E42-AF42-F528C98FD680
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f47614d5a9327f2d686a36db6bfe4afeb653788
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995454"
---
# <a name="dcl_uav_raw-sm5---asm"></a><span data-ttu-id="751df-104">DCL \_ UAV \_ RAW (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="751df-104">dcl\_uav\_raw (sm5 - asm)</span></span>

<span data-ttu-id="751df-105">Deklarieren Sie eine ungeordnete Zugriffs Ansicht (UAV) für die Verwendung durch einen Shader.</span><span class="sxs-lookup"><span data-stu-id="751df-105">Declare an unordered access view (UAV) for use by a shader.</span></span>



| <span data-ttu-id="751df-106">DCL \_ UAV \_ RAW \[ \_ GLC \] dstuav</span><span class="sxs-lookup"><span data-stu-id="751df-106">dcl\_uav\_raw\[\_glc\] dstUAV</span></span> |
|-------------------------------|



 



| <span data-ttu-id="751df-107">Element</span><span class="sxs-lookup"><span data-stu-id="751df-107">Item</span></span>                                                                                           | <span data-ttu-id="751df-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="751df-108">Description</span></span>                |
|------------------------------------------------------------------------------------------------|----------------------------|
| <span data-ttu-id="751df-109"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstuav*</span><span class="sxs-lookup"><span data-stu-id="751df-109"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*</span></span><br/> | <span data-ttu-id="751df-110">\[in \] der UAV.</span><span class="sxs-lookup"><span data-stu-id="751df-110">\[in\] The UAV.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="751df-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="751df-111">Remarks</span></span>

<span data-ttu-id="751df-112">*dstuav* ist ein u- \# Register, das als Verweis auf eine unorderedaccessview eines Puffers deklariert wird, wobei der Puffer als einfaches 1D-Array von nicht typisierten 32-Bit-Einträgen angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="751df-112">*dstUAV* is a u\# register declared as a reference to an UnorderedAccessView of a Buffer, where the buffer appears as a simple 1D array of 32-bit untyped entries.</span></span>

<span data-ttu-id="751df-113">Für den Arbeitsspeicher ausgeführte Vorgänge können die Daten implizit als Typ interpretieren.</span><span class="sxs-lookup"><span data-stu-id="751df-113">Operations performed on the memory may implicitly interpret the data as having a type.</span></span>

<span data-ttu-id="751df-114">Das \_ GLC-Flag bedeutet "Global kohärent".</span><span class="sxs-lookup"><span data-stu-id="751df-114">The \_glc flag means "globally coherent".</span></span> <span data-ttu-id="751df-115">Das Fehlen von \_ GLC bedeutet, dass die UAV im COMPUTE-Shader nur als "zusammenhängender Gruppe" oder "lokal kohärent" in einem einzelnen Pixelshader-Aufruf deklariert wird.</span><span class="sxs-lookup"><span data-stu-id="751df-115">The absence of \_glc means the UAV is being declared only as "group coherent" in the compute shader, or "locally coherent" in a single pixel shader invocation.</span></span>

<span data-ttu-id="751df-116">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="751df-116">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="751df-117">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="751df-117">Vertex</span></span> | <span data-ttu-id="751df-118">Hülle</span><span class="sxs-lookup"><span data-stu-id="751df-118">Hull</span></span> | <span data-ttu-id="751df-119">Domain</span><span class="sxs-lookup"><span data-stu-id="751df-119">Domain</span></span> | <span data-ttu-id="751df-120">Geometrie</span><span class="sxs-lookup"><span data-stu-id="751df-120">Geometry</span></span> | <span data-ttu-id="751df-121">Pixel</span><span class="sxs-lookup"><span data-stu-id="751df-121">Pixel</span></span> | <span data-ttu-id="751df-122">Compute</span><span class="sxs-lookup"><span data-stu-id="751df-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="751df-123">X</span><span class="sxs-lookup"><span data-stu-id="751df-123">X</span></span>     | <span data-ttu-id="751df-124">X</span><span class="sxs-lookup"><span data-stu-id="751df-124">X</span></span>       |



 

<span data-ttu-id="751df-125">Da UAVs in allen Shader-Phasen für Direct3D 11,1 verfügbar sind, gilt diese Anweisung für alle Shader-Phasen für die Direct3D 11,1-Laufzeit, die ab Windows 8 verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="751df-125">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="751df-126">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="751df-126">Vertex</span></span> | <span data-ttu-id="751df-127">Hülle</span><span class="sxs-lookup"><span data-stu-id="751df-127">Hull</span></span> | <span data-ttu-id="751df-128">Domain</span><span class="sxs-lookup"><span data-stu-id="751df-128">Domain</span></span> | <span data-ttu-id="751df-129">Geometrie</span><span class="sxs-lookup"><span data-stu-id="751df-129">Geometry</span></span> | <span data-ttu-id="751df-130">Pixel</span><span class="sxs-lookup"><span data-stu-id="751df-130">Pixel</span></span> | <span data-ttu-id="751df-131">Compute</span><span class="sxs-lookup"><span data-stu-id="751df-131">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="751df-132">X</span><span class="sxs-lookup"><span data-stu-id="751df-132">X</span></span>      | <span data-ttu-id="751df-133">X</span><span class="sxs-lookup"><span data-stu-id="751df-133">X</span></span>    | <span data-ttu-id="751df-134">X</span><span class="sxs-lookup"><span data-stu-id="751df-134">X</span></span>      | <span data-ttu-id="751df-135">X</span><span class="sxs-lookup"><span data-stu-id="751df-135">X</span></span>        | <span data-ttu-id="751df-136">X</span><span class="sxs-lookup"><span data-stu-id="751df-136">X</span></span>     | <span data-ttu-id="751df-137">X</span><span class="sxs-lookup"><span data-stu-id="751df-137">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="751df-138">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="751df-138">Minimum Shader Model</span></span>

<span data-ttu-id="751df-139">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="751df-139">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="751df-140">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="751df-140">Shader Model</span></span>                                              | <span data-ttu-id="751df-141">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="751df-141">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="751df-142">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="751df-142">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="751df-143">ja</span><span class="sxs-lookup"><span data-stu-id="751df-143">yes</span></span>       |
| [<span data-ttu-id="751df-144">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="751df-144">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="751df-145">nein</span><span class="sxs-lookup"><span data-stu-id="751df-145">no</span></span>        |
| [<span data-ttu-id="751df-146">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="751df-146">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="751df-147">nein</span><span class="sxs-lookup"><span data-stu-id="751df-147">no</span></span>        |
| [<span data-ttu-id="751df-148">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="751df-148">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="751df-149">nein</span><span class="sxs-lookup"><span data-stu-id="751df-149">no</span></span>        |
| [<span data-ttu-id="751df-150">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="751df-150">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="751df-151">nein</span><span class="sxs-lookup"><span data-stu-id="751df-151">no</span></span>        |
| [<span data-ttu-id="751df-152">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="751df-152">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="751df-153">nein</span><span class="sxs-lookup"><span data-stu-id="751df-153">no</span></span>        |



 

> [!Note]  
> <span data-ttu-id="751df-154">Diese Anweisung wird in CS \_ 4 \_ 0 und CS \_ 4 \_ 1 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="751df-154">This instruction is supported in cs\_4\_0 and cs\_4\_1.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="751df-155">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="751df-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="751df-156">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="751df-156">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





