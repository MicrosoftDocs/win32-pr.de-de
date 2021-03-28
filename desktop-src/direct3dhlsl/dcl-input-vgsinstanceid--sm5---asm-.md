---
title: dcl_input vgsinstanceid (SM5-ASM)
description: Aktivieren Sie die Instanziierung von Geometry-Shader.
ms.assetid: 47B9BAD5-0FFF-4DB7-B34A-7811B8A4F792
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3134a9d372f1fde5457f26235fe9a6a5439c58c1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313763"
---
# <a name="dcl_input-vgsinstanceid-sm5---asm"></a><span data-ttu-id="6f8d3-103">DCL \_ -Eingabe vgsinstanceid (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="6f8d3-103">dcl\_input vGSInstanceID (sm5 - asm)</span></span>

<span data-ttu-id="6f8d3-104">Aktivieren Sie die Instanziierung von Geometry-Shader.</span><span class="sxs-lookup"><span data-stu-id="6f8d3-104">Enable geometry shader instancing.</span></span>



| <span data-ttu-id="6f8d3-105">DCL \_ -Eingabe vgsinstanceid, InstanceCount</span><span class="sxs-lookup"><span data-stu-id="6f8d3-105">dcl\_input vGSInstanceID, instanceCount</span></span> |
|-----------------------------------------|



 



| <span data-ttu-id="6f8d3-106">Element</span><span class="sxs-lookup"><span data-stu-id="6f8d3-106">Item</span></span>                                                                                                                       | <span data-ttu-id="6f8d3-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6f8d3-107">Description</span></span>                           |
|----------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span data-ttu-id="6f8d3-108"><span id="vGSInstanceID"></span><span id="vgsinstanceid"></span><span id="VGSINSTANCEID"></span>*vgsinstanceid*</span><span class="sxs-lookup"><span data-stu-id="6f8d3-108"><span id="vGSInstanceID"></span><span id="vgsinstanceid"></span><span id="VGSINSTANCEID"></span>*vGSInstanceID*</span></span><br/> | <span data-ttu-id="6f8d3-109">\[in \] der Instanz-ID.</span><span class="sxs-lookup"><span data-stu-id="6f8d3-109">\[in\] The instance ID.</span></span><br/>    |
| <span data-ttu-id="6f8d3-110"><span id="instanceCount"></span><span id="instancecount"></span><span id="INSTANCECOUNT"></span>*instanceCount*</span><span class="sxs-lookup"><span data-stu-id="6f8d3-110"><span id="instanceCount"></span><span id="instancecount"></span><span id="INSTANCECOUNT"></span>*instanceCount*</span></span><br/> | <span data-ttu-id="6f8d3-111">\[in \] der Instanzanzahl.</span><span class="sxs-lookup"><span data-stu-id="6f8d3-111">\[in\] The instance count.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6f8d3-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6f8d3-112">Remarks</span></span>

<span data-ttu-id="6f8d3-113">Der *InstanceCount* -Parameter der Deklaration gibt an, wie viele Instanzen der Geometry-Shader für jede Eingabe primitive ausführen soll.</span><span class="sxs-lookup"><span data-stu-id="6f8d3-113">The *instanceCount* parameter of the declaration specifies how many instances the geometry shader should execute for each input primitive.</span></span> <span data-ttu-id="6f8d3-114">Der maximale Wert für *InstanceCount* ist 32.</span><span class="sxs-lookup"><span data-stu-id="6f8d3-114">The maximum value for *instanceCount* is 32.</span></span>

<span data-ttu-id="6f8d3-115">Die maximale Anzahl der für die Ausgabe deklarierten Scheitel Punkte über [**DCL \_ maxoutputvertexcount**](dcl-maxoutputvertexcount.md)gilt einzeln für jede Instanz.</span><span class="sxs-lookup"><span data-stu-id="6f8d3-115">The maximum number of vertices declared for output, via [**dcl\_maxOutputVertexCount**](dcl-maxoutputvertexcount.md), applies individually to each instance.</span></span>

