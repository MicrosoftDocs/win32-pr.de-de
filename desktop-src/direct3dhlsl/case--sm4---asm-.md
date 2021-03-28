---
title: Case (SM4-ASM)
description: Eine Bezeichnung in einer Switch-Anweisung.
ms.assetid: 456BB918-327E-4E15-8D38-F53850CAF666
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0278b8492575b1ef54fd64fc24b031fdec6cfb21
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104976369"
---
# <a name="case-sm4---asm"></a><span data-ttu-id="eed77-103">Case (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="eed77-103">case (sm4 - asm)</span></span>

<span data-ttu-id="eed77-104">Eine Bezeichnung in einer Switch-Anweisung.</span><span class="sxs-lookup"><span data-stu-id="eed77-104">A label in a switch instruction.</span></span>



| <span data-ttu-id="eed77-105">Groß-/Kleinschreibung \[ 32-Bit\]</span><span class="sxs-lookup"><span data-stu-id="eed77-105">case \[32-bit immediate\]</span></span> |
|---------------------------|



 

## <a name="remarks"></a><span data-ttu-id="eed77-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eed77-106">Remarks</span></span>

<span data-ttu-id="eed77-107">Da das Durchlaufen von **Fällen** nur gültig ist, wenn kein Code hinzugefügt wurde, können mehrere **Fälle** (einschließlich [Standard](default--sm4---asm-.md)) denselben Codeblock gemeinsam verwenden.</span><span class="sxs-lookup"><span data-stu-id="eed77-107">Because falling through **cases** is valid only if there is no code added, multiple **cases** (including [default](default--sm4---asm-.md)) can share the same code block.</span></span>

<span data-ttu-id="eed77-108">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="eed77-108">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="eed77-109">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="eed77-109">Vertex Shader</span></span> | <span data-ttu-id="eed77-110">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="eed77-110">Geometry Shader</span></span> | <span data-ttu-id="eed77-111">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="eed77-111">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="eed77-112">x</span><span class="sxs-lookup"><span data-stu-id="eed77-112">x</span></span>             | <span data-ttu-id="eed77-113">x</span><span class="sxs-lookup"><span data-stu-id="eed77-113">x</span></span>               | <span data-ttu-id="eed77-114">x</span><span class="sxs-lookup"><span data-stu-id="eed77-114">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="eed77-115">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="eed77-115">Minimum Shader Model</span></span>

<span data-ttu-id="eed77-116">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="eed77-116">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="eed77-117">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="eed77-117">Shader Model</span></span>                                              | <span data-ttu-id="eed77-118">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="eed77-118">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="eed77-119">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="eed77-119">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="eed77-120">ja</span><span class="sxs-lookup"><span data-stu-id="eed77-120">yes</span></span>       |
| [<span data-ttu-id="eed77-121">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="eed77-121">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="eed77-122">ja</span><span class="sxs-lookup"><span data-stu-id="eed77-122">yes</span></span>       |
| [<span data-ttu-id="eed77-123">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="eed77-123">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="eed77-124">ja</span><span class="sxs-lookup"><span data-stu-id="eed77-124">yes</span></span>       |
| [<span data-ttu-id="eed77-125">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="eed77-125">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="eed77-126">nein</span><span class="sxs-lookup"><span data-stu-id="eed77-126">no</span></span>        |
| [<span data-ttu-id="eed77-127">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="eed77-127">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="eed77-128">nein</span><span class="sxs-lookup"><span data-stu-id="eed77-128">no</span></span>        |
| [<span data-ttu-id="eed77-129">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="eed77-129">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="eed77-130">nein</span><span class="sxs-lookup"><span data-stu-id="eed77-130">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="eed77-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="eed77-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eed77-132">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="eed77-132">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




