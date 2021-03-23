---
title: Direct3D 12 Glossar
description: Diese Begriffe sind von Direct3D 12 unterschiedlichen.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 46B0F055-7E4F-4F8D-9915-3D195FD695B7
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a84b4b2e5a993b33b4c322b91682c8f9b5499bc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548735"
---
# <a name="direct3d-12-glossary"></a><span data-ttu-id="ac59e-103">Direct3D 12 Glossar</span><span class="sxs-lookup"><span data-stu-id="ac59e-103">Direct3D 12 glossary</span></span>

<span data-ttu-id="ac59e-104">Diese Begriffe sind von Direct3D 12 unterschiedlichen.</span><span class="sxs-lookup"><span data-stu-id="ac59e-104">These terms are distinctive of Direct3D 12.</span></span>

<dl> <dt>

<span data-ttu-id="ac59e-105"><span id="direct3d12.directx_12_glossary_binding"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_BINDING"></span>**lichere**</span><span class="sxs-lookup"><span data-stu-id="ac59e-105"><span id="direct3d12.directx_12_glossary_binding"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_BINDING"></span>**binding**</span></span>
</dt> <dd>

<span data-ttu-id="ac59e-106">Der Prozess des Anfügens von Speicher an die Grafik Pipeline.</span><span class="sxs-lookup"><span data-stu-id="ac59e-106">The process of attaching memory to the graphics pipeline.</span></span> <span data-ttu-id="ac59e-107">Die Ressourcen Bindung umfasst z. b. die Bindung einer Ressource, z. b. eine Textur an die Pipeline, die zum Rendern eines Objekts verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ac59e-107">Resource binding, for example, involves the binding of a resource such as a texture to the pipeline, for use in rendering an object.</span></span>

</dd> <dt>

<span data-ttu-id="ac59e-108"><span id="direct3d12.directx_12_glossary_buffer"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_BUFFER"></span>**ert**</span><span class="sxs-lookup"><span data-stu-id="ac59e-108"><span id="direct3d12.directx_12_glossary_buffer"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_BUFFER"></span>**buffer**</span></span>
</dt> <dd>

<span data-ttu-id="ac59e-109">Ein D3D-Ressourcentyp, der mit einer zusammenhängenden Speicher Belegung Synonym ist.</span><span class="sxs-lookup"><span data-stu-id="ac59e-109">A type of D3D resource that is synonymous with a contiguous memory allocation.</span></span>

</dd> <dt>

<span data-ttu-id="ac59e-110"><span id="direct3d12.directx_12_glossary_bundle"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_BUNDLE"></span>**dels**</span><span class="sxs-lookup"><span data-stu-id="ac59e-110"><span id="direct3d12.directx_12_glossary_bundle"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_BUNDLE"></span>**bundle**</span></span>
</dt> <dd>

<span data-ttu-id="ac59e-111">Ein Befehls Puffer, der von der GPU (Graphics Processing Unit) nur direkt über eine *direkte Befehlsliste* ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="ac59e-111">A command buffer that the graphics processing unit (GPU) can execute only directly via a *direct command list*.</span></span> <span data-ttu-id="ac59e-112">Ein Bundle erbt den gesamten GPU-Zustand (mit Ausnahme des aktuell festgelegten *Pipeline Zustands Objekts* und der primitiven Topologie).</span><span class="sxs-lookup"><span data-stu-id="ac59e-112">A bundle inherits all GPU state (except for the currently set *pipeline state object* and primitive topology).</span></span>

</dd> <dt>

<span data-ttu-id="ac59e-113"><span id="direct3d12.directx_12_glossary_command_allocator"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_COMMAND_ALLOCATOR"></span>**Befehls Zuweisung**</span><span class="sxs-lookup"><span data-stu-id="ac59e-113"><span id="direct3d12.directx_12_glossary_command_allocator"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_COMMAND_ALLOCATOR"></span>**command allocator**</span></span>
</dt> <dd>

<span data-ttu-id="ac59e-114">Die zugrunde liegenden Speicher Belegungen, in denen GPU-Befehle gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="ac59e-114">The underlying memory allocations in which GPU commands are stored.</span></span> <span data-ttu-id="ac59e-115">Das Befehls zuordnerobjekt gilt sowohl für *direkte Befehlslisten* als auch für *Pakete*.</span><span class="sxs-lookup"><span data-stu-id="ac59e-115">The command allocator object applies to both *direct command lists* and *bundles*.</span></span>

</dd> <dt>

<span data-ttu-id="ac59e-116"><span id="direct3d12.directx_12_glossary_command_list"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_COMMAND_LIST"></span>**Befehlsliste**</span><span class="sxs-lookup"><span data-stu-id="ac59e-116"><span id="direct3d12.directx_12_glossary_command_list"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_COMMAND_LIST"></span>**command list**</span></span>
</dt> <dd>

<span data-ttu-id="ac59e-117">Eine Befehlsliste entspricht einem Satz von Befehlen, die von der GPU ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="ac59e-117">A command list corresponds to a set of commands which the GPU executes.</span></span> <span data-ttu-id="ac59e-118">Dazu zählen Befehle wie z. b. das Festlegen von Status, zeichnen, löschen und kopieren.</span><span class="sxs-lookup"><span data-stu-id="ac59e-118">These include commands such as to set state, draw, clear, and copy.</span></span> <span data-ttu-id="ac59e-119">Die D3D12-Befehlslisten Schnittstelle unterscheidet sich deutlich von der-Schnittstelle der D3D11-Befehlsliste.</span><span class="sxs-lookup"><span data-stu-id="ac59e-119">The D3D12 command list interface is significantly different than the D3D11 command list interface.</span></span> <span data-ttu-id="ac59e-120">Die D3D12-Befehlslisten Schnittstelle enthält ähnliche APIs wie die D3D11-Gerätekontext-Rendering-APIs.</span><span class="sxs-lookup"><span data-stu-id="ac59e-120">The D3D12 command list interface contains APIs similar to the D3D11 device context rendering APIs.</span></span>

<span data-ttu-id="ac59e-121">In einer D3D12-Befehlsliste werden Ressourcen weder zugeordnet noch die Zuordnung aufgehoben, Kachel Zuordnungen geändert, die Größe der Kachel Pools geändert, Abfrage Daten erhalten oder es werden nie implizit Befehle zur Ausführung an die GPU übermittelt.</span><span class="sxs-lookup"><span data-stu-id="ac59e-121">A D3D12 command list does not map or unmap resources, change tile mappings, resize tile pools, get query data, nor does it ever implicitly submit commands to the GPU for execution.</span></span>

