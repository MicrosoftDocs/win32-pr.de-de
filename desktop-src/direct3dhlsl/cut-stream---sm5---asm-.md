---
title: cut_stream (SM5-ASM)
description: Die Geometry-Shader-Anweisung, die die aktuelle primitive Topologie im angegebenen Stream abschließt, wenn eine beliebige Scheitel Punkte ausgegeben wurden, und startet eine neue Topologie des Typs, der vom Geometry-Shader in diesem Stream deklariert wird.
ms.assetid: CEFDD13B-34FD-4E9C-94A0-CB8879A7DBDE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4650628d7f6b66130568f885e008a5163a9ee44f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389508"
---
# <a name="cut_stream-sm5---asm"></a><span data-ttu-id="86ee7-103">Ausschneide Daten \_ Strom (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="86ee7-103">cut\_stream (sm5 - asm)</span></span>

<span data-ttu-id="86ee7-104">Die Geometry-Shader-Anweisung, die die aktuelle primitive Topologie im angegebenen Stream abschließt, wenn eine beliebige Scheitel Punkte ausgegeben wurden, und startet eine neue Topologie des Typs, der vom Geometry-Shader in diesem Stream deklariert wird.</span><span class="sxs-lookup"><span data-stu-id="86ee7-104">The geometry shader instruction that completes the current primitive topology at the specified stream, if any vertices have been emitted to it, and starts a new topology of the type declared by the geometry shader at that stream.</span></span>



| <span data-ttu-id="86ee7-105">\_Stream streamindex Ausschneiden</span><span class="sxs-lookup"><span data-stu-id="86ee7-105">cut\_stream streamIndex</span></span> |
|-------------------------|



 



| <span data-ttu-id="86ee7-106">Element</span><span class="sxs-lookup"><span data-stu-id="86ee7-106">Item</span></span>                                                                                                               | <span data-ttu-id="86ee7-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="86ee7-107">Description</span></span>                         |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <span data-ttu-id="86ee7-108"><span id="streamIndex"></span><span id="streamindex"></span><span id="STREAMINDEX"></span>*streamIndex*</span><span class="sxs-lookup"><span data-stu-id="86ee7-108"><span id="streamIndex"></span><span id="streamindex"></span><span id="STREAMINDEX"></span>*streamIndex*</span></span><br/> | <span data-ttu-id="86ee7-109">\[im \] Stream-Index.</span><span class="sxs-lookup"><span data-stu-id="86ee7-109">\[in\] The stream index.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="86ee7-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="86ee7-110">Remarks</span></span>

<span data-ttu-id="86ee7-111">Wenn diese Anweisung ausgeführt wird, wird jede zuvor ausgegebene Topologie durch den Geometry-Shader-Aufruf abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="86ee7-111">When this instruction is executed, any previously emitted topology by the geometry shader invocation is completed.</span></span> <span data-ttu-id="86ee7-112">Wenn nicht genügend Scheitel Punkte für die vorherige primitive Topologie ausgegeben werden, werden Sie verworfen.</span><span class="sxs-lookup"><span data-stu-id="86ee7-112">If there are not enough vertices emitted for the previous primitive topology, then they are discarded.</span></span> <span data-ttu-id="86ee7-113">Da die einzigen verfügbaren ausgabetopologien für den Geometry-Shader PointList, linestrip und Trianglestrip sind, gibt es nie übrig gebliebene Scheitel Punkte.</span><span class="sxs-lookup"><span data-stu-id="86ee7-113">Because the only available output topologies for the geometry shader are pointlist, linestrip and trianglestrip, there are never any leftover vertices.</span></span>

<span data-ttu-id="86ee7-114">*streamindex* muss ein unmittelbarer Wert \[ von 0.. 3 \] für einen deklarierten Stream sein.</span><span class="sxs-lookup"><span data-stu-id="86ee7-114">*streamIndex* must be an immediate value \[0..3\] for a declared stream.</span></span>

<span data-ttu-id="86ee7-115">Nachdem die vorherige Topologie (sofern vorhanden) abgeschlossen ist, bewirkt diese Anweisung, dass eine neue Topologie beginnt, wobei die Topologie verwendet wird, die als Ausgabe für den Geometry-Shader deklariert ist.</span><span class="sxs-lookup"><span data-stu-id="86ee7-115">After the previous topology, if any, is completed, this instruction causes a new topology to begin, using the topology declared as the output for the geometry shader.</span></span>

