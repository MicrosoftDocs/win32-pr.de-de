---
title: Direct3D 12 Core 1.0-Featureebene
description: Die Core 1,0-Featureebene ist eine Teilmenge des vollständigen Direct3D 12-Funktions Satzes.
ms.topic: article
ms.date: 11/05/2019
ms.openlocfilehash: 42d13b71c516e55ecce378cf9cb415c45e520ba9
ms.sourcegitcommit: bba068130240d16de8a3f3468b7cd72b2cd760f6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/03/2020
ms.locfileid: "106340893"
---
# <a name="the-direct3d-12-core-10-feature-level"></a><span data-ttu-id="23697-103">Direct3D 12 Core 1.0-Featureebene</span><span class="sxs-lookup"><span data-stu-id="23697-103">The Direct3D 12 Core 1.0 Feature Level</span></span>

<span data-ttu-id="23697-104">Die Core 1,0-Featureebene ist eine Teilmenge des vollständigen Direct3D 12-Funktions Satzes.</span><span class="sxs-lookup"><span data-stu-id="23697-104">The Core 1.0 Feature Level is a subset of the full Direct3D 12 feature set.</span></span> <span data-ttu-id="23697-105">Die Funktionsebene "Core 1,0" kann durch eine Kategorie von Geräten verfügbar gemacht werden, die als *nur-Compute-Geräte* bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="23697-105">Core 1.0 Feature Level can be exposed by a category of devices known as *compute-only devices*.</span></span> <span data-ttu-id="23697-106">Das allgemeine Treibermodell für nur-computegeräte ist das Microsoft Compute Driver Model (mcdm).</span><span class="sxs-lookup"><span data-stu-id="23697-106">The overall driver model for compute-only devices is the Microsoft Compute Driver Model (MCDM).</span></span> <span data-ttu-id="23697-107">Mcdm ist ein herunter skalierter Peer des Windows-Gerätetreiber Modells (WDDM), das über einen größeren Bereich verfügt.</span><span class="sxs-lookup"><span data-stu-id="23697-107">MCDM is a scaled-down peer of the Windows Device Driver Model (WDDM), which has a larger scope.</span></span>

<span data-ttu-id="23697-108">Ein Gerät, das *nur* die Features innerhalb einer Kern Funktionsebene unterstützt, wird als *kerngerät* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="23697-108">A device that supports *only* the features within a Core Feature Level is known as a *Core device*.</span></span>

> [!NOTE]
> <span data-ttu-id="23697-109">Das *nur-computegerät*, das *mcdm-Gerät*, das *Core-Geräte Gerät* und das *kerngerät* bedeuten dasselbe.</span><span class="sxs-lookup"><span data-stu-id="23697-109">*Compute-only device*, *MCDM device*, *Core Feature Level device*, and *Core device* all mean the same thing.</span></span> <span data-ttu-id="23697-110">Wir bevorzugen das *kerngerät* zur Vereinfachung.</span><span class="sxs-lookup"><span data-stu-id="23697-110">We'll prefer *Core device* for simplicity.</span></span>

## <a name="creating-a-core-device"></a><span data-ttu-id="23697-111">Erstellen eines kerngeräts</span><span class="sxs-lookup"><span data-stu-id="23697-111">Creating a Core device</span></span>

<span data-ttu-id="23697-112">Um ein Direct3D 12-Gerät zu erstellen, rufen Sie im Allgemeinen die [**D3D12CreateDevice**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createdevice) -Funktion auf, und geben Sie eine minimale Funktionsebene an.</span><span class="sxs-lookup"><span data-stu-id="23697-112">In general, to create a Direct3D 12 device, you call the [**D3D12CreateDevice**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createdevice) function, and specify a minimum feature level.</span></span>

<span data-ttu-id="23697-113">Wenn Sie eine Featureebene von 9 bis 12 angeben, ist das zurückgegebene Gerät ein Funktions Reiches Gerät, wie z. b. eine herkömmliche GPU (die eine übergeordnete Funktion eines kerngeräts unterstützt).</span><span class="sxs-lookup"><span data-stu-id="23697-113">If you specify a feature level of 9 through 12, then the device that's returned is a feature-rich device, such as a traditional GPU (which supports a superset of the functionality of a Core device).</span></span> <span data-ttu-id="23697-114">Für diesen Bereich von featureebenen wird nie ein kerngerät zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="23697-114">A Core device is never returned for that range of feature levels.</span></span>

<span data-ttu-id="23697-115">Wenn Sie jedoch eine Kern Funktionsebene angeben (z. b. [**D3D_FEATURE_LEVEL::D 3D_FEATURE_LEVEL_1_0_CORE**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level)), kann das Gerät, das zurückgegeben wird, funktionsreich sein oder ein kerngerät sein.</span><span class="sxs-lookup"><span data-stu-id="23697-115">On the other hand, if you specify a Core feature level (for example, [**D3D_FEATURE_LEVEL::D3D_FEATURE_LEVEL_1_0_CORE**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level)), then the device that's returned could be feature-rich, or it could be a Core device.</span></span>

