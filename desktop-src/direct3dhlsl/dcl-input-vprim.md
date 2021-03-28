---
title: dcl_input vprim (SM4-ASM)
description: DCL \_ -Eingabe vprim (SM4-ASM)
ms.assetid: 75287673-21d6-4eb7-829f-7f2f340aec54
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9742c6066d66d7aa4121c1d1d1df98a37cb0147e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389600"
---
# <a name="dcl_input-vprim-sm4---asm"></a><span data-ttu-id="57199-103">DCL \_ -Eingabe vprim (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="57199-103">dcl\_input vPrim (sm4 - asm)</span></span>

<span data-ttu-id="57199-104">Deklariert, dass ein Geometry-Shader das skalareingabe-Register vprim verwendet.</span><span class="sxs-lookup"><span data-stu-id="57199-104">Declares that a geometry shader uses its scalar input-register vPrim.</span></span>



| <span data-ttu-id="57199-105">DCL- \_ Eingabe *vprim*</span><span class="sxs-lookup"><span data-stu-id="57199-105">dcl\_input *vPrim*</span></span> |
|--------------------|



 



| <span data-ttu-id="57199-106">Element</span><span class="sxs-lookup"><span data-stu-id="57199-106">Item</span></span>                                                                                       | <span data-ttu-id="57199-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="57199-107">Description</span></span>                                                                                              |
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57199-108"><span id="vPrim"></span><span id="vprim"></span><span id="VPRIM"></span>*vprim*</span><span class="sxs-lookup"><span data-stu-id="57199-108"><span id="vPrim"></span><span id="vprim"></span><span id="VPRIM"></span>*vPrim*</span></span><br/> | <span data-ttu-id="57199-109">\[in \] einem 32-Bit-Skalar, der auf jedes innere primitive in einem Geometry-Shader angewendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="57199-109">\[in\] A 32-bit scalar, which can be applied to each interior primitive in a geometry shader.</span></span><br/> |



 

<span data-ttu-id="57199-110">Der Skalar kann nicht auf benachbarte primitive angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="57199-110">The scalar cannot be applied to any adjacent primitives.</span></span>

<span data-ttu-id="57199-111">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="57199-111">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="57199-112">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="57199-112">Vertex Shader</span></span> | <span data-ttu-id="57199-113">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="57199-113">Geometry Shader</span></span> | <span data-ttu-id="57199-114">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="57199-114">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               | <span data-ttu-id="57199-115">x</span><span class="sxs-lookup"><span data-stu-id="57199-115">x</span></span>               |              |



 

<span data-ttu-id="57199-116">Diese Anweisung ist enthalten, um das Debuggen eines Shaders in der Assembly zu unterstützen. Es ist nicht möglich, einen Shader mit Shadermodell 4 in der Assemblysprache zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="57199-116">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="57199-117">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="57199-117">Minimum Shader Model</span></span>

<span data-ttu-id="57199-118">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="57199-118">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="57199-119">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="57199-119">Shader Model</span></span>                                              | <span data-ttu-id="57199-120">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="57199-120">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="57199-121">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="57199-121">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="57199-122">ja</span><span class="sxs-lookup"><span data-stu-id="57199-122">yes</span></span>       |
| [<span data-ttu-id="57199-123">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="57199-123">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="57199-124">ja</span><span class="sxs-lookup"><span data-stu-id="57199-124">yes</span></span>       |
| [<span data-ttu-id="57199-125">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="57199-125">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="57199-126">ja</span><span class="sxs-lookup"><span data-stu-id="57199-126">yes</span></span>       |
| [<span data-ttu-id="57199-127">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="57199-127">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="57199-128">nein</span><span class="sxs-lookup"><span data-stu-id="57199-128">no</span></span>        |
| [<span data-ttu-id="57199-129">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="57199-129">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="57199-130">nein</span><span class="sxs-lookup"><span data-stu-id="57199-130">no</span></span>        |
| [<span data-ttu-id="57199-131">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="57199-131">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="57199-132">nein</span><span class="sxs-lookup"><span data-stu-id="57199-132">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="57199-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="57199-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="57199-134">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="57199-134">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





