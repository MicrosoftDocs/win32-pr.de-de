---
title: dcl_constantBuffer (SM4-ASM)
description: DCL \_ constantbuffer (SM4-ASM)
ms.assetid: 164fb2a4-8782-42f0-b4ba-1f87d9c7255d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b2eeb9368af0121ee61fde5d106eb0f3b08e5acb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104101094"
---
# <a name="dcl_constantbuffer-sm4---asm"></a><span data-ttu-id="1690c-103">DCL \_ constantbuffer (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="1690c-103">dcl\_constantBuffer (sm4 - asm)</span></span>

<span data-ttu-id="1690c-104">Deklariert einen Shader-Konstantenpuffer.</span><span class="sxs-lookup"><span data-stu-id="1690c-104">Declares a shader constant buffer.</span></span>



| <span data-ttu-id="1690c-105">DCL \_ constantbuffer *CBN \[ - \] Größe*, *accesspattern*</span><span class="sxs-lookup"><span data-stu-id="1690c-105">dcl\_constantBuffer *cbN\[size\]*, *AccessPattern*</span></span> |
|----------------------------------------------------|



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1690c-106">Element</span><span class="sxs-lookup"><span data-stu-id="1690c-106">Item</span></span></th>
<th><span data-ttu-id="1690c-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1690c-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1690c-108"><span id="cbN_size_"></span><span id="cbn_size_"></span><span id="CBN_SIZE_"></span>CB<em>N [Größe]</em></span><span class="sxs-lookup"><span data-stu-id="1690c-108"><span id="cbN_size_"></span><span id="cbn_size_"></span><span id="CBN_SIZE_"></span>cb<em>N[size]</em></span></span><br/></td>
<td><span data-ttu-id="1690c-109">in Ein Shader-Konstantenpuffer, bei dem N eine ganze Zahl ist, die die Anzahl und Größe des Konstanten Puffers angibt, ist eine ganze Zahl, die die Anzahl der Elemente im Puffer angibt.</span><span class="sxs-lookup"><span data-stu-id="1690c-109">[in] A shader constant buffer where N is an integer that denotes the constant-buffer-register number and size is an integer that denotes the number of elements in the buffer.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1690c-110"><span id="AccessPattern"></span><span id="accesspattern"></span><span id="ACCESSPATTERN"></span><em>Accesspattern</em></span><span class="sxs-lookup"><span data-stu-id="1690c-110"><span id="AccessPattern"></span><span id="accesspattern"></span><span id="ACCESSPATTERN"></span><em>AccessPattern</em></span></span><br/></td>
<td><span data-ttu-id="1690c-111">in Der Zugriff auf den Puffer erfolgt über den Shader-Code, der eines der folgenden ist:</span><span class="sxs-lookup"><span data-stu-id="1690c-111">[in] The way that the buffer will be accessed by shader code, which is one of the following:</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1690c-112">Name</span><span class="sxs-lookup"><span data-stu-id="1690c-112">Name</span></span></th>
<th><span data-ttu-id="1690c-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1690c-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1690c-114">sofort eingepackt</span><span class="sxs-lookup"><span data-stu-id="1690c-114">immediateIndexed</span></span></td>
<td><span data-ttu-id="1690c-115">Indizieren Sie den Puffer mit einem Literalwert.</span><span class="sxs-lookup"><span data-stu-id="1690c-115">Index the buffer with a literal value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1690c-116">dynamic_indexed</span><span class="sxs-lookup"><span data-stu-id="1690c-116">dynamic_indexed</span></span></td>
<td><span data-ttu-id="1690c-117">Indizieren Sie den Puffer mit dem Ergebnis eines ausgewerteten Ausdrucks.</span><span class="sxs-lookup"><span data-stu-id="1690c-117">Index the buffer with the result of an evaluated expression.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="1690c-118">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="1690c-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="1690c-119">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="1690c-119">Vertex Shader</span></span> | <span data-ttu-id="1690c-120">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="1690c-120">Geometry Shader</span></span> | <span data-ttu-id="1690c-121">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="1690c-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="1690c-122">x</span><span class="sxs-lookup"><span data-stu-id="1690c-122">x</span></span>             | <span data-ttu-id="1690c-123">x</span><span class="sxs-lookup"><span data-stu-id="1690c-123">x</span></span>               | <span data-ttu-id="1690c-124">x</span><span class="sxs-lookup"><span data-stu-id="1690c-124">x</span></span>            |



 

<span data-ttu-id="1690c-125">Diese Anweisung ist enthalten, um das Debuggen eines Shaders in der Assembly zu unterstützen. Es ist nicht möglich, einen Shader mit Shadermodell 4 in der Assemblysprache zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1690c-125">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="1690c-126">Beispiel</span><span class="sxs-lookup"><span data-stu-id="1690c-126">Example</span></span>

<span data-ttu-id="1690c-127">In diesem Beispiel wird ein konstanter Puffer für Register CB0 mit 19 Elementen deklariert.</span><span class="sxs-lookup"><span data-stu-id="1690c-127">This example declares a constant buffer for register cb0, which has 19 elements.</span></span> <span data-ttu-id="1690c-128">Auf diese Elemente wird mit einem literalen Index zugegriffen.</span><span class="sxs-lookup"><span data-stu-id="1690c-128">These elements are accessed with a literal index.</span></span>


```
dcl_constantbuffer  cb0[19], immediateIndexed
```



## <a name="minimum-shader-model"></a><span data-ttu-id="1690c-129">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="1690c-129">Minimum Shader Model</span></span>

<span data-ttu-id="1690c-130">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1690c-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="1690c-131">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="1690c-131">Shader Model</span></span>                                              | <span data-ttu-id="1690c-132">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="1690c-132">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="1690c-133">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="1690c-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="1690c-134">ja</span><span class="sxs-lookup"><span data-stu-id="1690c-134">yes</span></span>       |
| [<span data-ttu-id="1690c-135">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="1690c-135">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="1690c-136">ja</span><span class="sxs-lookup"><span data-stu-id="1690c-136">yes</span></span>       |
| [<span data-ttu-id="1690c-137">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="1690c-137">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="1690c-138">ja</span><span class="sxs-lookup"><span data-stu-id="1690c-138">yes</span></span>       |
| [<span data-ttu-id="1690c-139">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1690c-139">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="1690c-140">nein</span><span class="sxs-lookup"><span data-stu-id="1690c-140">no</span></span>        |
| [<span data-ttu-id="1690c-141">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1690c-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="1690c-142">nein</span><span class="sxs-lookup"><span data-stu-id="1690c-142">no</span></span>        |
| [<span data-ttu-id="1690c-143">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1690c-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="1690c-144">nein</span><span class="sxs-lookup"><span data-stu-id="1690c-144">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="1690c-145">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1690c-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1690c-146">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1690c-146">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