```cpp
// d3dcommon.h
D3D_FEATURE_LEVEL_1_0_CORE = 0x1000
```

<span data-ttu-id="23697-116">Wenn Sie eine `_CORE` Featureebene angeben, überprüft die Runtime/Debug-Ebene, ob die von Ihrer Anwendung verwendeten Features von dieser `_CORE` Funktionsebene zugelassen werden.</span><span class="sxs-lookup"><span data-stu-id="23697-116">If you specify a `_CORE` feature level, then the runtime/debug layer validates that the features your application uses are allowed by that `_CORE` feature level.</span></span> <span data-ttu-id="23697-117">Diese Features werden weiter unten in diesem Thema definiert.</span><span class="sxs-lookup"><span data-stu-id="23697-117">That set of features is defined later in this topic.</span></span>

## <a name="shader-model-for-core-devices"></a><span data-ttu-id="23697-118">Shadermodell für kerngeräte</span><span class="sxs-lookup"><span data-stu-id="23697-118">Shader model for Core devices</span></span>

<span data-ttu-id="23697-119">Ein kerngerät unterstützt das Shader-Modell 5.0 und höher.</span><span class="sxs-lookup"><span data-stu-id="23697-119">A Core device supports Shader Model 5.0+.</span></span>

<span data-ttu-id="23697-120">Die Laufzeit führt die Konvertierung von 5. x-nicht-dxil-Shader-Modellen in 6,0 dxil aus.</span><span class="sxs-lookup"><span data-stu-id="23697-120">The runtime performs conversion of 5.x non DXIL shader models to 6.0 DXIL.</span></span> <span data-ttu-id="23697-121">Daher muss der Treiber nur 6. x unterstützen.</span><span class="sxs-lookup"><span data-stu-id="23697-121">So the driver need only support 6.x.</span></span>

## <a name="resource-management-model-for-core-devices"></a><span data-ttu-id="23697-122">Ressourcen Verwaltungsmodell für kerngeräte</span><span class="sxs-lookup"><span data-stu-id="23697-122">Resource management model for Core devices</span></span>

- <span data-ttu-id="23697-123">Unterstützte Ressourcen Dimensionen: nur Roh-und strukturierte Puffer (keine typisierten Puffer, texture1d/2D usw.)</span><span class="sxs-lookup"><span data-stu-id="23697-123">Supported resource dimensions: raw and structured buffers only (no typed buffers, texture1d/2D, etc.)</span></span>
- <span data-ttu-id="23697-124">Keine Unterstützung für reservierte (gekachelte) Ressourcen</span><span class="sxs-lookup"><span data-stu-id="23697-124">No support for reserved (tiled) resources</span></span>
- <span data-ttu-id="23697-125">Keine Unterstützung für benutzerdefinierte Heaps</span><span class="sxs-lookup"><span data-stu-id="23697-125">No support for custom heaps</span></span>
- <span data-ttu-id="23697-126">Keine Unterstützung für die folgenden Heap-Flags:</span><span class="sxs-lookup"><span data-stu-id="23697-126">No support for any of these heap flags:</span></span>
  - <span data-ttu-id="23697-127">D3D12_HEAP_FLAG_HARDWARE_PROTECTED</span><span class="sxs-lookup"><span data-stu-id="23697-127">D3D12_HEAP_FLAG_HARDWARE_PROTECTED</span></span>
  - <span data-ttu-id="23697-128">D3D12_HEAP_FLAG_ALLOW_WRITE_WATCH</span><span class="sxs-lookup"><span data-stu-id="23697-128">D3D12_HEAP_FLAG_ALLOW_WRITE_WATCH</span></span>
  - <span data-ttu-id="23697-129">D3D12_HEAP_FLAG_ALLOW_DISPLAY</span><span class="sxs-lookup"><span data-stu-id="23697-129">D3D12_HEAP_FLAG_ALLOW_DISPLAY</span></span>
  - <span data-ttu-id="23697-130">D3D12_HEAP_FLAG_ALLOW_SHADER_ATOMICS (Notiz der Shader-ATOMICS ist erforderlich, dieses Flag ist für eine andere Funktion, Adapter übergreifende ATOMICS).</span><span class="sxs-lookup"><span data-stu-id="23697-130">D3D12_HEAP_FLAG_ALLOW_SHADER_ATOMICS (note shader atomics are required, this flag is for another feature, cross adapter atomics)</span></span>

## <a name="resource-binding-model-for-core-devices"></a><span data-ttu-id="23697-131">Ressourcen Bindungs Modell für kerngeräte</span><span class="sxs-lookup"><span data-stu-id="23697-131">Resource binding model for Core devices</span></span>

