---
title: ENDLOOP-PS
description: Ende einer Schleife... ENDLOOP-Block.
ms.assetid: 8d05d0b3-88d2-44e3-a22d-54d8a8ceb5f4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ee1a7eb10146e40a39c05bcecb99d3a7667dee2c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "103948313"
---
# <a name="endloop---ps"></a><span data-ttu-id="6d8e8-103">ENDLOOP-PS</span><span class="sxs-lookup"><span data-stu-id="6d8e8-103">endloop - ps</span></span>

<span data-ttu-id="6d8e8-104">Ende einer [Schleife](loop---ps.md)... ENDLOOP-Block.</span><span class="sxs-lookup"><span data-stu-id="6d8e8-104">End of a [loop - ps](loop---ps.md)...endloop block.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d8e8-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6d8e8-105">Remarks</span></span>



| <span data-ttu-id="6d8e8-106">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="6d8e8-106">Pixel shader versions</span></span> | <span data-ttu-id="6d8e8-107">1\_1</span><span class="sxs-lookup"><span data-stu-id="6d8e8-107">1\_1</span></span> | <span data-ttu-id="6d8e8-108">1\_2</span><span class="sxs-lookup"><span data-stu-id="6d8e8-108">1\_2</span></span> | <span data-ttu-id="6d8e8-109">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="6d8e8-109">1\_3</span></span> | <span data-ttu-id="6d8e8-110">1\_4</span><span class="sxs-lookup"><span data-stu-id="6d8e8-110">1\_4</span></span> | <span data-ttu-id="6d8e8-111">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6d8e8-111">2\_0</span></span> | <span data-ttu-id="6d8e8-112">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="6d8e8-112">2\_x</span></span> | <span data-ttu-id="6d8e8-113">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="6d8e8-113">2\_sw</span></span> | <span data-ttu-id="6d8e8-114">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6d8e8-114">3\_0</span></span> | <span data-ttu-id="6d8e8-115">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="6d8e8-115">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="6d8e8-116">ENDLOOP</span><span class="sxs-lookup"><span data-stu-id="6d8e8-116">endloop</span></span>               |      |      |      |      |      |      |       | <span data-ttu-id="6d8e8-117">x</span><span class="sxs-lookup"><span data-stu-id="6d8e8-117">x</span></span>    | <span data-ttu-id="6d8e8-118">x</span><span class="sxs-lookup"><span data-stu-id="6d8e8-118">x</span></span>     |



 

<span data-ttu-id="6d8e8-119">ENDLOOP muss der letzten Anweisung eines [Schleifen-PS-](loop---ps.md) Blocks folgen.</span><span class="sxs-lookup"><span data-stu-id="6d8e8-119">endloop must follow the last instruction of a [loop - ps](loop---ps.md) block.</span></span>

## <a name="example"></a><span data-ttu-id="6d8e8-120">Beispiel</span><span class="sxs-lookup"><span data-stu-id="6d8e8-120">Example</span></span>


```
loop aL, i3
    add r1, r0, c2[ aL ]
endloop
```



## <a name="related-topics"></a><span data-ttu-id="6d8e8-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6d8e8-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d8e8-122">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="6d8e8-122">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




