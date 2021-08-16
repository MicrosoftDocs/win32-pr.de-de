---
title: Direct3D 12 Core 1.0-Featureebene
description: Die Core 1.0-Featureebene ist eine Teilmenge des vollständigen Direct3D 12-Featuresatzes.
ms.topic: article
ms.date: 11/05/2019
ms.openlocfilehash: 93eab39509074114bf2032cfb1cdea3e4e767dae9786241a34f970ca5cd51703
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118530720"
---
# <a name="the-direct3d-12-core-10-feature-level"></a>Direct3D 12 Core 1.0-Featureebene

Die Core 1.0-Featureebene ist eine Teilmenge des vollständigen Direct3D 12-Featuresatzes. Die Core 1.0-Featureebene kann durch eine Kategorie von Geräten verfügbar gemacht werden, die als *rein computebasierte Geräte* bezeichnet werden. Das allgemeine Treibermodell für Computer, die nur computebasierte Geräte sind, ist das Microsoft Compute Driver Model (MCDM). MCDM ist ein herunterskaliertes Peer des Windows Device Driver Model (WDDM), das über einen größeren Bereich verfügt.

Ein Gerät, das *nur* die Features innerhalb einer Kernfunktionsebene unterstützt, wird als *Core-Gerät* bezeichnet.

> [!NOTE]
> *Nur Computegerät,* *MCDM-Gerät,* *Core Feature Level-Gerät* und *Core-Gerät* bedeuten das gleiche. Der Einfachheit halber wird das *Core-Gerät* bevorzugt.

## <a name="creating-a-core-device"></a>Erstellen eines Core-Geräts

Im Allgemeinen rufen Sie zum Erstellen eines Direct3D 12-Geräts die [**Funktion D3D12CreateDevice**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createdevice) auf und geben eine Mindestfunktionsebene an.

Wenn Sie eine Featureebene von 9 bis 12 angeben, ist das zurückgegebene Gerät ein funktionsreiches Gerät, z. B. eine herkömmliche GPU (die eine Obermenge der Funktionalität eines Core-Geräts unterstützt). Ein Core-Gerät wird für diesen Bereich von Featureebenen nie zurückgegeben.

Wenn Sie andererseits eine Core-Featureebene angeben (z. B. [**D3D_FEATURE_LEVEL::D 3D_FEATURE_LEVEL_1_0_CORE),**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level)kann das zurückgegebene Gerät funktionsreich oder ein Core-Gerät sein.

```cpp
// d3dcommon.h
D3D_FEATURE_LEVEL_1_0_CORE = 0x1000
```

Wenn Sie eine `_CORE` Featureebene angeben, überprüft die Laufzeit-/Debugebene, ob die von Ihrer Anwendung verwendeten Features von dieser Featureebene zugelassen `_CORE` werden. Dieser Satz von Features wird weiter unten in diesem Thema definiert.

## <a name="shader-model-for-core-devices"></a>Shadermodell für Core-Geräte

Ein Core-Gerät unterstützt shader Model 5.0 oder mehr.

Die Runtime führt die Konvertierung von 5.x-Nicht-DXIL-Shadermodellen in 6.0 DXIL durch. Daher muss der Treiber nur 6.x unterstützen.

## <a name="resource-management-model-for-core-devices"></a>Ressourcenverwaltungsmodell für Core-Geräte

- Unterstützte Ressourcendimensionen: nur rohe und strukturierte Puffer (keine typisierten Puffer, texture1d/2D usw.)
- Keine Unterstützung für reservierte (gekachelte) Ressourcen
- Keine Unterstützung für benutzerdefinierte Heaps
- Keine Unterstützung für diese Heapflags:
  - D3D12_HEAP_FLAG_HARDWARE_PROTECTED
  - D3D12_HEAP_FLAG_ALLOW_WRITE_WATCH
  - D3D12_HEAP_FLAG_ALLOW_DISPLAY
  - D3D12_HEAP_FLAG_ALLOW_SHADER_ATOMICS (beachten Sie, dass Shader-Atomaren erforderlich sind, ist dieses Flag für ein anderes Feature, adapterübergreifende Atomaren)