<span data-ttu-id="6f8d3-116">Die Anzahl der Instanzen in dieser Deklaration, multipliziert mit der maximalen Vertex-Anzahl pro Instanz über [**DCL \_ maxoutputvertexcount**](dcl-maxoutputvertexcount.md), muss <= 1024 sein.</span><span class="sxs-lookup"><span data-stu-id="6f8d3-116">The instance count in this declaration, multiplied by the maximum vertex count per instance via [**dcl\_maxOutputVertexCount**](dcl-maxoutputvertexcount.md), must be <= 1024.</span></span>

<span data-ttu-id="6f8d3-117">Die Datenmenge, die eine bestimmte Geometry-Shader-Instanz ausgeben kann, beträgt 1024 skalare Höchstwerte, die überprüft werden, indem alle für die Eingabe deklarierten Skars gezählt und die Anzahl der deklarierten Ausgabe Vertex multipliziert wird.</span><span class="sxs-lookup"><span data-stu-id="6f8d3-117">The amount of data that a given geometry shader instance can emit is 1024 scalars maximum, validated by counting up all scalars declared for input and multiplying by the declared output vertex count.</span></span>

<span data-ttu-id="6f8d3-118">Die Verwendung der Geometrie-Shader-Instanziierung erhöht die Gesamtmenge der Daten, die pro Eingabe primitive ausgegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="6f8d3-118">Use of geometry shader instancing effectively increases the total amount of data that can be emitted per input primitive.</span></span> <span data-ttu-id="6f8d3-119">1024 skalare für eine einzelne Instanz ergeben bis zu 1024 \* 32 skalare der Ausgabedaten für alle Geometry-Shader-Instanzen für einen einzelnen Eingabe primitive.</span><span class="sxs-lookup"><span data-stu-id="6f8d3-119">1024 scalars for a single instance yields up to 1024\*32 scalars of output data across all geometry shader instances for a single input primitive.</span></span> <span data-ttu-id="6f8d3-120">Je mehr Instanzen jedoch, desto weniger Scheitel Punkte können von jeder Instanz ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="6f8d3-120">However the more instances, the fewer vertices each instance can emit.</span></span> <span data-ttu-id="6f8d3-121">Eine einzelne Instanz (keine Instanziierung) kann 1024 Vertices ausgeben.</span><span class="sxs-lookup"><span data-stu-id="6f8d3-121">A single instance (no instancing) can emit 1024 vertices.</span></span> <span data-ttu-id="6f8d3-122">Wenn Sie 32-Instanzen deklarieren, \* bedeutet dies, dass jede Instanz nur 1024/32 = 32 Vertices ausgeben kann.</span><span class="sxs-lookup"><span data-stu-id="6f8d3-122">If you declare \*32 instances it means each instance can only output 1024/32 = 32 vertices.</span></span>

<span data-ttu-id="6f8d3-123">Die Geometry-Shader-instanziierungsdeklaration stellt dem Programm ein eigenständiges 32-Bit-Ganzzahl-Eingabe Register ( *vgsinstanceid*) zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="6f8d3-123">The geometry shader instancing declaration makes available to the program a standalone 32-bit integer input register, *vGSInstanceID*.</span></span> <span data-ttu-id="6f8d3-124">Jede Geometry-Shader-Instanz wird durch den Wert identifiziert, der in " *vgsinstanceid* \[ 0, 1, 2..." enthalten \] ist.</span><span class="sxs-lookup"><span data-stu-id="6f8d3-124">Each geometry shader instance is identified by the value contained in *vGSInstanceID* \[0,1,2...\].</span></span>

<span data-ttu-id="6f8d3-125">*vgsinstanceid* ist nicht Teil des Geometry-Shader-Eingabe Vertex-Arrays (z. b. 3 Scheitel Punkte beim Einfügen eines Dreiecks).</span><span class="sxs-lookup"><span data-stu-id="6f8d3-125">*vGSInstanceID* is not part of the geometry shader input vertex array (e.g. 3 vertices when inputting a triangle).</span></span> <span data-ttu-id="6f8d3-126">Das *vgsinstanceid-* Register steht eigenständig, wie z. b. vprimitiveid.</span><span class="sxs-lookup"><span data-stu-id="6f8d3-126">The *vGSInstanceID* register stands on its own, like vPrimitiveID.</span></span>