<span data-ttu-id="ac59e-122">Anders als D3D11 verzögerte Kontexte unterstützen D3D12-Befehlslisten nur zwei Dereferenzierungsebenen.</span><span class="sxs-lookup"><span data-stu-id="ac59e-122">Unlike D3D11 deferred contexts, D3D12 command lists only support two levels of indirection.</span></span> <span data-ttu-id="ac59e-123">Eine *direkte Befehlsliste* entspricht einem Befehls Puffer, den die GPU ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="ac59e-123">A *direct command list* corresponds to a command buffer which the GPU can execute.</span></span> <span data-ttu-id="ac59e-124">Ein *Bundle* kann nur direkt über eine direkte Befehlsliste ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="ac59e-124">A *bundle* can be executed only directly via a direct command list.</span></span>

<span data-ttu-id="ac59e-125">Eine direkte Befehlsliste erbt keinen GPU-Zustand.</span><span class="sxs-lookup"><span data-stu-id="ac59e-125">A direct command list does not inherit any GPU state.</span></span> <span data-ttu-id="ac59e-126">Ein Bundle erbt den gesamten GPU-Zustand (mit Ausnahme des aktuell festgelegten Pipeline Zustands Objekts und der primitiven Topologie).</span><span class="sxs-lookup"><span data-stu-id="ac59e-126">A bundle inherits all GPU state (except for the currently set pipeline state object and primitive topology).</span></span>

<span data-ttu-id="ac59e-127">Der Arbeitsspeicher für eine Befehlsliste wird von der *Befehls Zuweisung* festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ac59e-127">Memory for a command list is set by the *command allocator*.</span></span> <span data-ttu-id="ac59e-128">Der Zweck der Befehlslisten besteht darin, dass Sie als einzelne Renderinganforderung an eine GPU übermittelt werden können.</span><span class="sxs-lookup"><span data-stu-id="ac59e-128">The purpose of command lists is that they can be submitted to a GPU as a single rendering request.</span></span>

</dd> <dt>

<span data-ttu-id="ac59e-129"><span id="direct3d12.directx_12_glossary_command_queue"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_COMMAND_QUEUE"></span>**Befehls Warteschlange**</span><span class="sxs-lookup"><span data-stu-id="ac59e-129"><span id="direct3d12.directx_12_glossary_command_queue"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_COMMAND_QUEUE"></span>**command queue**</span></span>
</dt> <dd>

<span data-ttu-id="ac59e-130">Eine *Befehls* Warteschlange, in der die GPU nacheinander ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ac59e-130">A queue of *command lists* that the GPU executes in succession.</span></span> <span data-ttu-id="ac59e-131">Anwendungen müssen *Befehlslisten* explizit zur Ausführung an eine Befehls Warteschlange übermitteln.</span><span class="sxs-lookup"><span data-stu-id="ac59e-131">Applications must explicitly submit *command lists* to a command queue for execution.</span></span> <span data-ttu-id="ac59e-132">In der Regel gibt es drei Befehls Warteschlangen: 3D-Grafiken, COMPUTE und Copy, die der 3D-Grafik Pipeline, der COMPUTE-Engine und einem oder mehreren Kopier Modulen auf der GPU entsprechen.</span><span class="sxs-lookup"><span data-stu-id="ac59e-132">Typically there are three command queues: 3D graphics, compute and copy, corresponding to the 3D graphics pipeline, the compute engine, and one or more copy engines, on the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="ac59e-133"><span id="direct3d12.directx_12_glossary_conservative_rasterization"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_CONSERVATIVE_RASTERIZATION"></span>**konservative rasterisierung**</span><span class="sxs-lookup"><span data-stu-id="ac59e-133"><span id="direct3d12.directx_12_glossary_conservative_rasterization"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_CONSERVATIVE_RASTERIZATION"></span>**conservative rasterization**</span></span>
</dt> <dd>

<span data-ttu-id="ac59e-134">Die konservative rasterisierung ist ein Betriebsmodus für die Raster-Phase der Direct3D-Grafik Pipeline.</span><span class="sxs-lookup"><span data-stu-id="ac59e-134">Conservative rasterization is a mode of operation for the rasterizer stage of the Direct3D graphics pipeline.</span></span> <span data-ttu-id="ac59e-135">Dadurch wird die standardmäßige, auf Stichproben basierende rasterisierung deaktiviert, und stattdessen wird ein Pixel, das von einem beliebigen Betrag durch ein primitiv abgedeckt wird, rasteriert.</span><span class="sxs-lookup"><span data-stu-id="ac59e-135">It disables the standard sample-based rasterization, and will instead rasterize a pixel that is covered by any amount by a primitive.</span></span> <span data-ttu-id="ac59e-136">Ein wichtiger Unterschied besteht darin, dass jede Abdeckung überhaupt ein rasterisiertes Pixel erzeugt, dass diese Abdeckung nicht durch die Hardware gekennzeichnet werden kann, sodass die Abdeckung immer Binär zu einem Pixelshader erscheint: entweder vollständig abgedeckt oder nicht abgedeckt.</span><span class="sxs-lookup"><span data-stu-id="ac59e-136">One important distinction is that, while any coverage at all produces a rasterized pixel, that coverage cannot be characterized by the hardware, so coverage always appears binary to a pixel shader: either fully covered or not covered.</span></span> <span data-ttu-id="ac59e-137">Es wird dem Pixelshader-Code überlassen, um die tatsächliche Abdeckung analytisch zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="ac59e-137">It is left to the pixel shader code to analytically determine the actual coverage.</span></span>

<span data-ttu-id="ac59e-138">Die konservative rasterisierung kann bei solchen Problemen hilfreich sein, z. b. bei der Kollision und Treffer Erkennung, bei der Klassifizierung und bei der Verschleierung, bei der die Farbe eines Pixels genauer ist, und die Kanten Fälle entfernt werden können.</span><span class="sxs-lookup"><span data-stu-id="ac59e-138">Conservative rasterization can help with such problems as collision and hit detection, binning, and occlusion culling, where the color of a pixel is more certain and edge cases can be eliminated.</span></span> <span data-ttu-id="ac59e-139">Siehe [konservative rasterization](conservative-rasterization.md).</span><span class="sxs-lookup"><span data-stu-id="ac59e-139">See [Conservative Rasterization](conservative-rasterization.md).</span></span>

</dd> <dt>

<span data-ttu-id="ac59e-140"><span id="direct3d12.directx_12_glossary_cbv"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_CBV"></span>**Konstante Puffer Ansicht (CBV)**</span><span class="sxs-lookup"><span data-stu-id="ac59e-140"><span id="direct3d12.directx_12_glossary_cbv"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_CBV"></span>**Constant Buffer View (CBV)**</span></span>
</dt> <dd>

