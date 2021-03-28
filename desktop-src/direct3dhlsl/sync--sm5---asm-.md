---
title: Sync (SM5-ASM)
description: Thread Gruppen Synchronisierung oder Speicherbarriere.
ms.assetid: DCA637FE-8F5C-41D0-8B5E-F913463BA387
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be072b51b4a18d9f1408df0907ec0a55131c18d2
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993263"
---
# <a name="sync-sm5---asm"></a><span data-ttu-id="38b0f-103">Sync (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="38b0f-103">sync (sm5 - asm)</span></span>

<span data-ttu-id="38b0f-104">Thread Gruppen Synchronisierung oder Speicherbarriere.</span><span class="sxs-lookup"><span data-stu-id="38b0f-104">Thread group sync or memory barrier.</span></span>



| <span data-ttu-id="38b0f-105">\[ \_ uglobal synchronisieren </span><span class="sxs-lookup"><span data-stu-id="38b0f-105">sync\[\_uglobal</span></span>\|<span data-ttu-id="38b0f-106">\_ugroup \] \[ \_ g \] \[ \_ t\]</span><span class="sxs-lookup"><span data-stu-id="38b0f-106">\_ugroup\]\[\_g\]\[\_t\]</span></span> |
|-------------------------------------------|



 

## <a name="remarks"></a><span data-ttu-id="38b0f-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="38b0f-107">Remarks</span></span>

<span data-ttu-id="38b0f-108">**Sync** verfügt über die Optionen \_ uglobal, \_ ugroup, \_ g und \_ t.</span><span class="sxs-lookup"><span data-stu-id="38b0f-108">**Sync** has options \_uglobal, \_ugroup, \_g and \_t.</span></span>

<span data-ttu-id="38b0f-109">Im Pixelshader ist nur die **Synchronisierung von \_ uglobal** zulässig.</span><span class="sxs-lookup"><span data-stu-id="38b0f-109">In the pixel shader, only **sync\_uglobal** is allowed.</span></span>

<span data-ttu-id="38b0f-110">Im COMPUTE-Shader müssen ( \_ uglobal oder \_ ugroup \* ) und/oder \_ g angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="38b0f-110">In the compute shader, (\_uglobal or \_ugroup\*) and/or \_g must be specified.</span></span> <span data-ttu-id="38b0f-111">\_t ist zusätzlich optional.</span><span class="sxs-lookup"><span data-stu-id="38b0f-111">\_t is optional in addition.</span></span>

### <a name="_uglobal"></a><span data-ttu-id="38b0f-112">\_uglobal</span><span class="sxs-lookup"><span data-stu-id="38b0f-112">\_uglobal</span></span>

<span data-ttu-id="38b0f-113">Arbeitsspeicher-Fence des globalen u \# (UAV).</span><span class="sxs-lookup"><span data-stu-id="38b0f-113">Global u\# (UAV) memory fence.</span></span>

<span data-ttu-id="38b0f-114">Alle früheren u \# -Speicher-Lese-/Schreibvorgänge durch diesen Thread in der Programm Reihenfolge werden für alle Threads auf der gesamten GPU sichtbar gemacht, bevor nachfolgende u- \# Speicherzugriffe durch diesen Thread durchgeführt</span><span class="sxs-lookup"><span data-stu-id="38b0f-114">All prior u\# memory reads/writes by this thread in program order are made visible to all threads on the entire GPU before any subsequent u\# memory accesses by this thread.</span></span> <span data-ttu-id="38b0f-115">Der gesamte GPU-Teil der Definition wird in einem Fall durch einen weniger globalen Bereich ersetzt, wie unten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="38b0f-115">The entire GPU part of the definition is replaced by a less-than-global scope in one case, described below.</span></span>

<span data-ttu-id="38b0f-116">Dies gilt für den gesamten UAV-Speicher, der in der aktuellen Shader-Phase gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="38b0f-116">This applies to all UAV memory bound at the current shader stage.</span></span>

