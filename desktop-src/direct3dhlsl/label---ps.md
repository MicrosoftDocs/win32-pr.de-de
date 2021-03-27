---
title: Bezeichnung-PS
description: Markieren Sie die nächste Anweisung mit einem Bezeichnungs Index. | Bezeichnung-PS
ms.assetid: 21afa062-c536-4891-ba69-ca5284b0539c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f3fb266b649642c82293e8310b6302c6763ddc27
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995575"
---
# <a name="label---ps"></a><span data-ttu-id="b4ccb-104">Bezeichnung-PS</span><span class="sxs-lookup"><span data-stu-id="b4ccb-104">label - ps</span></span>

<span data-ttu-id="b4ccb-105">Markieren Sie die nächste Anweisung mit einem Bezeichnungs Index.</span><span class="sxs-lookup"><span data-stu-id="b4ccb-105">Mark the next instruction as having a label index.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4ccb-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="b4ccb-106">Syntax</span></span>



| <span data-ttu-id="b4ccb-107">Bezeichnung l\#</span><span class="sxs-lookup"><span data-stu-id="b4ccb-107">label l\#</span></span> |
|-----------|



 

<span data-ttu-id="b4ccb-108">Gibt an, wo die Bezeichnungs \# Nummer identifiziert.</span><span class="sxs-lookup"><span data-stu-id="b4ccb-108">where \# identifies the label number.</span></span>

<span data-ttu-id="b4ccb-109">Für PS \_ 2 \_ x muss die Bezeichnungs Nummer zwischen 0 und 15 liegen.</span><span class="sxs-lookup"><span data-stu-id="b4ccb-109">For ps\_2\_x, the label number must be between between 0 and 15.</span></span>

<span data-ttu-id="b4ccb-110">Für PS \_ 2 \_ SW, PS \_ 3 \_ 0 und PS \_ 3 \_ SW muss die Bezeichnungs Nummer zwischen 0 und 2047 liegen.</span><span class="sxs-lookup"><span data-stu-id="b4ccb-110">For ps\_2\_sw, ps\_3\_0, and ps\_3\_sw, the label number must be between between 0 and 2047.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4ccb-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b4ccb-111">Remarks</span></span>



| <span data-ttu-id="b4ccb-112">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="b4ccb-112">Pixel shader versions</span></span> | <span data-ttu-id="b4ccb-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="b4ccb-113">1\_1</span></span> | <span data-ttu-id="b4ccb-114">1\_2</span><span class="sxs-lookup"><span data-stu-id="b4ccb-114">1\_2</span></span> | <span data-ttu-id="b4ccb-115">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="b4ccb-115">1\_3</span></span> | <span data-ttu-id="b4ccb-116">1\_4</span><span class="sxs-lookup"><span data-stu-id="b4ccb-116">1\_4</span></span> | <span data-ttu-id="b4ccb-117">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b4ccb-117">2\_0</span></span> | <span data-ttu-id="b4ccb-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="b4ccb-118">2\_x</span></span> | <span data-ttu-id="b4ccb-119">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b4ccb-119">2\_sw</span></span> | <span data-ttu-id="b4ccb-120">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b4ccb-120">3\_0</span></span> | <span data-ttu-id="b4ccb-121">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b4ccb-121">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="b4ccb-122">label</span><span class="sxs-lookup"><span data-stu-id="b4ccb-122">label</span></span>                 |      |      |      |      |      | <span data-ttu-id="b4ccb-123">x</span><span class="sxs-lookup"><span data-stu-id="b4ccb-123">x</span></span>    | <span data-ttu-id="b4ccb-124">x</span><span class="sxs-lookup"><span data-stu-id="b4ccb-124">x</span></span>     | <span data-ttu-id="b4ccb-125">x</span><span class="sxs-lookup"><span data-stu-id="b4ccb-125">x</span></span>    | <span data-ttu-id="b4ccb-126">x</span><span class="sxs-lookup"><span data-stu-id="b4ccb-126">x</span></span>     |



 

<span data-ttu-id="b4ccb-127">Diese Anweisung definiert eine Bezeichnung, die sich in der nächsten shaderanweisung befindet.</span><span class="sxs-lookup"><span data-stu-id="b4ccb-127">This instruction defines a label located at the next shader instruction.</span></span> <span data-ttu-id="b4ccb-128">Die Bezeichnungs Anweisung kann nur direkt nach einer [ret](ret---ps.md) -Anweisung vorhanden sein (die das Ende der vorherigen Unterroutine oder des Hauptprogramms definiert).</span><span class="sxs-lookup"><span data-stu-id="b4ccb-128">The label instruction can only be present directly after a [ret](ret---ps.md) instruction (which defines the end of the previous subroutine or main program).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b4ccb-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b4ccb-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4ccb-130">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="b4ccb-130">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