<span data-ttu-id="ac59e-141">Konstante Puffer enthalten Shader-Konstante Daten, z. b. eine Kameraansicht, Projektions Matrizen und Welt Matrizen.</span><span class="sxs-lookup"><span data-stu-id="ac59e-141">Constant buffers contain shader constant data, such as a camera view, projection matrices, and world matrices.</span></span> <span data-ttu-id="ac59e-142">Eine "Konstante Puffer Ansicht" ist die Format spezifische Ansicht des Puffers, wie von der Grafik Pipeline ersichtlich.</span><span class="sxs-lookup"><span data-stu-id="ac59e-142">A "constant buffer view" is the format-specific view of the buffer as seen by the graphics pipeline.</span></span>

</dd> <dt>

<span data-ttu-id="ac59e-143"><span id="direct3d12.directx_12_glossary_default_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DEFAULT_HEAP"></span>**Standard Heap**</span><span class="sxs-lookup"><span data-stu-id="ac59e-143"><span id="direct3d12.directx_12_glossary_default_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DEFAULT_HEAP"></span>**default heap**</span></span>
</dt> <dd>

<span data-ttu-id="ac59e-144">Ein Heap im Benutzermodus, der sich auf die Unterstützung von permanenten GPU-Ressourcentypen konzentriert, einschließlich von GPU-geschriebenen Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="ac59e-144">A user-mode heap that is focused on supporting persistent GPU resource types, including GPU-written resources.</span></span>

</dd> <dt>

<span data-ttu-id="ac59e-145"><span id="direct3d12.directx_12_glossary_descriptor"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DESCRIPTOR"></span>**Deskriptor**</span><span class="sxs-lookup"><span data-stu-id="ac59e-145"><span id="direct3d12.directx_12_glossary_descriptor"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DESCRIPTOR"></span>**descriptor**</span></span>
</dt> <dd>

<span data-ttu-id="ac59e-146">Deskriptoren sind die primäre Bindungs Einheit für eine einzelne Ressource in D3D12.</span><span class="sxs-lookup"><span data-stu-id="ac59e-146">Descriptors are the primary unit of binding for a single resource in D3D12.</span></span> <span data-ttu-id="ac59e-147">Ein Deskriptor ist ein relativ kleiner Datenblock, in dem ein Objekt für die GPU vollständig in einem GPU-spezifischen Format beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="ac59e-147">A descriptor is a relatively small block of data that fully describes an object to the GPU, in a GPU specific format.</span></span> <span data-ttu-id="ac59e-148">Es gibt viele verschiedene Arten von Deskriptoren: Shader-Ressourcen Sichten (Srvs), unsorderte Zugriffs Sichten (UAVs), Konstante Puffer Ansichten (cbvs) und Samplers sind einige Beispiele.</span><span class="sxs-lookup"><span data-stu-id="ac59e-148">There are many different types of descriptors: Shader Resource Views (SRVs), Unordered Access Views (UAVs), Constant Buffer Views (CBVs), and Samplers are a few examples.</span></span>

</dd> <dt>

<span data-ttu-id="ac59e-149"><span id="direct3d12.directx_12_glossary_descriptor_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DESCRIPTOR_HEAP"></span>**deskriptorheap**</span><span class="sxs-lookup"><span data-stu-id="ac59e-149"><span id="direct3d12.directx_12_glossary_descriptor_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DESCRIPTOR_HEAP"></span>**descriptor heap**</span></span>
</dt> <dd>

<span data-ttu-id="ac59e-150">Ein deskriptorheap ist eine Auflistung zusammenhängender Belegungen von Deskriptoren, eine Zuordnung für jeden Deskriptor.</span><span class="sxs-lookup"><span data-stu-id="ac59e-150">A descriptor heap is a collection of contiguous allocations of descriptors, one allocation for every descriptor.</span></span> <span data-ttu-id="ac59e-151">Der primäre Punkt eines deskriptorheaps besteht darin, den größten Teil der Arbeitsspeicher Belegung zu umfassen, der zum Speichern der deskriptorspezifikationen von Objekttypen erforderlich ist, auf die sich Shader für einen großen Teil des Renderings als möglich (idealerweise ein ganzer Renderingbereich) beziehen.</span><span class="sxs-lookup"><span data-stu-id="ac59e-151">The primary point of a descriptor heap is to encompass the bulk of memory allocation required for storing the descriptor specifications of object types that shaders reference for as large of a window of rendering as possible (ideally an entire frame of rendering or more).</span></span>

</dd> <dt>

<span data-ttu-id="ac59e-152"><span id="direct3d12.directx_12_glossary_descriptor_table"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DESCRIPTOR_TABLE"></span>**Deskriptortabelle**</span><span class="sxs-lookup"><span data-stu-id="ac59e-152"><span id="direct3d12.directx_12_glossary_descriptor_table"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DESCRIPTOR_TABLE"></span>**descriptor table**</span></span>
</dt> <dd>

<span data-ttu-id="ac59e-153">Eine Deskriptortabelle ist logisch ein Array von Deskriptoren.</span><span class="sxs-lookup"><span data-stu-id="ac59e-153">A descriptor table is logically an array of descriptors.</span></span> <span data-ttu-id="ac59e-154">Jede Deskriptortabelle speichert Deskriptoren von einem oder mehreren Typen, einschließlich Srvs, uave, cbvs und Samplers.</span><span class="sxs-lookup"><span data-stu-id="ac59e-154">Each descriptor table stores descriptors of one or more types, including SRVs, UAVe, CBVs, and Samplers.</span></span> <span data-ttu-id="ac59e-155">Eine Deskriptortabelle ist keine Speicher Belegung, sondern lediglich ein Offset und eine Länge in einem deskriptorheap.</span><span class="sxs-lookup"><span data-stu-id="ac59e-155">A descriptor table is not an allocation of memory, it is simply an offset and length into a descriptor heap.</span></span>

</dd> <dt>

<span data-ttu-id="ac59e-156"><span id="direct3d12.directx_12_glossary_direct_command_list"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DIRECT_COMMAND_LIST"></span>**direkte Befehlsliste**</span><span class="sxs-lookup"><span data-stu-id="ac59e-156"><span id="direct3d12.directx_12_glossary_direct_command_list"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DIRECT_COMMAND_LIST"></span>**direct command list**</span></span>
</dt> <dd>

<span data-ttu-id="ac59e-157">Ein Befehls Puffer, der von der GPU ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="ac59e-157">A command buffer that the GPU can execute.</span></span> <span data-ttu-id="ac59e-158">Eine direkte Befehlsliste erbt keinen GPU-Zustand.</span><span class="sxs-lookup"><span data-stu-id="ac59e-158">A direct command list doesn't inherit any GPU state.</span></span>