<span data-ttu-id="38b0f-117">\_uglobal ist im COMPUTE-Shader oder Pixel-Shader verfügbar.</span><span class="sxs-lookup"><span data-stu-id="38b0f-117">\_uglobal is available in the compute shader or pixel shader.</span></span>

<span data-ttu-id="38b0f-118">Für jede gebundene UAV, die nicht vom Shader als Global kohärent deklariert wurde, hat der \_ uglobal u- \# Speicher-Fence nur innerhalb der aktuellen Compute-Shader-Thread Gruppe für diese UAV eine Sichtbarkeit, so als ob Sie \_ ugroup anstelle von \_ uglobal ist.</span><span class="sxs-lookup"><span data-stu-id="38b0f-118">For any bound UAV that has not been declared by the shader as Globally Coherent, the \_uglobal u\# memory fence only has visibility within the current compute shader thread-group for that UAV, as if it is \_ugroup instead of \_uglobal.</span></span> <span data-ttu-id="38b0f-119">Dieses Problem gilt nur für den Compute-Shader, da der Pixelshader alle UAVs als Global kohärent deklarieren muss.</span><span class="sxs-lookup"><span data-stu-id="38b0f-119">This issue only applies to the compute shader, since the pixel shader must declare all UAVs as Globally Coherent.</span></span>

### <a name="_ugroup"></a><span data-ttu-id="38b0f-120">\_ugroup</span><span class="sxs-lookup"><span data-stu-id="38b0f-120">\_ugroup</span></span>

<span data-ttu-id="38b0f-121">Arbeitsspeicherfence für Thread Gruppenbereich u \# (UAV).</span><span class="sxs-lookup"><span data-stu-id="38b0f-121">Thread group scope u\# (UAV) memory fence.</span></span>

<span data-ttu-id="38b0f-122">Alle \# von diesem Thread in der Programm Reihenfolge in der Programm Reihenfolge vorgenommenen Lese-oder Schreibvorgänge für den u-Speicher werden für alle Threads in der Thread Gruppe sichtbar gemacht \# .</span><span class="sxs-lookup"><span data-stu-id="38b0f-122">All prior u\# memory reads or writes by this thread in program order are made visible to all threads in the thread group before any subsequent u\# memory accesses by this thread.</span></span>

<span data-ttu-id="38b0f-123">Dies gilt für den gesamten UAV-Speicher, der in der aktuellen Shader-Phase gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="38b0f-123">This applies to all UAV memory bound at the current shader stage.</span></span>

<span data-ttu-id="38b0f-124">\_ugroup ist nur im COMPUTE-Shader verfügbar.</span><span class="sxs-lookup"><span data-stu-id="38b0f-124">\_ugroup is available in the compute shader only.</span></span>

<span data-ttu-id="38b0f-125">Wenn \_ ugroup für einige Implementierungen verfügbar gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="38b0f-125">If \_ugroup is exposed, for some implementations.</span></span> <span data-ttu-id="38b0f-126">Der Vorteil der Angabe von \_ ugroup anstelle von \_ uglobal ist, dass der **Synchronisierungs** Vorgang schneller ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="38b0f-126">The advantage of specifying \_ugroup instead of \_uglobal is that the **sync** operation can complete more quickly.</span></span>

<span data-ttu-id="38b0f-127">Andere Implementierungen unterscheiden \_ ugroup nicht von \_ uglobal, sodass beide Vorgänge äquivalent sind und sich wie \_ uglobal Verhalten.</span><span class="sxs-lookup"><span data-stu-id="38b0f-127">Other implementations do not distinguish \_ugroup from \_uglobal, so both operations are equivalent and behave like \_uglobal.</span></span> <span data-ttu-id="38b0f-128">Anwendungen können Ihre Absicht angeben, indem Sie den engsten Bereich der erforderlichen **Synchronisierung** anfordern.</span><span class="sxs-lookup"><span data-stu-id="38b0f-128">Applications can specify their intent by requesting the narrowest scope of **sync** necessary.</span></span>

