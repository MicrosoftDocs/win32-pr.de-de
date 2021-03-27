---
title: MOV (VS)
description: Verschieben von Gleit Komma Daten zwischen Registern.
ms.assetid: bf013ab2-593e-4201-ba75-faebd0c9f97a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 00f207261ad8ba6ac83360c40bc6008530292816
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "103719452"
---
# <a name="mov---vs"></a><span data-ttu-id="17e3c-103">MOV (VS)</span><span class="sxs-lookup"><span data-stu-id="17e3c-103">mov - vs</span></span>

<span data-ttu-id="17e3c-104">Verschieben von Gleit Komma Daten zwischen Registern.</span><span class="sxs-lookup"><span data-stu-id="17e3c-104">Move floating-point data between registers.</span></span>

## <a name="syntax"></a><span data-ttu-id="17e3c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="17e3c-105">Syntax</span></span>



| <span data-ttu-id="17e3c-106">MOV DST, src</span><span class="sxs-lookup"><span data-stu-id="17e3c-106">mov dst, src</span></span> |
|--------------|



 

<span data-ttu-id="17e3c-107">where</span><span class="sxs-lookup"><span data-stu-id="17e3c-107">where</span></span>

-   <span data-ttu-id="17e3c-108">DST ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="17e3c-108">dst is the destination register.</span></span>
-   <span data-ttu-id="17e3c-109">src ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="17e3c-109">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="17e3c-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="17e3c-110">Remarks</span></span>



| <span data-ttu-id="17e3c-111">Vertex-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="17e3c-111">Vertex shader versions</span></span> | <span data-ttu-id="17e3c-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="17e3c-112">1\_1</span></span> | <span data-ttu-id="17e3c-113">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="17e3c-113">2\_0</span></span> | <span data-ttu-id="17e3c-114">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="17e3c-114">2\_x</span></span> | <span data-ttu-id="17e3c-115">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="17e3c-115">2\_sw</span></span> | <span data-ttu-id="17e3c-116">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="17e3c-116">3\_0</span></span> | <span data-ttu-id="17e3c-117">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="17e3c-117">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="17e3c-118">MOV</span><span class="sxs-lookup"><span data-stu-id="17e3c-118">mov</span></span>                    | <span data-ttu-id="17e3c-119">x</span><span class="sxs-lookup"><span data-stu-id="17e3c-119">x</span></span>    | <span data-ttu-id="17e3c-120">x</span><span class="sxs-lookup"><span data-stu-id="17e3c-120">x</span></span>    | <span data-ttu-id="17e3c-121">x</span><span class="sxs-lookup"><span data-stu-id="17e3c-121">x</span></span>    | <span data-ttu-id="17e3c-122">x</span><span class="sxs-lookup"><span data-stu-id="17e3c-122">x</span></span>     | <span data-ttu-id="17e3c-123">x</span><span class="sxs-lookup"><span data-stu-id="17e3c-123">x</span></span>    | <span data-ttu-id="17e3c-124">x</span><span class="sxs-lookup"><span data-stu-id="17e3c-124">x</span></span>     |



 

<span data-ttu-id="17e3c-125">Kann für Gleit Komma Daten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="17e3c-125">Can be used for floating point data.</span></span> <span data-ttu-id="17e3c-126">Für Version vs \_ 1 \_ 1 kann Sie auch verwendet werden, um das Adressregister zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="17e3c-126">For version vs\_1\_1, it can also be used to write the address register.</span></span> <span data-ttu-id="17e3c-127">Wenn Sie zum Aktualisieren von Adress Registern verwendet werden, werden die Werte von Gleit Komma Zahlen mithilfe der Rundung zum nächsten konvertiert.</span><span class="sxs-lookup"><span data-stu-id="17e3c-127">When used to update address registers, the values are converted from floating point using rounding to nearest.</span></span>

<span data-ttu-id="17e3c-128">Das folgende Code Fragment zeigt die ausgeführten Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="17e3c-128">The following code fragment shows the operations performed.</span></span>


```
if(dest is an integer register)
{
    int intSrc = RoundToNearest(src.w);
    dest = intSrc;
}
else
{
    dest = src;
}
```



## <a name="related-topics"></a><span data-ttu-id="17e3c-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="17e3c-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="17e3c-130">Vertex-shaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="17e3c-130">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




