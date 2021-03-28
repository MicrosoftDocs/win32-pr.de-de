---
title: ld_uav_typed (SM5-ASM)
description: Zufälliger Zugriffs Lesevorgang eines Elements aus einer typisierten nicht geordneten Zugriffs Ansicht (UAV).
ms.assetid: E5E03311-3596-4497-9271-FE6445DBFC62
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61b22392c802378c094b443c8ff2f2282909bd1f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313680"
---
# <a name="ld_uav_typed-sm5---asm"></a><span data-ttu-id="0b77f-103">LD \_ UAV \_ -typisiert (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="0b77f-103">ld\_uav\_typed (sm5 - asm)</span></span>

<span data-ttu-id="0b77f-104">Zufälliger Zugriffs Lesevorgang eines Elements aus einer typisierten nicht geordneten Zugriffs Ansicht (UAV).</span><span class="sxs-lookup"><span data-stu-id="0b77f-104">Random-access read of an element from a typed unordered access view (UAV).</span></span>



| <span data-ttu-id="0b77f-105">LD \_ UAV \_ typisiert dst0 \[ . mask \] , srcaddress \[ . Swizzle \] , srcuav \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="0b77f-105">ld\_uav\_typed dst0\[.mask\], srcAddress\[.swizzle\], srcUAV\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------|



 



| <span data-ttu-id="0b77f-106">Element</span><span class="sxs-lookup"><span data-stu-id="0b77f-106">Item</span></span>                                                                                                           | <span data-ttu-id="0b77f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0b77f-107">Description</span></span>                                                    |
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="0b77f-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="0b77f-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                                | <span data-ttu-id="0b77f-109">\[in \] der Adresse der Ergebnisse des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="0b77f-109">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="0b77f-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcaddress*</span><span class="sxs-lookup"><span data-stu-id="0b77f-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/> | <span data-ttu-id="0b77f-111">\[in \] gibt die Adresse an, aus der gelesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="0b77f-111">\[in\] Specifies the address to read from.</span></span><br/>          |
| <span data-ttu-id="0b77f-112"><span id="srcUAV"></span><span id="srcuav"></span><span id="SRCUAV"></span>*srcuav*</span><span class="sxs-lookup"><span data-stu-id="0b77f-112"><span id="srcUAV"></span><span id="srcuav"></span><span id="SRCUAV"></span>*srcUAV*</span></span><br/>                 | <span data-ttu-id="0b77f-113">\[in \] der Quelle, aus der gelesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="0b77f-113">\[in\] The source to read from.</span></span> <br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="0b77f-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0b77f-114">Remarks</span></span>

<span data-ttu-id="0b77f-115">Diese Anweisung führt ein aus *srcuav* gelesene 4-Component-Element an der ganzzahligen Adresse ohne Vorzeichen in *srcaddress* aus, die auf Grundlage des Formats in 32-Bit pro Komponente konvertiert und dann im Shader in *dst0* geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="0b77f-115">This instruction performs a 4-component element read from *srcUAV* at the unsigned integer address in *srcAddress*, converted to 32bit per component based on the format, then written to *dst0* in the shader.</span></span>