## <a name="resource-binding-model-for-core-devices"></a>Ressourcenbindungsmodell für Core-Geräte

- Unterstützung nur für Ressourcenbindungsebene 1
- Ausnahmen:
  - Keine Unterstützung für Textur-Sampler
  - Unterstützung für 64 UAVs wie Featureebene 11.1 und mehr (im Gegensatz zu nur 8)
  - Implementierungen müssen keine Begrenzungen implementieren, die bei Shaderzugriffen auf Ressourcen über Deskriptoren überprüft werden. Zugriffe außerhalb der Grenzen führen zu undefiniertem Verhalten.
    - Als Nebenprodukt wird das Deskriptorbereichsflag D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_STATIC_KEEPING_BUFFER_BOUNDS_CHECKS in Stammsignaturen nicht unterstützt.
- UAV-/CBV-Deskriptoren können nur für Ressourcen aus Standardheaps erstellt werden (also keine Upload-/Rückschreibeheaps). Dadurch wird ihre Anwendung gezwungen, Kopien durchzuführen, um Daten über CPU-<->GPU abzurufen.
- Obwohl es sich um die niedrigste Bindungsfunktionenebene handelt, sind auch in dieser Ebene noch einige Features erforderlich, die es wert sind, aufzurufen:
  - Deskriptorheaps können aktualisiert werden, nachdem Befehlslisten aufgezeichnet wurden (siehe D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_VOLATILE in der Ressourcenbindungsspezifikation).
  - Stammdeskriptoren sind im Grunde GPUVA-Zeiger.
    - Obwohl keine MMU-/VA-Unterstützung vorhanden ist, können Puffer-VAs, die in Stammdeskriptoren verwendet werden, durch Implementierungen durch Adresspatches emuliert werden.

### <a name="structured-buffer-restrictions"></a>Einschränkungen für strukturierte Puffer

Strukturierte Puffer müssen über eine Basisadresse verfügen, die auf 4 Byte ausgerichtet ist, und stride muss 2 oder ein Vielfaches von 4 sein. Der Fall für einen Schritt von 2 gilt für Apps mit 16-Bit-Daten, insbesondere wenn typisierte Puffer in D3D_FEATURE_LEVEL_1_0_CORE nicht unterstützt werden.

Die in Deskriptoren angegebene Stride muss mit dem in HLSL angegebenen Schritt übereinstimmen.  

## <a name="command-queue-support-for-core-devices"></a>Unterstützung von Befehlswarteschlangen für Core-Geräte

Nur Compute- und Kopierwarteschlangen (keine 3D-, Video- usw. Warteschlangen).

## <a name="shader-support-for-core-devices"></a>Shaderunterstützung für Core-Geräte

Nur Compute-Shader, keine Grafik-Shader (Scheitelpunkt, Pixel-Shader usw.) oder verwandte Funktionen wie Renderziele, Austauschketten, Eingabeassemblierer.

### <a name="arithmetic-precision"></a>Arithmetische Genauigkeit

Kerngeräte müssen keine Denormen für 16-Bit-Gleitkommavorgänge unterstützen.

## <a name="supported-apis-for-core-devices"></a>Unterstützte APIs für Core-Geräte

Die folgende Liste stellt die unterstützte Teilmenge der vollständigen Anwendungsprogrammierschnittstelle dar (APIs, die in Core 1.0 Feature Level *nicht* unterstützt werden, sind *nicht* aufgeführt).

### <a name="id3d12device-methods"></a>ID3D12Device-Methoden

