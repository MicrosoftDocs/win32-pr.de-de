---
title: DFMA (SM5-ASM)
description: Führt ein Add-in mit einer Fused-Multiplikation aus
ms.assetid: 5BE96CDB-1756-4EBE-B4CC-69EFF098A4F1
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2e6cafc71dbc7d57655524b1b87c9c5b9ba20f3
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313656"
---
# <a name="dfma-sm5---asm"></a><span data-ttu-id="eafaf-103">DFMA (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="eafaf-103">dfma (sm5 - asm)</span></span>

<span data-ttu-id="eafaf-104">Führt ein Add-in mit einer Fused-Multiplikation aus</span><span class="sxs-lookup"><span data-stu-id="eafaf-104">Performs a fused-multiply add.</span></span>



| <span data-ttu-id="eafaf-105">DFMA \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] Quelle1 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] Quelle2 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="eafaf-105">dfma\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\],\[-\]src2\[\_abs\]\[.swizzle\]</span></span> |
|----------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="eafaf-106">Element</span><span class="sxs-lookup"><span data-stu-id="eafaf-106">Item</span></span>                                                            | <span data-ttu-id="eafaf-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eafaf-107">Description</span></span>                                                                                                                                               |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eafaf-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="eafaf-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="eafaf-109">\[in \] der Adresse des Vorgangs Ergebnisses.</span><span class="sxs-lookup"><span data-stu-id="eafaf-109">\[in\] The address of the result of the operation.</span></span> <span data-ttu-id="eafaf-110">Der Ergebniswert muss auf 0,5 ULP genau sein.</span><span class="sxs-lookup"><span data-stu-id="eafaf-110">The result value must be accurate to 0.5 ULP.</span></span><br/> <span data-ttu-id="eafaf-111">*dest*  =  *src0* \* *Quelle1*  +  *Quelle2*</span><span class="sxs-lookup"><span data-stu-id="eafaf-111">*dest* = *src0* \* *src1* + *src2*</span></span><br/> |
| <span data-ttu-id="eafaf-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="eafaf-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="eafaf-113">\[in \] den Komponenten, die mit *Quelle1* multipliziert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="eafaf-113">\[in\] The components to multiply with *src1*.</span></span><br/>                                                                                                 |
| <span data-ttu-id="eafaf-114"><span id="src1"></span><span id="SRC1"></span>*Quelle1*</span><span class="sxs-lookup"><span data-stu-id="eafaf-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="eafaf-115">\[in \] den Komponenten, die mit *src0* multipliziert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="eafaf-115">\[in\] The components to multiply with *src0*.</span></span><br/>                                                                                                 |
| <span data-ttu-id="eafaf-116"><span id="src2"></span><span id="SRC2"></span>*Quelle2*</span><span class="sxs-lookup"><span data-stu-id="eafaf-116"><span id="src2"></span><span id="SRC2"></span>*src2*</span></span><br/> | <span data-ttu-id="eafaf-117">\[in \] den Komponenten, die zu *src0* Quelle1 hinzugefügt werden sollen \* .</span><span class="sxs-lookup"><span data-stu-id="eafaf-117">\[in\] The components to add to *src0* \* *src1*.</span></span><br/>                                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="eafaf-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eafaf-118">Remarks</span></span>

<span data-ttu-id="eafaf-119">Shader, die diese Anweisung verwenden, werden mit einem shaderflag gekennzeichnet, das dazu führt, dass Sie nicht gebunden werden, es sei denn, die folgenden Bedingungen sind erfüllt.</span><span class="sxs-lookup"><span data-stu-id="eafaf-119">Shaders that use this instruction will be marked with a shader flag that will cause them to fail to bind unless all the following conditions are met.</span></span>