</dd> <dt>

<span data-ttu-id="ac59e-159"><span id="direct3d12.directx_12_glossary_fence"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_FENCE"></span>**einzu**</span><span class="sxs-lookup"><span data-stu-id="ac59e-159"><span id="direct3d12.directx_12_glossary_fence"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_FENCE"></span>**fence**</span></span>
</dt> <dd>

<span data-ttu-id="ac59e-160">Ein Mechanismus zum Synchronisieren von GPU und CPU.</span><span class="sxs-lookup"><span data-stu-id="ac59e-160">A mechanism to synchronize the GPU and CPU.</span></span> <span data-ttu-id="ac59e-161">Sowohl die GPU als auch die CPU können angewiesen werden, auf einen Fence zu warten, und es wird darauf gewartet, dass der andere Prozessor in Kraft ist.</span><span class="sxs-lookup"><span data-stu-id="ac59e-161">Both the GPU and CPU can be instructed to wait at a fence, waiting in effect for the other processor to catch up.</span></span> <span data-ttu-id="ac59e-162">Siehe [Synchronisierung mit mehreren](./user-mode-heap-synchronization.md)Modulen.</span><span class="sxs-lookup"><span data-stu-id="ac59e-162">See [Multi-engine synchronization](./user-mode-heap-synchronization.md).</span></span>

</dd> <dt>

<span data-ttu-id="ac59e-163"><span id="direct3d12.directx_12_glossary_hazard"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_HAZARD"></span>**Gefährdung, Gefahren Verfolgung**</span><span class="sxs-lookup"><span data-stu-id="ac59e-163"><span id="direct3d12.directx_12_glossary_hazard"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_HAZARD"></span>**hazard, hazard tracking**</span></span>
</dt> <dd>

<span data-ttu-id="ac59e-164">Eine Gefahr tritt auf, wenn eine Ressource für einen Zweck verwendet wurde, und die APP beabsichtigt, Sie für einen anderen Zweck wiederzuverwenden.</span><span class="sxs-lookup"><span data-stu-id="ac59e-164">A hazard occurs when a resource has been used for one purpose, and the app intends to reuse it for another purpose.</span></span> <span data-ttu-id="ac59e-165">Um die Ressource erneut zu verwenden, müssen zwischengespeicherte Caches geleert oder ungültig gemacht werden. die Komprimierungs Anforderungen müssen mit der zweiten Verwendung konsistent sein, und die Ressource sollte sich im erforderlichen Zustand befinden, um das Lesen der Ressource zu vermeiden, nachdem Sie für den beabsichtigten Zweck geschrieben und für ungültig erklärt wurde.</span><span class="sxs-lookup"><span data-stu-id="ac59e-165">In order to use the resource again, intermediate caches will need to be flushed or invalidated, compression requirements will need to be consistent with the second use, and the resource should be in the required state to avoid reading the resource after it has been written to and invalidated for the intended purpose.</span></span>

<span data-ttu-id="ac59e-166">Der Prozess der Wartung von Ressourcen und die Vermeidung dieser Synchronisierungs Probleme wird als Risiko Verfolgung bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="ac59e-166">The process of maintaining resources and avoiding these sync issues is known as hazard tracking.</span></span> <span data-ttu-id="ac59e-167">Wenn keine Gefahren Nachverfolgung durch den Treiber vorhanden ist, ist die App dafür verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="ac59e-167">If there is no hazard tracking by the driver, then the app is responsible for this.</span></span> <span data-ttu-id="ac59e-168">In den meisten früheren Versionen von DirectX wurde die Gefahren Nachverfolgung durch den Treiber behandelt.</span><span class="sxs-lookup"><span data-stu-id="ac59e-168">In most earlier versions of DirectX, hazard tracking was handled by the driver.</span></span> <span data-ttu-id="ac59e-169">Um die Leistung zu verbessern, sind Methoden ohne Risiko Verfolgung in DirectX 12 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ac59e-169">To improve performance, methods without hazard tracking are available in DirectX 12.</span></span>

</dd> <dt>

<span data-ttu-id="ac59e-170"><span id="direct3d12.directx_12_glossary_hlsl"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_HLSL"></span>**High-Level-Shader-Sprache (HLSL)**</span><span class="sxs-lookup"><span data-stu-id="ac59e-170"><span id="direct3d12.directx_12_glossary_hlsl"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_HLSL"></span>**High-Level Shader Language (HLSL)**</span></span>
</dt> <dd>

<span data-ttu-id="ac59e-171">Eine Computersprache, die sich in vielerlei Hinsicht von C unterscheidet, die zum Schreiben von Shader-Code verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ac59e-171">A computer language, similar but distinct in many ways from C, that is used to write shader code.</span></span> <span data-ttu-id="ac59e-172">Vertex-, Pixel-, Geometrie-, COMPUTE-, Domänen-und Hull-Shader werden mithilfe von HLSL geschrieben.</span><span class="sxs-lookup"><span data-stu-id="ac59e-172">Vertex, pixel, geometry, compute, domain, and hull shaders are all written using HLSL.</span></span> <span data-ttu-id="ac59e-173">Ein Compiler konvertiert die HLSL-Quelle in ein binäres Format, das von der GPU verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ac59e-173">A compiler converts the HLSL source into a binary format for the GPU to consume.</span></span>

</dd> <dt>

<span data-ttu-id="ac59e-174"><span id="direct3d12.directx_12_glossary_multiengine"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_MULTIENGINE"></span>**multiengine**</span><span class="sxs-lookup"><span data-stu-id="ac59e-174"><span id="direct3d12.directx_12_glossary_multiengine"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_MULTIENGINE"></span>**multiengine**</span></span>
</dt> <dd>

<span data-ttu-id="ac59e-175">Die verschiedenen Instanzen und Typen von Engines in einer einzelnen GPU.</span><span class="sxs-lookup"><span data-stu-id="ac59e-175">The different instances and types of engines in a single GPU.</span></span> <span data-ttu-id="ac59e-176">Die Arten von Engines umfassen: Grafiken, COMPUTE und Copy.</span><span class="sxs-lookup"><span data-stu-id="ac59e-176">The types of engines include: graphics, compute, and copy.</span></span>

</dd> <dt>

<span data-ttu-id="ac59e-177"><span id="direct3d12.directx_12_glossary_multigpu"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_MULTIGPU"></span>**Multigpu**</span><span class="sxs-lookup"><span data-stu-id="ac59e-177"><span id="direct3d12.directx_12_glossary_multigpu"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_MULTIGPU"></span>**MultiGPU**</span></span>
</dt> <dd>