### <a name="restrictions"></a><span data-ttu-id="86ee7-116">Beschränkungen</span><span class="sxs-lookup"><span data-stu-id="86ee7-116">Restrictions</span></span>

-   <span data-ttu-id="86ee7-117">Diese Anweisung gilt nur für den Geometry-Shader.</span><span class="sxs-lookup"><span data-stu-id="86ee7-117">This instruction applies to the geometry shader only.</span></span>
-   <span data-ttu-id="86ee7-118">**Ausschneide Daten \_ Ströme** können beliebig oft im Geometry-Shader vorkommen, einschließlich innerhalb der Fluss Steuerung.</span><span class="sxs-lookup"><span data-stu-id="86ee7-118">**cut\_stream** can appear any number of times in the geometry shader, including within flow control.</span></span>
-   <span data-ttu-id="86ee7-119">Wenn der Geometrie-Shader endet und Scheitel Punkte ausgegeben wurden, wird die Topologie, die Sie aufbauen, abgeschlossen, als ob eine Anweisung zum **Ausschneiden eines \_ Streams** als letzte Anweisung ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="86ee7-119">If the geometry shader ends and vertices have been emitted, the topology they are building is completed, as if a **cut\_stream** instruction was executed as the last instruction.</span></span>
-   <span data-ttu-id="86ee7-120">Wenn Streams nicht deklariert wurden, müssen Sie [Ausschneiden](cut--sm4---asm-.md) anstelle von **Ausschneide Daten \_ Strom** verwenden.</span><span class="sxs-lookup"><span data-stu-id="86ee7-120">If streams have not been declared, you must use [cut](cut--sm4---asm-.md) instead of **cut\_stream**.</span></span>

<span data-ttu-id="86ee7-121">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="86ee7-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="86ee7-122">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="86ee7-122">Vertex</span></span> | <span data-ttu-id="86ee7-123">Hülle</span><span class="sxs-lookup"><span data-stu-id="86ee7-123">Hull</span></span> | <span data-ttu-id="86ee7-124">Domain</span><span class="sxs-lookup"><span data-stu-id="86ee7-124">Domain</span></span> | <span data-ttu-id="86ee7-125">Geometrie</span><span class="sxs-lookup"><span data-stu-id="86ee7-125">Geometry</span></span> | <span data-ttu-id="86ee7-126">Pixel</span><span class="sxs-lookup"><span data-stu-id="86ee7-126">Pixel</span></span> | <span data-ttu-id="86ee7-127">Compute</span><span class="sxs-lookup"><span data-stu-id="86ee7-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        | <span data-ttu-id="86ee7-128">X</span><span class="sxs-lookup"><span data-stu-id="86ee7-128">X</span></span>        |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="86ee7-129">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="86ee7-129">Minimum Shader Model</span></span>

<span data-ttu-id="86ee7-130">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="86ee7-130">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="86ee7-131">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="86ee7-131">Shader Model</span></span>                                              | <span data-ttu-id="86ee7-132">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="86ee7-132">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="86ee7-133">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="86ee7-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="86ee7-134">ja</span><span class="sxs-lookup"><span data-stu-id="86ee7-134">yes</span></span>       |
| [<span data-ttu-id="86ee7-135">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="86ee7-135">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="86ee7-136">nein</span><span class="sxs-lookup"><span data-stu-id="86ee7-136">no</span></span>        |
| [<span data-ttu-id="86ee7-137">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="86ee7-137">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="86ee7-138">nein</span><span class="sxs-lookup"><span data-stu-id="86ee7-138">no</span></span>        |
| [<span data-ttu-id="86ee7-139">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="86ee7-139">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="86ee7-140">nein</span><span class="sxs-lookup"><span data-stu-id="86ee7-140">no</span></span>        |
| [<span data-ttu-id="86ee7-141">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="86ee7-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="86ee7-142">nein</span><span class="sxs-lookup"><span data-stu-id="86ee7-142">no</span></span>        |
| [<span data-ttu-id="86ee7-143">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="86ee7-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="86ee7-144">nein</span><span class="sxs-lookup"><span data-stu-id="86ee7-144">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="86ee7-145">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="86ee7-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="86ee7-146">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="86ee7-146">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