<span data-ttu-id="6f8d3-127">Wenn jede Geometry-Shader-Instanz beendet wird, gibt es eine implizite Ausschneide in der Ausgabe Topologie, sodass aufeinander folgende Instanzen nicht voneinander abhängen.</span><span class="sxs-lookup"><span data-stu-id="6f8d3-127">When each geometry shader instance ends, there is an implicit cut in the output topology, so consecutive instances do not depend on each other.</span></span>

<span data-ttu-id="6f8d3-128">Obwohl jede Geometry-Shader-Instanz von der Hardware parallel ausgeführt werden kann, wird die Ausgabe aller Instanzen am Ende serialisiert, als ob alle instanzierten Geometry-shaderaufrufe nacheinander in einer Schleife ausgeführt werden, die *vgsinstanceid* von 0 bis *InstanceCount*-1 durchläuft, wobei am Ende jeder Instanz ein impliziter Wert für die Ausgabe Topologie erfolgt.</span><span class="sxs-lookup"><span data-stu-id="6f8d3-128">Although hardware may execute each geometry shader instance in parallel, the output of all instances at the end is serialized as if all the instanced geometry shader invocations ran sequentially in a loop iterating *vGSInstanceID* from 0 to *instanceCount*-1, with implicit output topology cuts at the end of each instance.</span></span>

<span data-ttu-id="6f8d3-129">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="6f8d3-129">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="6f8d3-130">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="6f8d3-130">Vertex</span></span> | <span data-ttu-id="6f8d3-131">Hülle</span><span class="sxs-lookup"><span data-stu-id="6f8d3-131">Hull</span></span> | <span data-ttu-id="6f8d3-132">Domain</span><span class="sxs-lookup"><span data-stu-id="6f8d3-132">Domain</span></span> | <span data-ttu-id="6f8d3-133">Geometrie</span><span class="sxs-lookup"><span data-stu-id="6f8d3-133">Geometry</span></span> | <span data-ttu-id="6f8d3-134">Pixel</span><span class="sxs-lookup"><span data-stu-id="6f8d3-134">Pixel</span></span> | <span data-ttu-id="6f8d3-135">Compute</span><span class="sxs-lookup"><span data-stu-id="6f8d3-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        | <span data-ttu-id="6f8d3-136">X</span><span class="sxs-lookup"><span data-stu-id="6f8d3-136">X</span></span>        |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="6f8d3-137">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="6f8d3-137">Minimum Shader Model</span></span>

<span data-ttu-id="6f8d3-138">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="6f8d3-138">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="6f8d3-139">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="6f8d3-139">Shader Model</span></span>                                              | <span data-ttu-id="6f8d3-140">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="6f8d3-140">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="6f8d3-141">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="6f8d3-141">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="6f8d3-142">ja</span><span class="sxs-lookup"><span data-stu-id="6f8d3-142">yes</span></span>       |
| [<span data-ttu-id="6f8d3-143">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="6f8d3-143">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="6f8d3-144">nein</span><span class="sxs-lookup"><span data-stu-id="6f8d3-144">no</span></span>        |
| [<span data-ttu-id="6f8d3-145">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="6f8d3-145">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="6f8d3-146">nein</span><span class="sxs-lookup"><span data-stu-id="6f8d3-146">no</span></span>        |
| [<span data-ttu-id="6f8d3-147">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6f8d3-147">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="6f8d3-148">nein</span><span class="sxs-lookup"><span data-stu-id="6f8d3-148">no</span></span>        |
| [<span data-ttu-id="6f8d3-149">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6f8d3-149">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="6f8d3-150">nein</span><span class="sxs-lookup"><span data-stu-id="6f8d3-150">no</span></span>        |
| [<span data-ttu-id="6f8d3-151">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6f8d3-151">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="6f8d3-152">nein</span><span class="sxs-lookup"><span data-stu-id="6f8d3-152">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="6f8d3-153">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6f8d3-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6f8d3-154">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6f8d3-154">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





