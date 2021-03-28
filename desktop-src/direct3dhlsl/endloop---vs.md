---
title: ENDLOOP-vs
description: Ende einer Schleife... ENDLOOP-Block.
ms.assetid: fd7df120-a927-4a66-b152-6ce5247446e4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8a9aec4d1b2c5237a87fae2c0beab4e8d995db97
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389486"
---
# <a name="endloop---vs"></a><span data-ttu-id="0e334-103">ENDLOOP-vs</span><span class="sxs-lookup"><span data-stu-id="0e334-103">endloop - vs</span></span>

<span data-ttu-id="0e334-104">Ende einer [Schleife](loop---vs.md)... ENDLOOP-Block.</span><span class="sxs-lookup"><span data-stu-id="0e334-104">End of a [loop](loop---vs.md)...endloop block.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e334-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0e334-105">Syntax</span></span>



| <span data-ttu-id="0e334-106">ENDLOOP</span><span class="sxs-lookup"><span data-stu-id="0e334-106">endloop</span></span> |
|---------|



 

## <a name="remarks"></a><span data-ttu-id="0e334-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0e334-107">Remarks</span></span>



| <span data-ttu-id="0e334-108">Vertex-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="0e334-108">Vertex shader versions</span></span> | <span data-ttu-id="0e334-109">1\_1</span><span class="sxs-lookup"><span data-stu-id="0e334-109">1\_1</span></span> | <span data-ttu-id="0e334-110">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0e334-110">2\_0</span></span> | <span data-ttu-id="0e334-111">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="0e334-111">2\_x</span></span> | <span data-ttu-id="0e334-112">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="0e334-112">2\_sw</span></span> | <span data-ttu-id="0e334-113">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0e334-113">3\_0</span></span> | <span data-ttu-id="0e334-114">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="0e334-114">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="0e334-115">ENDLOOP</span><span class="sxs-lookup"><span data-stu-id="0e334-115">endloop</span></span>                |      | <span data-ttu-id="0e334-116">x</span><span class="sxs-lookup"><span data-stu-id="0e334-116">x</span></span>    | <span data-ttu-id="0e334-117">x</span><span class="sxs-lookup"><span data-stu-id="0e334-117">x</span></span>    | <span data-ttu-id="0e334-118">x</span><span class="sxs-lookup"><span data-stu-id="0e334-118">x</span></span>     | <span data-ttu-id="0e334-119">x</span><span class="sxs-lookup"><span data-stu-id="0e334-119">x</span></span>    | <span data-ttu-id="0e334-120">x</span><span class="sxs-lookup"><span data-stu-id="0e334-120">x</span></span>     |



 

<span data-ttu-id="0e334-121">Diese Anweisung funktioniert wie hier gezeigt.</span><span class="sxs-lookup"><span data-stu-id="0e334-121">This instruction works as shown here.</span></span>


```
LoopCounter += LoopStep;
LoopInterationCount = LoopIterationCount - 1;
if (LoopIterationCount > 0)
    Continue execution at the StartLoopOffset
```



<span data-ttu-id="0e334-122">ENDLOOP muss der letzten Anweisung eines [Schleifen-vs-](loop---vs.md) Blocks folgen.</span><span class="sxs-lookup"><span data-stu-id="0e334-122">endloop must follow the last instruction of a [loop - vs](loop---vs.md) block.</span></span>

## <a name="example"></a><span data-ttu-id="0e334-123">Beispiel</span><span class="sxs-lookup"><span data-stu-id="0e334-123">Example</span></span>


```
loop aL, i3
    add r1, r0, c2[ aL ]
endloop
```



## <a name="related-topics"></a><span data-ttu-id="0e334-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0e334-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e334-125">Vertex-shaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="0e334-125">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




