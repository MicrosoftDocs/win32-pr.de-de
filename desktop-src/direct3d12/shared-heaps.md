---
title: Freigegebene Heaps
description: Die Freigabe eignet sich für Multiprozess-und multiadapterarchitekturen.
ms.assetid: 67C6B1D4-BF76-45A9-BADC-7C9520C900EB
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f4271055f88e38484041c225b6b17c6d75f0d98
ms.sourcegitcommit: d6102d9e2b26368142fe5b006c65acb50c98be65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/26/2019
ms.locfileid: "74103482"
---
# <a name="shared-heaps"></a>Freigegebene Heaps

Die Freigabe eignet sich für Multiprozess-und multiadapterarchitekturen.

-   [Übersicht über die Freigabe](#sharing-overview)
-   [Freigabe von Heaps für Prozesse](#sharing-heaps-across-processes)
-   [Freigeben von Heaps über Adapter hinweg](#sharing-heaps-across-adapters)
-   [Verwandte Themen](#related-topics)

## <a name="sharing-overview"></a>Übersicht über die Freigabe

Freigegebene Heaps ermöglichen zwei Dinge: das Freigeben von Daten in einem Heap über einen oder mehrere Prozesse hinweg und das Ausschließen einer nicht deterministischen Auswahl von nicht definiertem Textur Layout für Ressourcen, die im Heap abgelegt werden. Durch die gemeinsame Nutzung von Heaps für Adapter entfällt auch das CPU-Marshalling der Daten.

Sowohl Heaps als auch zugesicherte Ressourcen können freigegeben werden. Durch die Freigabe einer zugeordneten Ressource wird der implizite Heap gemeinsam mit der Beschreibung der zugeordneten Ressource gemeinsam genutzt, sodass eine kompatible Ressourcen Beschreibung dem Heap von einem anderen Gerät zugeordnet werden kann.

Alle Methoden sind frei Thread und erben die vorhandene D3D11-Semantik des Entwurfs Entwurfs für NT-Handles.

-   [**ID3D12Device:: kreatesharedhandle**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createsharedhandle)
-   [**ID3D12Device:: opensharedhandle**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-opensharedhandle)
-   [**ID3D12Device:: opensharedlenker byname**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-opensharedhandlebyname)

## <a name="sharing-heaps-across-processes"></a>Freigabe von Heaps für Prozesse

Freigegebene Heaps werden mit dem D3D12-Heap-Flag-Enumerationsmember der \_ D3D12- \_ \_ [**\_ \_ heapflags**](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_flags) -Enumeration angegeben.

Freigegebene Heaps werden für auf CPU zugängliche Heaps nicht unterstützt: D3D12 \_ Heap \_ Type \_ Upload, D3D12 \_ Heap \_ Type Read \_ Back und D3D12 \_ Heap \_ Type \_ Custom ohne D3D12 \_ CPU \_ Page \_ Property \_ Not \_ available.

Wenn eine nicht deterministische Auswahl von nicht definiertem Textur Layout ausgeschlossen wird, können verzögerte renderingszenarios für einige GPUs erheblich beeinträchtigt werden, sodass es sich nicht um das Standardverhalten für die Platzierung und die zugesicherte Ressourcen handelt. Verzögerte Renderingvorgänge sind bei einigen GPU-Architekturen beeinträchtigt, da deterministische Textur Layouts die effektive Speicherbandbreite verringern, die beim gleichzeitigen Rendering in mehrere renderzieltexturen desselben Formats und derselben Größe erreicht wird. GPU-Architekturen verbrauchen sich von der Nutzung nicht deterministischer Textur Layouts, um standardisierte swidingmuster und standardisierte Layouts für verzögertes Rendering effizient zu unterstützen.

Freigegebene Heaps sind auch mit anderen geringfügigen Kosten verbunden:

-   Freigegebene Heap Daten können aufgrund von Informationen zur Offenlegung von Informationen nicht so flexibel wie in-Process-Heaps wieder verwendet werden. Daher wird der physische Speicher häufiger in die Warteschlange gestellt.
-   Bei der Erstellung und Zerstörung von freigegebenen Heaps gibt es einen zusätzlichen CPU-Overhead und eine größere Systemspeicher Auslastung.

## <a name="sharing-heaps-across-adapters"></a>Freigeben von Heaps über Adapter hinweg

Freigegebene Heaps zwischen Adaptern werden mit dem D3D12 \_ Heap \_ Flag \_ Shared \_ Cross Adapter-Member der Enumeration \_ [**D3D12 \_ Heap \_ Flags**](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_flags) festgelegt.

Durch Kreuz Adapter freigegebene Heaps können mehrere Adapter Daten gemeinsam nutzen, ohne dass die CPU zwischen diesen Daten marshallert. Die unterschiedlichen Adapter Funktionen bestimmen, wie effiziente Adapter Daten zwischen Ihnen übergeben können. durch das Aktivieren von GPU-Kopien wird die effektive Bandbreite erhöht. Einige Textur Layouts sind auf Kreuz Adapter Heaps zulässig, um einen Austausch von Textur Daten zu unterstützen, auch wenn solche Textur Layouts nicht anderweitig unterstützt werden. Bestimmte Einschränkungen gelten möglicherweise für solche Texturen, z. b. nur das Kopieren.

Die Adapter übergreifende Freigabe funktioniert mit Heaps, die durch den Aufruf von [**ID3D12Device:: createheap**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createheap)erstellt wurden. Anwendungen können dann über [**createplacedresource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createplacedresource)Ressourcen erstellen. Sie ist auch durch Ressourcen/Heaps zulässig, die von [**createcommittedresource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource) erstellt wurden, aber nur für Row-Major D3D12 \_ Resource \_ Dimension \_ TEXTURE2D Resources (Weitere Informationen finden Sie unter [**D3D12 \_ Resource \_ Dimension**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_dimension)). Die Adapter übergreifende Freigabe funktioniert [**nicht mit "**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createreservedresource)" von "".

Bei der Adapter übergreifenden Freigabe gelten alle üblichen Regeln für die Warteschlangen übergreifende Ressourcen Freigabe weiterhin. Anwendungen müssen die entsprechenden Barrieren ausstellen, um die ordnungsgemäße Synchronisierung und Kohärenz zwischen den beiden Adaptern sicherzustellen. Anwendungen sollten Adapter übergreifende Zäune verwenden, um die Planung von Befehlslisten zu koordinieren, die an mehrere Adapter übermittelt werden. Es gibt keinen Mechanismus zum Freigeben von Adapter übergreifenden Ressourcen über D3D-API-Versionen hinweg. Netzwerk übergreifende freigegebene Ressourcen werden nur im Systemspeicher unterstützt. Netzwerk übergreifende freigegebene Heaps/Ressourcen werden in D3D12 \_ Heap \_ Type- \_ Standard Heaps und D3D12 \_ Heap \_ Type \_ Custom Heaps (mit dem L0-Speicherpool und den Eigenschaften der CPU-Seiten für die Schreib Kombination) unterstützt. Treiber müssen sicher sein, dass GPU-Lese-/Schreibvorgänge für Kreuz Adapter übergreifende freigegebene Heaps mit anderen GPUs auf dem System in Einklang stehen. Beispielsweise muss der Treiber möglicherweise die Heap Daten aus den GPU-Caches ausschließen, die in der Regel nicht geleert werden müssen, wenn die CPU nicht direkt auf die Heap Daten zugreifen kann.

Anwendungen sollten die Verwendung von Adapter übergreifenden Heaps auf die Szenarien beschränken, die die von Ihnen bereitgestellte Funktionalität erfordern. Adapter übergreifende Heaps befinden sich im D3D12- \_ Speicher \_ Pool \_ L0. Dies ist nicht immer das, was [**getcustomheapproperties**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getcustomheapproperties) vorschlägt. Dieser Speicherpool ist für diskrete/NUMA-Adapter Architekturen nicht effizient. Und die effizientesten Textur Layouts sind nicht immer verfügbar.

Außerdem gelten die folgenden Einschränkungen:

-   Die Heap Kennzeichen im Zusammenhang mit Heap Ebenen müssen das D3D12-Heap Kennzeichen sein, das \_ \_ \_ \_ alle \_ Puffer \_ und \_ Texturen zulässt.
-   Das D3D12- \_ Heap- \_ Flag \_ Shared muss ebenfalls festgelegt werden.
-   Der Standardwert für \_ \_ den D3D12-heaptyp \_ muss festgelegt werden, oder der D3D12 \_ \_ -heaptyp ist für \_ den D3D12 \_ -Speicher Pool L0 festgelegt, \_ \_ und \_ \_ \_ \_ \_ es muss eine D3D12 CPU
-   Nur Ressourcen mit dem D3D12- \_ Ressourcentyp \_ \_ Allow \_ Cross \_ Adapter können auf Adapter übergreifenden Heaps platziert werden.

Weitere Informationen zur Verwendung mehrerer Adapter finden Sie im Abschnitt [Systeme mit mehreren Adaptern](multi-engine.md) .

## <a name="related-topics"></a>Verwandte Themen

<dl> <dt>

[Untergeordnete Zuordnung innerhalb von Heaps](suballocation-within-heaps.md)
</dt> </dl>

 

 




