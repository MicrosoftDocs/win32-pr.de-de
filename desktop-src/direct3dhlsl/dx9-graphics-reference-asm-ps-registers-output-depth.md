---
title: Ausgabe tiefen Register
description: Das Pixel-Shader-Ausgabe tiefen Register (otiefe) ist ein Schreib geschütztes skalarregister mit dem Bereich "\ 0.. 1 \", der einen neuen tiefen Wert für einen tiefen Test gegen den tiefen Schablone-Puffer zurückgibt.
ms.assetid: 47b9afd9-4520-480d-b4a2-3d9a5569defb
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9be825d6117cf1cc14464973146dbe176d696d25
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311483"
---
# <a name="output-depth-register"></a><span data-ttu-id="fd242-103">Ausgabe tiefen Register</span><span class="sxs-lookup"><span data-stu-id="fd242-103">Output Depth Register</span></span>

<span data-ttu-id="fd242-104">Das Pixel-Shader-Ausgabe tiefen Register (otiefe) ist ein Schreib geschütztes skalarregister mit dem Bereich \[ 0.. 1 \] , das einen neuen tiefen Wert für einen tiefen Test mit dem tiefen Schablone-Puffer zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="fd242-104">The pixel shader output depth register (oDepth) is a write-only scalar register with the range \[0..1\] that returns a new depth value for a depth test against the depth-stencil buffer.</span></span>

<span data-ttu-id="fd242-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fd242-105">Syntax</span></span>



| <span data-ttu-id="fd242-106">otiefe</span><span class="sxs-lookup"><span data-stu-id="fd242-106">oDepth</span></span> |
|--------|



 

<span data-ttu-id="fd242-107">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="fd242-107">Where:</span></span>



| <span data-ttu-id="fd242-108">Name</span><span class="sxs-lookup"><span data-stu-id="fd242-108">Name</span></span>   | <span data-ttu-id="fd242-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fd242-109">Description</span></span>                                                       |
|--------|-------------------------------------------------------------------|
| <span data-ttu-id="fd242-110">otiefe</span><span class="sxs-lookup"><span data-stu-id="fd242-110">oDepth</span></span> | <span data-ttu-id="fd242-111">Neuer tiefen Wert für einen tiefen Test mit dem tiefen Schablone-Puffer</span><span class="sxs-lookup"><span data-stu-id="fd242-111">New depth value for a depth test against the depth-stencil buffer</span></span> |



 

<span data-ttu-id="fd242-112">Beachten Sie, dass das Schreiben in opaces den Verlust von Hardware spezifischen tiefen Puffer Optimierungsalgorithmen (z. b. hierarchische Z) verursacht, die die Tiefe Testleistung beschleunigen.</span><span class="sxs-lookup"><span data-stu-id="fd242-112">It is important to be aware that writing to oDepth causes the loss of any hardware-specific depth buffer optimization algorithms (i.e. hierarchical Z) which accelerate depth test performance.</span></span>

<span data-ttu-id="fd242-113">\|Beim Schreiben in den oausführlich ist das Replizieren der Quelle (. x. y \| . z \| . w) erforderlich.</span><span class="sxs-lookup"><span data-stu-id="fd242-113">Replicate source swizzle (.x \| .y \| .z \| .w) is required when writing to oDepth.</span></span> <span data-ttu-id="fd242-114">Explizite Schreib Masken sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="fd242-114">Explicit write masks are not allowed.</span></span>

<span data-ttu-id="fd242-115">Beim Schreiben in das otiefe-Register wird der interpoliert-tiefen Wert ersetzt (und alle tiefen Bias/slopescale-renderstates werden ignoriert).</span><span class="sxs-lookup"><span data-stu-id="fd242-115">Writing to the oDepth register replaces the interpolated depth value (and ignores any depth bias/slopescale renderstates).</span></span> <span data-ttu-id="fd242-116">Wenn kein tiefen Puffer erstellt oder an das Gerät angefügt wurde, wird der Schreibvorgang in die otiefe ignoriert.</span><span class="sxs-lookup"><span data-stu-id="fd242-116">If no depth buffer has been created or attached to the device, then write to oDepth is ignored.</span></span>

<span data-ttu-id="fd242-117">Wenn Sie multisamplinggrad ausführen und in den oespace schreiben, wird der tiefen Wert für alle behandelten unter Beispiel Speicherorte repliziert, da der Pixelshader nur einmal pro Pixel ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fd242-117">If you are multisampling and write to oDepth, since the pixel shader only runs once per pixel, your depth value is replicated for all covered sub-sample locations.</span></span> <span data-ttu-id="fd242-118">Der tiefen Test erfolgt immer noch pro Stichprobe, aber Sie haben keinen pro-Stichproben-tiefen Wert, der in den Vergleich mit dem Pixelshader erfolgt, wie Sie hätten, wenn Sie keine otiefen geschrieben hätten.</span><span class="sxs-lookup"><span data-stu-id="fd242-118">The depth test still happens per-sample, but you don't have a per-sample depth value going into the comparison from the pixel shader like you would have if you didn't write oDepth.</span></span>

