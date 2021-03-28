---
title: dcl_immediateConstantBuffer (SM4-ASM)
description: DCL \_ unmittelateconstantbuffer (SM4-ASM)
ms.assetid: 55e21ab1-0749-4200-8e68-bb098e935dac
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6f4b4868f3b07285465abb9080688adf6129e1bf
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313769"
---
# <a name="dcl_immediateconstantbuffer-sm4---asm"></a><span data-ttu-id="580d3-103">DCL \_ unmittelateconstantbuffer (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="580d3-103">dcl\_immediateConstantBuffer (sm4 - asm)</span></span>

<span data-ttu-id="580d3-104">Deklariert einen direkt Konstanten Shader-Puffer.</span><span class="sxs-lookup"><span data-stu-id="580d3-104">Declares a shader immediate-constant buffer.</span></span>



| <span data-ttu-id="580d3-105">DCL \_ unmittelateconstantbuffer- *Wert (e)*</span><span class="sxs-lookup"><span data-stu-id="580d3-105">dcl\_immediateConstantBuffer *value(s)*</span></span> |
|-----------------------------------------|



 

<dl> <dt>

<span data-ttu-id="580d3-106"><span id="value_s_"></span><span id="VALUE_S_"></span>*Wert (e)*</span><span class="sxs-lookup"><span data-stu-id="580d3-106"><span id="value_s_"></span><span id="VALUE_S_"></span>*value(s)*</span></span>
</dt> <dd>

<span data-ttu-id="580d3-107">\[im \] Puffer muss mindestens ein Wert, jedoch nicht mehr als 4096 Werte enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="580d3-107">\[in\] The buffer must contain at least one value, but not more than 4096 values.</span></span>

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="580d3-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="580d3-108">Remarks</span></span>

<span data-ttu-id="580d3-109">Ein Shader ist ein unmittelbar konstanter Puffer zulässig.</span><span class="sxs-lookup"><span data-stu-id="580d3-109">A shader is allowed one immediate-constant buffer.</span></span> <span data-ttu-id="580d3-110">Der Zugriff auf einen unmittelbar Konstanten Puffer erfolgt genau wie ein konstanter Puffer mit dynamischer Indizierung.</span><span class="sxs-lookup"><span data-stu-id="580d3-110">An immediate-constant buffer is accessed just like a constant buffer with dynamic indexing.</span></span>

<span data-ttu-id="580d3-111">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="580d3-111">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="580d3-112">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="580d3-112">Vertex Shader</span></span> | <span data-ttu-id="580d3-113">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="580d3-113">Geometry Shader</span></span> | <span data-ttu-id="580d3-114">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="580d3-114">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="580d3-115">x</span><span class="sxs-lookup"><span data-stu-id="580d3-115">x</span></span>             | <span data-ttu-id="580d3-116">x</span><span class="sxs-lookup"><span data-stu-id="580d3-116">x</span></span>               | <span data-ttu-id="580d3-117">x</span><span class="sxs-lookup"><span data-stu-id="580d3-117">x</span></span>            |



 

<span data-ttu-id="580d3-118">Diese Anweisung ist enthalten, um das Debuggen eines Shaders in der Assembly zu unterstützen. Es ist nicht möglich, einen Shader mit Shadermodell 4 in der Assemblysprache zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="580d3-118">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="580d3-119">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="580d3-119">Minimum Shader Model</span></span>

<span data-ttu-id="580d3-120">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="580d3-120">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="580d3-121">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="580d3-121">Shader Model</span></span>                                              | <span data-ttu-id="580d3-122">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="580d3-122">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="580d3-123">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="580d3-123">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="580d3-124">ja</span><span class="sxs-lookup"><span data-stu-id="580d3-124">yes</span></span>       |
| [<span data-ttu-id="580d3-125">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="580d3-125">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="580d3-126">ja</span><span class="sxs-lookup"><span data-stu-id="580d3-126">yes</span></span>       |
| [<span data-ttu-id="580d3-127">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="580d3-127">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="580d3-128">ja</span><span class="sxs-lookup"><span data-stu-id="580d3-128">yes</span></span>       |
| [<span data-ttu-id="580d3-129">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="580d3-129">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="580d3-130">nein</span><span class="sxs-lookup"><span data-stu-id="580d3-130">no</span></span>        |
| [<span data-ttu-id="580d3-131">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="580d3-131">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="580d3-132">nein</span><span class="sxs-lookup"><span data-stu-id="580d3-132">no</span></span>        |
| [<span data-ttu-id="580d3-133">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="580d3-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="580d3-134">nein</span><span class="sxs-lookup"><span data-stu-id="580d3-134">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="580d3-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="580d3-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="580d3-136">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="580d3-136">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