* [ID3D12Device::CheckFeatureSupport](/windows/win32/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport)
* [ID3D12Device::CopyDescriptors](/windows/win32/api/d3d12/nf-d3d12-id3d12device-copydescriptors)
* [ID3D12Device::CopyDescriptorsSimple](/windows/win32/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple)
* [ID3D12Device::CreateCommandAllocator](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandallocator)
* [ID3D12Device::CreateCommandList](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist)
* [ID3D12Device::CreateCommandQueue](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandqueue)
* [ID3D12Device::CreateCommandSignature](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandsignature)
* [ID3D12Device::CreateCommittedResource](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource)
* [ID3D12Device::CreateComputePipelineState](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate)
* [ID3D12Device::CreateConstantBufferView](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createconstantbufferview)
* [ID3D12Device::CreateDescriptorHeap](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createdescriptorheap)
* [ID3D12Device::CreateFence](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createfence)
* [ID3D12Device::CreateHeap](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createheap)
* [ID3D12Device::CreatePlacedResource](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createplacedresource)
* [ID3D12Device::CreateQueryHeap](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createqueryheap)
* [ID3D12Device::CreateRootSignature](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrootsignature)
* [ID3D12Device::CreateShaderResourceView](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview)
* [ID3D12Device::CreateSharedHandle](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createsharedhandle)
* [ID3D12Device::CreateUnorderedAccessView](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview)
* [ID3D12Device::Evict](/windows/win32/api/d3d12/nf-d3d12-id3d12device-evict)
* [ID3D12Device::GetAdapterLuid](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getadapterluid)
* [ID3D12Device::GetCopyableFootprints](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints)
* [ID3D12Device::GetCustomHeapProperties](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getcustomheapproperties)
* [ID3D12Device::GetDescriptorHandleIncrementSize](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize)
* [ID3D12Device::GetDeviceRemovedReason](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getdeviceremovedreason)
* [ID3D12Device::GetNodeCount](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getnodecount)
* [ID3D12Device::GetResourceAllocationInfo](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getresourceallocationinfo)
* [ID3D12Device::MakeResident](/windows/win32/api/d3d12/nf-d3d12-id3d12device-makeresident)
* [ID3D12Device::OpenSharedHandle](/windows/win32/api/d3d12/nf-d3d12-id3d12device-opensharedhandle)
* [ID3D12Device::OpenSharedHandleByName](/windows/win32/api/d3d12/nf-d3d12-id3d12device-opensharedhandlebyname)
* [ID3D12Device::SetStablePowerState](/windows/win32/api/d3d12/nf-d3d12-id3d12device-setstablepowerstate)

### <a name="id3d12device1-methods"></a>ID3D12Device1-Methoden

* [ID3D12Device1::CreatePipelineLibrary](/windows/win32/api/d3d12/nf-d3d12-id3d12device1-createpipelinelibrary)
* [ID3D12Device1::SetEventOnMultipleFenceCompletion](/windows/win32/api/d3d12/nf-d3d12-id3d12device1-seteventonmultiplefencecompletion)
* [ID3D12Device1::SetResidencySetEventOnMultipleFenceCompletionPriority](/windows/win32/api/d3d12/nf-d3d12-id3d12device1-setresidencypriority)

### <a name="id3d12device2-methods"></a>ID3D12Device2-Methoden

* [ID3D12Device2::CreatePipelineState](/windows/win32/api/d3d12/nf-d3d12-id3d12device2-createpipelinestate)

### <a name="id3d12device3-methods"></a>ID3D12Device3-Methoden

* [ID3D12Device3::OpenExistingHeapFromAddress](/windows/win32/api/d3d12/nf-d3d12-id3d12device3-openexistingheapfromaddress)
* [ID3D12Device3::OpenExistingHeapFromFileMapping](/previous-versions/windows/desktop/legacy/mt813613(v%3Dvs.85))
* [ID3D12Device3::EnqueueMakeResident](/windows/win32/api/d3d12/nf-d3d12-id3d12device3-enqueuemakeresident)

### <a name="id3d12device4-methods"></a>ID3D12Device4-Methoden

* [ID3D12Device4::GetResourceAllocationInfo1](/windows/win32/api/d3d12/nf-d3d12-id3d12device4-getresourceallocationinfo1)

### <a name="id3d12device5-methods"></a>ID3D12Device5-Methoden

* [ID3D12Device5::CreateMetaCommand](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-createmetacommand)
* [ID3D12Device5::CreateStateObject](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-createstateobject)
* [ID3D12Device5::EnumerateMetaCommandParameters](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-enumeratemetacommandparameters)
* [ID3D12Device5::EnumerateMetaCommands](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-enumeratemetacommands)
* [ID3D12Device5::RemoveDevice](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-removedevice)