- <span data-ttu-id="23697-132">Nur Unterstützung für Ressourcen Bindungs Ebene 1</span><span class="sxs-lookup"><span data-stu-id="23697-132">Support for resource binding tier 1 only</span></span>
- <span data-ttu-id="23697-133">Ausnahmen:</span><span class="sxs-lookup"><span data-stu-id="23697-133">Exceptions:</span></span>
  - <span data-ttu-id="23697-134">Keine Unterstützung für Textur-Samplern</span><span class="sxs-lookup"><span data-stu-id="23697-134">No support for texture samplers</span></span>
  - <span data-ttu-id="23697-135">Unterstützung für 64-UAVs wie Featureebene 11.1 + (im Gegensatz zu 8)</span><span class="sxs-lookup"><span data-stu-id="23697-135">Support for 64 UAVs like Feature Level 11.1+ (as opposed to only 8)</span></span>
  - <span data-ttu-id="23697-136">Bei Implementierungen ist es nicht erforderlich, die Begrenzungen-Überprüfung für Shader-Zugriffe auf Ressourcen über Deskriptoren zu implementieren</span><span class="sxs-lookup"><span data-stu-id="23697-136">Implementations do not have to implement bounds checking on shader accesses to resources through descriptors, out of bounds accesses produce undefined behavior.</span></span>
    - <span data-ttu-id="23697-137">Als byproduct wird das deskriptorbereichsflag, das in root-Signaturen D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_STATIC_KEEPING_BUFFER_BOUNDS_CHECKS wird, nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="23697-137">As a byproduct, the descriptor range flag D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_STATIC_KEEPING_BUFFER_BOUNDS_CHECKS in root signatures is not supported.</span></span>
- <span data-ttu-id="23697-138">UAV/CBV-Deskriptoren können nur für Ressourcen aus Standard Heaps (also keine Upload-/Back-Heaps) erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="23697-138">UAV/CBV descriptors can only be made on resources from default heaps (so no upload/readback heaps).</span></span> <span data-ttu-id="23697-139">Dadurch wird die Anwendung gezwungen, Kopien durchzuführen, um Daten über CPU-< >GPU zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="23697-139">This forces your application to do copies to get data across CPU<->GPU.</span></span>
- <span data-ttu-id="23697-140">Trotz der niedrigsten Bindungs Funktionsebene sind noch einige Features erforderlich, die auch auf dieser Ebene erforderlich sind, um Folgendes zu sagen:</span><span class="sxs-lookup"><span data-stu-id="23697-140">Despite being the lowest binding capability tier, there are still some features required even in this tier worth calling out:</span></span>
  - <span data-ttu-id="23697-141">Deskriptorheaps können aktualisiert werden, nachdem Befehlslisten aufgezeichnet wurden (siehe D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_VOLATILE in der Spezifikation der Ressourcen Bindung).</span><span class="sxs-lookup"><span data-stu-id="23697-141">Descriptor heaps can be updated after command lists are recorded (see D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_VOLATILE in the resource binding spec)</span></span>
  - <span data-ttu-id="23697-142">Stamm Deskriptoren sind im Grunde gpuva-Zeiger</span><span class="sxs-lookup"><span data-stu-id="23697-142">Root descriptors are basically GPUVA pointers</span></span>
    - <span data-ttu-id="23697-143">Obwohl keine Unterstützung für MMU/VA vorhanden ist, können Puffer-Vas, die in Stamm Deskriptoren verwendet werden, durch-Implementierungen emuliert werden, indem das Adress Patching durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="23697-143">Even though there is no MMU / VA support, buffer VAs that are used in root descriptors can be emulated by implementations by doing address patching.</span></span>

### <a name="structured-buffer-restrictions"></a><span data-ttu-id="23697-144">Einschränkungen für strukturierte Puffer</span><span class="sxs-lookup"><span data-stu-id="23697-144">Structured buffer restrictions</span></span>

<span data-ttu-id="23697-145">Strukturierte Puffer müssen eine Basisadresse aufweisen, die 4 Byte ausgerichtet ist, und STRIDE muss 2 oder ein Vielfaches von 4 sein.</span><span class="sxs-lookup"><span data-stu-id="23697-145">Structured buffers must have a base address that is 4 byte aligned, and stride must be 2 or a multiple of 4.</span></span> <span data-ttu-id="23697-146">Der Fall für einen Schritt von 2 ist für apps mit 16-Bit-Daten, insbesondere, wenn in D3D_FEATURE_LEVEL_1_0_CORE keine Unterstützung für typisierte Puffer vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="23697-146">The case for a stride of 2 is for apps with 16 bit data, particularly given there is no support for typed buffers in D3D_FEATURE_LEVEL_1_0_CORE.</span></span>

<span data-ttu-id="23697-147">Der in den Deskriptoren angegebene Stride muss mit dem in HLSL angegebenen Stride identisch sein.</span><span class="sxs-lookup"><span data-stu-id="23697-147">Stride specified in descriptors must match the stride specified in HLSL.</span></span>  

## <a name="command-queue-support-for-core-devices"></a><span data-ttu-id="23697-148">Unterstützung der Befehls Warteschlange für kerngeräte</span><span class="sxs-lookup"><span data-stu-id="23697-148">Command queue support for Core devices</span></span>

<span data-ttu-id="23697-149">Nur Warteschlangen berechnen und kopieren (keine 3D-, Video-usw.-Warteschlangen).</span><span class="sxs-lookup"><span data-stu-id="23697-149">Compute and copy queues only (no 3D, video, etc. queues).</span></span>

