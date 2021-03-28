---
title: Bezeichnung (VS)
description: Markieren Sie die nächste Anweisung mit einem Bezeichnungs Index. | Bezeichnung (VS)
ms.assetid: e1aee8bc-4655-4bd5-8012-bd7a2d46e712
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6e2b72fe21301aa66d8428dc3696ceb3f12e6214
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995722"
---
# <a name="label---vs"></a><span data-ttu-id="222f9-104">Bezeichnung (VS)</span><span class="sxs-lookup"><span data-stu-id="222f9-104">label - vs</span></span>

<span data-ttu-id="222f9-105">Markieren Sie die nächste Anweisung mit einem Bezeichnungs Index.</span><span class="sxs-lookup"><span data-stu-id="222f9-105">Mark the next instruction as having a label index.</span></span>

## <a name="syntax"></a><span data-ttu-id="222f9-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="222f9-106">Syntax</span></span>



| <span data-ttu-id="222f9-107">Bezeichnung l\#</span><span class="sxs-lookup"><span data-stu-id="222f9-107">label l\#</span></span> |
|-----------|



 

<span data-ttu-id="222f9-108">Gibt an, wo die Bezeichnungs \# Nummer identifiziert.</span><span class="sxs-lookup"><span data-stu-id="222f9-108">where \# identifies the label number.</span></span>

<span data-ttu-id="222f9-109">Für vs \_ 2 \_ 0 und vs \_ 2 \_ x muss die Bezeichnungs Nummer zwischen 0 und 15 liegen.</span><span class="sxs-lookup"><span data-stu-id="222f9-109">For vs\_2\_0, and vs\_2\_x, the label number must be between between 0 and 15.</span></span>

<span data-ttu-id="222f9-110">Für vs \_ 2 \_ SW, vs \_ 3 \_ 0 und vs \_ 3 \_ SW, muss die Nummer der Bezeichnung zwischen 0 und 2047 liegen.</span><span class="sxs-lookup"><span data-stu-id="222f9-110">For vs\_2\_sw, vs\_3\_0 and vs\_3\_sw, the label number must be between between 0 and 2047.</span></span>

## <a name="remarks"></a><span data-ttu-id="222f9-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="222f9-111">Remarks</span></span>



| <span data-ttu-id="222f9-112">Vertex-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="222f9-112">Vertex shader versions</span></span> | <span data-ttu-id="222f9-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="222f9-113">1\_1</span></span> | <span data-ttu-id="222f9-114">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="222f9-114">2\_0</span></span> | <span data-ttu-id="222f9-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="222f9-115">2\_x</span></span> | <span data-ttu-id="222f9-116">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="222f9-116">2\_sw</span></span> | <span data-ttu-id="222f9-117">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="222f9-117">3\_0</span></span> | <span data-ttu-id="222f9-118">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="222f9-118">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="222f9-119">label</span><span class="sxs-lookup"><span data-stu-id="222f9-119">label</span></span>                  |      | <span data-ttu-id="222f9-120">x</span><span class="sxs-lookup"><span data-stu-id="222f9-120">x</span></span>    | <span data-ttu-id="222f9-121">x</span><span class="sxs-lookup"><span data-stu-id="222f9-121">x</span></span>    | <span data-ttu-id="222f9-122">x</span><span class="sxs-lookup"><span data-stu-id="222f9-122">x</span></span>     | <span data-ttu-id="222f9-123">x</span><span class="sxs-lookup"><span data-stu-id="222f9-123">x</span></span>    | <span data-ttu-id="222f9-124">x</span><span class="sxs-lookup"><span data-stu-id="222f9-124">x</span></span>     |



 

<span data-ttu-id="222f9-125">Diese Anweisung definiert eine Bezeichnung, die sich in der nächsten shaderanweisung befindet.</span><span class="sxs-lookup"><span data-stu-id="222f9-125">This instruction defines a label located at the next shader instruction.</span></span> <span data-ttu-id="222f9-126">Die Bezeichnungs Anweisung kann nur direkt nach einer [ret](ret---vs.md) -Anweisung vorhanden sein (die das Ende der vorherigen Unterroutine oder des Hauptprogramms definiert).</span><span class="sxs-lookup"><span data-stu-id="222f9-126">The label instruction can only be present directly after a [ret](ret---vs.md) instruction (which defines the end of the previous subroutine or main program).</span></span>

## <a name="related-topics"></a><span data-ttu-id="222f9-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="222f9-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="222f9-128">Vertex-shaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="222f9-128">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