<span data-ttu-id="38b0f-129">Selbst wenn eine bestimmte UAV als Global kohärent deklariert ist, \_ wird ein ugroup- **Synchronisierungs** Vorgang auf dieser UAV effizienter funktionieren, wenn keine globale Barriere erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="38b0f-129">Even if a particular UAV is declared as Globally Coherent, a \_ugroup **sync** operation will function more efficiently on that UAV if a global barrier is not required.</span></span>

### <a name="_g"></a><span data-ttu-id="38b0f-130">\_selbst</span><span class="sxs-lookup"><span data-stu-id="38b0f-130">\_g</span></span>

<span data-ttu-id="38b0f-131">der \# fence "g (Thread Gruppe Shared Memory)".</span><span class="sxs-lookup"><span data-stu-id="38b0f-131">g\# (thread group shared memory) fence.</span></span>

<span data-ttu-id="38b0f-132">Alle vorherigen g- \# Speicher Lese-oder Schreibvorgänge durch diesen Thread in der Programm Reihenfolge werden für alle Threads in der Thread Gruppe vor allen nachfolgenden g- \# Speicherzugriffen durch diesen Thread sichtbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="38b0f-132">All prior g\# memory reads or writes by this thread in program order are made visible to all threads in the thread group before any subsequent g\# memory accesses by this thread.</span></span>

<span data-ttu-id="38b0f-133">Dies gilt für den gesamten g Shared Memory-Speicher der aktuellen Thread Gruppe \# .</span><span class="sxs-lookup"><span data-stu-id="38b0f-133">This applies to all of the current thread group's g\# shared memory.</span></span>

<span data-ttu-id="38b0f-134">\_g ist nur im COMPUTE-Shader verfügbar.</span><span class="sxs-lookup"><span data-stu-id="38b0f-134">\_g is available in the compute shader only.</span></span>

### <a name="_t"></a><span data-ttu-id="38b0f-135">\_t</span><span class="sxs-lookup"><span data-stu-id="38b0f-135">\_t</span></span>

<span data-ttu-id="38b0f-136">Synchronisierung der Thread Gruppe. Alle Threads innerhalb einer einzelnen Thread Gruppe (diejenigen, die den Zugriff auf einen gemeinsamen Satz von frei gegebenem Register Bereich freigeben können) werden bis zu dem Punkt ausgeführt, an dem Sie diese Anweisung erreichen, bevor ein Thread fortgesetzt werden kann.</span><span class="sxs-lookup"><span data-stu-id="38b0f-136">Thread group sync. All threads within a single thread group (those that can share access to a common set of shared register space) will be executed up to the point where they reach this instruction before any thread can continue.</span></span>

<span data-ttu-id="38b0f-137">\_t kann nicht in der dynamischen Fluss Steuerung platziert werden (Verzweigungen, die sich innerhalb einer Thread Gruppe unterscheiden können), aber in der einheitlichen Fluss Steuerung vorhanden sein, in der alle Threads in der Gruppe denselben Pfad auswählen.</span><span class="sxs-lookup"><span data-stu-id="38b0f-137">\_t cannot be placed in dynamic flow control, (branches which could vary within a thread group), but can be present in uniform flow control, where all threads in the group pick the same path.</span></span>

<span data-ttu-id="38b0f-138">\_t ist nur im COMPUTE-Shader verfügbar.</span><span class="sxs-lookup"><span data-stu-id="38b0f-138">\_t is available in the compute shader only.</span></span>

<span data-ttu-id="38b0f-139">Im folgenden finden Sie eine Liste der COMPUTE-Shader-Varianten "Sync".</span><span class="sxs-lookup"><span data-stu-id="38b0f-139">The following is a listing of compute shader ‘sync’ variants.</span></span>