## <a name="shader-support-for-core-devices"></a><span data-ttu-id="23697-150">Shaderunterstützung für kerngeräte</span><span class="sxs-lookup"><span data-stu-id="23697-150">Shader support for Core devices</span></span>

<span data-ttu-id="23697-151">Nur Compute-Shader, keine Grafik-Shader (Vertex, Pixel-Shader usw.) und keine zugehörigen Funktionen, wie z. b. Renderziele, Austausch Ketten, Eingabe Assembler.</span><span class="sxs-lookup"><span data-stu-id="23697-151">Compute shaders only, no graphics shaders (Vertex, Pixel Shaders, etc.) nor any related functionality such as render targets, swap chains, input assembler.</span></span>

### <a name="arithmetic-precision"></a><span data-ttu-id="23697-152">Arithmetische Genauigkeit</span><span class="sxs-lookup"><span data-stu-id="23697-152">Arithmetic precision</span></span>

<span data-ttu-id="23697-153">Kerngeräte müssen denorms für Gleit Komma Vorgänge mit 16 Bit nicht unterstützen.</span><span class="sxs-lookup"><span data-stu-id="23697-153">Core devices do not have to support denorms for 16 bit floating point operations.</span></span>

## <a name="supported-apis-for-core-devices"></a><span data-ttu-id="23697-154">Unterstützte APIs für kerngeräte</span><span class="sxs-lookup"><span data-stu-id="23697-154">Supported APIs for Core devices</span></span>

<span data-ttu-id="23697-155">Die nachstehende Liste zeigt die unterstützte Teilmenge der vollständigen Anwendungsprogrammierschnittstelle (APIs, die *nicht* in der Core 1,0-Funktionsebene unterstützt werden) sind *nicht* aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="23697-155">The list below represents the supported subset of the full application programming interface (APIs that are *not* supported in Core 1.0 Feature Level are *not* listed).</span></span>

### <a name="id3d12device-methods"></a><span data-ttu-id="23697-156">ID3D12Device-Methoden</span><span class="sxs-lookup"><span data-stu-id="23697-156">ID3D12Device methods</span></span>