### <a name="id3d12commandqueue-methods"></a>ID3D12CommandQueue-Methoden

* [ID3D12CommandQueue::BeginEvent](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-beginevent)
* [ID3D12CommandQueue::EndEvent](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-endevent)
* [ID3D12CommandQueue::ExecuteCommandLists](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists)
* [ID3D12CommandQueue::GetClockCalibration](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration)
* [ID3D12CommandQueue::GetDesc](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-getdesc)
* [ID3D12CommandQueue::GetTimestampFrequency](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-gettimestampfrequency)
* [ID3D12CommandQueue::SetMarker](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-setmarker)
* [ID3D12CommandQueue::Signal](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal)
* [ID3D12CommandQueue::Wait](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-wait)

### <a name="id3d12commandlist-methods"></a>ID3D12CommandList-Methoden

* [ID3D12CommandList::GetType](/windows/win32/api/d3d12/nf-d3d12-id3d12commandlist-gettype)

### <a name="id3d12graphicscommandlist-methods"></a>ID3D12GraphicsCommandList-Methoden

* [ID3D12GraphicsCommandList::BeginEvent](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginevent)
* [ID3D12GraphicsCommandList::BeginQuery](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery)
* [ID3D12GraphicsCommandList::ClearState](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearstate)
* [ID3D12GraphicsCommandList::ClearUnorderedAccessViewFloat](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewfloat)
* [ID3D12GraphicsCommandList::ClearUnorderedAccessViewUint](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewuint)
* [ID3D12GraphicsCommandList::Close](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close)
* [ID3D12GraphicsCommandList::CopyBufferRegion](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)
* [ID3D12GraphicsCommandList::CopyResource](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)
* [ID3D12GraphicsCommandList::CopyTextureRegion](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)
* [ID3D12GraphicsCommandList::D ispatch](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)
* [ID3D12GraphicsCommandList::EndEvent](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endevent)
* [ID3D12GraphicsCommandList::EndQuery](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery)
* [ID3D12GraphicsCommandList::Reset](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset)
* [ID3D12GraphicsCommandList::ResolveQueryData](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata)
* [ID3D12GraphicsCommandList::ResourceBarrier](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)
* [ID3D12GraphicsCommandList::SetComputeRoot32BitConstant](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstant)
* [ID3D12GraphicsCommandList::SetComputeRoot32BitConstants](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstants)
* [ID3D12GraphicsCommandList::SetComputeRootConstantBufferView](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootconstantbufferview)
* [ID3D12GraphicsCommandList::SetComputeRootDescriptorTable](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable)
* [ID3D12GraphicsCommandList::SetComputeRootShaderResourceView](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootshaderresourceview)
* [ID3D12GraphicsCommandList::SetComputeRootSignature](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootsignature)
* [ID3D12GraphicsCommandList::SetComputeRootUnorderedAccessView](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootunorderedaccessview)
* [ID3D12GraphicsCommandList::SetDescriptorHeaps](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps)
* [ID3D12GraphicsCommandList::SetMarker](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setmarker)
* [ID3D12GraphicsCommandList::SetPipelineState](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate)
* [ID3D12GraphicsCommandList::SetPredication](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication)

### <a name="id3d12graphicscommandlist1-methods"></a>ID3D12GraphicsCommandList1-Methoden

* [ID3D12GraphicsCommandList1::AtomicCopyBufferUINT](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-atomiccopybufferuint)
* [ID3D12GraphicsCommandList1::AtomicCopyBufferUINT64](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-atomiccopybufferuint64)

### <a name="id3d12graphicscommandlist2-methods"></a>ID3D12GraphicsCommandList2-Methoden

* [ID3D12GraphicsCommandList2::WriteBufferImmediate](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist2-writebufferimmediate)

### <a name="id3d12graphicscommandlist4-methods"></a>ID3D12GraphicsCommandList4-Methoden

* [ID3D12GraphicsCommandList4::ExecuteMetaCommand](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-executemetacommand)
* [ID3D12GraphicsCommandList4::InitializeMetaCommand](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-initializemetacommand)
