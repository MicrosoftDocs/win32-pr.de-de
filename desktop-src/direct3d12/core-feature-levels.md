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
# <a name="the-direct3d-12-core-10-feature-level"></a>Direct3D 12 Core 1.0-Featureebene

Die Core 1,0-Featureebene ist eine Teilmenge des vollständigen Direct3D 12-Funktions Satzes. Die Funktionsebene "Core 1,0" kann durch eine Kategorie von Geräten verfügbar gemacht werden, die als *nur-Compute-Geräte* bezeichnet werden. Das allgemeine Treibermodell für nur-computegeräte ist das Microsoft Compute Driver Model (mcdm). Mcdm ist ein herunter skalierter Peer des Windows-Gerätetreiber Modells (WDDM), das über einen größeren Bereich verfügt.

Ein Gerät, das *nur* die Features innerhalb einer Kern Funktionsebene unterstützt, wird als *kerngerät* bezeichnet.

> [!NOTE]
> Das *nur-computegerät*, das *mcdm-Gerät*, das *Core-Geräte Gerät* und das *kerngerät* bedeuten dasselbe. Wir bevorzugen das *kerngerät* zur Vereinfachung.

## <a name="creating-a-core-device"></a>Erstellen eines kerngeräts

Um ein Direct3D 12-Gerät zu erstellen, rufen Sie im Allgemeinen die [**D3D12CreateDevice**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createdevice) -Funktion auf, und geben Sie eine minimale Funktionsebene an.

Wenn Sie eine Featureebene von 9 bis 12 angeben, ist das zurückgegebene Gerät ein Funktions Reiches Gerät, wie z. b. eine herkömmliche GPU (die eine übergeordnete Funktion eines kerngeräts unterstützt). Für diesen Bereich von featureebenen wird nie ein kerngerät zurückgegeben.

Wenn Sie jedoch eine Kern Funktionsebene angeben (z. b. [**D3D_FEATURE_LEVEL::D 3D_FEATURE_LEVEL_1_0_CORE**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level)), kann das Gerät, das zurückgegeben wird, funktionsreich sein oder ein kerngerät sein.

```cpp
// d3dcommon.h
D3D_FEATURE_LEVEL_1_0_CORE = 0x1000
```

Wenn Sie eine `_CORE` Featureebene angeben, überprüft die Runtime/Debug-Ebene, ob die von Ihrer Anwendung verwendeten Features von dieser `_CORE` Funktionsebene zugelassen werden. Diese Features werden weiter unten in diesem Thema definiert.

## <a name="shader-model-for-core-devices"></a>Shadermodell für kerngeräte

Ein kerngerät unterstützt das Shader-Modell 5.0 und höher.

Die Laufzeit führt die Konvertierung von 5. x-nicht-dxil-Shader-Modellen in 6,0 dxil aus. Daher muss der Treiber nur 6. x unterstützen.

## <a name="resource-management-model-for-core-devices"></a>Ressourcen Verwaltungsmodell für kerngeräte

- Unterstützte Ressourcen Dimensionen: nur Roh-und strukturierte Puffer (keine typisierten Puffer, texture1d/2D usw.)
- Keine Unterstützung für reservierte (gekachelte) Ressourcen
- Keine Unterstützung für benutzerdefinierte Heaps
- Keine Unterstützung für die folgenden Heap-Flags:
  - D3D12_HEAP_FLAG_HARDWARE_PROTECTED
  - D3D12_HEAP_FLAG_ALLOW_WRITE_WATCH
  - D3D12_HEAP_FLAG_ALLOW_DISPLAY
  - D3D12_HEAP_FLAG_ALLOW_SHADER_ATOMICS (Notiz der Shader-ATOMICS ist erforderlich, dieses Flag ist für eine andere Funktion, Adapter übergreifende ATOMICS).

## <a name="resource-binding-model-for-core-devices"></a>Ressourcen Bindungs Modell für kerngeräte