* [<span data-ttu-id="23697-157">ID3D12Device:: checkfeaturesupport</span><span class="sxs-lookup"><span data-stu-id="23697-157">ID3D12Device::CheckFeatureSupport</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport)
* [<span data-ttu-id="23697-158">ID3D12Device:: copydescriptors</span><span class="sxs-lookup"><span data-stu-id="23697-158">ID3D12Device::CopyDescriptors</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-copydescriptors)
* [<span data-ttu-id="23697-159">ID3D12Device:: copydescriptor ssimple</span><span class="sxs-lookup"><span data-stu-id="23697-159">ID3D12Device::CopyDescriptorsSimple</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple)
* [<span data-ttu-id="23697-160">ID3D12Device:: kreatecommandzuweisung</span><span class="sxs-lookup"><span data-stu-id="23697-160">ID3D12Device::CreateCommandAllocator</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandallocator)
* [<span data-ttu-id="23697-161">ID3D12Device:: kreatecommandlist</span><span class="sxs-lookup"><span data-stu-id="23697-161">ID3D12Device::CreateCommandList</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist)
* [<span data-ttu-id="23697-162">ID3D12Device:: kreatecommandqueue</span><span class="sxs-lookup"><span data-stu-id="23697-162">ID3D12Device::CreateCommandQueue</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandqueue)
* [<span data-ttu-id="23697-163">ID3D12Device:: kreatecommandsignature</span><span class="sxs-lookup"><span data-stu-id="23697-163">ID3D12Device::CreateCommandSignature</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandsignature)
* [<span data-ttu-id="23697-164">ID3D12Device:: kreatecommittedresource</span><span class="sxs-lookup"><span data-stu-id="23697-164">ID3D12Device::CreateCommittedResource</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource)
* [<span data-ttu-id="23697-165">ID3D12Device:: kreatecomputepipelinestate</span><span class="sxs-lookup"><span data-stu-id="23697-165">ID3D12Device::CreateComputePipelineState</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate)
* [<span data-ttu-id="23697-166">ID3D12Device:: kreateconstantbufferview</span><span class="sxs-lookup"><span data-stu-id="23697-166">ID3D12Device::CreateConstantBufferView</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createconstantbufferview)
* [<span data-ttu-id="23697-167">ID3D12Device:: kreatedescriptorheap</span><span class="sxs-lookup"><span data-stu-id="23697-167">ID3D12Device::CreateDescriptorHeap</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createdescriptorheap)
* [<span data-ttu-id="23697-168">ID3D12Device:: kreatefence</span><span class="sxs-lookup"><span data-stu-id="23697-168">ID3D12Device::CreateFence</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createfence)
* [<span data-ttu-id="23697-169">ID3D12Device:: kreateheap</span><span class="sxs-lookup"><span data-stu-id="23697-169">ID3D12Device::CreateHeap</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createheap)
* [<span data-ttu-id="23697-170">ID3D12Device:: kreateplacedresource</span><span class="sxs-lookup"><span data-stu-id="23697-170">ID3D12Device::CreatePlacedResource</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createplacedresource)
* [<span data-ttu-id="23697-171">ID3D12Device:: kreatequeryheap</span><span class="sxs-lookup"><span data-stu-id="23697-171">ID3D12Device::CreateQueryHeap</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createqueryheap)
* [<span data-ttu-id="23697-172">ID3D12Device:: kreaterootsignature</span><span class="sxs-lookup"><span data-stu-id="23697-172">ID3D12Device::CreateRootSignature</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrootsignature)
* [<span data-ttu-id="23697-173">ID3D12Device:: kreateshaderresourceview</span><span class="sxs-lookup"><span data-stu-id="23697-173">ID3D12Device::CreateShaderResourceView</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview)
* [<span data-ttu-id="23697-174">ID3D12Device:: kreatesharedhandle</span><span class="sxs-lookup"><span data-stu-id="23697-174">ID3D12Device::CreateSharedHandle</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createsharedhandle)
* [<span data-ttu-id="23697-175">ID3D12Device:: kreateunorderedaccessview</span><span class="sxs-lookup"><span data-stu-id="23697-175">ID3D12Device::CreateUnorderedAccessView</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview)
* [<span data-ttu-id="23697-176">ID3D12Device:: entferct</span><span class="sxs-lookup"><span data-stu-id="23697-176">ID3D12Device::Evict</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-evict)
* [<span data-ttu-id="23697-177">ID3D12Device:: getadapterluid</span><span class="sxs-lookup"><span data-stu-id="23697-177">ID3D12Device::GetAdapterLuid</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getadapterluid)
* [<span data-ttu-id="23697-178">ID3D12Device:: getcopyablefootprints</span><span class="sxs-lookup"><span data-stu-id="23697-178">ID3D12Device::GetCopyableFootprints</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints)
* [<span data-ttu-id="23697-179">ID3D12Device:: getcustomheapproperties</span><span class="sxs-lookup"><span data-stu-id="23697-179">ID3D12Device::GetCustomHeapProperties</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getcustomheapproperties)
* [<span data-ttu-id="23697-180">ID3D12Device:: getDescriptor handleinkrementsize</span><span class="sxs-lookup"><span data-stu-id="23697-180">ID3D12Device::GetDescriptorHandleIncrementSize</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize)
* [<span data-ttu-id="23697-181">ID3D12Device:: getdeviceremovedreason</span><span class="sxs-lookup"><span data-stu-id="23697-181">ID3D12Device::GetDeviceRemovedReason</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getdeviceremovedreason)
* [<span data-ttu-id="23697-182">ID3D12Device:: getnoentcount</span><span class="sxs-lookup"><span data-stu-id="23697-182">ID3D12Device::GetNodeCount</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getnodecount)
* [<span data-ttu-id="23697-183">ID3D12Device:: getresourcezucationinfo</span><span class="sxs-lookup"><span data-stu-id="23697-183">ID3D12Device::GetResourceAllocationInfo</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getresourceallocationinfo)
* [<span data-ttu-id="23697-184">ID3D12Device:: makeresident</span><span class="sxs-lookup"><span data-stu-id="23697-184">ID3D12Device::MakeResident</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-makeresident)
* [<span data-ttu-id="23697-185">ID3D12Device:: opensharedhandle</span><span class="sxs-lookup"><span data-stu-id="23697-185">ID3D12Device::OpenSharedHandle</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-opensharedhandle)
* [<span data-ttu-id="23697-186">ID3D12Device:: opensharedlenker byname</span><span class="sxs-lookup"><span data-stu-id="23697-186">ID3D12Device::OpenSharedHandleByName</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-opensharedhandlebyname)
* [<span data-ttu-id="23697-187">ID3D12Device:: setstablepowerstate</span><span class="sxs-lookup"><span data-stu-id="23697-187">ID3D12Device::SetStablePowerState</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-setstablepowerstate)

### <a name="id3d12device1-methods"></a><span data-ttu-id="23697-188">ID3D12Device1-Methoden</span><span class="sxs-lookup"><span data-stu-id="23697-188">ID3D12Device1 methods</span></span>

* [<span data-ttu-id="23697-189">ID3D12Device1:: kreatepipelinelibrary</span><span class="sxs-lookup"><span data-stu-id="23697-189">ID3D12Device1::CreatePipelineLibrary</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device1-createpipelinelibrary)
* [<span data-ttu-id="23697-190">ID3D12Device1:: ab.</span><span class="sxs-lookup"><span data-stu-id="23697-190">ID3D12Device1::SetEventOnMultipleFenceCompletion</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device1-seteventonmultiplefencecompletion)
* [<span data-ttu-id="23697-191">ID3D12Device1:: "abtresidencymenteventonmultiplefencecompletionpriority"</span><span class="sxs-lookup"><span data-stu-id="23697-191">ID3D12Device1::SetResidencySetEventOnMultipleFenceCompletionPriority</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device1-setresidencypriority)

