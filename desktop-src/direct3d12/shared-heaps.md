---
title: Freigegebene Heaps
description: Die Freigabe ist für Architekturen mit mehreren Prozessen und mehreren Adaptern nützlich.
ms.assetid: 67C6B1D4-BF76-45A9-BADC-7C9520C900EB
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31e1bc0826651334d3d137466cc34d194fb79ae4900075b9a145859c5fd37fbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118300811"
---
# <a name="shared-heaps"></a>Freigegebene Heaps

Die Freigabe ist für Architekturen mit mehreren Prozessen und mehreren Adaptern nützlich.

-   [Übersicht über die Freigabe](#sharing-overview)
-   [Prozessübergreifendes Freigeben von Heaps](#sharing-heaps-across-processes)
-   [Freigeben von Heaps über Adapter hinweg](#sharing-heaps-across-adapters)
-   [Zugehörige Themen](#related-topics)

## <a name="sharing-overview"></a>Übersicht über die Freigabe

Freigegebene Heaps ermöglichen zwei Dinge: das Freigeben von Daten in einem Heap für einen oder mehrere Prozesse und das Vorziehen einer nicht deterministischen Auswahl eines nicht definierten Texturlayouts für Ressourcen, die im Heap platziert werden. Das Freigeben von Heaps über Adapter hinweg enthebt auch die Notwendigkeit des CPU-Marshallings der Daten.

Sowohl Heaps als auch Ressourcen, für die ein Commit ausgeführt wurde, können freigegeben werden. Die Freigabe einer ressource, für die ein Commit ausgeführt wurde, verwendet tatsächlich den impliziten Heap zusammen mit der Beschreibung der ressource, für die ein Commit ausgeführt wurde, sodass dem Heap von einem anderen Gerät aus eine kompatible Ressourcenbeschreibung zugeordnet werden kann.

Alle Methoden sind Freithreading und erben die vorhandene D3D11-Semantik des NT-Handlefreigabeentwurfs.

-   [**ID3D12Device::CreateSharedHandle**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createsharedhandle)
-   [**ID3D12Device::OpenSharedHandle**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-opensharedhandle)
-   [**ID3D12Device::OpenSharedHandleByName**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-opensharedhandlebyname)

## <a name="sharing-heaps-across-processes"></a>Prozessübergreifendes Freigeben von Heaps

Freigegebene Heaps werden mit dem D3D12 \_ HEAP \_ FLAG \_ SHARED-Member der [**D3D12 \_ HEAP \_ FLAGS-Enumeration**](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_flags) angegeben.

Freigegebene Heaps werden auf Heaps mit CPU-Zugriff nicht unterstützt: D3D12 \_ HEAP \_ TYPE \_ UPLOAD, D3D12 \_ HEAP TYPE \_ \_ READBACK und D3D12 \_ HEAP TYPE CUSTOM without \_ \_ D3D12 \_ CPU PAGE PROPERTY NOT \_ \_ \_ \_ AVAILABLE.

Wenn Sie eine nicht deterministische Auswahl eines nicht definierten Texturlayouts vorziehen, können verzögerte Renderingszenarien für einige GPUs erheblich beeinträchtigt werden, sodass dies nicht das Standardverhalten für platzierte und ausgeführte Ressourcen ist. Verzögertes Rendering ist bei einigen GPU-Architekturen beeinträchtigt, da deterministische Texturlayouts die effektive Arbeitsspeicherbandbreite verringern, die beim gleichzeitigen Rendern in mehrere Renderzieltexturen des gleichen Formats und derselben Größe erreicht wird. GPU-Architekturen entwickeln sich von der Nutzung nicht deterministischer Texturlayouts ab, um standardisierte Swizzlemuster und standardisierte Layouts effizient für verzögertes Rendering zu unterstützen.

Für freigegebene Heaps fallen auch andere kleinere Kosten an:

-   Freigegebene Heapdaten können aufgrund von Bedenken hinsichtlich der Offenlegung von Informationen nicht so flexibel wie In-Process-Heaps wiederverwendet werden, sodass der physische Arbeitsspeicher häufiger null ist.
-   Es gibt einen geringfügigen zusätzlichen CPU-Mehraufwand und eine erhöhte Systemspeicherauslastung während der Erstellung und Zerstörung freigegebener Heaps.

## <a name="sharing-heaps-across-adapters"></a>Freigeben von Heaps über Adapter hinweg

Freigegebene Heaps über Adapter hinweg werden mit dem D3D12 \_ HEAP FLAG SHARED CROSS \_ \_ \_ \_ ADAPTER-Member der [**D3D12 \_ HEAP \_ FLAGS-Enumeration**](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_flags) angegeben.

Adapterübergreifende freigegebene Heaps ermöglichen es mehreren Adaptern, Daten freizugeben, ohne dass die CPU die Daten zwischen ihnen marshallt. Unterschiedliche Adapterfunktionen bestimmen zwar, wie effizient Adapter Daten zwischen ihnen übergeben können, aber durch die Aktivierung von GPU-Kopien wird die effektive Bandbreite erhöht. Einige Texturlayouts sind auf adapterübergreifenden Heaps zulässig, um einen Austausch von Texturdaten zu unterstützen, auch wenn solche Texturlayouts anderweitig nicht unterstützt werden. Bestimmte Einschränkungen können für solche Texturen gelten, z. B. nur das Kopieren.

Die adapterübergreifende Freigabe funktioniert mit Heaps, die durch Aufrufen von [**ID3D12Device::CreateHeap**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createheap)erstellt wurden. Anwendungen können dann Ressourcen über [**CreatePlacedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createplacedresource)erstellen. Dies ist auch für Ressourcen/Heaps zulässig, die von [**CreateCommittedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource) erstellt wurden, jedoch nur für Ressourcen mit zeilenbasierter Hauptversion D3D12 \_ RESOURCE DIMENSION \_ \_ TEXTURE2D (siehe [**D3D12 \_ RESOURCE \_ DIMENSION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_dimension)). Die adapterübergreifende Freigabe funktioniert nicht mit [**CreateReservedResource.**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createreservedresource)

Für die adapterübergreifende Freigabe gelten weiterhin alle üblichen Regeln für die warteschlangenübergreifende Ressourcenfreigabe. Anwendungen müssen die entsprechenden Barrieren ausstellen, um eine ordnungsgemäße Synchronisierung und Einheitlichkeit zwischen den beiden Adaptern sicherzustellen. Anwendungen sollten adapterübergreifende Umgrenzungen verwenden, um die Planung von Befehlslisten zu koordinieren, die an mehrere Adapter übermittelt werden. Es gibt keinen Mechanismus, um adapterübergreifende Ressourcen für D3D-API-Versionen freizugeben. Adapterübergreifende freigegebene Ressourcen werden nur im Systemspeicher unterstützt. Adapterübergreifende freigegebene Heaps/Ressourcen werden in D3D12 \_ HEAP \_ TYPE \_ DEFAULT-Heaps und D3D12 \_ HEAP TYPE CUSTOM \_ \_ Heaps (mit dem L0-Speicherpool und den Eigenschaften der Seite "Write-Combine CPU") unterstützt. Treiber müssen sicherstellen, dass GPU-Lese-/Schreibvorgänge für adapterübergreifende freigegebene Heaps mit anderen GPUs im System kompatibel sind. Beispielsweise muss der Treiber die Heapdaten möglicherweise von GPU-Caches ausschließen, die normalerweise nicht geleert werden müssen, wenn die CPU nicht direkt auf die Heapdaten zugreifen kann.

Anwendungen sollten die Verwendung von adapterübergreifenden Heaps auf die Szenarien beschränken, die die von ihnen bereitzustellende Funktionalität erfordern. Adapterübergreifende Heaps befinden sich in D3D12 \_ MEMORY \_ POOL \_ L0. Dies ist nicht immer das, was [**GetCustomHeapProperties**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getcustomheapproperties) vorschlägt. Dieser Speicherpool ist für diskrete/NUMA-Adapterarchitekturen nicht effizient. Und die effizientesten Texturlayouts sind nicht immer verfügbar.

Außerdem gelten die folgenden Einschränkungen:

-   Die Heapflags im Zusammenhang mit Heapebenen müssen D3D12 \_ HEAP FLAG ALLOW ALL \_ \_ \_ \_ BUFFERS AND \_ \_ TEXTURES sein.
-   D3D12 \_ HEAP FLAG SHARED muss ebenfalls festgelegt \_ \_ werden.
-   Entweder muss D3D12 \_ HEAP TYPE DEFAULT festgelegt \_ \_ werden, oder D3D12 \_ HEAP TYPE CUSTOM with \_ \_ D3D12 \_ MEMORY POOL \_ \_ L0 and D3D12 \_ CPU PAGE PROPERTY NOT AVAILABLE muss festgelegt \_ \_ \_ \_ werden.
-   Nur Ressourcen mit D3D12 \_ RESOURCE FLAG ALLOW CROSS ADAPTER \_ \_ \_ \_ dürfen auf adapterübergreifenden Heaps platziert werden.

Weitere Informationen zur Verwendung mehrerer Adapter finden Sie im Abschnitt Systeme mit mehreren [Adaptern.](multi-engine.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Unterzuweisung innerhalb von Heaps](suballocation-within-heaps.md)
</dt> </dl>

 

 




