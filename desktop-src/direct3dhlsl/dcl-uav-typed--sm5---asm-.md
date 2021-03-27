---
title: dcl_uav_typed (SM5-ASM)
description: Deklarieren Sie eine ungeordnete Zugriffs Ansicht (UAV) für die Verwendung durch einen Shader. | dcl_uav_typed (SM5-ASM)
ms.assetid: F9F5583F-E3D0-447F-9227-BBB1B4E71934
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b789714c7ec825620b73e387fa8a4dd73e1a590d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995745"
---
# <a name="dcl_uav_typed-sm5---asm"></a><span data-ttu-id="5e52a-104">DCL \_ -UAV- \_ typisiert (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="5e52a-104">dcl\_uav\_typed (sm5 - asm)</span></span>

<span data-ttu-id="5e52a-105">Deklarieren Sie eine ungeordnete Zugriffs Ansicht (UAV) für die Verwendung durch einen Shader.</span><span class="sxs-lookup"><span data-stu-id="5e52a-105">Declare an unordered access view (UAV) for use by a shader.</span></span>



| <span data-ttu-id="5e52a-106">DCL \_ UAV \_ typisiertes \[ \_ GLC \] dstuav, Dimension, Typ</span><span class="sxs-lookup"><span data-stu-id="5e52a-106">dcl\_uav\_typed\[\_glc\] dstUAV, dimension, type</span></span> |
|--------------------------------------------------|



 



| <span data-ttu-id="5e52a-107">Element</span><span class="sxs-lookup"><span data-stu-id="5e52a-107">Item</span></span>                                                                                           | <span data-ttu-id="5e52a-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5e52a-108">Description</span></span>                                                                                       |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e52a-109"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstuav*</span><span class="sxs-lookup"><span data-stu-id="5e52a-109"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*</span></span><br/> | <span data-ttu-id="5e52a-110">\[in \] der UAV.</span><span class="sxs-lookup"><span data-stu-id="5e52a-110">\[in\] The UAV.</span></span><br/>                                                                        |
| <span data-ttu-id="5e52a-111"><span id="dimension"></span><span id="DIMENSION"></span>*Maß*</span><span class="sxs-lookup"><span data-stu-id="5e52a-111"><span id="dimension"></span><span id="DIMENSION"></span>*dimension*</span></span><br/>                 | <span data-ttu-id="5e52a-112">\[in \] gibt an, wie viele Dimensionen die Anweisungen für den Zugriff auf die UAV bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="5e52a-112">\[in\] Specifies how many dimensions the instructions accessing the UAV are providing.</span></span><br/> |
| <span data-ttu-id="5e52a-113"><span id="type"></span><span id="TYPE"></span>*Sorte*</span><span class="sxs-lookup"><span data-stu-id="5e52a-113"><span id="type"></span><span id="TYPE"></span>*type*</span></span><br/>                                | <span data-ttu-id="5e52a-114">\[in \] der UAV-Art.</span><span class="sxs-lookup"><span data-stu-id="5e52a-114">\[in\] The type of the UAV.</span></span><br/>                                                            |



 

## <a name="remarks"></a><span data-ttu-id="5e52a-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5e52a-115">Remarks</span></span>

<span data-ttu-id="5e52a-116">*dstuav* wird \# als Verweis auf eine unorderedaccessview deklariert, die an den UAV-Slot \# an der API gebunden werden muss.</span><span class="sxs-lookup"><span data-stu-id="5e52a-116">*dstUAV* is a u\# register being declared as a reference to an UnorderedAccessView that must be bound to UAV slot \# at the API.</span></span>

<span data-ttu-id="5e52a-117">Die Dimension muss Buffer, Texture1D, Texture1DArray, Texture2D, Texture2DArray oder Texture3D lauten.</span><span class="sxs-lookup"><span data-stu-id="5e52a-117">The dimension must be buffer, Texture1D, Texture1DArray, Texture2D, Texture2DArray, or Texture3D.</span></span> <span data-ttu-id="5e52a-118">Dies gibt an, wie viele Dimensionen alle Anweisungen, die auf die UAV zugreifen, bereitstellen: 1 (Texture1D, Buffer), 2 (Texture1DArray, Texture2D) oder 3 (Texture2DArray, Texture3D).</span><span class="sxs-lookup"><span data-stu-id="5e52a-118">This indicates how many dimensions any instructions accessing the UAV are providing: 1 (Texture1D, Buffer), 2 (Texture1DArray, Texture2D) or 3 (Texture2DArray, Texture3D).</span></span>

<span data-ttu-id="5e52a-119">Typ: {unorm, snorm, uint, Sint, float}.</span><span class="sxs-lookup"><span data-stu-id="5e52a-119">Type is {UNORM,SNORM,UINT,SINT,FLOAT}.</span></span> <span data-ttu-id="5e52a-120">Vorgänge, die mit der deklarierten u ausgeführt \# werden, müssen mit dem hier deklarierten Typ kompatibel sein, und die an Slot gebundene UAV \# muss ebenfalls denselben Typ aufweisen.</span><span class="sxs-lookup"><span data-stu-id="5e52a-120">Operations done with the declared u\# must be compatible with the type declared here, and the UAV bound to slot \# must also have the same type.</span></span>

