---
title: Absoluter Wert
description: Verwenden Sie den absoluten Wert eines Quell Operanden, der in einer arithmetischen Operation verwendet wird.
ms.assetid: FD2ACE91-0AF6-43E8-80C5-849488E39BEF
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 27ceefa2c4b4ee2eb890b0692a33266e89a18cfb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313740"
---
# <a name="absolute-value"></a><span data-ttu-id="350e0-103">Absoluter Wert</span><span class="sxs-lookup"><span data-stu-id="350e0-103">Absolute Value</span></span>

<span data-ttu-id="350e0-104">Verwenden Sie den absoluten Wert eines Quell Operanden, der in einer arithmetischen Operation verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="350e0-104">Take the absolute value of a source operand used in an arithmetic operation.</span></span>



| <span data-ttu-id="350e0-105">\_Stäbchen</span><span class="sxs-lookup"><span data-stu-id="350e0-105">\_abs</span></span> |
|-------|



 

<span data-ttu-id="350e0-106">Dieser Modifizierer wird für Gleit Komma-und Gleit Komma Zahlen mit doppelter Genauigkeit und nur Anweisungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="350e0-106">This modifier is used for single and double precision floating point and instructions only.</span></span> <span data-ttu-id="350e0-107">Der **\_ ABS** -Modifizierer erzwingt das Vorzeichen der Zahl (en) im Quell Operanden, einschließlich der INF-Werte.</span><span class="sxs-lookup"><span data-stu-id="350e0-107">The **\_abs** modifier forces the sign of the number(s) on the source operand positive, including on INF values.</span></span>

<span data-ttu-id="350e0-108">Das Anwenden von **\_ ABS** auf NaN behält Nan bei, obwohl das betreffende Nan-Bitmuster nicht definiert ist.</span><span class="sxs-lookup"><span data-stu-id="350e0-108">Applying **\_abs** on NaN preserves NaN, although the particular NaN bit pattern that results is not defined.</span></span>

<span data-ttu-id="350e0-109">Wenn \_ ABS mit dem [Negation-Modifizierer](negate.md) kombiniert wird, erzwingt die Kombination das Vorzeichen, dass das Vorzeichen negativ ist, als wenn der **\_ ABS** - **Modifizierer** zuerst angewendet wird, dann die Negation.</span><span class="sxs-lookup"><span data-stu-id="350e0-109">When \_abs is combined with the [negate](negate.md) modifier, the combination forces the sign to be negative, as if the **\_abs** modifier is applied first, then the **negate**.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="350e0-110">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="350e0-110">Minimum Shader Model</span></span>

<span data-ttu-id="350e0-111">Dieser Modifizierer wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="350e0-111">This modifier is supported in the following shader models.</span></span>



| <span data-ttu-id="350e0-112">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="350e0-112">Shader Model</span></span>                                              | <span data-ttu-id="350e0-113">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="350e0-113">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="350e0-114">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="350e0-114">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="350e0-115">ja</span><span class="sxs-lookup"><span data-stu-id="350e0-115">yes</span></span>       |
| [<span data-ttu-id="350e0-116">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="350e0-116">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="350e0-117">ja</span><span class="sxs-lookup"><span data-stu-id="350e0-117">yes</span></span>       |
| [<span data-ttu-id="350e0-118">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="350e0-118">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="350e0-119">ja</span><span class="sxs-lookup"><span data-stu-id="350e0-119">yes</span></span>       |
| [<span data-ttu-id="350e0-120">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="350e0-120">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="350e0-121">nein</span><span class="sxs-lookup"><span data-stu-id="350e0-121">no</span></span>        |
| [<span data-ttu-id="350e0-122">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="350e0-122">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="350e0-123">nein</span><span class="sxs-lookup"><span data-stu-id="350e0-123">no</span></span>        |
| [<span data-ttu-id="350e0-124">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="350e0-124">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="350e0-125">nein</span><span class="sxs-lookup"><span data-stu-id="350e0-125">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="350e0-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="350e0-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="350e0-127">Anweisungs Modifizierer</span><span class="sxs-lookup"><span data-stu-id="350e0-127">Instruction Modifiers</span></span>](instruction-modifiers.md)
</dt> </dl>

 

 