### <a name="id3d12device2-methods"></a><span data-ttu-id="23697-192">ID3D12Device2-Methoden</span><span class="sxs-lookup"><span data-stu-id="23697-192">ID3D12Device2 methods</span></span>

* [<span data-ttu-id="23697-193">ID3D12Device2:: kreatepipelinestate</span><span class="sxs-lookup"><span data-stu-id="23697-193">ID3D12Device2::CreatePipelineState</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device2-createpipelinestate)

### <a name="id3d12device3-methods"></a><span data-ttu-id="23697-194">ID3D12Device3-Methoden</span><span class="sxs-lookup"><span data-stu-id="23697-194">ID3D12Device3 methods</span></span>

* [<span data-ttu-id="23697-195">ID3D12Device3:: openexistingheapfromaddress</span><span class="sxs-lookup"><span data-stu-id="23697-195">ID3D12Device3::OpenExistingHeapFromAddress</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device3-openexistingheapfromaddress)
* <span data-ttu-id="23697-196">[ID3D12Device3:: openexistingheapfromfilemapping](/previous-versions/windows/desktop/legacy/mt813613(v%3Dvs.85))</span><span class="sxs-lookup"><span data-stu-id="23697-196">[ID3D12Device3::OpenExistingHeapFromFileMapping](/previous-versions/windows/desktop/legacy/mt813613(v%3Dvs.85))</span></span>
* [<span data-ttu-id="23697-197">ID3D12Device3:: einqueuemakeresident</span><span class="sxs-lookup"><span data-stu-id="23697-197">ID3D12Device3::EnqueueMakeResident</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device3-enqueuemakeresident)

### <a name="id3d12device4-methods"></a><span data-ttu-id="23697-198">ID3D12Device4-Methoden</span><span class="sxs-lookup"><span data-stu-id="23697-198">ID3D12Device4 methods</span></span>

* [<span data-ttu-id="23697-199">ID3D12Device4::GetResourceAllocationInfo1</span><span class="sxs-lookup"><span data-stu-id="23697-199">ID3D12Device4::GetResourceAllocationInfo1</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device4-getresourceallocationinfo1)

### <a name="id3d12device5-methods"></a><span data-ttu-id="23697-200">ID3D12Device5-Methoden</span><span class="sxs-lookup"><span data-stu-id="23697-200">ID3D12Device5 methods</span></span>

* [<span data-ttu-id="23697-201">ID3D12Device5:: kreatemetacommand</span><span class="sxs-lookup"><span data-stu-id="23697-201">ID3D12Device5::CreateMetaCommand</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-createmetacommand)
* [<span data-ttu-id="23697-202">ID3D12Device5:: kreatestateobject</span><span class="sxs-lookup"><span data-stu-id="23697-202">ID3D12Device5::CreateStateObject</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-createstateobject)
* [<span data-ttu-id="23697-203">ID3D12Device5:: enumeratemetacommandparameters</span><span class="sxs-lookup"><span data-stu-id="23697-203">ID3D12Device5::EnumerateMetaCommandParameters</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-enumeratemetacommandparameters)
* [<span data-ttu-id="23697-204">ID3D12Device5:: enumeratemetacommands</span><span class="sxs-lookup"><span data-stu-id="23697-204">ID3D12Device5::EnumerateMetaCommands</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-enumeratemetacommands)
* [<span data-ttu-id="23697-205">ID3D12Device5:: removedevice</span><span class="sxs-lookup"><span data-stu-id="23697-205">ID3D12Device5::RemoveDevice</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-removedevice)

### <a name="id3d12commandqueue-methods"></a><span data-ttu-id="23697-206">ID3D12CommandQueue-Methoden</span><span class="sxs-lookup"><span data-stu-id="23697-206">ID3D12CommandQueue methods</span></span>

* [<span data-ttu-id="23697-207">ID3D12CommandQueue:: beginevent</span><span class="sxs-lookup"><span data-stu-id="23697-207">ID3D12CommandQueue::BeginEvent</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-beginevent)
* [<span data-ttu-id="23697-208">ID3D12CommandQueue:: endevent</span><span class="sxs-lookup"><span data-stu-id="23697-208">ID3D12CommandQueue::EndEvent</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-endevent)
* [<span data-ttu-id="23697-209">ID3D12CommandQueue:: executecommandlists</span><span class="sxs-lookup"><span data-stu-id="23697-209">ID3D12CommandQueue::ExecuteCommandLists</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists)
* [<span data-ttu-id="23697-210">ID3D12CommandQueue:: getclockkalibrierung</span><span class="sxs-lookup"><span data-stu-id="23697-210">ID3D12CommandQueue::GetClockCalibration</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration)
* [<span data-ttu-id="23697-211">ID3D12CommandQueue:: getdebug</span><span class="sxs-lookup"><span data-stu-id="23697-211">ID3D12CommandQueue::GetDesc</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-getdesc)
* [<span data-ttu-id="23697-212">ID3D12CommandQueue:: gettimestampfrequency</span><span class="sxs-lookup"><span data-stu-id="23697-212">ID3D12CommandQueue::GetTimestampFrequency</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-gettimestampfrequency)
* [<span data-ttu-id="23697-213">ID3D12CommandQueue:: setmarker</span><span class="sxs-lookup"><span data-stu-id="23697-213">ID3D12CommandQueue::SetMarker</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-setmarker)
* [<span data-ttu-id="23697-214">ID3D12CommandQueue:: Signal</span><span class="sxs-lookup"><span data-stu-id="23697-214">ID3D12CommandQueue::Signal</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal)
* [<span data-ttu-id="23697-215">ID3D12CommandQueue:: Wait</span><span class="sxs-lookup"><span data-stu-id="23697-215">ID3D12CommandQueue::Wait</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-wait)