<span data-ttu-id="5e52a-121">Das \_ GLC-Flag steht für "Global kohärent".</span><span class="sxs-lookup"><span data-stu-id="5e52a-121">The \_glc flag stands for "globally coherent".</span></span> <span data-ttu-id="5e52a-122">Das Fehlen von \_ GLC bedeutet, dass die UAV im COMPUTE-Shader nur als "zusammenhängender Gruppe" oder "lokal kohärent" in einem einzelnen Pixelshader-Aufruf deklariert wird.</span><span class="sxs-lookup"><span data-stu-id="5e52a-122">The absence of \_glc means the UAV is being declared only as "group coherent" in the compute shader, or "locally coherent" in a single pixel shader invocation.</span></span>

<span data-ttu-id="5e52a-123">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="5e52a-123">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="5e52a-124">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="5e52a-124">Vertex</span></span> | <span data-ttu-id="5e52a-125">Hülle</span><span class="sxs-lookup"><span data-stu-id="5e52a-125">Hull</span></span> | <span data-ttu-id="5e52a-126">Domain</span><span class="sxs-lookup"><span data-stu-id="5e52a-126">Domain</span></span> | <span data-ttu-id="5e52a-127">Geometrie</span><span class="sxs-lookup"><span data-stu-id="5e52a-127">Geometry</span></span> | <span data-ttu-id="5e52a-128">Pixel</span><span class="sxs-lookup"><span data-stu-id="5e52a-128">Pixel</span></span> | <span data-ttu-id="5e52a-129">Compute</span><span class="sxs-lookup"><span data-stu-id="5e52a-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="5e52a-130">X</span><span class="sxs-lookup"><span data-stu-id="5e52a-130">X</span></span>     | <span data-ttu-id="5e52a-131">X</span><span class="sxs-lookup"><span data-stu-id="5e52a-131">X</span></span>       |



 

<span data-ttu-id="5e52a-132">Da UAVs in allen Shader-Phasen für Direct3D 11,1 verfügbar sind, gilt diese Anweisung für alle Shader-Phasen für die Direct3D 11,1-Laufzeit, die ab Windows 8 verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="5e52a-132">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="5e52a-133">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="5e52a-133">Vertex</span></span> | <span data-ttu-id="5e52a-134">Hülle</span><span class="sxs-lookup"><span data-stu-id="5e52a-134">Hull</span></span> | <span data-ttu-id="5e52a-135">Domain</span><span class="sxs-lookup"><span data-stu-id="5e52a-135">Domain</span></span> | <span data-ttu-id="5e52a-136">Geometrie</span><span class="sxs-lookup"><span data-stu-id="5e52a-136">Geometry</span></span> | <span data-ttu-id="5e52a-137">Pixel</span><span class="sxs-lookup"><span data-stu-id="5e52a-137">Pixel</span></span> | <span data-ttu-id="5e52a-138">Compute</span><span class="sxs-lookup"><span data-stu-id="5e52a-138">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="5e52a-139">X</span><span class="sxs-lookup"><span data-stu-id="5e52a-139">X</span></span>      | <span data-ttu-id="5e52a-140">X</span><span class="sxs-lookup"><span data-stu-id="5e52a-140">X</span></span>    | <span data-ttu-id="5e52a-141">X</span><span class="sxs-lookup"><span data-stu-id="5e52a-141">X</span></span>      | <span data-ttu-id="5e52a-142">X</span><span class="sxs-lookup"><span data-stu-id="5e52a-142">X</span></span>        | <span data-ttu-id="5e52a-143">X</span><span class="sxs-lookup"><span data-stu-id="5e52a-143">X</span></span>     | <span data-ttu-id="5e52a-144">X</span><span class="sxs-lookup"><span data-stu-id="5e52a-144">X</span></span>       |



 

> [!Note]  
> <span data-ttu-id="5e52a-145">Diese Anweisung wird in Compute-Shader 4. x nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5e52a-145">This instruction is not supported in compute shader 4.x.</span></span>

 

## <a name="minimum-shader-model"></a><span data-ttu-id="5e52a-146">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="5e52a-146">Minimum Shader Model</span></span>

<span data-ttu-id="5e52a-147">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="5e52a-147">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="5e52a-148">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="5e52a-148">Shader Model</span></span>                                              | <span data-ttu-id="5e52a-149">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="5e52a-149">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="5e52a-150">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="5e52a-150">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="5e52a-151">ja</span><span class="sxs-lookup"><span data-stu-id="5e52a-151">yes</span></span>       |
| [<span data-ttu-id="5e52a-152">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="5e52a-152">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="5e52a-153">nein</span><span class="sxs-lookup"><span data-stu-id="5e52a-153">no</span></span>        |
| [<span data-ttu-id="5e52a-154">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="5e52a-154">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="5e52a-155">nein</span><span class="sxs-lookup"><span data-stu-id="5e52a-155">no</span></span>        |
| [<span data-ttu-id="5e52a-156">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5e52a-156">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="5e52a-157">nein</span><span class="sxs-lookup"><span data-stu-id="5e52a-157">no</span></span>        |
| [<span data-ttu-id="5e52a-158">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5e52a-158">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="5e52a-159">nein</span><span class="sxs-lookup"><span data-stu-id="5e52a-159">no</span></span>        |
| [<span data-ttu-id="5e52a-160">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5e52a-160">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="5e52a-161">nein</span><span class="sxs-lookup"><span data-stu-id="5e52a-161">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="5e52a-162">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5e52a-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e52a-163">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5e52a-163">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