<span data-ttu-id="fd242-119">Wenn für eine Anwendung ein w-Puffer als tiefen Puffer festgelegt ist, muss Sie beim Schreiben in den oausführlich berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="fd242-119">If an application has a w-buffer set as its depth buffer, then it needs to take that into account while writing to oDepth.</span></span> <span data-ttu-id="fd242-120">Möglicherweise muss Sie w-Range-Informationen an den Pixelshader senden und den w-Bereich berechnen, um die in den otiefe geschriebenen w-Werte zu skalieren.</span><span class="sxs-lookup"><span data-stu-id="fd242-120">It potentially needs to send w-range information to the pixel shader and compute the w-range to scale the w-values written out to oDepth.</span></span>

### <a name="ps_2_0-and-ps_2_x-restrictions"></a><span data-ttu-id="fd242-121">PS \_ 2 \_ 0-und PS \_ 2 \_ x-Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="fd242-121">ps\_2\_0 and ps\_2\_x Restrictions</span></span>

-   <span data-ttu-id="fd242-122">otiefen können nur mit der [MOV-PS-](mov---ps.md) Anweisung geschrieben werden und können nur einmal ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="fd242-122">oDepth can only be written with the [mov - ps](mov---ps.md) instruction and can only be done once.</span></span>
-   <span data-ttu-id="fd242-123">Beim Schreiben in den otiefe ist kein quellmodifizierer zulässig.</span><span class="sxs-lookup"><span data-stu-id="fd242-123">No source modifier is allowed when writing to oDepth.</span></span>
-   <span data-ttu-id="fd242-124">Beim Schreiben in den otiefe ist kein Anweisungs Modifizierer zulässig.</span><span class="sxs-lookup"><span data-stu-id="fd242-124">No instruction modifier is allowed when writing to oDepth.</span></span>
-   <span data-ttu-id="fd242-125">Kein Schreiben in den otiefe-Vorgang innerhalb eines Fluss Steuerungs Konstrukts oder bei Verwendung von Prädikat.</span><span class="sxs-lookup"><span data-stu-id="fd242-125">No writing to oDepth from within a flow control construct, or when using predication.</span></span>

### <a name="ps_3_0-restrictions"></a><span data-ttu-id="fd242-126">PS \_ 3 \_ 0-Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="fd242-126">ps\_3\_0 Restrictions</span></span>

-   <span data-ttu-id="fd242-127">Bei PS \_ 3 \_ 0 können die Ausgabe Register "OC #" und "od" \# beliebig oft geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="fd242-127">For ps\_3\_0, output registers oC# and oD\# can be written any number of times.</span></span> <span data-ttu-id="fd242-128">Die Ausgabe des Pixelshaders stammt aus dem Inhalt der Ausgabe Register am Ende der Shader-Ausführung.</span><span class="sxs-lookup"><span data-stu-id="fd242-128">The output of the pixel shader comes from the contents of the output registers at the end of shader execution.</span></span> <span data-ttu-id="fd242-129">Wenn kein Schreibzugriff auf ein Ausgabe Register erfolgt, möglicherweise aufgrund der Fluss Steuerung, oder wenn der Shader ihn eben nicht geschrieben hat, wird auch das entsprechende Renderziel nicht aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="fd242-129">If a write to an output register does not happen, perhaps due to flow control or if the shader just did not write it, the corresponding render target is also not updated.</span></span> <span data-ttu-id="fd242-130">Wenn eine Teilmenge der Kanäle in einem Ausgabe Register geschrieben wird, werden nicht definierte Werte in die restlichen Kanäle geschrieben.</span><span class="sxs-lookup"><span data-stu-id="fd242-130">If a subset of the channels in an output register are written, then undefined values will be written to the remaining channels.</span></span>
-   <span data-ttu-id="fd242-131">Wenn alle möglichen Pfade in das Register schreiben, können Sie in der Fluss Steuerung oder dem Prädikat in den ofuß schreiben.</span><span class="sxs-lookup"><span data-stu-id="fd242-131">You can write to oDepth within flow control or predication as long as all possible paths eventually write into the register.</span></span>
-   <span data-ttu-id="fd242-132">Sie können keine Farbverlaufs Berechnungen (oder Vorgänge, die implizit Farbverlaufs Berechnungen wie [texld-PS \_ 2 \_ 0 und up](texld---ps-2-0.md), [texldb-PS](texldb---ps.md), [texldp-PS](texldp---ps.md)) in Fluss Steuerungs Anweisungen ausführen, deren Verzweigungs Bedingungen auf primitiver Basis variieren (d.h. dynamische Fluss Steuerungs Anweisungen).</span><span class="sxs-lookup"><span data-stu-id="fd242-132">You may not perform any gradient calculations (or operations that implicitly invoke gradient calculations such as [texld - ps\_2\_0 and up](texld---ps-2-0.md), [texldb - ps](texldb---ps.md), [texldp - ps](texldp---ps.md)) inside of flow control statements whose branching conditions vary on a per-primitive basis (ie: dynamic flow control instructions).</span></span> <span data-ttu-id="fd242-133">Das Anweisungs Prädikat gilt nicht als dynamische Fluss Steuerung.</span><span class="sxs-lookup"><span data-stu-id="fd242-133">Instruction predication is not considered dynamic flow control.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fd242-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fd242-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd242-135">Register</span><span class="sxs-lookup"><span data-stu-id="fd242-135">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




