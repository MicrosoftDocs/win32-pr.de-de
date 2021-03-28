---
title: CND-PS
description: Wählt bedingt zwischen Quelle1 und Quelle2 basierend auf dem Vergleich src0 0,5 aus.
ms.assetid: 7a3b49e9-d146-47dc-99a8-4f336db7d0d5
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1fd3a14e2ac4bd283a4e67724fbb42ac965ea707
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104101082"
---
# <a name="cnd---ps"></a><span data-ttu-id="f6276-103">CND-PS</span><span class="sxs-lookup"><span data-stu-id="f6276-103">cnd - ps</span></span>

<span data-ttu-id="f6276-104">Wählt bedingt zwischen Quelle1 und Quelle2 basierend auf dem Vergleich src0 > 0,5 aus.</span><span class="sxs-lookup"><span data-stu-id="f6276-104">Conditionally chooses between src1 and src2, based on the comparison src0 > 0.5.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6276-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f6276-105">Syntax</span></span>



| <span data-ttu-id="f6276-106">CND DST, src0, Quelle1, Quelle2</span><span class="sxs-lookup"><span data-stu-id="f6276-106">cnd dst, src0, src1, src2</span></span> |
|---------------------------|



 

<span data-ttu-id="f6276-107">where</span><span class="sxs-lookup"><span data-stu-id="f6276-107">where</span></span>

-   <span data-ttu-id="f6276-108">DST ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="f6276-108">dst is the destination register.</span></span>
-   <span data-ttu-id="f6276-109">src0 ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="f6276-109">src0 is a source register.</span></span>
-   <span data-ttu-id="f6276-110">Quelle1 ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="f6276-110">src1 is a source register.</span></span>
-   <span data-ttu-id="f6276-111">Quelle2 ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="f6276-111">src2 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6276-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f6276-112">Remarks</span></span>



| <span data-ttu-id="f6276-113">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="f6276-113">Pixel shader versions</span></span> | <span data-ttu-id="f6276-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="f6276-114">1\_1</span></span> | <span data-ttu-id="f6276-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="f6276-115">1\_2</span></span> | <span data-ttu-id="f6276-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="f6276-116">1\_3</span></span> | <span data-ttu-id="f6276-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="f6276-117">1\_4</span></span> | <span data-ttu-id="f6276-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f6276-118">2\_0</span></span> | <span data-ttu-id="f6276-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="f6276-119">2\_x</span></span> | <span data-ttu-id="f6276-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="f6276-120">2\_sw</span></span> | <span data-ttu-id="f6276-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f6276-121">3\_0</span></span> | <span data-ttu-id="f6276-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="f6276-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="f6276-123">CND</span><span class="sxs-lookup"><span data-stu-id="f6276-123">cnd</span></span>                   | <span data-ttu-id="f6276-124">x</span><span class="sxs-lookup"><span data-stu-id="f6276-124">x</span></span>    | <span data-ttu-id="f6276-125">x</span><span class="sxs-lookup"><span data-stu-id="f6276-125">x</span></span>    | <span data-ttu-id="f6276-126">x</span><span class="sxs-lookup"><span data-stu-id="f6276-126">x</span></span>    | <span data-ttu-id="f6276-127">x</span><span class="sxs-lookup"><span data-stu-id="f6276-127">x</span></span>    |      |      |       |      |       |



 

<span data-ttu-id="f6276-128">Für die Versionen 1 \_ 1 bis 1 \_ 3 muss src0 r0. a lauten.</span><span class="sxs-lookup"><span data-stu-id="f6276-128">For versions 1\_1 to 1\_3, src0 must be r0.a.</span></span>


```
// Version 1_1 to 1_3
if (r0.a > 0.5)
  dest = src1
else
  dest = src2
```



<span data-ttu-id="f6276-129">Version 1 \_ 4 vergleicht jeden Kanal separat.</span><span class="sxs-lookup"><span data-stu-id="f6276-129">Version 1\_4 compares each channel separately.</span></span>


```
for each component in src0
{
   if (src0.component > 0.5)
     dest.component = src1.component
   else
     dest.component = src2.component
}
```



<span data-ttu-id="f6276-130">Diese Beispiele zeigen einen Vergleich mit vier Kanälen, der in einem Shader der Version 1 \_ 4 ausgeführt wird, sowie einen Vergleich mit einem einzelnen Kanal, der in einem Shader der Version 1 1 möglich ist \_ .</span><span class="sxs-lookup"><span data-stu-id="f6276-130">These examples show a four-channel comparison done in a version 1\_4 shader, as well as a single-channel comparison possible in a version 1\_1 shader.</span></span>


```
ps_1_4
def c0, -0.5, 0.5, 0, 0.6
def c1,  0,0,0,0
def c2,  1,1,1,1

cnd r1, c0, c1, c2   // r0 contains 1,1,1,0 because
// r1.x = c2.x because c0.x <= 0.5
// r1.y = c2.y because c0.y <= 0.5
// r1.z = c2.z because c0.z <= 0.5
// r1.w = c1.w because c0.w >  0.5
```



<span data-ttu-id="f6276-131">Version 1 \_ 1 bis 1 \_ 3 vergleicht nur mit dem replizierten Alphakanal von r0.</span><span class="sxs-lookup"><span data-stu-id="f6276-131">Version 1\_1 to 1\_3 compares against the replicated alpha channel of r0 only.</span></span>


```
ps_1_1
def c0, -0.5, 0.5, 0, 0.6
def c1,  0,0,0,0
def c2,  1,1,1,1
mov r0, c0
cnd r1, r0.a, c1, c2   // r1 gets assigned 0,0,0,0 because 
                       // r0.a > 0.5, therefore r1.xyzw = c1.xyzw
```



<span data-ttu-id="f6276-132">In diesem Beispiel werden zwei Werte verglichen: A und B. Im Beispiel wird davon ausgegangen, dass ein in V0 geladen und B in v1 geladen wird.</span><span class="sxs-lookup"><span data-stu-id="f6276-132">This example compares two values, A and B. The example assumes A is loaded into v0 and B is loaded into v1.</span></span> <span data-ttu-id="f6276-133">A und B müssen im Bereich von-1 bis + 1 liegen, und da die Farbregister (VN) zwischen 0 und 1 liegen, wird die Einschränkung in diesem Beispiel erfüllt.</span><span class="sxs-lookup"><span data-stu-id="f6276-133">Both A and B must be in the range of -1 to +1, and since the color registers (vₙ) are defined to be between 0 and 1, the restriction happens to be satisfied in this example.</span></span>


```
ps_1_1                // Version instruction
sub r0, v0, v1_bias   // r0 = A - (B - 0.5)
cnd r0, r0.a, c0, c1  // r0 = ( A > B ? c0 : c1 )

// r0 = c0 if A > B, otherwise, r0 = c1
```



## <a name="related-topics"></a><span data-ttu-id="f6276-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f6276-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6276-135">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="f6276-135">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




