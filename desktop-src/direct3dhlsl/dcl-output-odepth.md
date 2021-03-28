---
title: dcl_output otiefe (SM4-ASM)
description: DCL- \_ Ausgabe-otiefe (SM4-ASM)
ms.assetid: 7ee3026d-507f-4aa8-8335-d92c5f649f46
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 43580a542c1a66961cfa7434c65cd8d271fb0367
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313757"
---
# <a name="dcl_output-odepth-sm4---asm"></a><span data-ttu-id="53c6c-103">DCL- \_ Ausgabe-otiefe (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="53c6c-103">dcl\_output oDepth (sm4 - asm)</span></span>

<span data-ttu-id="53c6c-104">Deklariert, dass ein Pixelshader das Ausgabe tiefen Register verwendet.</span><span class="sxs-lookup"><span data-stu-id="53c6c-104">Declares that a pixel shader will use the output-depth register.</span></span>



| <span data-ttu-id="53c6c-105">DCL- \_ Ausgabe-otiefe</span><span class="sxs-lookup"><span data-stu-id="53c6c-105">dcl\_output oDepth</span></span> |
|--------------------|



 

<span data-ttu-id="53c6c-106">Der Wert im Ausgabe tiefen Register wird bei einem tiefen Vergleich verwendet (wenn der tiefen Vergleich aktiviert ist).</span><span class="sxs-lookup"><span data-stu-id="53c6c-106">The value in the output-depth register is used during a depth comparison (if depth compare is enabled).</span></span>

<span data-ttu-id="53c6c-107">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="53c6c-107">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="53c6c-108">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="53c6c-108">Vertex Shader</span></span> | <span data-ttu-id="53c6c-109">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="53c6c-109">Geometry Shader</span></span> | <span data-ttu-id="53c6c-110">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="53c6c-110">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               |                 | <span data-ttu-id="53c6c-111">x</span><span class="sxs-lookup"><span data-stu-id="53c6c-111">x</span></span>            |



 

<span data-ttu-id="53c6c-112">Diese Anweisung ist enthalten, um das Debuggen eines Shaders in der Assembly zu unterstützen. Es ist nicht möglich, einen Shader mit Shadermodell 4 in der Assemblysprache zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="53c6c-112">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="53c6c-113">Beispiel</span><span class="sxs-lookup"><span data-stu-id="53c6c-113">Example</span></span>

<span data-ttu-id="53c6c-114">Hier einige Beispiele.</span><span class="sxs-lookup"><span data-stu-id="53c6c-114">Here are some examples.</span></span>


```
dcl_output oDepth
```



## <a name="minimum-shader-model"></a><span data-ttu-id="53c6c-115">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="53c6c-115">Minimum Shader Model</span></span>

<span data-ttu-id="53c6c-116">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="53c6c-116">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="53c6c-117">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="53c6c-117">Shader Model</span></span>                                              | <span data-ttu-id="53c6c-118">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="53c6c-118">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="53c6c-119">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="53c6c-119">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="53c6c-120">ja</span><span class="sxs-lookup"><span data-stu-id="53c6c-120">yes</span></span>       |
| [<span data-ttu-id="53c6c-121">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="53c6c-121">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="53c6c-122">ja</span><span class="sxs-lookup"><span data-stu-id="53c6c-122">yes</span></span>       |
| [<span data-ttu-id="53c6c-123">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="53c6c-123">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="53c6c-124">ja</span><span class="sxs-lookup"><span data-stu-id="53c6c-124">yes</span></span>       |
| [<span data-ttu-id="53c6c-125">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="53c6c-125">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="53c6c-126">nein</span><span class="sxs-lookup"><span data-stu-id="53c6c-126">no</span></span>        |
| [<span data-ttu-id="53c6c-127">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="53c6c-127">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="53c6c-128">nein</span><span class="sxs-lookup"><span data-stu-id="53c6c-128">no</span></span>        |
| [<span data-ttu-id="53c6c-129">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="53c6c-129">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="53c6c-130">nein</span><span class="sxs-lookup"><span data-stu-id="53c6c-130">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="53c6c-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="53c6c-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53c6c-132">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="53c6c-132">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




