---
title: dcl_globalFlags (SM4-ASM)
description: DCL \_ globalflags (SM4-ASM)
ms.assetid: 7289db9e-f0cd-4849-854f-34aa38ec2c2d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e15fce958056f91a41954b987850ad4c5a43e521
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389604"
---
# <a name="dcl_globalflags-sm4---asm"></a><span data-ttu-id="6a2a7-103">DCL \_ globalflags (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="6a2a7-103">dcl\_globalFlags (sm4 - asm)</span></span>

<span data-ttu-id="6a2a7-104">Deklariert globale Shader-Flags.</span><span class="sxs-lookup"><span data-stu-id="6a2a7-104">Declares shader global flags.</span></span>



| <span data-ttu-id="6a2a7-105">DCL \_ globalflags- *Flags*</span><span class="sxs-lookup"><span data-stu-id="6a2a7-105">dcl\_globalFlags *flags*</span></span> |
|--------------------------|



 

<dl> <dt>

<span data-ttu-id="6a2a7-106"><span id="flags"></span><span id="FLAGS"></span>*fahren*</span><span class="sxs-lookup"><span data-stu-id="6a2a7-106"><span id="flags"></span><span id="FLAGS"></span>*flags*</span></span>
</dt> <dd>

<span data-ttu-id="6a2a7-107">\[in \] einem globalen Shader-Flag.</span><span class="sxs-lookup"><span data-stu-id="6a2a7-107">\[in\] A global shader flag.</span></span> <span data-ttu-id="6a2a7-108">Zurzeit ist ein Flag definiert.</span><span class="sxs-lookup"><span data-stu-id="6a2a7-108">There is currently one flag defined.</span></span>

-   <span data-ttu-id="6a2a7-109">Refactoring \_ zulässig: erlaubt dem Treiber das Neuordnen arithmetischer Vorgänge zur Optimierung, wie hier gezeigt.</span><span class="sxs-lookup"><span data-stu-id="6a2a7-109">REFACTORING\_ALLOWED - Permits the driver to reorder arithmetic operations for optimization, as shown here.</span></span>

    ```
    // Original code
    a = b*c + b*d + b*e + b*f

    // Reordered code
    a = b*(c + d + e + f)
    // or 
    a = dot4((b,b,b,b), (c,d,e,f))
    ```

    

> [!Note]
>
> <span data-ttu-id="6a2a7-110">Durch die Neuanordnung arithmetischer Vorgänge werden möglicherweise andere Ergebnisse generiert.</span><span class="sxs-lookup"><span data-stu-id="6a2a7-110">Reordering arithmetic operations may generate different results.</span></span>

 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="6a2a7-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6a2a7-111">Remarks</span></span>

<span data-ttu-id="6a2a7-112">Diese optionale Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="6a2a7-112">This optional instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="6a2a7-113">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="6a2a7-113">Vertex Shader</span></span> | <span data-ttu-id="6a2a7-114">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="6a2a7-114">Geometry Shader</span></span> | <span data-ttu-id="6a2a7-115">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="6a2a7-115">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="6a2a7-116">x</span><span class="sxs-lookup"><span data-stu-id="6a2a7-116">x</span></span>             | <span data-ttu-id="6a2a7-117">x</span><span class="sxs-lookup"><span data-stu-id="6a2a7-117">x</span></span>               | <span data-ttu-id="6a2a7-118">x</span><span class="sxs-lookup"><span data-stu-id="6a2a7-118">x</span></span>            |



 

<span data-ttu-id="6a2a7-119">Diese Anweisung ist enthalten, um das Debuggen eines Shaders in der Assembly zu unterstützen. Es ist nicht möglich, einen Shader mit Shadermodell 4 in der Assemblysprache zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="6a2a7-119">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="6a2a7-120">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="6a2a7-120">Minimum Shader Model</span></span>

<span data-ttu-id="6a2a7-121">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6a2a7-121">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="6a2a7-122">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="6a2a7-122">Shader Model</span></span>                                              | <span data-ttu-id="6a2a7-123">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="6a2a7-123">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="6a2a7-124">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="6a2a7-124">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="6a2a7-125">ja</span><span class="sxs-lookup"><span data-stu-id="6a2a7-125">yes</span></span>       |
| [<span data-ttu-id="6a2a7-126">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="6a2a7-126">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="6a2a7-127">ja</span><span class="sxs-lookup"><span data-stu-id="6a2a7-127">yes</span></span>       |
| [<span data-ttu-id="6a2a7-128">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="6a2a7-128">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="6a2a7-129">ja</span><span class="sxs-lookup"><span data-stu-id="6a2a7-129">yes</span></span>       |
| [<span data-ttu-id="6a2a7-130">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6a2a7-130">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="6a2a7-131">nein</span><span class="sxs-lookup"><span data-stu-id="6a2a7-131">no</span></span>        |
| [<span data-ttu-id="6a2a7-132">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6a2a7-132">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="6a2a7-133">nein</span><span class="sxs-lookup"><span data-stu-id="6a2a7-133">no</span></span>        |
| [<span data-ttu-id="6a2a7-134">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6a2a7-134">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="6a2a7-135">nein</span><span class="sxs-lookup"><span data-stu-id="6a2a7-135">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="6a2a7-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6a2a7-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a2a7-137">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6a2a7-137">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




