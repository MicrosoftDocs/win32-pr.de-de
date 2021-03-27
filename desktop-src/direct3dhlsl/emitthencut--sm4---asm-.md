---
title: emitthencut (SM4-ASM)
description: Entspricht einem Ausgabe Befehl gefolgt von einem Befehl zum Ausschneiden. | emitthencut (SM4-ASM)
ms.assetid: 80DE112A-790A-4DDF-A5BE-51F70BD7872C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb5b413ca11e22c7cfc17691fc0a39fe96bf7c0f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353859"
---
# <a name="emitthencut-sm4---asm"></a><span data-ttu-id="23963-104">emitthencut (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="23963-104">emitThenCut (sm4 - asm)</span></span>

<span data-ttu-id="23963-105">Entspricht einem Ausgabe [Befehl gefolgt von einem Befehl zum](emit--sm4---asm-.md) [Ausschneiden](cut--sm4---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="23963-105">Equivalent to an [emit](emit--sm4---asm-.md) command followed by a [cut](cut--sm4---asm-.md) command.</span></span>



| <span data-ttu-id="23963-106">emitthencut</span><span class="sxs-lookup"><span data-stu-id="23963-106">emitThenCut</span></span> |
|-------------|



 

## <a name="remarks"></a><span data-ttu-id="23963-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="23963-107">Remarks</span></span>

<span data-ttu-id="23963-108">Dieser Befehl ist nützlich, wenn der letzte Scheitelpunkt in einer Topologie wissentlich ausgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="23963-108">This command is useful when knowingly outputting the last vertex in a topology.</span></span>

<span data-ttu-id="23963-109">Wenn Streams deklariert wurden, müssen Sie [emitthenausschneide Daten \_ Strom](emitthencut-stream--sm5---asm-.md)verwenden.</span><span class="sxs-lookup"><span data-stu-id="23963-109">If streams have been declared, you must use [emitthencut\_stream](emitthencut-stream--sm5---asm-.md).</span></span>

<span data-ttu-id="23963-110">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="23963-110">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="23963-111">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="23963-111">Vertex Shader</span></span> | <span data-ttu-id="23963-112">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="23963-112">Geometry Shader</span></span> | <span data-ttu-id="23963-113">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="23963-113">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               | <span data-ttu-id="23963-114">x</span><span class="sxs-lookup"><span data-stu-id="23963-114">x</span></span>               |              |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="23963-115">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="23963-115">Minimum Shader Model</span></span>

<span data-ttu-id="23963-116">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="23963-116">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="23963-117">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="23963-117">Shader Model</span></span>                                              | <span data-ttu-id="23963-118">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="23963-118">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="23963-119">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="23963-119">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="23963-120">ja</span><span class="sxs-lookup"><span data-stu-id="23963-120">yes</span></span>       |
| [<span data-ttu-id="23963-121">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="23963-121">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="23963-122">ja</span><span class="sxs-lookup"><span data-stu-id="23963-122">yes</span></span>       |
| [<span data-ttu-id="23963-123">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="23963-123">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="23963-124">ja</span><span class="sxs-lookup"><span data-stu-id="23963-124">yes</span></span>       |
| [<span data-ttu-id="23963-125">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="23963-125">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="23963-126">nein</span><span class="sxs-lookup"><span data-stu-id="23963-126">no</span></span>        |
| [<span data-ttu-id="23963-127">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="23963-127">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="23963-128">nein</span><span class="sxs-lookup"><span data-stu-id="23963-128">no</span></span>        |
| [<span data-ttu-id="23963-129">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="23963-129">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="23963-130">nein</span><span class="sxs-lookup"><span data-stu-id="23963-130">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="23963-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="23963-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23963-132">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="23963-132">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




