---
title: dcl_output_sgv (SM4-ASM)
description: DCL \_ \_ -Ausgabe scalable (SM4-ASM)
ms.assetid: 0723541e-a97d-4b31-aaba-e7d1172137a6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7cfc5da7724a7e661f84ae5e7b293e5e84b61f15
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389596"
---
# <a name="dcl_output_sgv-sm4---asm"></a><span data-ttu-id="019c1-103">DCL \_ \_ -Ausgabe scalable (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="019c1-103">dcl\_output\_sgv (sm4 - asm)</span></span>

<span data-ttu-id="019c1-104">Deklariert ein Ausgabe Register, das einen [System Wert](dx-graphics-hlsl-semantics.md) Parameter enthält.</span><span class="sxs-lookup"><span data-stu-id="019c1-104">Declares an output register that contains a [system-value](dx-graphics-hlsl-semantics.md) parameter.</span></span>



| <span data-ttu-id="019c1-105">DCL- \_ Ausgabe \_ Scalable on *\[ . \] Mask*, *systemvalue*</span><span class="sxs-lookup"><span data-stu-id="019c1-105">dcl\_output\_sgv oN *\[.mask\]*, *systemValue*</span></span> |
|-----------------------------------------------|



 



| <span data-ttu-id="019c1-106">Element</span><span class="sxs-lookup"><span data-stu-id="019c1-106">Item</span></span>                                                                                                                               | <span data-ttu-id="019c1-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="019c1-107">Description</span></span>                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="019c1-108"><span id="oN"></span><span id="on"></span><span id="ON"></span>o *N*</span><span class="sxs-lookup"><span data-stu-id="019c1-108"><span id="oN"></span><span id="on"></span><span id="ON"></span>o *N*</span></span><br/>                                                     | <span data-ttu-id="019c1-109">\[in \] einem Ausgabedaten Register; *N* ist eine ganze Zahl, die die Registernummer bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="019c1-109">\[in\] An output data register; *N* is an integer that denotes the register number.</span></span><br/>                                                      |
| <span data-ttu-id="019c1-110"><span id="_.mask_"></span><span id="_.MASK_"></span>*\[. Mask\]*</span><span class="sxs-lookup"><span data-stu-id="019c1-110"><span id="_.mask_"></span><span id="_.MASK_"></span>*\[.mask\]*</span></span><br/>                                                         | <span data-ttu-id="019c1-111">\[in \] optional.</span><span class="sxs-lookup"><span data-stu-id="019c1-111">\[in\] Optional.</span></span> <span data-ttu-id="019c1-112">Eine Komponenten Maske (. xyzw), die angibt, welche der zu verwendenden Registrierungs Komponenten verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="019c1-112">A component mask (.xyzw) that specifies which of the register components to use.</span></span><br/>                                        |
| <span data-ttu-id="019c1-113"><span id="systemValueName"></span><span id="systemvaluename"></span><span id="SYSTEMVALUENAME"></span>*systemvaluename*</span><span class="sxs-lookup"><span data-stu-id="019c1-113"><span id="systemValueName"></span><span id="systemvaluename"></span><span id="SYSTEMVALUENAME"></span>*systemValueName*</span></span><br/> | <span data-ttu-id="019c1-114">\[\]der Name des System Werts, bei dem es sich um eine Zeichenfolge handelt (siehe [System-Wert-Semantik](dx-graphics-hlsl-semantics.md)), ohne das Präfix "SV" \_ .</span><span class="sxs-lookup"><span data-stu-id="019c1-114">\[in\] The system-value name which is a string (see [system-value semantics](dx-graphics-hlsl-semantics.md)) without the "SV\_" prefix.</span></span><br/> |



 

<span data-ttu-id="019c1-115">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="019c1-115">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="019c1-116">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="019c1-116">Vertex Shader</span></span> | <span data-ttu-id="019c1-117">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="019c1-117">Geometry Shader</span></span> | <span data-ttu-id="019c1-118">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="019c1-118">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               | <span data-ttu-id="019c1-119">x</span><span class="sxs-lookup"><span data-stu-id="019c1-119">x</span></span>               |              |



 

<span data-ttu-id="019c1-120">Diese Anweisung ist enthalten, um das Debuggen eines Shaders in der Assembly zu unterstützen. Es ist nicht möglich, einen Shader mit Shadermodell 4 in der Assemblysprache zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="019c1-120">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="019c1-121">Beispiel</span><span class="sxs-lookup"><span data-stu-id="019c1-121">Example</span></span>

<span data-ttu-id="019c1-122">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="019c1-122">Here is an example.</span></span>


```
dcl_output_sgv o4.x, primitiveID
```



## <a name="minimum-shader-model"></a><span data-ttu-id="019c1-123">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="019c1-123">Minimum Shader Model</span></span>

<span data-ttu-id="019c1-124">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="019c1-124">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="019c1-125">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="019c1-125">Shader Model</span></span>                                              | <span data-ttu-id="019c1-126">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="019c1-126">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="019c1-127">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="019c1-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="019c1-128">ja</span><span class="sxs-lookup"><span data-stu-id="019c1-128">yes</span></span>       |
| [<span data-ttu-id="019c1-129">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="019c1-129">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="019c1-130">ja</span><span class="sxs-lookup"><span data-stu-id="019c1-130">yes</span></span>       |
| [<span data-ttu-id="019c1-131">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="019c1-131">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="019c1-132">ja</span><span class="sxs-lookup"><span data-stu-id="019c1-132">yes</span></span>       |
| [<span data-ttu-id="019c1-133">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="019c1-133">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="019c1-134">nein</span><span class="sxs-lookup"><span data-stu-id="019c1-134">no</span></span>        |
| [<span data-ttu-id="019c1-135">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="019c1-135">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="019c1-136">nein</span><span class="sxs-lookup"><span data-stu-id="019c1-136">no</span></span>        |
| [<span data-ttu-id="019c1-137">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="019c1-137">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="019c1-138">nein</span><span class="sxs-lookup"><span data-stu-id="019c1-138">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="019c1-139">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="019c1-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="019c1-140">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="019c1-140">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