-   <span data-ttu-id="38b0f-140">Synchronisieren \_ g</span><span class="sxs-lookup"><span data-stu-id="38b0f-140">sync\_g</span></span>
-   <span data-ttu-id="38b0f-141">\_ugroup synchronisieren\*</span><span class="sxs-lookup"><span data-stu-id="38b0f-141">sync\_ugroup\*</span></span>
-   <span data-ttu-id="38b0f-142">Synchronisieren von \_ uglobal</span><span class="sxs-lookup"><span data-stu-id="38b0f-142">sync\_uglobal</span></span>
-   <span data-ttu-id="38b0f-143">Synchronisieren \_ g \_ t</span><span class="sxs-lookup"><span data-stu-id="38b0f-143">sync\_g\_t</span></span>
-   <span data-ttu-id="38b0f-144">\_ugroup \_ t synchronisieren\*</span><span class="sxs-lookup"><span data-stu-id="38b0f-144">sync\_ugroup\_t\*</span></span>
-   <span data-ttu-id="38b0f-145">Synchronisieren von \_ uglobal \_ t</span><span class="sxs-lookup"><span data-stu-id="38b0f-145">sync\_uglobal\_t</span></span>
-   <span data-ttu-id="38b0f-146">\_ugroup \_ g synchronisieren\*</span><span class="sxs-lookup"><span data-stu-id="38b0f-146">sync\_ugroup\_g\*</span></span>
-   <span data-ttu-id="38b0f-147">Synchronisieren von \_ uglobal \_ g</span><span class="sxs-lookup"><span data-stu-id="38b0f-147">sync\_uglobal\_g</span></span>
-   <span data-ttu-id="38b0f-148">\_ugroup-Gruppe \_ g \_ t synchronisieren\*</span><span class="sxs-lookup"><span data-stu-id="38b0f-148">sync\_ugroup\_g\_t\*</span></span>
-   <span data-ttu-id="38b0f-149">\_uglobal \_ g \_ t synchronisieren</span><span class="sxs-lookup"><span data-stu-id="38b0f-149">sync\_uglobal\_g\_t</span></span>

<span data-ttu-id="38b0f-150">\*Varianten mit \_ ugroup werden möglicherweise nicht durch den HLSL-Compiler als Ziel angesehen \_</span><span class="sxs-lookup"><span data-stu-id="38b0f-150">\*Variants with \_ugroup may not be targeted by the HLSL compiler, per the earlier discussion in the \_ugroup section above.</span></span>

<span data-ttu-id="38b0f-151">Die Auflistung der Pixel-shadersynchronisierungsvarianten umfasst nur die synchrone \_ uglobal.</span><span class="sxs-lookup"><span data-stu-id="38b0f-151">Listing of pixel shader sync variants include sync\_uglobal only.</span></span>

<span data-ttu-id="38b0f-152">Durch Speicher Zäune wird verhindert, dass betroffene Anweisungen durch Compiler oder Hardware auf dem Fence neu angeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="38b0f-152">Memory fences prevent affected instructions from being reordered by compilers or hardware across the fence.</span></span>

<span data-ttu-id="38b0f-153">Mehrere Lesevorgänge von derselben Adresse durch einen shaderaufruf, die nicht durch Speicherbarrieren oder Schreibvorgänge in die Adresse getrennt sind, können zusammen reduziert werden.</span><span class="sxs-lookup"><span data-stu-id="38b0f-153">Multiple reads from the same address by a shader invocation that are not separated by memory barriers or writes to the address can be collapsed together.</span></span> <span data-ttu-id="38b0f-154">Gleiches gilt für Schreibvorgänge.</span><span class="sxs-lookup"><span data-stu-id="38b0f-154">The same applies to writes.</span></span> <span data-ttu-id="38b0f-155">Durch eine Barriere getrennte Zugriffe können nicht zusammengeführt oder über die Barriere verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="38b0f-155">Accesses separated by a barrier cannot be merged or moved across the barrier.</span></span>

