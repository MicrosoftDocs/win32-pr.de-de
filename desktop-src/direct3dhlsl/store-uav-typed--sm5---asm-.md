---
title: store_uav_typed (SM5-ASM)
description: Zufälliger Zugriff auf das Schreiben eines Elements in eine typisierte, unsortierter Zugriffs Ansicht (UAV).
ms.assetid: AD8E035B-DACD-4241-A05B-7D6DC8E3222C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6243e6fbb2092bac699dbbce04cb3c3478880866
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104038322"
---
# <a name="store_uav_typed-sm5---asm"></a><span data-ttu-id="b46d2-103">Store- \_ UAV \_ -typisiert (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="b46d2-103">store\_uav\_typed (sm5 - asm)</span></span>

<span data-ttu-id="b46d2-104">Zufälliger Zugriff auf das Schreiben eines Elements in eine typisierte, unsortierter Zugriffs Ansicht (UAV).</span><span class="sxs-lookup"><span data-stu-id="b46d2-104">Random-access write of an element into a typed unordered access view (UAV).</span></span>



| <span data-ttu-id="b46d2-105">Store \_ UAV \_ typisiertes dstuav. xyzw, dstaddress \[ . Swizzle \] , src0 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="b46d2-105">store\_uav\_typed dstUAV.xyzw, dstAddress\[.swizzle\], src0\[.swizzle\]</span></span> |
|-------------------------------------------------------------------------|



 



| <span data-ttu-id="b46d2-106">Element</span><span class="sxs-lookup"><span data-stu-id="b46d2-106">Item</span></span>                                                                                                           | <span data-ttu-id="b46d2-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b46d2-107">Description</span></span>                                             |
|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="b46d2-108"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstuav*</span><span class="sxs-lookup"><span data-stu-id="b46d2-108"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*</span></span><br/>                 | <span data-ttu-id="b46d2-109">\[in \] enthält das Ergebnis des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="b46d2-109">\[in\] Contains the result of the operation.</span></span><br/> |
| <span data-ttu-id="b46d2-110"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstaddress*</span><span class="sxs-lookup"><span data-stu-id="b46d2-110"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span></span><br/> | <span data-ttu-id="b46d2-111">\[in \] der Adresse, an der geschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="b46d2-111">\[in\] The address at which to write.</span></span><br/>        |
| <span data-ttu-id="b46d2-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="b46d2-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                | <span data-ttu-id="b46d2-113">\[in \] den zu schreibende Komponenten.</span><span class="sxs-lookup"><span data-stu-id="b46d2-113">\[in\] The components to write.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="b46d2-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b46d2-114">Remarks</span></span>

