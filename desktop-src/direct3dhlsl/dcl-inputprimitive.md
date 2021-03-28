---
title: dcl_inputPrimitive (SM4-ASM)
description: DCL \_ inputprimitiv (SM4-ASM)
ms.assetid: 86672fd3-7955-45ac-a8b2-a9cc8d1e8805
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 76c131b7c4225c0b30ad1183e4da1fe6c0561754
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "103948331"
---
# <a name="dcl_inputprimitive-sm4---asm"></a><span data-ttu-id="07442-103">DCL \_ inputprimitiv (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="07442-103">dcl\_inputPrimitive (sm4 - asm)</span></span>

<span data-ttu-id="07442-104">Deklariert den primitiven Typ für Geometry-shadereingaben.</span><span class="sxs-lookup"><span data-stu-id="07442-104">Declares the primitive type for geometry-shader inputs.</span></span>



| <span data-ttu-id="07442-105">DCL- \_ inputprimitiver *Typ*</span><span class="sxs-lookup"><span data-stu-id="07442-105">dcl\_inputPrimitive *type*</span></span> |
|----------------------------|



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="07442-106">Element</span><span class="sxs-lookup"><span data-stu-id="07442-106">Item</span></span></th>
<th><span data-ttu-id="07442-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07442-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="07442-108"><span id="type"></span><span id="TYPE"></span><em>Sorte</em></span><span class="sxs-lookup"><span data-stu-id="07442-108"><span id="type"></span><span id="TYPE"></span><em>type</em></span></span><br/></td>
<td><span data-ttu-id="07442-109">in Primitiver Typ der Eingabe-Data, der einer der folgenden Typen ist:</span><span class="sxs-lookup"><span data-stu-id="07442-109">[in] Input-data primitive type, which is one of the following:</span></span> <br/>
<ul>
<li><span data-ttu-id="07442-110"><em>Punkt</em> - Punkt Liste</span><span class="sxs-lookup"><span data-stu-id="07442-110"><em>point</em> - point list</span></span></li>
<li><span data-ttu-id="07442-111"><em>Zeile</em> - Zeilen Liste</span><span class="sxs-lookup"><span data-stu-id="07442-111"><em>line</em> - line list</span></span></li>
<li><span data-ttu-id="07442-112"><em>Dreieck</em> - Dreiecks Liste</span><span class="sxs-lookup"><span data-stu-id="07442-112"><em>triangle</em> - triangle list</span></span></li>
<li><span data-ttu-id="07442-113"><em>line_adj</em> - Zeilen Liste mit Daten</span><span class="sxs-lookup"><span data-stu-id="07442-113"><em>line_adj</em> - line list with adjacency data</span></span></li>
<li><span data-ttu-id="07442-114"><em>triangle_adj</em> - Dreiecks Liste mit Daten</span><span class="sxs-lookup"><span data-stu-id="07442-114"><em>triangle_adj</em> - triangle list with adjacency data</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="07442-115">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="07442-115">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="07442-116">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="07442-116">Vertex Shader</span></span> | <span data-ttu-id="07442-117">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="07442-117">Geometry Shader</span></span> | <span data-ttu-id="07442-118">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="07442-118">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               | <span data-ttu-id="07442-119">x</span><span class="sxs-lookup"><span data-stu-id="07442-119">x</span></span>               |              |



 

<span data-ttu-id="07442-120">Diese Anweisung ist enthalten, um das Debuggen eines Shaders in der Assembly zu unterstützen. Es ist nicht möglich, einen Shader mit Shadermodell 4 in der Assemblysprache zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="07442-120">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="07442-121">Beispiel</span><span class="sxs-lookup"><span data-stu-id="07442-121">Example</span></span>

<span data-ttu-id="07442-122">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="07442-122">Here is an example.</span></span>


```
dcl_inputPrimitive triangle
```



## <a name="minimum-shader-model"></a><span data-ttu-id="07442-123">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="07442-123">Minimum Shader Model</span></span>

<span data-ttu-id="07442-124">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="07442-124">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="07442-125">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="07442-125">Shader Model</span></span>                                              | <span data-ttu-id="07442-126">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="07442-126">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="07442-127">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="07442-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="07442-128">ja</span><span class="sxs-lookup"><span data-stu-id="07442-128">yes</span></span>       |
| [<span data-ttu-id="07442-129">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="07442-129">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="07442-130">ja</span><span class="sxs-lookup"><span data-stu-id="07442-130">yes</span></span>       |
| [<span data-ttu-id="07442-131">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="07442-131">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="07442-132">ja</span><span class="sxs-lookup"><span data-stu-id="07442-132">yes</span></span>       |
| [<span data-ttu-id="07442-133">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="07442-133">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="07442-134">nein</span><span class="sxs-lookup"><span data-stu-id="07442-134">no</span></span>        |
| [<span data-ttu-id="07442-135">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="07442-135">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="07442-136">nein</span><span class="sxs-lookup"><span data-stu-id="07442-136">no</span></span>        |
| [<span data-ttu-id="07442-137">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="07442-137">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="07442-138">nein</span><span class="sxs-lookup"><span data-stu-id="07442-138">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="07442-139">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="07442-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07442-140">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="07442-140">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