<span data-ttu-id="ac59e-178">Eine Hardwarekonfiguration, bei der mehr als ein Grafikadapter vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="ac59e-178">A hardware configuration where there is more than one graphics adapter.</span></span> <span data-ttu-id="ac59e-179">Die separaten Adapter werden manchmal als Knoten bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="ac59e-179">The separate adapters are sometimes referred to as nodes.</span></span> <span data-ttu-id="ac59e-180">Wenn Sie über mehrere GPUs verfügen, können Sie die Synchronisierung mit der CPU und einander erheblich komplexer machen als mit einer einzelnen GPU.</span><span class="sxs-lookup"><span data-stu-id="ac59e-180">Having multiple GPUs can make the task of synchronizing them with the CPU, and each other, considerably more complex than with a single GPU.</span></span>

</dd> <dt>

<span data-ttu-id="ac59e-181"><span id="direct3d12.directx_12_glossary_pipeline_state_object"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_PIPELINE_STATE_OBJECT"></span>**Pipeline Zustands Objekt (PSO)**</span><span class="sxs-lookup"><span data-stu-id="ac59e-181"><span id="direct3d12.directx_12_glossary_pipeline_state_object"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_PIPELINE_STATE_OBJECT"></span>**Pipeline State object (PSO)**</span></span>
</dt> <dd>

<span data-ttu-id="ac59e-182">Ein erheblicher Teil des Status der GPU.</span><span class="sxs-lookup"><span data-stu-id="ac59e-182">A significant portion of the state of the GPU.</span></span> <span data-ttu-id="ac59e-183">Dieser Status umfasst alle aktuell festgelegten Shader und bestimmte Zustands Objekte mit fester Funktions Zeit.</span><span class="sxs-lookup"><span data-stu-id="ac59e-183">This state includes all currently set shaders and certain fixed-function state objects.</span></span> <span data-ttu-id="ac59e-184">Die einzige Möglichkeit zum Ändern von Zuständen, die im Pipeline Objekt enthalten sind, besteht darin, das zurzeit gebundene Pipeline Objekt zu ändern.</span><span class="sxs-lookup"><span data-stu-id="ac59e-184">The only way to change states contained within the pipeline object is to change the currently bound pipeline object.</span></span>

</dd> <dt>

<span data-ttu-id="ac59e-185"><span id="direct3d12.directx_12_glossary_predication"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_PREDICATION"></span>**Prädikation übersprungen**</span><span class="sxs-lookup"><span data-stu-id="ac59e-185"><span id="direct3d12.directx_12_glossary_predication"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_PREDICATION"></span>**predication**</span></span>
</dt> <dd>

<span data-ttu-id="ac59e-186">Das-Prädikat ist ein Feature, mit dem die GPU anstelle der CPU feststellen kann, ob ein Objekt nicht gezeichnet, kopiert oder versendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ac59e-186">Predication is a feature that enables the GPU rather than the CPU to determine to not draw, copy or dispatch an object.</span></span> <span data-ttu-id="ac59e-187">Wenn z. b. ein Begrenzungsfeld eines Objekts vollständig von einem anderen Objekt oder einer Perspektive vollständig auf eine geringere Größe als die Pixelgröße reduziert wurde, ist es möglicherweise nicht sinnvoll, das verborgene Objekt zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="ac59e-187">For example, if a bounding box of an object is totally occluded by another object or perspective has reduced the object to less than the size of a pixel, there may be no point in attempting to draw the hidden object at all.</span></span> <span data-ttu-id="ac59e-188">Siehe [prediation](predication.md).</span><span class="sxs-lookup"><span data-stu-id="ac59e-188">See [Predication](predication.md).</span></span>

</dd> <dt>

<span data-ttu-id="ac59e-189"><span id="direct3d12.directx_12_glossary_rov"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_ROV"></span>**Reihen folgen Ansicht des Rasterizers (Row)**</span><span class="sxs-lookup"><span data-stu-id="ac59e-189"><span id="direct3d12.directx_12_glossary_rov"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_ROV"></span>**Rasterizer Order View (ROV)**</span></span>
</dt> <dd>

<span data-ttu-id="ac59e-190">Standard Grafik Pipelines haben möglicherweise Probleme mit der ordnungsgemäßen Zusammensetzung mehrerer Texturen, die Transparenz enthalten.</span><span class="sxs-lookup"><span data-stu-id="ac59e-190">Standard graphics pipelines may have trouble correctly compositing together multiple textures that contain transparency.</span></span> <span data-ttu-id="ac59e-191">Objekte wie z. b. Drahtzäune, Rauch, Feuer, Vegetation und farbige Glas verwenden Transparenz, um den gewünschten Effekt zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="ac59e-191">Objects such as wire fences, smoke, fire, vegetation, and colored glass use transparency to get the desired effect.</span></span> <span data-ttu-id="ac59e-192">Es treten Probleme auf, wenn mehrere Texturen, die Transparenz enthalten, aufeinander zueinander stehen (Feuer vor einem Fence vor einem Glasgebäude, das eine Vegetations enthält).</span><span class="sxs-lookup"><span data-stu-id="ac59e-192">Problems arise when multiple textures that contain transparency are in line with each other (smoke in front of a fence in front of a glass building containing vegetation, as an example).</span></span> <span data-ttu-id="ac59e-193">Mithilfe von "Rasterizer-Ansichten" (ROVs) können die zugrunde liegenden OIT-Algorithmen (Order Independent Transparenz) die Features der Hardware zum ordnungsgemäßen Auflösen der Transparenz Reihenfolge verwenden.</span><span class="sxs-lookup"><span data-stu-id="ac59e-193">Rasterizer ordered views (ROVs) enable the underlying Order Independent Transparency (OIT) algorithms to use features of the hardware to try to resolve the transparency order correctly.</span></span> <span data-ttu-id="ac59e-194">Transparenz wird vom Pixelshader behandelt.</span><span class="sxs-lookup"><span data-stu-id="ac59e-194">Transparency is handled by the pixel shader.</span></span>

<span data-ttu-id="ac59e-195">Mithilfe geordneter Ansichten von Rasterizer (ROVs) können Pixel-Shader-Code ungeordnete zugriffsansichts-Bindungen (UAV) mit einer Deklaration markieren, die die normalen Anforderungen für die Reihenfolge der Ergebnisse der Grafik Pipeline für UAVs ändert.</span><span class="sxs-lookup"><span data-stu-id="ac59e-195">Rasterizer Ordered Views (ROVs) allow pixel shader code to mark Unordered Access View (UAV) bindings with a declaration that alters the normal requirements for the order of graphics pipeline results for UAVs.</span></span>

