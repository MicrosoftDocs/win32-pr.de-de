---
title: dcl_temps (SM4-ASM)
description: DCL \_ -Temps (SM4-ASM)
ms.assetid: ecfbdd1e-0f2d-4371-91cc-ebc3e5ee8ee7
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5fc3a468575b30836d4574edb13c4fc77a3505fc
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993199"
---
# <a name="dcl_temps-sm4---asm"></a><span data-ttu-id="d6e8f-103">DCL \_ -Temps (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="d6e8f-103">dcl\_temps (sm4 - asm)</span></span>

<span data-ttu-id="d6e8f-104">Deklariert temporäre Register.</span><span class="sxs-lookup"><span data-stu-id="d6e8f-104">Declares temporary registers.</span></span>



| <span data-ttu-id="d6e8f-105">DCL- \_ Temps N</span><span class="sxs-lookup"><span data-stu-id="d6e8f-105">dcl\_temps N</span></span> |
|--------------|



 



| <span data-ttu-id="d6e8f-106">Element</span><span class="sxs-lookup"><span data-stu-id="d6e8f-106">Item</span></span>                                                   | <span data-ttu-id="d6e8f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d6e8f-107">Description</span></span>                                          |
|--------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d6e8f-108"><span id="N"></span><span id="n"></span>*Nr*</span><span class="sxs-lookup"><span data-stu-id="d6e8f-108"><span id="N"></span><span id="n"></span>*N*</span></span><br/> | <span data-ttu-id="d6e8f-109">\[in \] der Anzahl der temporären Register.</span><span class="sxs-lookup"><span data-stu-id="d6e8f-109">\[in\] The number of temporary registers.</span></span><br/> |



 

<span data-ttu-id="d6e8f-110">Jedes Register verfügt über Platz für einen Wert von 32-Bit-vier Komponenten.</span><span class="sxs-lookup"><span data-stu-id="d6e8f-110">Each register has space for a 32-bit four-component value.</span></span> <span data-ttu-id="d6e8f-111">Die Gesamtanzahl der temporären und [indizierbaren temporären](dcl-indexabletemp.md) Register muss kleiner oder gleich 4096 sein.</span><span class="sxs-lookup"><span data-stu-id="d6e8f-111">The total number of temporary and [indexable-temporary](dcl-indexabletemp.md) registers must be less than or equal to 4096.</span></span>

<span data-ttu-id="d6e8f-112">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="d6e8f-112">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="d6e8f-113">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="d6e8f-113">Vertex Shader</span></span> | <span data-ttu-id="d6e8f-114">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="d6e8f-114">Geometry Shader</span></span> | <span data-ttu-id="d6e8f-115">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="d6e8f-115">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="d6e8f-116">x</span><span class="sxs-lookup"><span data-stu-id="d6e8f-116">x</span></span>             | <span data-ttu-id="d6e8f-117">x</span><span class="sxs-lookup"><span data-stu-id="d6e8f-117">x</span></span>               | <span data-ttu-id="d6e8f-118">x</span><span class="sxs-lookup"><span data-stu-id="d6e8f-118">x</span></span>            |



 

<span data-ttu-id="d6e8f-119">Diese Anweisung ist enthalten, um das Debuggen eines Shaders in der Assembly zu unterstützen. Es ist nicht möglich, einen Shader mit Shadermodell 4 in der Assemblysprache zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d6e8f-119">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="d6e8f-120">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d6e8f-120">Example</span></span>

<span data-ttu-id="d6e8f-121">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="d6e8f-121">Here is an example.</span></span>


```
dcl_temps 10; // Declare r0-r9
```



## <a name="minimum-shader-model"></a><span data-ttu-id="d6e8f-122">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="d6e8f-122">Minimum Shader Model</span></span>

<span data-ttu-id="d6e8f-123">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d6e8f-123">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d6e8f-124">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="d6e8f-124">Shader Model</span></span>                                              | <span data-ttu-id="d6e8f-125">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="d6e8f-125">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="d6e8f-126">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="d6e8f-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="d6e8f-127">ja</span><span class="sxs-lookup"><span data-stu-id="d6e8f-127">yes</span></span>       |
| [<span data-ttu-id="d6e8f-128">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="d6e8f-128">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="d6e8f-129">ja</span><span class="sxs-lookup"><span data-stu-id="d6e8f-129">yes</span></span>       |
| [<span data-ttu-id="d6e8f-130">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="d6e8f-130">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="d6e8f-131">ja</span><span class="sxs-lookup"><span data-stu-id="d6e8f-131">yes</span></span>       |
| [<span data-ttu-id="d6e8f-132">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d6e8f-132">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="d6e8f-133">nein</span><span class="sxs-lookup"><span data-stu-id="d6e8f-133">no</span></span>        |
| [<span data-ttu-id="d6e8f-134">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d6e8f-134">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="d6e8f-135">nein</span><span class="sxs-lookup"><span data-stu-id="d6e8f-135">no</span></span>        |
| [<span data-ttu-id="d6e8f-136">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d6e8f-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="d6e8f-137">nein</span><span class="sxs-lookup"><span data-stu-id="d6e8f-137">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="d6e8f-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d6e8f-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6e8f-139">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d6e8f-139">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