- Nur Unterstützung für Ressourcen Bindungs Ebene 1
- Ausnahmen:
  - Keine Unterstützung für Textur-Samplern
  - Unterstützung für 64-UAVs wie Featureebene 11.1 + (im Gegensatz zu 8)
  - Bei Implementierungen ist es nicht erforderlich, die Begrenzungen-Überprüfung für Shader-Zugriffe auf Ressourcen über Deskriptoren zu implementieren
    - Als byproduct wird das deskriptorbereichsflag, das in root-Signaturen D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_STATIC_KEEPING_BUFFER_BOUNDS_CHECKS wird, nicht unterstützt.
- UAV/CBV-Deskriptoren können nur für Ressourcen aus Standard Heaps (also keine Upload-/Back-Heaps) erstellt werden. Dadurch wird die Anwendung gezwungen, Kopien durchzuführen, um Daten über CPU-< >GPU zu erhalten.
- Trotz der niedrigsten Bindungs Funktionsebene sind noch einige Features erforderlich, die auch auf dieser Ebene erforderlich sind, um Folgendes zu sagen:
  - Deskriptorheaps können aktualisiert werden, nachdem Befehlslisten aufgezeichnet wurden (siehe D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_VOLATILE in der Spezifikation der Ressourcen Bindung).
  - Stamm Deskriptoren sind im Grunde gpuva-Zeiger
    - Obwohl keine Unterstützung für MMU/VA vorhanden ist, können Puffer-Vas, die in Stamm Deskriptoren verwendet werden, durch-Implementierungen emuliert werden, indem das Adress Patching durchgeführt wird.

### <a name="structured-buffer-restrictions"></a>Einschränkungen für strukturierte Puffer

Strukturierte Puffer müssen eine Basisadresse aufweisen, die 4 Byte ausgerichtet ist, und STRIDE muss 2 oder ein Vielfaches von 4 sein. Der Fall für einen Schritt von 2 ist für apps mit 16-Bit-Daten, insbesondere, wenn in D3D_FEATURE_LEVEL_1_0_CORE keine Unterstützung für typisierte Puffer vorhanden ist.

Der in den Deskriptoren angegebene Stride muss mit dem in HLSL angegebenen Stride identisch sein.  

## <a name="command-queue-support-for-core-devices"></a>Unterstützung der Befehls Warteschlange für kerngeräte

Nur Warteschlangen berechnen und kopieren (keine 3D-, Video-usw.-Warteschlangen).

## <a name="shader-support-for-core-devices"></a>Shaderunterstützung für kerngeräte

Nur Compute-Shader, keine Grafik-Shader (Vertex, Pixel-Shader usw.) und keine zugehörigen Funktionen, wie z. b. Renderziele, Austausch Ketten, Eingabe Assembler.

### <a name="arithmetic-precision"></a>Arithmetische Genauigkeit

Kerngeräte müssen denorms für Gleit Komma Vorgänge mit 16 Bit nicht unterstützen.

## <a name="supported-apis-for-core-devices"></a>Unterstützte APIs für kerngeräte

Die nachstehende Liste zeigt die unterstützte Teilmenge der vollständigen Anwendungsprogrammierschnittstelle (APIs, die *nicht* in der Core 1,0-Funktionsebene unterstützt werden) sind *nicht* aufgeführt.

### <a name="id3d12device-methods"></a>ID3D12Device-Methoden