</dd> <dt>

<span data-ttu-id="ac59e-196"><span id="direct3d12.directx_12_glossary_readback_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_READBACK_HEAP"></span>**Read-Back-Heap**</span><span class="sxs-lookup"><span data-stu-id="ac59e-196"><span id="direct3d12.directx_12_glossary_readback_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_READBACK_HEAP"></span>**readback heap**</span></span>
</dt> <dd>

<span data-ttu-id="ac59e-197">Ein Heap im Benutzermodus, der sich auf die Datenübertragung von der GPU zurück zur CPU konzentriert.</span><span class="sxs-lookup"><span data-stu-id="ac59e-197">A user-mode heap that is focused on data transfer from the GPU back to the CPU.</span></span>

</dd> <dt>

<span data-ttu-id="ac59e-198"><span id="direct3d12.directx_12_glossary_resource"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE"></span>**Ressource**</span><span class="sxs-lookup"><span data-stu-id="ac59e-198"><span id="direct3d12.directx_12_glossary_resource"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE"></span>**resource**</span></span>
</dt> <dd>

<span data-ttu-id="ac59e-199">Eine Entität, die Daten für die Pipeline bereitstellt und definiert, was während der Szene gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="ac59e-199">An entity that provides data to the pipeline and defines what is rendered during your scene.</span></span> <span data-ttu-id="ac59e-200">Ressourcen können von ihren Spiel Medien geladen oder dynamisch zur Laufzeit erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="ac59e-200">Resources can be loaded from your game media or created dynamically at run time.</span></span> <span data-ttu-id="ac59e-201">In der Regel enthalten Ressourcen Textur Daten, Scheitelpunkt Daten und shaderdaten.</span><span class="sxs-lookup"><span data-stu-id="ac59e-201">Typically, resources include texture data, vertex data, and shader data.</span></span> <span data-ttu-id="ac59e-202">Die meisten Direct3D-Anwendungen erstellen und zerstören Ressourcen in der gesamten Lebensdauer.</span><span class="sxs-lookup"><span data-stu-id="ac59e-202">Most Direct3D applications create and destroy resources extensively throughout their lifespan.</span></span>

</dd> <dt>

<span data-ttu-id="ac59e-203"><span id="direct3d12.directx_12_glossary_resource_barrier"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE_BARRIER"></span>**Ressourcen Barriere**</span><span class="sxs-lookup"><span data-stu-id="ac59e-203"><span id="direct3d12.directx_12_glossary_resource_barrier"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE_BARRIER"></span>**resource barrier**</span></span>
</dt> <dd>

<span data-ttu-id="ac59e-204">Eine Ressourcengrenze benachrichtigt den Treiber, dass möglicherweise eine Synchronisierung mehrerer Zugriffe auf eine einzelne Ressource erforderlich ist, z. b. das Lesen und Schreiben in dieselbe Textur.</span><span class="sxs-lookup"><span data-stu-id="ac59e-204">A resource barrier notifies the driver that synchronization of multiple accesses to a single resource may be required, for example, reading and writing to the same texture.</span></span>

</dd> <dt>

<span data-ttu-id="ac59e-205"><span id="direct3d12.directx_12_glossary_resource_binding"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE_BINDING"></span>**Ressourcen Bindung**</span><span class="sxs-lookup"><span data-stu-id="ac59e-205"><span id="direct3d12.directx_12_glossary_resource_binding"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE_BINDING"></span>**resource binding**</span></span>
</dt> <dd>

<span data-ttu-id="ac59e-206">Bei der Ressourcen Bindung werden Ressourcen (Texturen, Vertex-Puffer, Index Puffer usw.) mit der Grafik Pipeline verknüpft, sodass die Shader der Pipeline die richtige Ressource verarbeiten können.</span><span class="sxs-lookup"><span data-stu-id="ac59e-206">Resource binding is the process of linking resources (textures, vertex buffers, index buffers, and so on), to the graphics pipeline, enabling the shaders of the pipeline to process the correct resource.</span></span>

</dd> <dt>

<span data-ttu-id="ac59e-207"><span id="direct3d12.directx_12_glossary_resource_heaps"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE_HEAPS"></span>**Ressourcen Heaps**</span><span class="sxs-lookup"><span data-stu-id="ac59e-207"><span id="direct3d12.directx_12_glossary_resource_heaps"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE_HEAPS"></span>**resource heaps**</span></span>
</dt> <dd>

<span data-ttu-id="ac59e-208">Ressourcen Heaps sind ein allgemeiner Begriff für die Heaps, bei denen es sich um Speicherpuffer handelt, die bei der Übertragung an und von der GPU reserviert werden.</span><span class="sxs-lookup"><span data-stu-id="ac59e-208">Resource heaps is a generic term for the heaps that are memory buffers set aside to hold resources as they are transferred to and from the GPU.</span></span> <span data-ttu-id="ac59e-209">Eine Übertragung an die GPU erfordert einen uploadheap, von der GPU bis zur CPU erfordert einen abzurufenden Heap, und ein persistenter Heap für die GPU, der über mehrere renderingframes gewartet werden soll, wird als Standard Heap bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="ac59e-209">A transfer to the GPU requires an Upload Heap, from the GPU to the CPU requires a Readback Heap, and a persistent heap for the GPU to maintain over multiple rendering frames is called a Default Heap.</span></span>

</dd> <dt>

<span data-ttu-id="ac59e-210"><span id="direct3d12.directx_12_glossary_root_signature"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_ROOT_SIGNATURE"></span>**Stamm Signatur**</span><span class="sxs-lookup"><span data-stu-id="ac59e-210"><span id="direct3d12.directx_12_glossary_root_signature"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_ROOT_SIGNATURE"></span>**root signature**</span></span>
</dt> <dd>

<span data-ttu-id="ac59e-211">Stamm Signaturen definieren alle Ressourcen, die an die Grafiken oder COMPUTE-Pipelines gebunden werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ac59e-211">Root signatures define all the resources that are to be bound to the graphics, or compute, pipelines.</span></span> <span data-ttu-id="ac59e-212">Eine Stamm Signatur wird von der APP und Verknüpfungen Befehlslisten mit den Ressourcen konfiguriert, die für die Shader normalerweise erforderlich sind. es gibt jeweils eine Grafik und eine computestammsignatur pro app.</span><span class="sxs-lookup"><span data-stu-id="ac59e-212">A root signature is configured by the app and links command lists to the resources that the shaders require Typically, there is one graphics and one compute root signature per app.</span></span>

</dd> <dt>

