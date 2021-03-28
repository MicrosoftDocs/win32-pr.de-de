---
title: Standard (SM4-ASM)
description: Eine optionale Bezeichnung in einer Switch-Anweisung.
ms.assetid: DB10F654-4A98-4ED8-A3B4-CA9FE1DFE6CD
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b92364212e4d20a6e9229c057ba424f43f8f8556
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104976337"
---
# <a name="default-sm4---asm"></a><span data-ttu-id="0bc47-103">Standard (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="0bc47-103">default (sm4 - asm)</span></span>

<span data-ttu-id="0bc47-104">Eine optionale Bezeichnung in einer [Switch](switch--sm4---asm-.md) -Anweisung.</span><span class="sxs-lookup"><span data-stu-id="0bc47-104">An optional label in a [switch](switch--sm4---asm-.md) statement.</span></span>



| <span data-ttu-id="0bc47-105">default</span><span class="sxs-lookup"><span data-stu-id="0bc47-105">default</span></span> |
|---------|



 

## <a name="remarks"></a><span data-ttu-id="0bc47-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0bc47-106">Remarks</span></span>

<span data-ttu-id="0bc47-107">Diese Anweisung funktioniert genau wie **Standard** in C. das durchlaufen ist nur gültig, wenn kein Code hinzugefügt wurde, sodass mehrere Fälle (einschließlich **Standard**) denselben Codeblock gemeinsam verwenden können.</span><span class="sxs-lookup"><span data-stu-id="0bc47-107">This instruction operates just like **default** in C. Falling through is valid only if there is no code added, so multiple cases (including **default**) can share the same code block.</span></span>

<span data-ttu-id="0bc47-108">In einem switchkonstrukt ist **nur eine** **default** -Anweisung zulässig.</span><span class="sxs-lookup"><span data-stu-id="0bc47-108">Only one **default** statement is permitted in a **switch** construct.</span></span>

<span data-ttu-id="0bc47-109">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="0bc47-109">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="0bc47-110">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="0bc47-110">Vertex Shader</span></span> | <span data-ttu-id="0bc47-111">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="0bc47-111">Geometry Shader</span></span> | <span data-ttu-id="0bc47-112">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="0bc47-112">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="0bc47-113">x</span><span class="sxs-lookup"><span data-stu-id="0bc47-113">x</span></span>             | <span data-ttu-id="0bc47-114">x</span><span class="sxs-lookup"><span data-stu-id="0bc47-114">x</span></span>               | <span data-ttu-id="0bc47-115">x</span><span class="sxs-lookup"><span data-stu-id="0bc47-115">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="0bc47-116">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="0bc47-116">Minimum Shader Model</span></span>

<span data-ttu-id="0bc47-117">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0bc47-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="0bc47-118">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="0bc47-118">Shader Model</span></span>                                              | <span data-ttu-id="0bc47-119">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="0bc47-119">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="0bc47-120">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="0bc47-120">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="0bc47-121">ja</span><span class="sxs-lookup"><span data-stu-id="0bc47-121">yes</span></span>       |
| [<span data-ttu-id="0bc47-122">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="0bc47-122">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="0bc47-123">ja</span><span class="sxs-lookup"><span data-stu-id="0bc47-123">yes</span></span>       |
| [<span data-ttu-id="0bc47-124">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="0bc47-124">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="0bc47-125">ja</span><span class="sxs-lookup"><span data-stu-id="0bc47-125">yes</span></span>       |
| [<span data-ttu-id="0bc47-126">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0bc47-126">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="0bc47-127">nein</span><span class="sxs-lookup"><span data-stu-id="0bc47-127">no</span></span>        |
| [<span data-ttu-id="0bc47-128">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0bc47-128">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="0bc47-129">nein</span><span class="sxs-lookup"><span data-stu-id="0bc47-129">no</span></span>        |
| [<span data-ttu-id="0bc47-130">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0bc47-130">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="0bc47-131">nein</span><span class="sxs-lookup"><span data-stu-id="0bc47-131">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="0bc47-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0bc47-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0bc47-133">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0bc47-133">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




