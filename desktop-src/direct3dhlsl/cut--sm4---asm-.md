---
title: Ausschneiden (SM4-ASM)
description: Geometry-shaderanweisung, die die aktuelle primitive Topologie (wenn beliebige Scheitel Punkte ausgegeben wurden) vervollständigt und eine neue Topologie des vom Geometry-Shader deklarierten Typs startet.
ms.assetid: 9B28E33D-F518-4844-BE3F-BE61B5F08B4F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c462d2f4dc2e0c6b4076f577610c93794e890af
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104976328"
---
# <a name="cut-sm4---asm"></a><span data-ttu-id="d5f67-103">Ausschneiden (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="d5f67-103">cut (sm4 - asm)</span></span>

<span data-ttu-id="d5f67-104">Geometry-shaderanweisung, die die aktuelle primitive Topologie (wenn beliebige Scheitel Punkte ausgegeben wurden) vervollständigt und eine neue Topologie des vom Geometry-Shader deklarierten Typs startet.</span><span class="sxs-lookup"><span data-stu-id="d5f67-104">Geometry Shader instruction that completes the current primitive topology (if any vertices have been emitted), and starts a new topology of the type declared by the Geometry Shader.</span></span>



| <span data-ttu-id="d5f67-105">cut</span><span class="sxs-lookup"><span data-stu-id="d5f67-105">cut</span></span> |
|-----|



 

## <a name="remarks"></a><span data-ttu-id="d5f67-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d5f67-106">Remarks</span></span>

<span data-ttu-id="d5f67-107">Wenn **Ausschneiden** ausgeführt wird, ist das erste, dass jede zuvor ausgegebene Topologie durch den Geometry-Shader-Aufruf abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="d5f67-107">When **cut** is executed, the first thing that happens is that any previously emitted topology by the Geometry Shader invocation is completed.</span></span> <span data-ttu-id="d5f67-108">Wenn nicht genügend Scheitel Punkte für die vorherige primitive Topologie ausgegeben wurden, werden Sie verworfen.</span><span class="sxs-lookup"><span data-stu-id="d5f67-108">If not enough vertices were emitted for the previous primitive topology, they are discarded.</span></span> <span data-ttu-id="d5f67-109">Da die einzigen verfügbaren ausgabetopologien für den Geometry-Shader "PointList", "linestrip" und "Trianglestrip" sind, gibt es keine übrig gebliebenen Scheitel Punkte beim **Ausschneiden**.</span><span class="sxs-lookup"><span data-stu-id="d5f67-109">Because the only available output topologies for the Geometry Shader are pointlist, linestrip, and trianglestrip, there are never any leftover vertices upon **cut**.</span></span>

<span data-ttu-id="d5f67-110">Wenn die vorherige Topologie (sofern vorhanden) abgeschlossen ist, bewirkt die **Ausschneide** , dass eine neue Topologie beginnt, wobei die Topologie verwendet wird, die als Geometry-Shader-Ausgabe deklariert ist.</span><span class="sxs-lookup"><span data-stu-id="d5f67-110">After the previous topology, if any, is completed, **cut** causes a new topology to begin, using the topology declared as the Geometry Shader output.</span></span>

## <a name="restrictions"></a><span data-ttu-id="d5f67-111">Beschränkungen</span><span class="sxs-lookup"><span data-stu-id="d5f67-111">Restrictions</span></span>

-   <span data-ttu-id="d5f67-112">Die **Ausschneide** Anweisung gilt nur für den Geometry-Shader.</span><span class="sxs-lookup"><span data-stu-id="d5f67-112">The **cut** instruction applies only to the Geometry Shader.</span></span>
-   <span data-ttu-id="d5f67-113">**Ausschneiden** kann beliebig oft im Geometry-Shader vorkommen, einschließlich innerhalb der Fluss Steuerung.</span><span class="sxs-lookup"><span data-stu-id="d5f67-113">**cut** can appear any number of times in the Geometry Shader, including within flow control.</span></span>
-   <span data-ttu-id="d5f67-114">Wenn der Geometrie-Shader endet und Scheitel Punkte ausgegeben wurden, wird die Topologie, die Sie aufbauen, abgeschlossen, als ob eine **Ausschneide** als letzte Anweisung ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="d5f67-114">If the Geometry Shader ends and vertices have been emitted, the topology they are building is completed, as if a **cut** was executed as the last instruction.</span></span>
-   <span data-ttu-id="d5f67-115">Wenn Streams deklariert wurden, muss [Ausschneide Daten \_ Strom](cut-stream---sm5---asm-.md) anstelle von **Ausschneiden** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d5f67-115">If streams have been declared, then [cut\_stream](cut-stream---sm5---asm-.md) must be used instead of **cut**.</span></span>

<span data-ttu-id="d5f67-116">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="d5f67-116">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="d5f67-117">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="d5f67-117">Vertex Shader</span></span> | <span data-ttu-id="d5f67-118">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="d5f67-118">Geometry Shader</span></span> | <span data-ttu-id="d5f67-119">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="d5f67-119">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               | <span data-ttu-id="d5f67-120">x</span><span class="sxs-lookup"><span data-stu-id="d5f67-120">x</span></span>               |              |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d5f67-121">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="d5f67-121">Minimum Shader Model</span></span>

<span data-ttu-id="d5f67-122">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d5f67-122">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d5f67-123">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="d5f67-123">Shader Model</span></span>                                              | <span data-ttu-id="d5f67-124">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="d5f67-124">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="d5f67-125">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="d5f67-125">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="d5f67-126">ja</span><span class="sxs-lookup"><span data-stu-id="d5f67-126">yes</span></span>       |
| [<span data-ttu-id="d5f67-127">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="d5f67-127">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="d5f67-128">ja</span><span class="sxs-lookup"><span data-stu-id="d5f67-128">yes</span></span>       |
| [<span data-ttu-id="d5f67-129">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="d5f67-129">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="d5f67-130">ja</span><span class="sxs-lookup"><span data-stu-id="d5f67-130">yes</span></span>       |
| [<span data-ttu-id="d5f67-131">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d5f67-131">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="d5f67-132">nein</span><span class="sxs-lookup"><span data-stu-id="d5f67-132">no</span></span>        |
| [<span data-ttu-id="d5f67-133">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d5f67-133">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="d5f67-134">nein</span><span class="sxs-lookup"><span data-stu-id="d5f67-134">no</span></span>        |
| [<span data-ttu-id="d5f67-135">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d5f67-135">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="d5f67-136">nein</span><span class="sxs-lookup"><span data-stu-id="d5f67-136">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="d5f67-137">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d5f67-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5f67-138">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d5f67-138">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