* [ID3D12Device:: checkfeaturesupport](/windows/win32/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport)
* [ID3D12Device:: copydescriptors](/windows/win32/api/d3d12/nf-d3d12-id3d12device-copydescriptors)
* [ID3D12Device:: copydescriptor ssimple](/windows/win32/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple)
* [ID3D12Device:: kreatecommandzuweisung](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandallocator)
* [ID3D12Device:: kreatecommandlist](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist)
* [ID3D12Device:: kreatecommandqueue](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandqueue)
* [ID3D12Device:: kreatecommandsignature](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandsignature)
* [ID3D12Device:: kreatecommittedresource](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource)
* [ID3D12Device:: kreatecomputepipelinestate](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate)
* [ID3D12Device:: kreateconstantbufferview](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createconstantbufferview)
* [ID3D12Device:: kreatedescriptorheap](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createdescriptorheap)
* [ID3D12Device:: kreatefence](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createfence)
* [ID3D12Device:: kreateheap](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createheap)
* [ID3D12Device:: kreateplacedresource](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createplacedresource)
* [ID3D12Device:: kreatequeryheap](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createqueryheap)
* [ID3D12Device:: kreaterootsignature](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrootsignature)
* [ID3D12Device:: kreateshaderresourceview](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview)
* [ID3D12Device:: kreatesharedhandle](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createsharedhandle)
* [ID3D12Device:: kreateunorderedaccessview](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview)
* [ID3D12Device:: entferct](/windows/win32/api/d3d12/nf-d3d12-id3d12device-evict)
* [ID3D12Device:: getadapterluid](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getadapterluid)
* [ID3D12Device:: getcopyablefootprints](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints)
* [ID3D12Device:: getcustomheapproperties](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getcustomheapproperties)
* [ID3D12Device:: getDescriptor handleinkrementsize](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize)
* [ID3D12Device:: getdeviceremovedreason](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getdeviceremovedreason)
* [ID3D12Device:: getnoentcount](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getnodecount)
* [ID3D12Device:: getresourcezucationinfo](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getresourceallocationinfo)
* [ID3D12Device:: makeresident](/windows/win32/api/d3d12/nf-d3d12-id3d12device-makeresident)
* [ID3D12Device:: opensharedhandle](/windows/win32/api/d3d12/nf-d3d12-id3d12device-opensharedhandle)
* [ID3D12Device:: opensharedlenker byname](/windows/win32/api/d3d12/nf-d3d12-id3d12device-opensharedhandlebyname)
* [ID3D12Device:: setstablepowerstate](/windows/win32/api/d3d12/nf-d3d12-id3d12device-setstablepowerstate)

### <a name="id3d12device1-methods"></a>ID3D12Device1-Methoden

* [ID3D12Device1:: kreatepipelinelibrary](/windows/win32/api/d3d12/nf-d3d12-id3d12device1-createpipelinelibrary)
* [ID3D12Device1:: ab.](/windows/win32/api/d3d12/nf-d3d12-id3d12device1-seteventonmultiplefencecompletion)
* [ID3D12Device1:: "abtresidencymenteventonmultiplefencecompletionpriority"](/windows/win32/api/d3d12/nf-d3d12-id3d12device1-setresidencypriority)

### <a name="id3d12device2-methods"></a>ID3D12Device2-Methoden

* [ID3D12Device2:: kreatepipelinestate](/windows/win32/api/d3d12/nf-d3d12-id3d12device2-createpipelinestate)

### <a name="id3d12device3-methods"></a>ID3D12Device3-Methoden

* [ID3D12Device3:: openexistingheapfromaddress](/windows/win32/api/d3d12/nf-d3d12-id3d12device3-openexistingheapfromaddress)
* [ID3D12Device3:: openexistingheapfromfilemapping](/previous-versions/windows/desktop/legacy/mt813613(v%3Dvs.85))
* [ID3D12Device3:: einqueuemakeresident](/windows/win32/api/d3d12/nf-d3d12-id3d12device3-enqueuemakeresident)

### <a name="id3d12device4-methods"></a>ID3D12Device4-Methoden

* [ID3D12Device4::GetResourceAllocationInfo1](/windows/win32/api/d3d12/nf-d3d12-id3d12device4-getresourceallocationinfo1)

### <a name="id3d12device5-methods"></a>ID3D12Device5-Methoden

* [ID3D12Device5:: kreatemetacommand](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-createmetacommand)
* [ID3D12Device5:: kreatestateobject](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-createstateobject)
* [ID3D12Device5:: enumeratemetacommandparameters](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-enumeratemetacommandparameters)
* [ID3D12Device5:: enumeratemetacommands](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-enumeratemetacommands)
* [ID3D12Device5:: removedevice](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-removedevice)