<span data-ttu-id="0b77f-116">*srcuav* ist ein UAV (u \# ), das als typisiert deklariert ist.</span><span class="sxs-lookup"><span data-stu-id="0b77f-116">*srcUAV* is a UAV (u\#) declared as typed.</span></span> <span data-ttu-id="0b77f-117">Der Typ der gebundenen Ressource muss jedoch "R32 \_ uint/Sint/float" lauten.</span><span class="sxs-lookup"><span data-stu-id="0b77f-117">However, the type of the bound resource must be R32\_UINT/SINT/FLOAT.</span></span>

<span data-ttu-id="0b77f-118">Die Anzahl der Komponenten, die von der Adresse aus der 32-Bit-Ganzzahl ohne Vorzeichen entnommen werden, hängt von der Dimensionalität der in *srcuav* deklarierten Ressource ab.</span><span class="sxs-lookup"><span data-stu-id="0b77f-118">The number of 32-bit unsigned integer components taken from the address are determined by the dimensionality of the resource declared at *srcUAV*.</span></span> <span data-ttu-id="0b77f-119">Adressierung ist mit der [LD](ld--sm4---asm-.md) -Anweisung identisch.</span><span class="sxs-lookup"><span data-stu-id="0b77f-119">Addressing is the same as the [ld](ld--sm4---asm-.md) instruction.</span></span>

<span data-ttu-id="0b77f-120">Die Adressierung außerhalb der Begrenzungen ist mit der **LD** -Anweisung identisch.</span><span class="sxs-lookup"><span data-stu-id="0b77f-120">Out of bounds addressing is the same as the **ld** instruction.</span></span>

<span data-ttu-id="0b77f-121">Das Verhalten dieser Anweisung ist mit der **LD** -Anweisung identisch, wenn Sie als **LD dst0 \[ . mask \] , srcaddress \[ . Swizzle \] , srcuav \[ . Swizzle \]** aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="0b77f-121">The behavior of this instruction is identical to the **ld** instruction if called as **ld dst0\[.mask\], srcAddress\[.swizzle\], srcUAV\[.swizzle\]**</span></span>

<span data-ttu-id="0b77f-122">Es ist ungültig und nicht definiert, diese Anweisung für eine UAV zu verwenden, die nicht als typisiert deklariert ist.</span><span class="sxs-lookup"><span data-stu-id="0b77f-122">It is invalid and undefined to use this instruction on a UAV that is not declared as typed.</span></span> <span data-ttu-id="0b77f-123">Eine strukturierte oder typlose UAV ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="0b77f-123">Doing this on a structured or typeless UAV is invalid.</span></span>

<span data-ttu-id="0b77f-124">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="0b77f-124">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="0b77f-125">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="0b77f-125">Vertex</span></span> | <span data-ttu-id="0b77f-126">Hülle</span><span class="sxs-lookup"><span data-stu-id="0b77f-126">Hull</span></span> | <span data-ttu-id="0b77f-127">Domain</span><span class="sxs-lookup"><span data-stu-id="0b77f-127">Domain</span></span> | <span data-ttu-id="0b77f-128">Geometrie</span><span class="sxs-lookup"><span data-stu-id="0b77f-128">Geometry</span></span> | <span data-ttu-id="0b77f-129">Pixel</span><span class="sxs-lookup"><span data-stu-id="0b77f-129">Pixel</span></span> | <span data-ttu-id="0b77f-130">Compute</span><span class="sxs-lookup"><span data-stu-id="0b77f-130">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="0b77f-131">X</span><span class="sxs-lookup"><span data-stu-id="0b77f-131">X</span></span>     | <span data-ttu-id="0b77f-132">X</span><span class="sxs-lookup"><span data-stu-id="0b77f-132">X</span></span>       |



 

<span data-ttu-id="0b77f-133">Da UAVs in allen Shader-Phasen für Direct3D 11,1 verfügbar sind, gilt diese Anweisung für alle Shader-Phasen für die Direct3D 11,1-Laufzeit, die ab Windows 8 verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="0b77f-133">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="0b77f-134">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="0b77f-134">Vertex</span></span> | <span data-ttu-id="0b77f-135">Hülle</span><span class="sxs-lookup"><span data-stu-id="0b77f-135">Hull</span></span> | <span data-ttu-id="0b77f-136">Domain</span><span class="sxs-lookup"><span data-stu-id="0b77f-136">Domain</span></span> | <span data-ttu-id="0b77f-137">Geometrie</span><span class="sxs-lookup"><span data-stu-id="0b77f-137">Geometry</span></span> | <span data-ttu-id="0b77f-138">Pixel</span><span class="sxs-lookup"><span data-stu-id="0b77f-138">Pixel</span></span> | <span data-ttu-id="0b77f-139">Compute</span><span class="sxs-lookup"><span data-stu-id="0b77f-139">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="0b77f-140">X</span><span class="sxs-lookup"><span data-stu-id="0b77f-140">X</span></span>      | <span data-ttu-id="0b77f-141">X</span><span class="sxs-lookup"><span data-stu-id="0b77f-141">X</span></span>    | <span data-ttu-id="0b77f-142">X</span><span class="sxs-lookup"><span data-stu-id="0b77f-142">X</span></span>      | <span data-ttu-id="0b77f-143">X</span><span class="sxs-lookup"><span data-stu-id="0b77f-143">X</span></span>        | <span data-ttu-id="0b77f-144">X</span><span class="sxs-lookup"><span data-stu-id="0b77f-144">X</span></span>     | <span data-ttu-id="0b77f-145">X</span><span class="sxs-lookup"><span data-stu-id="0b77f-145">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="0b77f-146">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="0b77f-146">Minimum Shader Model</span></span>

<span data-ttu-id="0b77f-147">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="0b77f-147">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="0b77f-148">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="0b77f-148">Shader Model</span></span>                                              | <span data-ttu-id="0b77f-149">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="0b77f-149">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="0b77f-150">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="0b77f-150">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="0b77f-151">ja</span><span class="sxs-lookup"><span data-stu-id="0b77f-151">yes</span></span>       |
| [<span data-ttu-id="0b77f-152">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="0b77f-152">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="0b77f-153">nein</span><span class="sxs-lookup"><span data-stu-id="0b77f-153">no</span></span>        |
| [<span data-ttu-id="0b77f-154">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="0b77f-154">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="0b77f-155">nein</span><span class="sxs-lookup"><span data-stu-id="0b77f-155">no</span></span>        |
| [<span data-ttu-id="0b77f-156">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0b77f-156">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="0b77f-157">nein</span><span class="sxs-lookup"><span data-stu-id="0b77f-157">no</span></span>        |
| [<span data-ttu-id="0b77f-158">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0b77f-158">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="0b77f-159">nein</span><span class="sxs-lookup"><span data-stu-id="0b77f-159">no</span></span>        |
| [<span data-ttu-id="0b77f-160">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0b77f-160">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="0b77f-161">nein</span><span class="sxs-lookup"><span data-stu-id="0b77f-161">no</span></span>        |



 

<span data-ttu-id="0b77f-162">CS \_ 4 \_ 0 und CS \_ 4 \_ 1 unterstützen diese Anweisung für UAV, SRV und TGSM.</span><span class="sxs-lookup"><span data-stu-id="0b77f-162">cs\_4\_0 and cs\_4\_1 support this instruction for UAV, SRV and TGSM.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0b77f-163">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0b77f-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b77f-164">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0b77f-164">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