### <a name="id3d12commandlist-methods"></a><span data-ttu-id="23697-216">ID3D12CommandList-Methoden</span><span class="sxs-lookup"><span data-stu-id="23697-216">ID3D12CommandList methods</span></span>

* [<span data-ttu-id="23697-217">ID3D12CommandList:: GetType</span><span class="sxs-lookup"><span data-stu-id="23697-217">ID3D12CommandList::GetType</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandlist-gettype)

### <a name="id3d12graphicscommandlist-methods"></a><span data-ttu-id="23697-218">ID3D12GraphicsCommandList-Methoden</span><span class="sxs-lookup"><span data-stu-id="23697-218">ID3D12GraphicsCommandList methods</span></span>

* [<span data-ttu-id="23697-219">ID3D12GraphicsCommandList:: beginevent</span><span class="sxs-lookup"><span data-stu-id="23697-219">ID3D12GraphicsCommandList::BeginEvent</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginevent)
* [<span data-ttu-id="23697-220">ID3D12GraphicsCommandList:: beginquery</span><span class="sxs-lookup"><span data-stu-id="23697-220">ID3D12GraphicsCommandList::BeginQuery</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery)
* [<span data-ttu-id="23697-221">ID3D12GraphicsCommandList:: clearstate</span><span class="sxs-lookup"><span data-stu-id="23697-221">ID3D12GraphicsCommandList::ClearState</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearstate)
* [<span data-ttu-id="23697-222">ID3D12GraphicsCommandList:: clearunorderedaccessviewfloat</span><span class="sxs-lookup"><span data-stu-id="23697-222">ID3D12GraphicsCommandList::ClearUnorderedAccessViewFloat</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewfloat)
* [<span data-ttu-id="23697-223">ID3D12GraphicsCommandList:: clearunorderedaccessviewuint</span><span class="sxs-lookup"><span data-stu-id="23697-223">ID3D12GraphicsCommandList::ClearUnorderedAccessViewUint</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewuint)
* [<span data-ttu-id="23697-224">ID3D12GraphicsCommandList:: Close</span><span class="sxs-lookup"><span data-stu-id="23697-224">ID3D12GraphicsCommandList::Close</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close)
* [<span data-ttu-id="23697-225">ID3D12GraphicsCommandList:: copybufferregion</span><span class="sxs-lookup"><span data-stu-id="23697-225">ID3D12GraphicsCommandList::CopyBufferRegion</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)
* [<span data-ttu-id="23697-226">ID3D12GraphicsCommandList:: copyresource</span><span class="sxs-lookup"><span data-stu-id="23697-226">ID3D12GraphicsCommandList::CopyResource</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)
* [<span data-ttu-id="23697-227">ID3D12GraphicsCommandList:: copytextureregion</span><span class="sxs-lookup"><span data-stu-id="23697-227">ID3D12GraphicsCommandList::CopyTextureRegion</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)
* [<span data-ttu-id="23697-228">ID3D12GraphicsCommandList::D ispatch</span><span class="sxs-lookup"><span data-stu-id="23697-228">ID3D12GraphicsCommandList::Dispatch</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)
* [<span data-ttu-id="23697-229">ID3D12GraphicsCommandList:: endevent</span><span class="sxs-lookup"><span data-stu-id="23697-229">ID3D12GraphicsCommandList::EndEvent</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endevent)
* [<span data-ttu-id="23697-230">ID3D12GraphicsCommandList:: endquery</span><span class="sxs-lookup"><span data-stu-id="23697-230">ID3D12GraphicsCommandList::EndQuery</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery)
* [<span data-ttu-id="23697-231">ID3D12GraphicsCommandList:: Reset</span><span class="sxs-lookup"><span data-stu-id="23697-231">ID3D12GraphicsCommandList::Reset</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset)
* [<span data-ttu-id="23697-232">ID3D12GraphicsCommandList:: resolvequerydata</span><span class="sxs-lookup"><span data-stu-id="23697-232">ID3D12GraphicsCommandList::ResolveQueryData</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata)
* [<span data-ttu-id="23697-233">ID3D12GraphicsCommandList:: resourcebarrier</span><span class="sxs-lookup"><span data-stu-id="23697-233">ID3D12GraphicsCommandList::ResourceBarrier</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)
* [<span data-ttu-id="23697-234">ID3D12GraphicsCommandList::SetComputeRoot32BitConstant</span><span class="sxs-lookup"><span data-stu-id="23697-234">ID3D12GraphicsCommandList::SetComputeRoot32BitConstant</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstant)
* [<span data-ttu-id="23697-235">ID3D12GraphicsCommandList::SetComputeRoot32BitConstants</span><span class="sxs-lookup"><span data-stu-id="23697-235">ID3D12GraphicsCommandList::SetComputeRoot32BitConstants</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstants)
* [<span data-ttu-id="23697-236">ID3D12GraphicsCommandList:: setcomputerootconstantbufferview</span><span class="sxs-lookup"><span data-stu-id="23697-236">ID3D12GraphicsCommandList::SetComputeRootConstantBufferView</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootconstantbufferview)
* [<span data-ttu-id="23697-237">ID3D12GraphicsCommandList:: setcomputerootdescriptor Table</span><span class="sxs-lookup"><span data-stu-id="23697-237">ID3D12GraphicsCommandList::SetComputeRootDescriptorTable</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable)
* [<span data-ttu-id="23697-238">ID3D12GraphicsCommandList:: setcomputerootshaderresourceview</span><span class="sxs-lookup"><span data-stu-id="23697-238">ID3D12GraphicsCommandList::SetComputeRootShaderResourceView</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootshaderresourceview)
* [<span data-ttu-id="23697-239">ID3D12GraphicsCommandList:: setcomputerootsignature</span><span class="sxs-lookup"><span data-stu-id="23697-239">ID3D12GraphicsCommandList::SetComputeRootSignature</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootsignature)
* [<span data-ttu-id="23697-240">ID3D12GraphicsCommandList:: setcomputerootunorderedaccessview</span><span class="sxs-lookup"><span data-stu-id="23697-240">ID3D12GraphicsCommandList::SetComputeRootUnorderedAccessView</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootunorderedaccessview)
* [<span data-ttu-id="23697-241">ID3D12GraphicsCommandList:: setdescriptorheaps</span><span class="sxs-lookup"><span data-stu-id="23697-241">ID3D12GraphicsCommandList::SetDescriptorHeaps</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps)
* [<span data-ttu-id="23697-242">ID3D12GraphicsCommandList:: setmarker</span><span class="sxs-lookup"><span data-stu-id="23697-242">ID3D12GraphicsCommandList::SetMarker</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setmarker)
* [<span data-ttu-id="23697-243">ID3D12GraphicsCommandList:: setpipelinestate</span><span class="sxs-lookup"><span data-stu-id="23697-243">ID3D12GraphicsCommandList::SetPipelineState</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate)
* [<span data-ttu-id="23697-244">ID3D12GraphicsCommandList:: setprediation</span><span class="sxs-lookup"><span data-stu-id="23697-244">ID3D12GraphicsCommandList::SetPredication</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication)

