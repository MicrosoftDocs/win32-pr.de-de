---
title: Lit-vs
description: Bietet partielle Unterstützung für Beleuchtung durch Berechnen von Beleuchtungs Koeffizienten aus zwei Punkt Produkten und einem Exponenten.
ms.assetid: e0ed1a75-6682-4d05-b0e5-dc65e201de98
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 99c25c377ff6064a704d56b9e7b31d41b37117e5
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104976393"
---
# <a name="lit---vs"></a><span data-ttu-id="3366c-103">Lit-vs</span><span class="sxs-lookup"><span data-stu-id="3366c-103">lit - vs</span></span>

<span data-ttu-id="3366c-104">Bietet partielle Unterstützung für Beleuchtung durch Berechnen von Beleuchtungs Koeffizienten aus zwei Punkt Produkten und einem Exponenten.</span><span class="sxs-lookup"><span data-stu-id="3366c-104">Provides partial support for lighting by calculating lighting coefficients from two dot products and an exponent.</span></span>

## <a name="syntax"></a><span data-ttu-id="3366c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3366c-105">Syntax</span></span>



| <span data-ttu-id="3366c-106">Lit DST, src</span><span class="sxs-lookup"><span data-stu-id="3366c-106">lit dst, src</span></span> |
|--------------|



 

<span data-ttu-id="3366c-107">where</span><span class="sxs-lookup"><span data-stu-id="3366c-107">where</span></span>

-   <span data-ttu-id="3366c-108">DST ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="3366c-108">dst is the destination register.</span></span>
-   <span data-ttu-id="3366c-109">src ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="3366c-109">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="3366c-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3366c-110">Remarks</span></span>



| <span data-ttu-id="3366c-111">Vertex-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="3366c-111">Vertex shader versions</span></span> | <span data-ttu-id="3366c-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="3366c-112">1\_1</span></span> | <span data-ttu-id="3366c-113">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3366c-113">2\_0</span></span> | <span data-ttu-id="3366c-114">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="3366c-114">2\_x</span></span> | <span data-ttu-id="3366c-115">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="3366c-115">2\_sw</span></span> | <span data-ttu-id="3366c-116">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3366c-116">3\_0</span></span> | <span data-ttu-id="3366c-117">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="3366c-117">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="3366c-118">gezündet</span><span class="sxs-lookup"><span data-stu-id="3366c-118">lit</span></span>                    | <span data-ttu-id="3366c-119">x</span><span class="sxs-lookup"><span data-stu-id="3366c-119">x</span></span>    | <span data-ttu-id="3366c-120">x</span><span class="sxs-lookup"><span data-stu-id="3366c-120">x</span></span>    | <span data-ttu-id="3366c-121">x</span><span class="sxs-lookup"><span data-stu-id="3366c-121">x</span></span>    | <span data-ttu-id="3366c-122">x</span><span class="sxs-lookup"><span data-stu-id="3366c-122">x</span></span>     | <span data-ttu-id="3366c-123">x</span><span class="sxs-lookup"><span data-stu-id="3366c-123">x</span></span>    | <span data-ttu-id="3366c-124">x</span><span class="sxs-lookup"><span data-stu-id="3366c-124">x</span></span>     |



 

<span data-ttu-id="3366c-125">Es wird davon ausgegangen, dass der Quell Vektor die Werte enthält, die im folgenden Pseudocode angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="3366c-125">The source vector is assumed to contain the values shown in the following pseudocode.</span></span>


```
src.x = N*L        ; The dot product between normal and direction to light
src.y = N*H        ; The dot product between normal and half vector
src.z = ignored    ; This value is ignored
src.w = exponent   ; The value must be between -128.0 and 128.0
```



<span data-ttu-id="3366c-126">Das folgende Code Fragment zeigt die ausgeführten Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="3366c-126">The following code fragment shows the operations performed.</span></span>


```
dest.x = 1;
dest.y = 0;
dest.z = 0;
dest.w = 1;

float power = src.w;
const float MAXPOWER = 127.9961f;
if (power < -MAXPOWER)
    power = -MAXPOWER;          // Fits into 8.8 fixed point format
else if (power > MAXPOWER)
    power = MAXPOWER;          // Fits into 8.8 fixed point format

if (src.x > 0)
{
    dest.y = src.x;
    if (src.y > 0)
    {
        // Allowed approximation is EXP(power * LOG(src.y))
        dest.z = (float)(pow(src.y, power));
    }
}
```



<span data-ttu-id="3366c-127">Die arithmetische Genauigkeit mit eingeschränkter Genauigkeit ist bei der Auswertung der y-Zielkomponente (dest. y) zulässig.</span><span class="sxs-lookup"><span data-stu-id="3366c-127">Reduced precision arithmetic is acceptable in evaluating the destination y component (dest.y).</span></span> <span data-ttu-id="3366c-128">Eine-Implementierung muss mindestens acht Bruch Bits im Power-Argument unterstützen.</span><span class="sxs-lookup"><span data-stu-id="3366c-128">An implementation must support at least eight fraction bits in the power argument.</span></span> <span data-ttu-id="3366c-129">Punkt Produkte werden mit normalisierten Vektoren berechnet, und die Grenzwerte liegen zwischen-128 und 128.</span><span class="sxs-lookup"><span data-stu-id="3366c-129">Dot products are calculated with normalized vectors, and clamp limits are -128 to 128.</span></span>

<span data-ttu-id="3366c-130">Der Fehler sollte mit einer Kombination aus [LogP-vs](logp---vs.md) und [Exp-vs](exp---vs.md) oder nicht mehr als ungefähr einem signifikanten Bit für eine 8-Bit-Farbkomponente übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="3366c-130">Error should correspond to a [logp - vs](logp---vs.md) and [exp - vs](exp---vs.md) combination, or no more than approximately one significant bit for an 8-bit color component.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3366c-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3366c-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3366c-132">Vertex-shaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="3366c-132">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




