---
title: Sätftigen (HLSL-Referenz)
description: Bindet das Ergebnis einer arithmetischen Operation mit einer Gleit Komma Zahl oder einer Gleit Komma Zahl mit doppelter Genauigkeit in \ 0,0 f... 1.0 f \ Bereich.
ms.assetid: ce3e79c7-c3e6-4a2c-910a-2cd568aece50
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 05b6048777ac7b6ecd2c4b59ff3c9e0287380949
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/23/2019
ms.locfileid: "104389632"
---
# <a name="saturate-hlsl-reference"></a><span data-ttu-id="8310b-103">Sätftigen (HLSL-Referenz)</span><span class="sxs-lookup"><span data-stu-id="8310b-103">Saturate (HLSL reference)</span></span>

<span data-ttu-id="8310b-104">Bindet das Ergebnis einer arithmetischen Operation mit einer Gleit Komma Zahl oder einer Gleit Komma Zahl mit doppelter Genauigkeit auf \[ 0,0 f... 1.0 f \] Bereich.</span><span class="sxs-lookup"><span data-stu-id="8310b-104">Clamps the result of a single or double precision floating point arithmetic operation to \[0.0f...1.0f\] range.</span></span>



| <span data-ttu-id="8310b-105">\_gesetzt</span><span class="sxs-lookup"><span data-stu-id="8310b-105">\_sat</span></span> |
|-------|



 

<span data-ttu-id="8310b-106">Der **ergebnismodifizierer** "Bezeichner" führt die folgenden Vorgänge für die Ergebnis Werte aus einer arithmetischen Operation für Gleit Komma Operationen aus, auf die festgelegt wurde \_ :</span><span class="sxs-lookup"><span data-stu-id="8310b-106">The **saturate** instruction result modifier performs the following operation on the result values(s) from a floating point arithmetic operation that has \_sat applied to it:</span></span>

`min(1.0f, max(0.0f, value))`

<span data-ttu-id="8310b-107">Dabei verhalten sich "min ()" und "Max ()" im obigen Ausdruck in der Art und Weise, wie [Min](min--sm4---asm-.md), [Max](max--sm4---asm-.md), [DMin](dmin--sm5---asm-.md)oder [DMax](dmax--sm5---asm-.md) betrieben werden.</span><span class="sxs-lookup"><span data-stu-id="8310b-107">where min() and max() in the above expression behave in the way [min](min--sm4---asm-.md), [max](max--sm4---asm-.md), [dmin](dmin--sm5---asm-.md), or [dmax](dmax--sm5---asm-.md) operate.</span></span>

<span data-ttu-id="8310b-108">`_sat(NaN)` gibt 0 zurück, durch die Regeln für min und Max.</span><span class="sxs-lookup"><span data-stu-id="8310b-108">`_sat(NaN)` returns 0, by the rules for min and max.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="8310b-109">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="8310b-109">Minimum Shader Model</span></span>

<span data-ttu-id="8310b-110">Dieser Modifizierer wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8310b-110">This modifier is supported in the following shader models.</span></span>



| <span data-ttu-id="8310b-111">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="8310b-111">Shader Model</span></span>                                              | <span data-ttu-id="8310b-112">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="8310b-112">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="8310b-113">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="8310b-113">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="8310b-114">ja</span><span class="sxs-lookup"><span data-stu-id="8310b-114">yes</span></span>       |
| [<span data-ttu-id="8310b-115">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="8310b-115">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="8310b-116">ja</span><span class="sxs-lookup"><span data-stu-id="8310b-116">yes</span></span>       |
| [<span data-ttu-id="8310b-117">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="8310b-117">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="8310b-118">ja</span><span class="sxs-lookup"><span data-stu-id="8310b-118">yes</span></span>       |
| [<span data-ttu-id="8310b-119">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8310b-119">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="8310b-120">nein</span><span class="sxs-lookup"><span data-stu-id="8310b-120">no</span></span>        |
| [<span data-ttu-id="8310b-121">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8310b-121">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="8310b-122">nein</span><span class="sxs-lookup"><span data-stu-id="8310b-122">no</span></span>        |
| [<span data-ttu-id="8310b-123">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8310b-123">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="8310b-124">nein</span><span class="sxs-lookup"><span data-stu-id="8310b-124">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="8310b-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8310b-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8310b-126">Anweisungs Modifizierer</span><span class="sxs-lookup"><span data-stu-id="8310b-126">Instruction Modifiers</span></span>](instruction-modifiers.md)
</dt> </dl>

 

 