### <a name="id3d12graphicscommandlist1-methods"></a><span data-ttu-id="23697-245">ID3D12GraphicsCommandList1-Methoden</span><span class="sxs-lookup"><span data-stu-id="23697-245">ID3D12GraphicsCommandList1 methods</span></span>

* [<span data-ttu-id="23697-246">ID3D12GraphicsCommandList1:: atomiccopybufferuint</span><span class="sxs-lookup"><span data-stu-id="23697-246">ID3D12GraphicsCommandList1::AtomicCopyBufferUINT</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-atomiccopybufferuint)
* [<span data-ttu-id="23697-247">ID3D12GraphicsCommandList1::AtomicCopyBufferUINT64</span><span class="sxs-lookup"><span data-stu-id="23697-247">ID3D12GraphicsCommandList1::AtomicCopyBufferUINT64</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-atomiccopybufferuint64)

### <a name="id3d12graphicscommandlist2-methods"></a><span data-ttu-id="23697-248">ID3D12GraphicsCommandList2-Methoden</span><span class="sxs-lookup"><span data-stu-id="23697-248">ID3D12GraphicsCommandList2 methods</span></span>

* [<span data-ttu-id="23697-249">ID3D12GraphicsCommandList2:: Write-bufferimmediate</span><span class="sxs-lookup"><span data-stu-id="23697-249">ID3D12GraphicsCommandList2::WriteBufferImmediate</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist2-writebufferimmediate)

### <a name="id3d12graphicscommandlist4-methods"></a><span data-ttu-id="23697-250">ID3D12GraphicsCommandList4-Methoden</span><span class="sxs-lookup"><span data-stu-id="23697-250">ID3D12GraphicsCommandList4 methods</span></span>

* [<span data-ttu-id="23697-251">ID3D12GraphicsCommandList4:: executemetacommand</span><span class="sxs-lookup"><span data-stu-id="23697-251">ID3D12GraphicsCommandList4::ExecuteMetaCommand</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-executemetacommand)
* [<span data-ttu-id="23697-252">ID3D12GraphicsCommandList4:: initializemetacommand</span><span class="sxs-lookup"><span data-stu-id="23697-252">ID3D12GraphicsCommandList4::InitializeMetaCommand</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-initializemetacommand)
