---
title: dcl_outputTopology (SM4-ASM)
description: DCL \_ outputtopology (SM4-ASM)
ms.assetid: a03a6feb-ec34-4655-a68c-a91e31e7140b
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e3b305d195ca09a1ef95c99624b47a50058021ca
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "103719475"
---
# <a name="dcl_outputtopology-sm4---asm"></a><span data-ttu-id="9457e-103">DCL \_ outputtopology (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="9457e-103">dcl\_outputTopology (sm4 - asm)</span></span>

<span data-ttu-id="9457e-104">Deklariert den primitiven Typ Geometry-Shader-Ausgabedaten.</span><span class="sxs-lookup"><span data-stu-id="9457e-104">Declares the primitive type geometry-shader output data.</span></span>



| <span data-ttu-id="9457e-105">DCL- \_ outputtopology- *Typ*</span><span class="sxs-lookup"><span data-stu-id="9457e-105">dcl\_outputTopology *Type*</span></span> |
|----------------------------|



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9457e-106">Element</span><span class="sxs-lookup"><span data-stu-id="9457e-106">Item</span></span></th>
<th><span data-ttu-id="9457e-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9457e-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9457e-108"><span id="Type"></span><span id="type"></span><span id="TYPE"></span><em>Sorte</em></span><span class="sxs-lookup"><span data-stu-id="9457e-108"><span id="Type"></span><span id="type"></span><span id="TYPE"></span><em>Type</em></span></span><br/></td>
<td><span data-ttu-id="9457e-109">in Eine primitive Ausgabe Topologie, die einen der folgenden Werte hat:</span><span class="sxs-lookup"><span data-stu-id="9457e-109">[in] An output primitive topology, which is one of the following values:</span></span> <br/>
<ul>
<li><span data-ttu-id="9457e-110"><em>PointList</em></span><span class="sxs-lookup"><span data-stu-id="9457e-110"><em>pointlist</em></span></span></li>
<li><span data-ttu-id="9457e-111"><em>linestrip</em></span><span class="sxs-lookup"><span data-stu-id="9457e-111"><em>linestrip</em></span></span></li>
<li><span data-ttu-id="9457e-112"><em>"Trip Strip"</em></span><span class="sxs-lookup"><span data-stu-id="9457e-112"><em>trianglestrip</em></span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="9457e-113">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="9457e-113">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="9457e-114">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="9457e-114">Vertex Shader</span></span> | <span data-ttu-id="9457e-115">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="9457e-115">Geometry Shader</span></span> | <span data-ttu-id="9457e-116">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="9457e-116">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               | <span data-ttu-id="9457e-117">x</span><span class="sxs-lookup"><span data-stu-id="9457e-117">x</span></span>               |              |



 

<span data-ttu-id="9457e-118">Diese Anweisung ist enthalten, um das Debuggen eines Shaders in der Assembly zu unterstützen. Es ist nicht möglich, einen Shader mit Shadermodell 4 in der Assemblysprache zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9457e-118">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="9457e-119">Beispiel</span><span class="sxs-lookup"><span data-stu-id="9457e-119">Example</span></span>

<span data-ttu-id="9457e-120">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="9457e-120">Here is an example.</span></span>


```
dcl_outputTopology trianglestrip
```



## <a name="minimum-shader-model"></a><span data-ttu-id="9457e-121">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="9457e-121">Minimum Shader Model</span></span>

<span data-ttu-id="9457e-122">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9457e-122">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="9457e-123">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="9457e-123">Shader Model</span></span>                                              | <span data-ttu-id="9457e-124">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="9457e-124">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="9457e-125">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="9457e-125">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="9457e-126">ja</span><span class="sxs-lookup"><span data-stu-id="9457e-126">yes</span></span>       |
| [<span data-ttu-id="9457e-127">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="9457e-127">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="9457e-128">ja</span><span class="sxs-lookup"><span data-stu-id="9457e-128">yes</span></span>       |
| [<span data-ttu-id="9457e-129">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="9457e-129">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="9457e-130">ja</span><span class="sxs-lookup"><span data-stu-id="9457e-130">yes</span></span>       |
| [<span data-ttu-id="9457e-131">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9457e-131">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="9457e-132">nein</span><span class="sxs-lookup"><span data-stu-id="9457e-132">no</span></span>        |
| [<span data-ttu-id="9457e-133">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9457e-133">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="9457e-134">nein</span><span class="sxs-lookup"><span data-stu-id="9457e-134">no</span></span>        |
| [<span data-ttu-id="9457e-135">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9457e-135">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="9457e-136">nein</span><span class="sxs-lookup"><span data-stu-id="9457e-136">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="9457e-137">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9457e-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9457e-138">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9457e-138">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





