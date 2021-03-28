---
title: callvs
description: Führt einen Funktions Aufrufder Anweisung aus, die mit der angegebenen Bezeichnung gekennzeichnet ist. | callvs
ms.assetid: 3c1ec529-1ee4-40d9-8ce5-f8e7a61fde9c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c797e7ef6745f5710752fe059d2a2ff1f94a8aa3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103961528"
---
# <a name="call---vs"></a><span data-ttu-id="eaa20-104">callvs</span><span class="sxs-lookup"><span data-stu-id="eaa20-104">call - vs</span></span>

<span data-ttu-id="eaa20-105">Führt einen Funktions Aufrufder Anweisung aus, die mit der angegebenen Bezeichnung gekennzeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="eaa20-105">Performs a function call to the instruction marked with the provided label.</span></span>

## <a name="syntax"></a><span data-ttu-id="eaa20-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="eaa20-106">Syntax</span></span>



| <span data-ttu-id="eaa20-107">l anrufen\#</span><span class="sxs-lookup"><span data-stu-id="eaa20-107">call l\#</span></span> |
|----------|



 

<span data-ttu-id="eaa20-108">Where l \# ist eine [Bezeichnung-vs](label---vs.md) , die den Anfang der aufzurufenden Unterroutine kennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="eaa20-108">where l\# is a [label - vs](label---vs.md) marking the beginning of the subroutine to be called.</span></span>

## <a name="remarks"></a><span data-ttu-id="eaa20-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eaa20-109">Remarks</span></span>



| <span data-ttu-id="eaa20-110">Vertex-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="eaa20-110">Vertex shader versions</span></span> | <span data-ttu-id="eaa20-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="eaa20-111">1\_1</span></span> | <span data-ttu-id="eaa20-112">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="eaa20-112">2\_0</span></span> | <span data-ttu-id="eaa20-113">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="eaa20-113">2\_x</span></span> | <span data-ttu-id="eaa20-114">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="eaa20-114">2\_sw</span></span> | <span data-ttu-id="eaa20-115">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="eaa20-115">3\_0</span></span> | <span data-ttu-id="eaa20-116">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="eaa20-116">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="eaa20-117">Aufruf</span><span class="sxs-lookup"><span data-stu-id="eaa20-117">call</span></span>                   |      | <span data-ttu-id="eaa20-118">x</span><span class="sxs-lookup"><span data-stu-id="eaa20-118">x</span></span>    | <span data-ttu-id="eaa20-119">x</span><span class="sxs-lookup"><span data-stu-id="eaa20-119">x</span></span>    | <span data-ttu-id="eaa20-120">x</span><span class="sxs-lookup"><span data-stu-id="eaa20-120">x</span></span>     | <span data-ttu-id="eaa20-121">x</span><span class="sxs-lookup"><span data-stu-id="eaa20-121">x</span></span>    | <span data-ttu-id="eaa20-122">x</span><span class="sxs-lookup"><span data-stu-id="eaa20-122">x</span></span>     |



 

<span data-ttu-id="eaa20-123">Diese Anweisung führt Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="eaa20-123">This instruction does the following:</span></span>

1.  <span data-ttu-id="eaa20-124">Die pushadresse der nächsten Anweisung in den Rückgabe Adress Stapel.</span><span class="sxs-lookup"><span data-stu-id="eaa20-124">Push address of the next instruction to the return address stack.</span></span>
2.  <span data-ttu-id="eaa20-125">Setzen Sie die Ausführung mit der von der Bezeichnung markierten Anweisung fort.</span><span class="sxs-lookup"><span data-stu-id="eaa20-125">Continue execution from the instruction marked by the label.</span></span>

<span data-ttu-id="eaa20-126">In Vertex-Shader 2 \_ 0 sind Verschachtelungs Aufrufe nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="eaa20-126">In vertex shader 2\_0, nesting calls are not allowed.</span></span>

<span data-ttu-id="eaa20-127">In Vertex Shader 2 \_ x wird die Schachtelungs Tiefe durch das staticflowcontroltiefe-Element der [**D3DVSHADERCAPS2 \_ 0**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dvshadercaps2_0) -Struktur eingeschränkt.</span><span class="sxs-lookup"><span data-stu-id="eaa20-127">In vertex shader 2\_x, the nesting depth is limited by the StaticFlowControlDepth element of the [**D3DVSHADERCAPS2\_0**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dvshadercaps2_0) structure.</span></span> <span data-ttu-id="eaa20-128">Weitere Informationen finden Sie unter [**GetDeviceCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-getdevicecaps).</span><span class="sxs-lookup"><span data-stu-id="eaa20-128">For more information, see [**GetDeviceCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-getdevicecaps).</span></span>

<span data-ttu-id="eaa20-129">In Vertex-Shader 3 0 sind vier Ebenen der Schachtelungs Schachtelung \_ zulässig.</span><span class="sxs-lookup"><span data-stu-id="eaa20-129">In vertex shader 3\_0, four levels of call nesting are allowed.</span></span>

<span data-ttu-id="eaa20-130">Nur vorwärts Aufrufe sind zulässig.</span><span class="sxs-lookup"><span data-stu-id="eaa20-130">Only forward calls are allowed.</span></span> <span data-ttu-id="eaa20-131">Dies bedeutet, dass der Speicherort der Bezeichnung innerhalb des Vertex-Shaders nach der Anweisung zum Aufrufen der Anweisung liegen muss.</span><span class="sxs-lookup"><span data-stu-id="eaa20-131">This means that the location of the label inside the vertex shader should be after the call instruction referencing it.</span></span>

<span data-ttu-id="eaa20-132">Wenn eine Aufruf Anweisung innerhalb einer [Schleife](loop---vs.md)aufgerufen wird... [ENDLOOP](endloop---vs.md) -Block: auf den Wert des [Schleifen zählungs Leistungs Zählers](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (Al) kann innerhalb der Unterroutine zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="eaa20-132">If a call instruction is invoked inside [loop](loop---vs.md)...[endloop](endloop---vs.md) block, the value of the [Loop Counter Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (aL) is accessible inside the subroutine.</span></span>

<span data-ttu-id="eaa20-133">Wenn eine Unterroutine auf das Schleifen- [Counter-Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (Al) verweist, das sich außerhalb der Unterroutine befindet, sollte jede Instanz des Aufrufes dieser Unterroutine von einer [Schleife](loop---vs.md)umgeben werden... [ENDLOOP](endloop---vs.md) -Block.</span><span class="sxs-lookup"><span data-stu-id="eaa20-133">If a subroutine is referencing the [Loop Counter Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (aL) located outside of the subroutine, every instance of the call to this subroutine should be surrounded by a [loop](loop---vs.md)...[endloop](endloop---vs.md) block.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eaa20-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="eaa20-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eaa20-135">Vertex-shaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="eaa20-135">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 