<span data-ttu-id="ac59e-213"><span id="direct3d12.directx_12_glossary_sampler"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SAMPLER"></span>**Sammel**</span><span class="sxs-lookup"><span data-stu-id="ac59e-213"><span id="direct3d12.directx_12_glossary_sampler"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SAMPLER"></span>**sampler**</span></span>
</dt> <dd>

<span data-ttu-id="ac59e-214">Ein Sampler ist Code, der aus einer Textur liest.</span><span class="sxs-lookup"><span data-stu-id="ac59e-214">A sampler is code that reads from a texture.</span></span>

</dd> <dt>

<span data-ttu-id="ac59e-215"><span id="direct3d12.directx_12_glossary_srv"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SRV"></span>**Shader-Ressourcenansicht (SRV)**</span><span class="sxs-lookup"><span data-stu-id="ac59e-215"><span id="direct3d12.directx_12_glossary_srv"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SRV"></span>**Shader Resource View (SRV)**</span></span>
</dt> <dd>

<span data-ttu-id="ac59e-216">Eine Format spezifische Methode zum Überprüfen der Daten in einer Shader-Ressource, z. b. eine Textur.</span><span class="sxs-lookup"><span data-stu-id="ac59e-216">A format-specific way to look at the data in a shader resource, such as a texture.</span></span>

</dd> <dt>

<span data-ttu-id="ac59e-217"><span id="direct3d12.directx_12_glossary_static_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_STATIC_HEAP"></span>**statischer Heap**</span><span class="sxs-lookup"><span data-stu-id="ac59e-217"><span id="direct3d12.directx_12_glossary_static_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_STATIC_HEAP"></span>**static heap**</span></span>
</dt> <dd>

<span data-ttu-id="ac59e-218">Ein Heap im Benutzermodus, der sich auf mehrere GPU-schreibgeschützte Ressourcen konzentriert, die normalerweise gleichzeitig verwendet werden und nicht häufig geändert werden.</span><span class="sxs-lookup"><span data-stu-id="ac59e-218">A user-mode heap that is focused on multiple GPU-read-only resources that are typically used at the same time and are not changed frequently.</span></span>

</dd> <dt>

<span data-ttu-id="ac59e-219"><span id="direct3d12.directx_12_glossary_swap_chain"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SWAP_CHAIN"></span>**Austausch Kette**</span><span class="sxs-lookup"><span data-stu-id="ac59e-219"><span id="direct3d12.directx_12_glossary_swap_chain"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SWAP_CHAIN"></span>**swap chain**</span></span>
</dt> <dd>

<span data-ttu-id="ac59e-220">Austausch Ketten steuern die Hintergrund Puffer Drehung und bilden die Grundlage der Grafik Animation.</span><span class="sxs-lookup"><span data-stu-id="ac59e-220">Swap chains control the back buffer rotation, forming the basis of graphics animation.</span></span> <span data-ttu-id="ac59e-221">Swapketten werden vom Low-Level-API-Satz DXGI behandelt (Weitere Informationen finden Sie unter [DXGI Overview](../direct3ddxgi/d3d10-graphics-programming-guide-dxgi.md)).</span><span class="sxs-lookup"><span data-stu-id="ac59e-221">Swap chains are handled by the low level API set DXGI (see [DXGI Overview](../direct3ddxgi/d3d10-graphics-programming-guide-dxgi.md)).</span></span>

</dd> <dt>

<span data-ttu-id="ac59e-222"><span id="direct3d12.directx_12_glossary_swizzle"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SWIZZLE"></span>**Swizzle**</span><span class="sxs-lookup"><span data-stu-id="ac59e-222"><span id="direct3d12.directx_12_glossary_swizzle"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SWIZZLE"></span>**swizzle**</span></span>
</dt> <dd>

<span data-ttu-id="ac59e-223">Eine Technik, mit der Mehrdimensionale Daten im Arbeitsspeicher gesucht werden, sodass Daten aus der nahen Dimensionalität in der Regel nahe gelegene Adressen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="ac59e-223">A technique of locating multidimensional data in memory such that data of nearby dimensionality tends to have nearby addresses.</span></span> <span data-ttu-id="ac59e-224">Vor allem werden alle Daten für eine Zeile vor den Daten für die nächste Zeile nicht zusammenhängend gefunden.</span><span class="sxs-lookup"><span data-stu-id="ac59e-224">In particular, all the data for one row is not located contiguously before the data for the next row.</span></span> <span data-ttu-id="ac59e-225">Ein "parametrisiertes schwenken" beschreibt eine standardisierte Methode zum Beschreiben von swidingmustern.</span><span class="sxs-lookup"><span data-stu-id="ac59e-225">A "Parameterized Swizzle" describes a standardized way to describe swizzle patterns.</span></span>

</dd> <dt>

<span data-ttu-id="ac59e-226"><span id="direct3d12.directx_12_glossary_static_texture"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_STATIC_TEXTURE"></span>**Konsistenz**</span><span class="sxs-lookup"><span data-stu-id="ac59e-226"><span id="direct3d12.directx_12_glossary_static_texture"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_STATIC_TEXTURE"></span>**texture**</span></span>
</dt> <dd>

<span data-ttu-id="ac59e-227">Ein D3D-Ressourcentyp, der mehrdimensional ist und über ein Speicher Layout verfügt, das für den mehrdimensionalen Zugriff von der GPU optimiert ist.</span><span class="sxs-lookup"><span data-stu-id="ac59e-227">A type of D3D resource that is multi-dimensional and has a memory layout that is optimized for multi-dimensional access from the GPU.</span></span> <span data-ttu-id="ac59e-228">Texturen enthalten häufig das Rohbild, das zum Renderingvorgang auf einer Oberfläche erforderlich ist, bevor Beleuchtung und Vermischung stattfinden, aber auch andere Formen von Daten enthalten können, z. b. Farbverläufe und Bezugs Farben.</span><span class="sxs-lookup"><span data-stu-id="ac59e-228">Textures often contain the raw image required to render onto a surface, before lighting and blending takes place, but can contain other forms of data such as color gradients and reference colors.</span></span> <span data-ttu-id="ac59e-229">Direct3D 12 unterstützt eine, zwei und dreidimensionale Texturen.</span><span class="sxs-lookup"><span data-stu-id="ac59e-229">Direct3D 12 supports one, two, and three dimensional textures.</span></span>

</dd> <dt>

<span data-ttu-id="ac59e-230"><span id="direct3d12.directx_12_glossary_tile"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_TILE"></span>**Stein**</span><span class="sxs-lookup"><span data-stu-id="ac59e-230"><span id="direct3d12.directx_12_glossary_tile"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_TILE"></span>**tile**</span></span>
</dt> <dd>