<span data-ttu-id="38b0f-156">Arbeitsspeicherzäune sind nicht erforderlich, damit atomarische Vorgänge an einer bestimmten Adresse von verschiedenen Threads ordnungsgemäß funktionieren.</span><span class="sxs-lookup"><span data-stu-id="38b0f-156">Memory fences are not necessary for atomic operations to a given address by different threads to function correctly.</span></span> <span data-ttu-id="38b0f-157">Es sind Zäune erforderlich, wenn Atomics-und/oder lade-/Speicher Vorgänge in Bezug zueinander synchronisiert werden müssen, da Sie in einzelnen Threads aus der Sicht anderer Threads angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="38b0f-157">Fences are needed when atomics and/or load/store operations need to be synchronized with respect to each other as they appear in individual threads from the point of view of other threads.</span></span>

<span data-ttu-id="38b0f-158">In der Pixelshader weisen die Anweisungen zum [verwerfen](discard--sm4---asm-.md) einen \_ globalen Fence der Synchronisierung auf, da diese Anweisungen nicht über den **verwerfen** hinweg neu angeordnet werden können.</span><span class="sxs-lookup"><span data-stu-id="38b0f-158">In the pixel shader, [discard](discard--sm4---asm-.md) instructions imply a sync\_uglobal fence, in that instructions cannot be reordered across the **discard**.</span></span> <span data-ttu-id="38b0f-159">Synchronisieren \_ von uglobal in hilfspixeln (die nur zur Unterstützung von Ableitungen ausgeführt werden) oder verworfene Pixel haben möglicherweise keinerlei Auswirkung.</span><span class="sxs-lookup"><span data-stu-id="38b0f-159">sync\_uglobal in helper pixels (which run only to support derivatives) or discarded pixels may or may not have any affect.</span></span> <span data-ttu-id="38b0f-160">Es ist nicht zulässig, dass Hilfsobjekte oder verworfene Pixel in UAVs geschrieben werden, wenn die Schreibvorgänge im Fall von verwerfen nach dem verwerfen ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="38b0f-160">It is not allowed for helper or discarded pixels to write to UAVs if, in the case of discard, the writes are issued after the discard.</span></span> <span data-ttu-id="38b0f-161">Zurückgegebene Werte von UAVs dürfen nicht zu abgeleiteten Berechnungen beitragen.</span><span class="sxs-lookup"><span data-stu-id="38b0f-161">Returned values from UAVs are not allowed to contribute to derivative calculations.</span></span> <span data-ttu-id="38b0f-162">Daher ist die Synchronisierung \_ von u für Hilfsskripts oder bei der Ausstellung nach einem Verwerfungs Bedarf nicht mehr zu tun.</span><span class="sxs-lookup"><span data-stu-id="38b0f-162">Therefore whether or not sync\_u is honored for helper pixels or when issued after a discard is moot.</span></span>

<span data-ttu-id="38b0f-163">CS \_ 4 \_ 0 und CS \_ 4 \_ 1 unterstützen diese Anweisung.</span><span class="sxs-lookup"><span data-stu-id="38b0f-163">cs\_4\_0 and cs\_4\_1 support this instruction.</span></span>

<span data-ttu-id="38b0f-164">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="38b0f-164">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="38b0f-165">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="38b0f-165">Vertex</span></span> | <span data-ttu-id="38b0f-166">Hülle</span><span class="sxs-lookup"><span data-stu-id="38b0f-166">Hull</span></span> | <span data-ttu-id="38b0f-167">Domain</span><span class="sxs-lookup"><span data-stu-id="38b0f-167">Domain</span></span> | <span data-ttu-id="38b0f-168">Geometrie</span><span class="sxs-lookup"><span data-stu-id="38b0f-168">Geometry</span></span> | <span data-ttu-id="38b0f-169">Pixel</span><span class="sxs-lookup"><span data-stu-id="38b0f-169">Pixel</span></span> | <span data-ttu-id="38b0f-170">Compute</span><span class="sxs-lookup"><span data-stu-id="38b0f-170">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="38b0f-171">X</span><span class="sxs-lookup"><span data-stu-id="38b0f-171">X</span></span>     | <span data-ttu-id="38b0f-172">X</span><span class="sxs-lookup"><span data-stu-id="38b0f-172">X</span></span>       |



 

