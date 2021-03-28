---
title: Negate
description: Flippt das Vorzeichen des Werts eines Quell Operanden, der in einer arithmetischen Operation verwendet wird.
ms.assetid: 83ef3f61-7b0b-4033-8f7b-5345b205c441
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cc2637a76b52b28eefcfb3637cc8b2d406c02c06
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104038320"
---
# <a name="negate"></a><span data-ttu-id="4aa1c-103">Negate</span><span class="sxs-lookup"><span data-stu-id="4aa1c-103">Negate</span></span>

<span data-ttu-id="4aa1c-104">Flippt das Vorzeichen des Werts eines Quell Operanden, der in einer arithmetischen Operation verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4aa1c-104">Flips the sign of the value of a source operand used in an arithmetic operation.</span></span>



| \-  |
|-----|



 

<span data-ttu-id="4aa1c-105">Für Gleit Komma-und-Anweisungen mit einfacher und doppelter Genauigkeit flippt der Negation-Modifizierer das Vorzeichen der Zahl (n) im Quell Operanden, einschließlich der INF-Werte.</span><span class="sxs-lookup"><span data-stu-id="4aa1c-105">For single and double precision floating point and instructions, the negate modifier flips the sign of the number(s) in the source operand, including on INF values.</span></span> <span data-ttu-id="4aa1c-106">Das Anwenden von **Negation** auf NaN behält Nan bei, obwohl das betreffende Nan-Bitmuster nicht definiert ist.</span><span class="sxs-lookup"><span data-stu-id="4aa1c-106">Applying **negate** on NaN preserves NaN, although the particular NaN bit pattern that results is not defined.</span></span>

<span data-ttu-id="4aa1c-107">Für ganzzahlige Anweisungen nimmt der **Negation-Modifizierer** das 2-Komplement der Zahl (n) im Quell Operanden an.</span><span class="sxs-lookup"><span data-stu-id="4aa1c-107">For integer instructions, the **negate** modifier takes the 2's complement of the number(s) in the source operand.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="4aa1c-108">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="4aa1c-108">Minimum Shader Model</span></span>

<span data-ttu-id="4aa1c-109">Dieser Modifizierer wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4aa1c-109">This modifier is supported in the following shader models.</span></span>



| <span data-ttu-id="4aa1c-110">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="4aa1c-110">Shader Model</span></span>                                              | <span data-ttu-id="4aa1c-111">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="4aa1c-111">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="4aa1c-112">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="4aa1c-112">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="4aa1c-113">ja</span><span class="sxs-lookup"><span data-stu-id="4aa1c-113">yes</span></span>       |
| [<span data-ttu-id="4aa1c-114">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="4aa1c-114">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="4aa1c-115">ja</span><span class="sxs-lookup"><span data-stu-id="4aa1c-115">yes</span></span>       |
| [<span data-ttu-id="4aa1c-116">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="4aa1c-116">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="4aa1c-117">ja</span><span class="sxs-lookup"><span data-stu-id="4aa1c-117">yes</span></span>       |
| [<span data-ttu-id="4aa1c-118">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4aa1c-118">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="4aa1c-119">nein</span><span class="sxs-lookup"><span data-stu-id="4aa1c-119">no</span></span>        |
| [<span data-ttu-id="4aa1c-120">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4aa1c-120">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="4aa1c-121">nein</span><span class="sxs-lookup"><span data-stu-id="4aa1c-121">no</span></span>        |
| [<span data-ttu-id="4aa1c-122">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4aa1c-122">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="4aa1c-123">nein</span><span class="sxs-lookup"><span data-stu-id="4aa1c-123">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="4aa1c-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4aa1c-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4aa1c-125">Anweisungs Modifizierer</span><span class="sxs-lookup"><span data-stu-id="4aa1c-125">Instruction Modifiers</span></span>](instruction-modifiers.md)
</dt> </dl>

 

 




