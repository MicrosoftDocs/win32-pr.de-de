---
title: callps
description: Führt einen Funktions Aufrufder Anweisung aus, die mit der angegebenen Bezeichnung gekennzeichnet ist. | callps
ms.assetid: d5f5e5a1-f205-477d-a11b-ff9eeeec6c95
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 27be29c478afdf92c29fefd16a82319e0899d2ec
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995494"
---
# <a name="call---ps"></a><span data-ttu-id="58b61-104">callps</span><span class="sxs-lookup"><span data-stu-id="58b61-104">call - ps</span></span>

<span data-ttu-id="58b61-105">Führt einen Funktions Aufrufder Anweisung aus, die mit der angegebenen Bezeichnung gekennzeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="58b61-105">Performs a function call to the instruction marked with the provided label.</span></span>

## <a name="syntax"></a><span data-ttu-id="58b61-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="58b61-106">Syntax</span></span>



| <span data-ttu-id="58b61-107">l anrufen\#</span><span class="sxs-lookup"><span data-stu-id="58b61-107">call l\#</span></span> |
|----------|



 

<span data-ttu-id="58b61-108">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="58b61-108">Where:</span></span>

-   <span data-ttu-id="58b61-109">l \# ist eine [Bezeichnung-PS](label---ps.md) , die den Anfang der aufzurufenden Unterroutine markiert.</span><span class="sxs-lookup"><span data-stu-id="58b61-109">l\# is a [label - ps](label---ps.md) marking the beginning of the subroutine to be called.</span></span>

## <a name="remarks"></a><span data-ttu-id="58b61-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="58b61-110">Remarks</span></span>



| <span data-ttu-id="58b61-111">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="58b61-111">Pixel shader versions</span></span> | <span data-ttu-id="58b61-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="58b61-112">1\_1</span></span> | <span data-ttu-id="58b61-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="58b61-113">1\_2</span></span> | <span data-ttu-id="58b61-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="58b61-114">1\_3</span></span> | <span data-ttu-id="58b61-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="58b61-115">1\_4</span></span> | <span data-ttu-id="58b61-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="58b61-116">2\_0</span></span> | <span data-ttu-id="58b61-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="58b61-117">2\_x</span></span> | <span data-ttu-id="58b61-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="58b61-118">2\_sw</span></span> | <span data-ttu-id="58b61-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="58b61-119">3\_0</span></span> | <span data-ttu-id="58b61-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="58b61-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="58b61-121">Aufruf</span><span class="sxs-lookup"><span data-stu-id="58b61-121">call</span></span>                  |      |      |      |      |      | <span data-ttu-id="58b61-122">x</span><span class="sxs-lookup"><span data-stu-id="58b61-122">x</span></span>    | <span data-ttu-id="58b61-123">x</span><span class="sxs-lookup"><span data-stu-id="58b61-123">x</span></span>     | <span data-ttu-id="58b61-124">x</span><span class="sxs-lookup"><span data-stu-id="58b61-124">x</span></span>    | <span data-ttu-id="58b61-125">x</span><span class="sxs-lookup"><span data-stu-id="58b61-125">x</span></span>     |



 

<span data-ttu-id="58b61-126">Diese Anweisung führt Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="58b61-126">This instruction does the following:</span></span>

1.  <span data-ttu-id="58b61-127">Die pushadresse der nächsten Anweisung in den Rückgabe Adress Stapel.</span><span class="sxs-lookup"><span data-stu-id="58b61-127">Push address of the next instruction to the return address stack.</span></span>
2.  <span data-ttu-id="58b61-128">Setzen Sie die Ausführung mit der von der Bezeichnung markierten Anweisung fort.</span><span class="sxs-lookup"><span data-stu-id="58b61-128">Continue execution from the instruction marked by the label.</span></span>

## <a name="related-topics"></a><span data-ttu-id="58b61-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="58b61-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58b61-130">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="58b61-130">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




