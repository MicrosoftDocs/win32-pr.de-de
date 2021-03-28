---
title: Endswitch (SM4-ASM)
description: Beendet eine Switch-Anweisung.
ms.assetid: ECAEECFD-B955-4356-B5C9-1D6A04C71D8F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 523a4008ab976ee299758349d57c6e32a3f336b2
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389484"
---
# <a name="endswitch-sm4---asm"></a><span data-ttu-id="34b4a-103">Endswitch (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="34b4a-103">endswitch (sm4 - asm)</span></span>

<span data-ttu-id="34b4a-104">Beendet eine [Switch](switch--sm4---asm-.md) -Anweisung.</span><span class="sxs-lookup"><span data-stu-id="34b4a-104">Ends a [switch](switch--sm4---asm-.md) statement.</span></span>



| <span data-ttu-id="34b4a-105">Endswitch</span><span class="sxs-lookup"><span data-stu-id="34b4a-105">endswitch</span></span> |
|-----------|



 

## <a name="remarks"></a><span data-ttu-id="34b4a-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="34b4a-106">Remarks</span></span>

<span data-ttu-id="34b4a-107">Das tokenformat enthält den Offset der entsprechenden Switch-Anweisung im Shader.</span><span class="sxs-lookup"><span data-stu-id="34b4a-107">The token format contains the offset of the corresponding switch instruction in the Shader as a convenience.</span></span>

<span data-ttu-id="34b4a-108">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="34b4a-108">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="34b4a-109">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="34b4a-109">Vertex Shader</span></span> | <span data-ttu-id="34b4a-110">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="34b4a-110">Geometry Shader</span></span> | <span data-ttu-id="34b4a-111">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="34b4a-111">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="34b4a-112">x</span><span class="sxs-lookup"><span data-stu-id="34b4a-112">x</span></span>             | <span data-ttu-id="34b4a-113">x</span><span class="sxs-lookup"><span data-stu-id="34b4a-113">x</span></span>               | <span data-ttu-id="34b4a-114">x</span><span class="sxs-lookup"><span data-stu-id="34b4a-114">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="34b4a-115">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="34b4a-115">Minimum Shader Model</span></span>

<span data-ttu-id="34b4a-116">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="34b4a-116">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="34b4a-117">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="34b4a-117">Shader Model</span></span>                                              | <span data-ttu-id="34b4a-118">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="34b4a-118">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="34b4a-119">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="34b4a-119">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="34b4a-120">ja</span><span class="sxs-lookup"><span data-stu-id="34b4a-120">yes</span></span>       |
| [<span data-ttu-id="34b4a-121">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="34b4a-121">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="34b4a-122">ja</span><span class="sxs-lookup"><span data-stu-id="34b4a-122">yes</span></span>       |
| [<span data-ttu-id="34b4a-123">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="34b4a-123">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="34b4a-124">ja</span><span class="sxs-lookup"><span data-stu-id="34b4a-124">yes</span></span>       |
| [<span data-ttu-id="34b4a-125">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="34b4a-125">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="34b4a-126">nein</span><span class="sxs-lookup"><span data-stu-id="34b4a-126">no</span></span>        |
| [<span data-ttu-id="34b4a-127">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="34b4a-127">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="34b4a-128">nein</span><span class="sxs-lookup"><span data-stu-id="34b4a-128">no</span></span>        |
| [<span data-ttu-id="34b4a-129">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="34b4a-129">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="34b4a-130">nein</span><span class="sxs-lookup"><span data-stu-id="34b4a-130">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="34b4a-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="34b4a-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34b4a-132">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="34b4a-132">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




