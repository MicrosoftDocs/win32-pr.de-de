---
title: dcl_indexableTemp (SM4-ASM)
description: DCL \_ indexabletemp (SM4-ASM)
ms.assetid: 32d8e7ce-4b28-48c3-b794-56ace96394f0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1ec3ef1222cd3bf73b4ea3f9ac6e2c3e706aa18e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993239"
---
# <a name="dcl_indexabletemp-sm4---asm"></a><span data-ttu-id="aa390-103">DCL \_ indexabletemp (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="aa390-103">dcl\_indexableTemp (sm4 - asm)</span></span>

<span data-ttu-id="aa390-104">Deklariert ein indexbares temporäres Register.</span><span class="sxs-lookup"><span data-stu-id="aa390-104">Declares an indexable, temporary register.</span></span>



| <span data-ttu-id="aa390-105">DCL \_ indexabletemp x *N \[ Größe \] , ComponentCount*</span><span class="sxs-lookup"><span data-stu-id="aa390-105">dcl\_indexableTemp x *N\[size\], ComponentCount*</span></span> |
|-------------------------------------------------|



 



| <span data-ttu-id="aa390-106">Element</span><span class="sxs-lookup"><span data-stu-id="aa390-106">Item</span></span>                                                                                                                           | <span data-ttu-id="aa390-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="aa390-107">Description</span></span>                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa390-108"><span id="N"></span><span id="n"></span>*Nr*</span><span class="sxs-lookup"><span data-stu-id="aa390-108"><span id="N"></span><span id="n"></span>*N*</span></span><br/>                                                                         | <span data-ttu-id="aa390-109">\[in \] einer Ganzzahl, die die Registernummer angibt.</span><span class="sxs-lookup"><span data-stu-id="aa390-109">\[in\] An integer that denotes the register number.</span></span><br/>                              |
| <span data-ttu-id="aa390-110"><span id="_size_"></span><span id="_SIZE_"></span>*\[Größe\]*</span><span class="sxs-lookup"><span data-stu-id="aa390-110"><span id="_size_"></span><span id="_SIZE_"></span>*\[size\]*</span></span><br/>                                                        | <span data-ttu-id="aa390-111">\[in \] einem optionalen ganzzahligen Wert.</span><span class="sxs-lookup"><span data-stu-id="aa390-111">\[in\] An optional integer value.</span></span> <span data-ttu-id="aa390-112">Die Anzahl der Elemente im Register Array.</span><span class="sxs-lookup"><span data-stu-id="aa390-112">The number of elements in the register array.</span></span><br/>  |
| <span data-ttu-id="aa390-113"><span id="ComponentCount"></span><span id="componentcount"></span><span id="COMPONENTCOUNT"></span>*ComponentCount*</span><span class="sxs-lookup"><span data-stu-id="aa390-113"><span id="ComponentCount"></span><span id="componentcount"></span><span id="COMPONENTCOUNT"></span>*ComponentCount*</span></span><br/> | <span data-ttu-id="aa390-114">\[in \] einem optionalen ganzzahligen Wert. Die Anzahl der Komponenten im Register Array.</span><span class="sxs-lookup"><span data-stu-id="aa390-114">\[in\] An optional integer value.The number of components in the register array.</span></span><br/> |



 

<span data-ttu-id="aa390-115">Ein Register enthält ausreichend Speicherplatz für einen Wert von 32-Bit-vier Komponenten. die Anzahl der Elemente im Array von temporären Registern (indizierbar und [nicht indizierbar](dcl-temps.md)) darf 4096 nicht überschreiten.</span><span class="sxs-lookup"><span data-stu-id="aa390-115">A register contains enough space for a 32-bit four-component value; the number of elements in the array of temporary registers (indexable and [non-indexable](dcl-temps.md)) cannot exceed 4096.</span></span>

<span data-ttu-id="aa390-116">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="aa390-116">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="aa390-117">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="aa390-117">Vertex Shader</span></span> | <span data-ttu-id="aa390-118">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="aa390-118">Geometry Shader</span></span> | <span data-ttu-id="aa390-119">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="aa390-119">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="aa390-120">x</span><span class="sxs-lookup"><span data-stu-id="aa390-120">x</span></span>             | <span data-ttu-id="aa390-121">x</span><span class="sxs-lookup"><span data-stu-id="aa390-121">x</span></span>               | <span data-ttu-id="aa390-122">x</span><span class="sxs-lookup"><span data-stu-id="aa390-122">x</span></span>            |



 

<span data-ttu-id="aa390-123">Diese Anweisung ist enthalten, um das Debuggen eines Shaders in der Assembly zu unterstützen. Es ist nicht möglich, einen Shader mit Shadermodell 4 in der Assemblysprache zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="aa390-123">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="aa390-124">Beispiel</span><span class="sxs-lookup"><span data-stu-id="aa390-124">Example</span></span>

<span data-ttu-id="aa390-125">Im folgenden finden Sie einige Beispiele für den Code, der für indizierbare Register generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="aa390-125">Here are some examples of the code generated for indexable registers.</span></span>


```
dcl_indexableTemp x0[23], 2 ; // An indexable array of 23, 2-component, 32-bit elements
dcl_indexableTemp x1[16], 4 ; // An indexable array of 16, 4-component, 32-bit elements
```



## <a name="minimum-shader-model"></a><span data-ttu-id="aa390-126">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="aa390-126">Minimum Shader Model</span></span>

<span data-ttu-id="aa390-127">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="aa390-127">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="aa390-128">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="aa390-128">Shader Model</span></span>                                              | <span data-ttu-id="aa390-129">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="aa390-129">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="aa390-130">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="aa390-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="aa390-131">ja</span><span class="sxs-lookup"><span data-stu-id="aa390-131">yes</span></span>       |
| [<span data-ttu-id="aa390-132">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="aa390-132">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="aa390-133">ja</span><span class="sxs-lookup"><span data-stu-id="aa390-133">yes</span></span>       |
| [<span data-ttu-id="aa390-134">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="aa390-134">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="aa390-135">ja</span><span class="sxs-lookup"><span data-stu-id="aa390-135">yes</span></span>       |
| [<span data-ttu-id="aa390-136">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="aa390-136">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="aa390-137">nein</span><span class="sxs-lookup"><span data-stu-id="aa390-137">no</span></span>        |
| [<span data-ttu-id="aa390-138">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="aa390-138">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="aa390-139">nein</span><span class="sxs-lookup"><span data-stu-id="aa390-139">no</span></span>        |
| [<span data-ttu-id="aa390-140">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="aa390-140">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="aa390-141">nein</span><span class="sxs-lookup"><span data-stu-id="aa390-141">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="aa390-142">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="aa390-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa390-143">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="aa390-143">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