<span data-ttu-id="b46d2-115">Diese Anweisung führt ein 4 \* -Bit-32-Bit-Element aus, das von *src0* auf *dstuav* an der Adresse in *dstaddress* geschrieben wurde.</span><span class="sxs-lookup"><span data-stu-id="b46d2-115">This instruction performs a 4 component \*32-bit element written from *src0* to *dstUAV* at the address in *dstAddress*.</span></span> <span data-ttu-id="b46d2-116">*dstuav* ist ein typisiertes UAV (u \# ).</span><span class="sxs-lookup"><span data-stu-id="b46d2-116">*dstUAV* is a typed UAV (u\#).</span></span>

<span data-ttu-id="b46d2-117">Das Format der UAV bestimmt die Formatkonvertierung.</span><span class="sxs-lookup"><span data-stu-id="b46d2-117">The format of the UAV determines format conversion.</span></span>

<span data-ttu-id="b46d2-118">Die Anzahl der Komponenten, die von der Adresse aus der 32-Bit-Ganzzahl ohne Vorzeichen entnommen werden, hängt von der Dimensionalität der in *dstuav* deklarierten Ressource ab.</span><span class="sxs-lookup"><span data-stu-id="b46d2-118">The number of 32-bit unsigned integer components taken from the address are determined by the dimensionality of the resource declared at *dstUAV*.</span></span> <span data-ttu-id="b46d2-119">Diese Adresse befindet sich in-Elementen.</span><span class="sxs-lookup"><span data-stu-id="b46d2-119">This address is in elements.</span></span>

<span data-ttu-id="b46d2-120">Die Adressierung außerhalb der Grenzen bedeutet, dass nichts in den Speicher geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="b46d2-120">Out of bounds addressing means nothing gets written to memory.</span></span>

<span data-ttu-id="b46d2-121">*dstuav* hat immer eine. xyzw-Schreib Maske.</span><span class="sxs-lookup"><span data-stu-id="b46d2-121">*dstUAV* always has a .xyzw write mask.</span></span> <span data-ttu-id="b46d2-122">Alle Komponenten müssen geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="b46d2-122">All components must be written.</span></span>

<span data-ttu-id="b46d2-123">Es ist ungültig und nicht definiert, diese Anweisung für eine UAV zu verwenden, die nicht als typisiert deklariert ist.</span><span class="sxs-lookup"><span data-stu-id="b46d2-123">It is invalid and undefined to use this instruction on a UAV that is not declared as typed.</span></span> <span data-ttu-id="b46d2-124">Das heißt, dass dies auf einer strukturierten oder typlosen UAV durchgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="b46d2-124">That is, doing this on a structured or typeless UAV is invalid.</span></span>

<span data-ttu-id="b46d2-125">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="b46d2-125">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="b46d2-126">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="b46d2-126">Vertex</span></span> | <span data-ttu-id="b46d2-127">Hülle</span><span class="sxs-lookup"><span data-stu-id="b46d2-127">Hull</span></span> | <span data-ttu-id="b46d2-128">Domain</span><span class="sxs-lookup"><span data-stu-id="b46d2-128">Domain</span></span> | <span data-ttu-id="b46d2-129">Geometrie</span><span class="sxs-lookup"><span data-stu-id="b46d2-129">Geometry</span></span> | <span data-ttu-id="b46d2-130">Pixel</span><span class="sxs-lookup"><span data-stu-id="b46d2-130">Pixel</span></span> | <span data-ttu-id="b46d2-131">Compute</span><span class="sxs-lookup"><span data-stu-id="b46d2-131">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="b46d2-132">X</span><span class="sxs-lookup"><span data-stu-id="b46d2-132">X</span></span>     | <span data-ttu-id="b46d2-133">X</span><span class="sxs-lookup"><span data-stu-id="b46d2-133">X</span></span>       |



 

<span data-ttu-id="b46d2-134">Da UAVs in allen Shader-Phasen für Direct3D 11,1 verfügbar sind, gilt diese Anweisung für alle Shader-Phasen für die Direct3D 11,1-Laufzeit, die ab Windows 8 verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="b46d2-134">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="b46d2-135">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="b46d2-135">Vertex</span></span> | <span data-ttu-id="b46d2-136">Hülle</span><span class="sxs-lookup"><span data-stu-id="b46d2-136">Hull</span></span> | <span data-ttu-id="b46d2-137">Domain</span><span class="sxs-lookup"><span data-stu-id="b46d2-137">Domain</span></span> | <span data-ttu-id="b46d2-138">Geometrie</span><span class="sxs-lookup"><span data-stu-id="b46d2-138">Geometry</span></span> | <span data-ttu-id="b46d2-139">Pixel</span><span class="sxs-lookup"><span data-stu-id="b46d2-139">Pixel</span></span> | <span data-ttu-id="b46d2-140">Compute</span><span class="sxs-lookup"><span data-stu-id="b46d2-140">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="b46d2-141">X</span><span class="sxs-lookup"><span data-stu-id="b46d2-141">X</span></span>      | <span data-ttu-id="b46d2-142">X</span><span class="sxs-lookup"><span data-stu-id="b46d2-142">X</span></span>    | <span data-ttu-id="b46d2-143">X</span><span class="sxs-lookup"><span data-stu-id="b46d2-143">X</span></span>      | <span data-ttu-id="b46d2-144">X</span><span class="sxs-lookup"><span data-stu-id="b46d2-144">X</span></span>        | <span data-ttu-id="b46d2-145">X</span><span class="sxs-lookup"><span data-stu-id="b46d2-145">X</span></span>     | <span data-ttu-id="b46d2-146">X</span><span class="sxs-lookup"><span data-stu-id="b46d2-146">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="b46d2-147">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="b46d2-147">Minimum Shader Model</span></span>

<span data-ttu-id="b46d2-148">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="b46d2-148">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="b46d2-149">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="b46d2-149">Shader Model</span></span>                                              | <span data-ttu-id="b46d2-150">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="b46d2-150">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="b46d2-151">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="b46d2-151">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="b46d2-152">ja</span><span class="sxs-lookup"><span data-stu-id="b46d2-152">yes</span></span>       |
| [<span data-ttu-id="b46d2-153">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="b46d2-153">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="b46d2-154">nein</span><span class="sxs-lookup"><span data-stu-id="b46d2-154">no</span></span>        |
| [<span data-ttu-id="b46d2-155">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="b46d2-155">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="b46d2-156">nein</span><span class="sxs-lookup"><span data-stu-id="b46d2-156">no</span></span>        |
| [<span data-ttu-id="b46d2-157">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b46d2-157">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="b46d2-158">nein</span><span class="sxs-lookup"><span data-stu-id="b46d2-158">no</span></span>        |
| [<span data-ttu-id="b46d2-159">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b46d2-159">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="b46d2-160">nein</span><span class="sxs-lookup"><span data-stu-id="b46d2-160">no</span></span>        |
| [<span data-ttu-id="b46d2-161">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b46d2-161">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="b46d2-162">nein</span><span class="sxs-lookup"><span data-stu-id="b46d2-162">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="b46d2-163">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b46d2-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b46d2-164">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b46d2-164">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