### <a name="id3d12commandqueue-methods"></a>ID3D12CommandQueue-Methoden

* [ID3D12CommandQueue:: beginevent](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-beginevent)
* [ID3D12CommandQueue:: endevent](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-endevent)
* [ID3D12CommandQueue:: executecommandlists](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists)
* [ID3D12CommandQueue:: getclockkalibrierung](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration)
* [ID3D12CommandQueue:: getdebug](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-getdesc)
* [ID3D12CommandQueue:: gettimestampfrequency](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-gettimestampfrequency)
* [ID3D12CommandQueue:: setmarker](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-setmarker)
* [ID3D12CommandQueue:: Signal](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal)
* [ID3D12CommandQueue:: Wait](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-wait)

### <a name="id3d12commandlist-methods"></a>ID3D12CommandList-Methoden

* [ID3D12CommandList:: GetType](/windows/win32/api/d3d12/nf-d3d12-id3d12commandlist-gettype)

### <a name="id3d12graphicscommandlist-methods"></a>ID3D12GraphicsCommandList-Methoden

* [ID3D12GraphicsCommandList:: beginevent](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginevent)
* [ID3D12GraphicsCommandList:: beginquery](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery)
* [ID3D12GraphicsCommandList:: clearstate](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearstate)
* [ID3D12GraphicsCommandList:: clearunorderedaccessviewfloat](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewfloat)
* [ID3D12GraphicsCommandList:: clearunorderedaccessviewuint](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewuint)
* [ID3D12GraphicsCommandList:: Close](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close)
* [ID3D12GraphicsCommandList:: copybufferregion](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)
* [ID3D12GraphicsCommandList:: copyresource](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)
* [ID3D12GraphicsCommandList:: copytextureregion](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)
* [ID3D12GraphicsCommandList::D ispatch](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)
* [ID3D12GraphicsCommandList:: endevent](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endevent)
* [ID3D12GraphicsCommandList:: endquery](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery)
* [ID3D12GraphicsCommandList:: Reset](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset)
* [ID3D12GraphicsCommandList:: resolvequerydata](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata)
* [ID3D12GraphicsCommandList:: resourcebarrier](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)
* [ID3D12GraphicsCommandList::SetComputeRoot32BitConstant](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstant)
* [ID3D12GraphicsCommandList::SetComputeRoot32BitConstants](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstants)
* [ID3D12GraphicsCommandList:: setcomputerootconstantbufferview](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootconstantbufferview)
* [ID3D12GraphicsCommandList:: setcomputerootdescriptor Table](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable)
* [ID3D12GraphicsCommandList:: setcomputerootshaderresourceview](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootshaderresourceview)
* [ID3D12GraphicsCommandList:: setcomputerootsignature](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootsignature)
* [ID3D12GraphicsCommandList:: setcomputerootunorderedaccessview](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootunorderedaccessview)
* [ID3D12GraphicsCommandList:: setdescriptorheaps](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps)
* [ID3D12GraphicsCommandList:: setmarker](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setmarker)
* [ID3D12GraphicsCommandList:: setpipelinestate](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate)
* [ID3D12GraphicsCommandList:: setprediation](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication)

### <a name="id3d12graphicscommandlist1-methods"></a>ID3D12GraphicsCommandList1-Methoden

* [ID3D12GraphicsCommandList1:: atomiccopybufferuint](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-atomiccopybufferuint)
* [ID3D12GraphicsCommandList1::AtomicCopyBufferUINT64](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-atomiccopybufferuint64)

### <a name="id3d12graphicscommandlist2-methods"></a>ID3D12GraphicsCommandList2-Methoden

* [ID3D12GraphicsCommandList2:: Write-bufferimmediate](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist2-writebufferimmediate)

### <a name="id3d12graphicscommandlist4-methods"></a>ID3D12GraphicsCommandList4-Methoden

* [ID3D12GraphicsCommandList4:: executemetacommand](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-executemetacommand)
* [ID3D12GraphicsCommandList4:: initializemetacommand](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-initializemetacommand)
