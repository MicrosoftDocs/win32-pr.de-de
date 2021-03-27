---
title: Ausgabe Farb Register
description: Die Pixel-Shader-Farbausgabe Register (OC \) sind schreibgeschützt, die Ergebnisse an mehrere Renderziele ausgeben.
ms.assetid: 88e69189-3956-47de-a336-921f1e62c025
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 316160e39ce172d56e4ecac17dfbd1d53077005b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390812"
---
# <a name="output-color-register"></a><span data-ttu-id="dd203-103">Ausgabe Farb Register</span><span class="sxs-lookup"><span data-stu-id="dd203-103">Output Color Register</span></span>

<span data-ttu-id="dd203-104">Die Pixel-Shader-Farbausgabe Register (OC #) sind schreibgeschützte Registrierungen, die Ergebnisse an mehrere Renderziele ausgeben.</span><span class="sxs-lookup"><span data-stu-id="dd203-104">The pixel shader color output registers (oC#) are write-only registers that output results to multiple render targets.</span></span>

<span data-ttu-id="dd203-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="dd203-105">Syntax</span></span>



| <span data-ttu-id="dd203-106">d #</span><span class="sxs-lookup"><span data-stu-id="dd203-106">oC#</span></span> |
|------|



 

<span data-ttu-id="dd203-107">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="dd203-107">Where:</span></span>



| <span data-ttu-id="dd203-108">Name</span><span class="sxs-lookup"><span data-stu-id="dd203-108">Name</span></span> | <span data-ttu-id="dd203-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dd203-109">Description</span></span>       |
|------|-------------------|
| <span data-ttu-id="dd203-110">oC0</span><span class="sxs-lookup"><span data-stu-id="dd203-110">oC0</span></span>  | <span data-ttu-id="dd203-111">Renderziel \# 0</span><span class="sxs-lookup"><span data-stu-id="dd203-111">render target \#0</span></span> |
| <span data-ttu-id="dd203-112">oC1</span><span class="sxs-lookup"><span data-stu-id="dd203-112">oC1</span></span>  | <span data-ttu-id="dd203-113">Renderziel \# 1</span><span class="sxs-lookup"><span data-stu-id="dd203-113">render target \#1</span></span> |
| <span data-ttu-id="dd203-114">oC2</span><span class="sxs-lookup"><span data-stu-id="dd203-114">oC2</span></span>  | <span data-ttu-id="dd203-115">Renderziel \# 2</span><span class="sxs-lookup"><span data-stu-id="dd203-115">render target \#2</span></span> |
| <span data-ttu-id="dd203-116">oC3</span><span class="sxs-lookup"><span data-stu-id="dd203-116">oC3</span></span>  | <span data-ttu-id="dd203-117">Renderziel \# 3</span><span class="sxs-lookup"><span data-stu-id="dd203-117">render target \#3</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="dd203-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dd203-118">Remarks</span></span>

-   <span data-ttu-id="dd203-119">Wenn OCN geschrieben ist, aber kein entsprechendes Renderziel vorhanden ist, wird dieser Schreibvorgang in OCN ignoriert.</span><span class="sxs-lookup"><span data-stu-id="dd203-119">If oCn is written but there is no corresponding render target, then this write to oCn is ignored.</span></span>
-   <span data-ttu-id="dd203-120">Die renderzustände D3DRS \_ colorschreiteenable, D3DRS \_ COLORWRITEENABLE1, D3DRS \_ COLORWRITEENABLE2 und D3DRS \_ COLORWRITEENABLE3 bestimmen, welche Komponenten von OCN letztendlich in das Renderziel geschrieben werden (sofern zutreffend).</span><span class="sxs-lookup"><span data-stu-id="dd203-120">The render states D3DRS\_COLORWRITEENABLE, D3DRS\_COLORWRITEENABLE1, D3DRS\_COLORWRITEENABLE2 and D3DRS\_COLORWRITEENABLE3 determine which components of oCn ultimately get written to the render target (after blend, if applicable).</span></span> <span data-ttu-id="dd203-121">Wenn der Shader einige, jedoch nicht alle Komponenten schreibt, die von den D3DRS \_ ColorWriteEnable- \* renderzuständen für ein bestimmtes OCN-Register definiert werden, erzeugen die nicht geschriebenen Kanäle nicht definierte Werte im entsprechenden Renderziel.</span><span class="sxs-lookup"><span data-stu-id="dd203-121">If the shader writes some but not all of the components defined by the D3DRS\_COLORWRITEENABLE\* render states for a given oCn register, then the unwritten channels produce undefined values in the corresponding render target.</span></span> <span data-ttu-id="dd203-122">Wenn keine der Komponenten eines OCN geschrieben wird, darf das entsprechende Renderziel überhaupt nicht aktualisiert werden (wie oben beschrieben), sodass die \_ renderzustände von D3DRS colorschreiteenable \* nicht zutreffen.</span><span class="sxs-lookup"><span data-stu-id="dd203-122">If none of the components of an oCn are written, the corresponding render target must not be updated at all (as stated above), so the D3DRS\_COLORWRITEENABLE\* render states do not apply.</span></span>

### <a name="shader-model-2-restrictions"></a><span data-ttu-id="dd203-123">Einschränkungen für Shader Model 2</span><span class="sxs-lookup"><span data-stu-id="dd203-123">Shader Model 2 Restrictions</span></span>

-   <span data-ttu-id="dd203-124">OCN kann nur mit der [MOV-PS-](mov---ps.md) Anweisung geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="dd203-124">oCn can only be written with the [mov - ps](mov---ps.md) instruction.</span></span>
-   <span data-ttu-id="dd203-125">oC0 muss immer im Shader geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="dd203-125">oC0 must be always written in the shader.</span></span>
-   <span data-ttu-id="dd203-126">Beim Schreiben in einen beliebigen OCN ist kein quellswidwert (mit Ausnahme von. xyzw = default Swizzle) oder der quellmodifizierer zulässig.</span><span class="sxs-lookup"><span data-stu-id="dd203-126">No source swizzle (except .xyzw = default swizzle) or source modifier is allowed when writing to any oCn.</span></span>
-   <span data-ttu-id="dd203-127">Beim Schreiben in einen beliebigen OCN ist keine Ziel Schreib Maske (mit Ausnahme von. xyzw = default Mask) oder ein Anweisungs Modifizierer zulässig.</span><span class="sxs-lookup"><span data-stu-id="dd203-127">No destination write mask (except .xyzw = default mask) or instruction modifier is allowed when writing to any oCn.</span></span>
-   <span data-ttu-id="dd203-128">Wenn OCN geschrieben ist, muss auch oC0-OCN-1 geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="dd203-128">If oCn is written, then oC0 - oCn-1 must also be written.</span></span> <span data-ttu-id="dd203-129">Wenn Sie z. b. in oC2 schreiben möchten, müssen Sie auch in oC0 und oC1 schreiben.</span><span class="sxs-lookup"><span data-stu-id="dd203-129">For example, to write to oC2, you must also write to oC0 and oC1.</span></span>
-   <span data-ttu-id="dd203-130">Höchstens ein Schreibvorgang in einen oC # pro Shader ist zulässig.</span><span class="sxs-lookup"><span data-stu-id="dd203-130">At most one write to any oC# per shader is allowed.</span></span>
-   <span data-ttu-id="dd203-131">Für PS \_ 2 \_ x und PS \_ 3 \_ 0 können Sie nicht in oC #-und od- \# Register in der dynamischen Fluss Steuerung oder im Prädikat schreiben (Schreibvorgänge in OC # innerhalb der statischen Fluss Steuerung ist in Ordnung).</span><span class="sxs-lookup"><span data-stu-id="dd203-131">For ps\_2\_x and ps\_3\_0, you cannot write to oC# and oD\# registers within dynamic flow control or predication (writes to oC# inside static flow control is fine).</span></span>

### <a name="shader-model-3-restrictions"></a><span data-ttu-id="dd203-132">Shader Model 3-Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="dd203-132">Shader Model 3 Restrictions</span></span>

-   <span data-ttu-id="dd203-133">Bei PS \_ 3 \_ 0 können die Ausgabe Register "OC #" und "od" \# beliebig oft geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="dd203-133">For ps\_3\_0, output registers oC# and oD\# can be written any number of times.</span></span> <span data-ttu-id="dd203-134">Die Ausgabe des Pixelshaders stammt aus dem Inhalt der Ausgabe Register am Ende der Shader-Ausführung.</span><span class="sxs-lookup"><span data-stu-id="dd203-134">The output of the pixel shader comes from the contents of the output registers at the end of shader execution.</span></span> <span data-ttu-id="dd203-135">Wenn kein Schreibzugriff auf ein Ausgabe Register erfolgt, möglicherweise aufgrund der Fluss Steuerung, oder wenn der Shader ihn eben nicht geschrieben hat, wird auch das zugehörige renderTarget-Element nicht aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="dd203-135">If a write to an output register does not happen, perhaps due to flow control or if the shader just did not write it, the corresponding rendertarget is also not updated.</span></span> <span data-ttu-id="dd203-136">Wenn eine Teilmenge der Kanäle in einem Ausgabe Register geschrieben wird, werden nicht definierte Werte in die restlichen Kanäle geschrieben.</span><span class="sxs-lookup"><span data-stu-id="dd203-136">If a subset of the channels in an output register are written, then undefined values will be written to the remaining channels.</span></span>
-   <span data-ttu-id="dd203-137">Für PS \_ 3 \_ 0 können die OC #-Register mit allen Schreib Vorwörtern geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="dd203-137">For ps\_3\_0, the oC# registers can be written with any writemasks.</span></span>
-   <span data-ttu-id="dd203-138">Für PS \_ 2 \_ x und PS \_ 3 \_ 0 können Sie nicht in oC #-und od- \# Register in der dynamischen Fluss Steuerung oder im Prädikat schreiben (Schreibvorgänge in OC # innerhalb der statischen Fluss Steuerung ist in Ordnung).</span><span class="sxs-lookup"><span data-stu-id="dd203-138">For ps\_2\_x and ps\_3\_0, you cannot write to oC# and oD\# registers within dynamic flow control or predication (writes to oC# inside static flow control is fine).</span></span>
-   <span data-ttu-id="dd203-139">Sie können keine Farbverlaufs Berechnungen (oder Vorgänge, die implizit Farbverlaufs Berechnungen wie [texld-PS \_ 2 \_ 0 und up](texld---ps-2-0.md), [texldb-PS](texldb---ps.md), [texldp-PS](texldp---ps.md)) in Fluss Steuerungs Anweisungen ausführen, deren Verzweigungs Bedingungen auf primitiver Basis variieren (d.h. dynamische Fluss Steuerungs Anweisungen).</span><span class="sxs-lookup"><span data-stu-id="dd203-139">You may not perform any gradient calculations (or operations that implicitly invoke gradient calculations such as [texld - ps\_2\_0 and up](texld---ps-2-0.md), [texldb - ps](texldb---ps.md), [texldp - ps](texldp---ps.md)) inside of flow control statements whose branching conditions vary on a per-primitive basis (ie: dynamic flow control instructions).</span></span> <span data-ttu-id="dd203-140">Das Anweisungs Prädikat gilt nicht als dynamische Fluss Steuerung.</span><span class="sxs-lookup"><span data-stu-id="dd203-140">Instruction predication is not considered dynamic flow control.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dd203-141">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="dd203-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd203-142">Register</span><span class="sxs-lookup"><span data-stu-id="dd203-142">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> <dt>

[<span data-ttu-id="dd203-143">Mehrere Renderziele (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="dd203-143">Multiple Render Targets (Direct3D 9)</span></span>](/windows/desktop/direct3d9/multiple-render-targets)
</dt> </dl>

 

 