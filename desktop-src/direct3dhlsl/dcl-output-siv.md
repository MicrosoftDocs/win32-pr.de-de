---
title: dcl_output_siv (SM4-ASM)
description: DCL \_ \_ -Ausgabe (SM4-ASM)
ms.assetid: 5a87a113-7413-48ef-9a6a-13eb185650be
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: df57ea991b9177dc081443301e426560834df894
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993215"
---
# <a name="dcl_output_siv-sm4---asm"></a><span data-ttu-id="8e282-103">DCL \_ \_ -Ausgabe (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="8e282-103">dcl\_output\_siv (sm4 - asm)</span></span>

<span data-ttu-id="8e282-104">Deklariert ein Ausgabe Register, das einen [System Wert](dx-graphics-hlsl-semantics.md) Parameter enthält.</span><span class="sxs-lookup"><span data-stu-id="8e282-104">Declares an output register that contains a [system-value](dx-graphics-hlsl-semantics.md) parameter.</span></span>



| <span data-ttu-id="8e282-105">DCL- \_ Ausgabe \_ SIV on \[ *. Masken* \] , *Systemwert*</span><span class="sxs-lookup"><span data-stu-id="8e282-105">dcl\_output\_siv oN\[*.masks*\], *systemValue*</span></span> |
|------------------------------------------------|



 



| <span data-ttu-id="8e282-106">Element</span><span class="sxs-lookup"><span data-stu-id="8e282-106">Item</span></span>                                                                                                                               | <span data-ttu-id="8e282-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8e282-107">Description</span></span>                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e282-108"><span id="oN"></span><span id="on"></span><span id="ON"></span>o *N*</span><span class="sxs-lookup"><span data-stu-id="8e282-108"><span id="oN"></span><span id="on"></span><span id="ON"></span>o *N*</span></span><br/>                                                     | <span data-ttu-id="8e282-109">\[in \] einem Ausgabedaten Register; *N* ist eine ganze Zahl, die die Registernummer bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="8e282-109">\[in\] An output data register; *N* is an integer that denotes the register number.</span></span><br/>                                                      |
| <span data-ttu-id="8e282-110"><span id="_.mask_"></span><span id="_.MASK_"></span>*\[. Mask\]*</span><span class="sxs-lookup"><span data-stu-id="8e282-110"><span id="_.mask_"></span><span id="_.MASK_"></span>*\[.mask\]*</span></span><br/>                                                         | <span data-ttu-id="8e282-111">\[in \] optional.</span><span class="sxs-lookup"><span data-stu-id="8e282-111">\[in\] Optional.</span></span> <span data-ttu-id="8e282-112">Eine Komponenten Maske (. xyzw), die angibt, welche der zu verwendenden Registrierungs Komponenten verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8e282-112">A component mask (.xyzw) that specifies which of the register components to use.</span></span><br/>                                        |
| <span data-ttu-id="8e282-113"><span id="systemValueName"></span><span id="systemvaluename"></span><span id="SYSTEMVALUENAME"></span>*systemvaluename*</span><span class="sxs-lookup"><span data-stu-id="8e282-113"><span id="systemValueName"></span><span id="systemvaluename"></span><span id="SYSTEMVALUENAME"></span>*systemValueName*</span></span><br/> | <span data-ttu-id="8e282-114">\[\]der Name des System Werts, bei dem es sich um eine Zeichenfolge handelt (siehe [System-Wert-Semantik](dx-graphics-hlsl-semantics.md)), ohne das Präfix "SV" \_ .</span><span class="sxs-lookup"><span data-stu-id="8e282-114">\[in\] The system-value name which is a string (see [system-value semantics](dx-graphics-hlsl-semantics.md)) without the "SV\_" prefix.</span></span><br/> |



 

<span data-ttu-id="8e282-115">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="8e282-115">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="8e282-116">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="8e282-116">Vertex Shader</span></span> | <span data-ttu-id="8e282-117">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="8e282-117">Geometry Shader</span></span> | <span data-ttu-id="8e282-118">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="8e282-118">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="8e282-119">x</span><span class="sxs-lookup"><span data-stu-id="8e282-119">x</span></span>             | <span data-ttu-id="8e282-120">x</span><span class="sxs-lookup"><span data-stu-id="8e282-120">x</span></span>               |              |



 

<span data-ttu-id="8e282-121">Diese Anweisung ist enthalten, um das Debuggen eines Shaders in der Assembly zu unterstützen. Es ist nicht möglich, einen Shader mit Shadermodell 4 in der Assemblysprache zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8e282-121">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="8e282-122">Beispiel</span><span class="sxs-lookup"><span data-stu-id="8e282-122">Example</span></span>

<span data-ttu-id="8e282-123">Hier einige Beispiele.</span><span class="sxs-lookup"><span data-stu-id="8e282-123">Here are some examples.</span></span>


```
dcl_output o[0].y
dcl_output_siv o[0].w, clipDistance
dcl_output_siv o[0].z, cullDistance
```



## <a name="minimum-shader-model"></a><span data-ttu-id="8e282-124">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="8e282-124">Minimum Shader Model</span></span>

<span data-ttu-id="8e282-125">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8e282-125">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="8e282-126">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="8e282-126">Shader Model</span></span>                                              | <span data-ttu-id="8e282-127">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="8e282-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="8e282-128">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="8e282-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="8e282-129">ja</span><span class="sxs-lookup"><span data-stu-id="8e282-129">yes</span></span>       |
| [<span data-ttu-id="8e282-130">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="8e282-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="8e282-131">ja</span><span class="sxs-lookup"><span data-stu-id="8e282-131">yes</span></span>       |
| [<span data-ttu-id="8e282-132">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="8e282-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="8e282-133">ja</span><span class="sxs-lookup"><span data-stu-id="8e282-133">yes</span></span>       |
| [<span data-ttu-id="8e282-134">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8e282-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="8e282-135">nein</span><span class="sxs-lookup"><span data-stu-id="8e282-135">no</span></span>        |
| [<span data-ttu-id="8e282-136">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8e282-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="8e282-137">nein</span><span class="sxs-lookup"><span data-stu-id="8e282-137">no</span></span>        |
| [<span data-ttu-id="8e282-138">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8e282-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="8e282-139">nein</span><span class="sxs-lookup"><span data-stu-id="8e282-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="8e282-140">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8e282-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e282-141">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8e282-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