<span data-ttu-id="38b0f-173">Da UAVs in allen Shader-Phasen für Direct3D 11,1 verfügbar sind, gilt die synchrone uglobal-Variante dieser Anweisung für alle **\_ shaderphasen** der Direct3D 11,1-Laufzeit, die ab Windows 8 verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="38b0f-173">Because UAVs are available at all shader stages for Direct3D 11.1, the **sync\_uglobal** variant of this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="38b0f-174">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="38b0f-174">Vertex</span></span> | <span data-ttu-id="38b0f-175">Hülle</span><span class="sxs-lookup"><span data-stu-id="38b0f-175">Hull</span></span> | <span data-ttu-id="38b0f-176">Domain</span><span class="sxs-lookup"><span data-stu-id="38b0f-176">Domain</span></span> | <span data-ttu-id="38b0f-177">Geometrie</span><span class="sxs-lookup"><span data-stu-id="38b0f-177">Geometry</span></span> | <span data-ttu-id="38b0f-178">Pixel</span><span class="sxs-lookup"><span data-stu-id="38b0f-178">Pixel</span></span> | <span data-ttu-id="38b0f-179">Compute</span><span class="sxs-lookup"><span data-stu-id="38b0f-179">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="38b0f-180">X</span><span class="sxs-lookup"><span data-stu-id="38b0f-180">X</span></span>      | <span data-ttu-id="38b0f-181">X</span><span class="sxs-lookup"><span data-stu-id="38b0f-181">X</span></span>    | <span data-ttu-id="38b0f-182">X</span><span class="sxs-lookup"><span data-stu-id="38b0f-182">X</span></span>      | <span data-ttu-id="38b0f-183">X</span><span class="sxs-lookup"><span data-stu-id="38b0f-183">X</span></span>        | <span data-ttu-id="38b0f-184">X</span><span class="sxs-lookup"><span data-stu-id="38b0f-184">X</span></span>     | <span data-ttu-id="38b0f-185">X</span><span class="sxs-lookup"><span data-stu-id="38b0f-185">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="38b0f-186">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="38b0f-186">Minimum Shader Model</span></span>

<span data-ttu-id="38b0f-187">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="38b0f-187">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="38b0f-188">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="38b0f-188">Shader Model</span></span>                                              | <span data-ttu-id="38b0f-189">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="38b0f-189">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="38b0f-190">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="38b0f-190">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="38b0f-191">ja</span><span class="sxs-lookup"><span data-stu-id="38b0f-191">yes</span></span>       |
| [<span data-ttu-id="38b0f-192">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="38b0f-192">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="38b0f-193">nein</span><span class="sxs-lookup"><span data-stu-id="38b0f-193">no</span></span>        |
| [<span data-ttu-id="38b0f-194">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="38b0f-194">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="38b0f-195">nein</span><span class="sxs-lookup"><span data-stu-id="38b0f-195">no</span></span>        |
| [<span data-ttu-id="38b0f-196">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="38b0f-196">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="38b0f-197">nein</span><span class="sxs-lookup"><span data-stu-id="38b0f-197">no</span></span>        |
| [<span data-ttu-id="38b0f-198">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="38b0f-198">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="38b0f-199">nein</span><span class="sxs-lookup"><span data-stu-id="38b0f-199">no</span></span>        |
| [<span data-ttu-id="38b0f-200">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="38b0f-200">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="38b0f-201">nein</span><span class="sxs-lookup"><span data-stu-id="38b0f-201">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="38b0f-202">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="38b0f-202">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38b0f-203">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="38b0f-203">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 




