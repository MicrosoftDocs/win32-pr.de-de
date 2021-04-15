---
title: dcl_output (SM4-ASM)
description: DCL \_ -Ausgabe (SM4-ASM)
ms.assetid: 47e707ad-3ca4-477e-9eb8-3ec462abe864
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4391a30e172ef28133b8fe09a99bae7f77c971af
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104976489"
---
# <a name="dcl_output-sm4---asm"></a><span data-ttu-id="edb89-103">DCL \_ -Ausgabe (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="edb89-103">dcl\_output (sm4 - asm)</span></span>

<span data-ttu-id="edb89-104">Deklariert ein Shader-Output-Register.</span><span class="sxs-lookup"><span data-stu-id="edb89-104">Declares a shader-output register.</span></span>



| <span data-ttu-id="edb89-105">DCL- \_ Ausgabe o *N \[ . \] Mask*</span><span class="sxs-lookup"><span data-stu-id="edb89-105">dcl\_output o *N\[.mask\]*</span></span> |
|---------------------------|



 



| <span data-ttu-id="edb89-106">Element</span><span class="sxs-lookup"><span data-stu-id="edb89-106">Item</span></span>                                                                           | <span data-ttu-id="edb89-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="edb89-107">Description</span></span>                                                                                                  |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="edb89-108"><span id="oN"></span><span id="on"></span><span id="ON"></span>o *N*</span><span class="sxs-lookup"><span data-stu-id="edb89-108"><span id="oN"></span><span id="on"></span><span id="ON"></span>o *N*</span></span><br/> | <span data-ttu-id="edb89-109">\[in \] einem Ausgabedaten Register; *N* ist eine ganze Zahl, die die Registernummer bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="edb89-109">\[in\] An output data register; *N* is an integer that denotes the register number.</span></span><br/>               |
| <span data-ttu-id="edb89-110"><span id="_.mask_"></span><span id="_.MASK_"></span>*\[. Mask\]*</span><span class="sxs-lookup"><span data-stu-id="edb89-110"><span id="_.mask_"></span><span id="_.MASK_"></span>*\[.mask\]*</span></span><br/>     | <span data-ttu-id="edb89-111">\[in \] optional.</span><span class="sxs-lookup"><span data-stu-id="edb89-111">\[in\] Optional.</span></span> <span data-ttu-id="edb89-112">Eine Komponenten Maske (. xyzw), die angibt, welche der zu verwendenden Registrierungs Komponenten verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="edb89-112">A component mask (.xyzw) that specifies which of the register components to use.</span></span><br/> |



 

<span data-ttu-id="edb89-113">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="edb89-113">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="edb89-114">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="edb89-114">Vertex Shader</span></span> | <span data-ttu-id="edb89-115">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="edb89-115">Geometry Shader</span></span> | <span data-ttu-id="edb89-116">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="edb89-116">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="edb89-117">x</span><span class="sxs-lookup"><span data-stu-id="edb89-117">x</span></span>             | <span data-ttu-id="edb89-118">x</span><span class="sxs-lookup"><span data-stu-id="edb89-118">x</span></span>               | <span data-ttu-id="edb89-119">x</span><span class="sxs-lookup"><span data-stu-id="edb89-119">x</span></span>            |



 

<span data-ttu-id="edb89-120">Diese Anweisung ist enthalten, um das Debuggen eines Shaders in der Assembly zu unterstützen. Es ist nicht möglich, einen Shader mit Shadermodell 4 in der Assemblysprache zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="edb89-120">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="edb89-121">Beispiel</span><span class="sxs-lookup"><span data-stu-id="edb89-121">Example</span></span>

<span data-ttu-id="edb89-122">Hier einige Beispiele.</span><span class="sxs-lookup"><span data-stu-id="edb89-122">Here are some examples.</span></span>


```
dcl_output o0.xyz
dcl_output o1
dcl_output o2.xw
```



## <a name="minimum-shader-model"></a><span data-ttu-id="edb89-123">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="edb89-123">Minimum Shader Model</span></span>

<span data-ttu-id="edb89-124">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="edb89-124">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="edb89-125">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="edb89-125">Shader Model</span></span>                                              | <span data-ttu-id="edb89-126">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="edb89-126">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="edb89-127">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="edb89-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="edb89-128">ja</span><span class="sxs-lookup"><span data-stu-id="edb89-128">yes</span></span>       |
| [<span data-ttu-id="edb89-129">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="edb89-129">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="edb89-130">ja</span><span class="sxs-lookup"><span data-stu-id="edb89-130">yes</span></span>       |
| [<span data-ttu-id="edb89-131">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="edb89-131">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="edb89-132">ja</span><span class="sxs-lookup"><span data-stu-id="edb89-132">yes</span></span>       |
| [<span data-ttu-id="edb89-133">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="edb89-133">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="edb89-134">nein</span><span class="sxs-lookup"><span data-stu-id="edb89-134">no</span></span>        |
| [<span data-ttu-id="edb89-135">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="edb89-135">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="edb89-136">nein</span><span class="sxs-lookup"><span data-stu-id="edb89-136">no</span></span>        |
| [<span data-ttu-id="edb89-137">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="edb89-137">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="edb89-138">nein</span><span class="sxs-lookup"><span data-stu-id="edb89-138">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="edb89-139">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="edb89-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="edb89-140">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="edb89-140">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