-   <span data-ttu-id="eafaf-120">Das System unterstützt DirectX 11,1.</span><span class="sxs-lookup"><span data-stu-id="eafaf-120">The system supports DirectX 11.1.</span></span>
-   <span data-ttu-id="eafaf-121">Das System enthält einen WDDM 1,2-Treiber.</span><span class="sxs-lookup"><span data-stu-id="eafaf-121">The system includes a WDDM 1.2 driver.</span></span>
-   <span data-ttu-id="eafaf-122">Der Treiber meldet die Unterstützung für diese Anweisung über **D3D11 \_ Feature \_ Data \_ D3D11 \_ options. "Extendeddoublesshaderinstructions** " ist auf " **true**" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="eafaf-122">The driver reports support for this instruction via **D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS.ExtendedDoublesShaderInstructions** set to **TRUE**.</span></span>

<span data-ttu-id="eafaf-123">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="eafaf-123">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="eafaf-124">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="eafaf-124">Vertex</span></span> | <span data-ttu-id="eafaf-125">Hülle</span><span class="sxs-lookup"><span data-stu-id="eafaf-125">Hull</span></span> | <span data-ttu-id="eafaf-126">Domain</span><span class="sxs-lookup"><span data-stu-id="eafaf-126">Domain</span></span> | <span data-ttu-id="eafaf-127">Geometrie</span><span class="sxs-lookup"><span data-stu-id="eafaf-127">Geometry</span></span> | <span data-ttu-id="eafaf-128">Pixel</span><span class="sxs-lookup"><span data-stu-id="eafaf-128">Pixel</span></span> | <span data-ttu-id="eafaf-129">Compute</span><span class="sxs-lookup"><span data-stu-id="eafaf-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="eafaf-130">X</span><span class="sxs-lookup"><span data-stu-id="eafaf-130">X</span></span>      | <span data-ttu-id="eafaf-131">X</span><span class="sxs-lookup"><span data-stu-id="eafaf-131">X</span></span>    | <span data-ttu-id="eafaf-132">X</span><span class="sxs-lookup"><span data-stu-id="eafaf-132">X</span></span>      | <span data-ttu-id="eafaf-133">X</span><span class="sxs-lookup"><span data-stu-id="eafaf-133">X</span></span>        | <span data-ttu-id="eafaf-134">X</span><span class="sxs-lookup"><span data-stu-id="eafaf-134">X</span></span>     | <span data-ttu-id="eafaf-135">X</span><span class="sxs-lookup"><span data-stu-id="eafaf-135">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="eafaf-136">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="eafaf-136">Minimum Shader Model</span></span>

<span data-ttu-id="eafaf-137">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="eafaf-137">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="eafaf-138">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="eafaf-138">Shader Model</span></span>                                              | <span data-ttu-id="eafaf-139">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="eafaf-139">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="eafaf-140">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="eafaf-140">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="eafaf-141">ja</span><span class="sxs-lookup"><span data-stu-id="eafaf-141">yes</span></span>       |
| [<span data-ttu-id="eafaf-142">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="eafaf-142">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="eafaf-143">nein</span><span class="sxs-lookup"><span data-stu-id="eafaf-143">no</span></span>        |
| [<span data-ttu-id="eafaf-144">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="eafaf-144">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="eafaf-145">nein</span><span class="sxs-lookup"><span data-stu-id="eafaf-145">no</span></span>        |
| [<span data-ttu-id="eafaf-146">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="eafaf-146">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="eafaf-147">nein</span><span class="sxs-lookup"><span data-stu-id="eafaf-147">no</span></span>        |
| [<span data-ttu-id="eafaf-148">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="eafaf-148">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="eafaf-149">nein</span><span class="sxs-lookup"><span data-stu-id="eafaf-149">no</span></span>        |
| [<span data-ttu-id="eafaf-150">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="eafaf-150">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="eafaf-151">nein</span><span class="sxs-lookup"><span data-stu-id="eafaf-151">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="eafaf-152">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="eafaf-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eafaf-153">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="eafaf-153">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