<span data-ttu-id="ac59e-231">Eine Seite mit Video Arbeitsspeicher, ähnlich einer CPU/System-Seite des Speichers.</span><span class="sxs-lookup"><span data-stu-id="ac59e-231">A page of video memory, similar to a CPU/System page of memory.</span></span> <span data-ttu-id="ac59e-232">Mithilfe der Kachel Notation kann das subsubsystem des virtuellen GPU-Speichers vom virtuellen CPU-Speichersubsystem unterschieden werden.</span><span class="sxs-lookup"><span data-stu-id="ac59e-232">The tile notation helps to distinguish the GPU virtual memory subsystem from the CPU virtual memory subsystem.</span></span> <span data-ttu-id="ac59e-233">GPUs bieten ähnliche Funktionen für den virtuellen Arbeitsspeicher wie der virtuelle Systemspeicher.</span><span class="sxs-lookup"><span data-stu-id="ac59e-233">GPUs provide similar virtual memory capabilities as system virtual memory.</span></span> <span data-ttu-id="ac59e-234">Einige GPUs verfügen über freigegebene Funktionen für den virtuellen Arbeitsspeicher, die die Freigabe einiger Seiten des virtuellen Speicher Subsystems sowohl mit der CPU als auch mit der GPU ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="ac59e-234">Some GPUs have shared virtual memory capabilities, which allow for the sharing of some pages of the virtual memory subsystem with both the CPU and GPU.</span></span>

</dd> <dt>

<span data-ttu-id="ac59e-235"><span id="direct3d12.directx_12_glossary_tiled_resources"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_TILED_RESOURCES"></span>**Gekachelte Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="ac59e-235"><span id="direct3d12.directx_12_glossary_tiled_resources"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_TILED_RESOURCES"></span>**tiled resources**</span></span>
</dt> <dd>

<span data-ttu-id="ac59e-236">Gekachelte Ressourcen werden benötigt, sodass weniger GPU-Speicherplatz für das Speichern von Bereichen von Oberflächen verschwendet wird, auf die die Anwendung keinen Zugriff hat, und die Hardware weiß, wie Sie über angrenzende Kacheln filtern kann.</span><span class="sxs-lookup"><span data-stu-id="ac59e-236">Tiled resources are needed so less GPU memory is wasted storing regions of surfaces that the application knows will not be accessed, and the hardware can understand how to filter across adjacent tiles.</span></span> <span data-ttu-id="ac59e-237">Bei gekachelten Ressourcen handelt es sich um große logische Ressourcen, die jedoch nur wenige physische Speichermengen erfordern.</span><span class="sxs-lookup"><span data-stu-id="ac59e-237">Tiled resources are large logical resources, but requiring small amounts of physical memory.</span></span>

</dd> <dt>

<span data-ttu-id="ac59e-238"><span id="direct3d12.directx_12_glossary_uav"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_UAV"></span>**Unsortierter Zugriffs Ansicht (UAV)**</span><span class="sxs-lookup"><span data-stu-id="ac59e-238"><span id="direct3d12.directx_12_glossary_uav"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_UAV"></span>**Unordered Access View (UAV)**</span></span>
</dt> <dd>

<span data-ttu-id="ac59e-239">Eine ungeordnete Zugriffs Ansicht in eine Ressource (die Puffer, Texturen und Textur Arrays enthält, ohne Multisampling), ermöglicht temporalen ungeordneten Lese-/Schreibzugriff von mehreren Threads.</span><span class="sxs-lookup"><span data-stu-id="ac59e-239">An unordered access view into a resource (which includes buffers, textures, and texture arrays - without multi-sampling), allows temporally unordered read/write access from multiple threads.</span></span> <span data-ttu-id="ac59e-240">Dies bedeutet, dass dieser Ressourcentyp gleichzeitig von mehreren Threads gelesen/geschrieben werden kann, ohne dass Speicher Konflikte entstehen.</span><span class="sxs-lookup"><span data-stu-id="ac59e-240">This means that this resource type can be read/written simultaneously by multiple threads without generating memory conflicts.</span></span>

</dd> <dt>

<span data-ttu-id="ac59e-241"><span id="direct3d12.directx_12_glossary_upload_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_UPLOAD_HEAP"></span>**Heap hochladen**</span><span class="sxs-lookup"><span data-stu-id="ac59e-241"><span id="direct3d12.directx_12_glossary_upload_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_UPLOAD_HEAP"></span>**upload heap**</span></span>
</dt> <dd>

<span data-ttu-id="ac59e-242">Ein Heap im Benutzermodus, der sich auf die Datenübertragung von der CPU an die GPU konzentriert.</span><span class="sxs-lookup"><span data-stu-id="ac59e-242">A user-mode heap that is focused on data transfer from the CPU to the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="ac59e-243"><span id="direct3d12.directx_12_glossary_user_mode_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_USER_MODE_HEAP"></span>**benutzermodusheap**</span><span class="sxs-lookup"><span data-stu-id="ac59e-243"><span id="direct3d12.directx_12_glossary_user_mode_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_USER_MODE_HEAP"></span>**user-mode heap**</span></span>
</dt> <dd>

<span data-ttu-id="ac59e-244">Eine Auflistung großer, zusammenhängender Speicher Belegungen, die ohne das Wissen der Kernel Komponente wieder verwendet werden: die Zuordnungs-und Zerstörungs Methoden werden während des stabilen Zustands nicht als Kernel Zuordnungs-und Zerstörungs Methoden bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="ac59e-244">A collection of large, contiguous memory allocations that are recycled without any kernel component's awareness: the allocation and destruction methods do not call kernel allocation and destruction methods during steady state.</span></span> <span data-ttu-id="ac59e-245">Upload-, leseback-und Standard-Heaps sind Varianten von Heaps im Benutzermodus.</span><span class="sxs-lookup"><span data-stu-id="ac59e-245">Upload, Readback, and Default heaps are variants of user mode heaps.</span></span>

</dd> <dt>

<span data-ttu-id="ac59e-246"><span id="direct3d12.directx_12_glossary_volume_tiled_resources"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_VOLUME_TILED_RESOURCES"></span>**Menge an Kacheln**</span><span class="sxs-lookup"><span data-stu-id="ac59e-246"><span id="direct3d12.directx_12_glossary_volume_tiled_resources"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_VOLUME_TILED_RESOURCES"></span>**volume tiled resources**</span></span>
</dt> <dd>

<span data-ttu-id="ac59e-247">Dreidimensionale [gekachelte Ressourcen](/windows).</span><span class="sxs-lookup"><span data-stu-id="ac59e-247">Three-dimensional [tiled resources](/windows).</span></span>

</dd> </dl>

 

 