---
title: Residenz
description: Ein Objekt gilt als resident, wenn es von der GPU zugänglich ist.
ms.assetid: 956F80D7-EEC8-4D88-B251-EE325614F31E
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 257af2526120df5509a38fcc0c81984aa53a954f8eed6a8ce9194fa2aadb020a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989454"
---
# <a name="residency"></a>Residenz

Ein Objekt gilt als *resident,* wenn die GPU darauf zugreifen kann.

-   [Budget für die Residency](#residency-budget)
-   [Heapressourcen](#heap-resources)
-   [Residencyprioritäten](#residency-priorities)
    -   [Standardprioritätsalgorithmus](#default-priority-algorithm)
-   [Programmieren der Residencyverwaltung](#programming-residency-management)
-   [Zugehörige Themen](#related-topics)

## <a name="residency-budget"></a>Budget für die Residency

GPUs unterstützen noch keine Seitenfehler, sodass Anwendungen Daten in den physischen Speicher committen müssen, während die GPU darauf zugreifen kann. Dieser Prozess wird als "Machen eines Residenten" bezeichnet und muss sowohl für den physischen Systemspeicher als auch für den physischen diskreten Videospeicher ausgeführt werden. In D3D12 kapseln die meisten API-Objekte eine gewisse Menge an GPU-zugänglichen Arbeitsspeicher. Dieser GPU-zugängliche Arbeitsspeicher wird während der Erstellung des API-Objekts als "resident" gespeichert und bei der Zerstörung von API-Objekten entfernt.

Der für den Prozess verfügbare physische Arbeitsspeicher wird als Videospeicherbudget bezeichnet. Das Budget kann merklich schwanken, wenn Hintergrundprozesse reaktivieren und in den Standbymodus versetzt werden. und schwanken erheblich, wenn der Benutzer zu einer anderen Anwendung wechselt. Die Anwendung kann benachrichtigt werden, wenn sich das Budget ändert und sowohl das aktuelle Budget als auch die aktuell verbrauchte Arbeitsspeichermenge abgefragt werden. Wenn eine Anwendung nicht innerhalb ihres Budgets bleibt, wird der Prozess zeitweilig eingefroren, damit andere Anwendungen ausgeführt werden können, und/oder die Erstellungs-APIs geben Fehler zurück. Die [**IDXGIAdapter3-Schnittstelle**](/windows/desktop/api/dxgi1_4/nn-dxgi1_4-idxgiadapter3) stellt die Methoden für diese Funktionalität bereit, insbesondere [**QueryVideoMemoryInfo**](/windows/desktop/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-queryvideomemoryinfo) und [**RegisterVideoMemoryBudgetChangeNotificationEvent.**](/windows/desktop/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-registervideomemorybudgetchangenotificationevent)

Anwendungen wird empfohlen, eine Reservierung zu verwenden, um die Menge an Arbeitsspeicher zu kennzeichnen, auf die sie nicht verzichten können. Im Idealfall sind die vom Benutzer angegebenen "niedrigen" Grafikeinstellungen oder etwas niedriger der richtige Wert für eine solche Reservierung. Wenn Sie eine Reservierung festlegen, erhält eine Anwendung niemals ein höheres Budget, als sie normalerweise erhalten würde. Stattdessen helfen die Reservierungsinformationen dem Betriebssystemkernel dabei, die Auswirkungen von Situationen mit hoher Arbeitsspeicherauslastung schnell zu minimieren. Selbst die Reservierung ist nicht garantiert für die Anwendung verfügbar, wenn die Anwendung nicht die Vordergrundanwendung ist.

## <a name="heap-resources"></a>Heapressourcen

Viele API-Objekte kapseln zwar einen teil des gpu-zugänglichen Speichers, Heaps & Ressourcen werden jedoch voraussichtlich die wichtigste Art und Weise sein, wie Anwendungen physischen Speicher nutzen und verwalten. Ein Heap ist die niedrigste Einheit zum Verwalten des physischen Speichers, daher ist es gut, mit den Eigenschaften der Residency vertraut zu sein.

-   Heaps können nicht teilweise als residente Heaps erstellt werden, es gibt jedoch Problemumgehungen mit reservierten Ressourcen.
-   Heaps sollten als Teil eines bestimmten Pools budgetiert werden. UMA-Adapter verfügen über einen Pool, während diskrete Adapter über zwei Pools verfügen. Es ist zwar richtig, dass der Kernel einige Heaps auf diskreten Adaptern aus dem Videospeicher in den Systemspeicher verschieben kann, aber dies nur als äußersten letzten Ausweg. Anwendungen sollten sich nicht auf das Überbudgetverhalten des Kernels verlassen und sich stattdessen auf eine gute Budgetverwaltung konzentrieren.
-   Heaps können aus der Residency entfernt werden, wodurch ihre Inhalte auf den Datenträger ausgelagern werden können. Die Zerstörung von Heaps ist jedoch eine zuverlässigere Technik, um die Residency für alle Adapterarchitekturen frei zu machen. Auf Adaptern, bei denen *sich das FeldMaxGPUVirtualAddressBitsPerProcess* von [**D3D12 \_ FEATURE DATA GPU VIRTUAL ADDRESS \_ \_ \_ \_ \_ SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_gpu_virtual_address_support) in der Nähe der Budgetgröße befindet, gibt [**Evict**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-evict) die Residency nicht zuverlässig frei.
-   Die Heaperstellung kann langsam sein. ist aber für die Hintergrundthreadverarbeitung optimiert. Es wird empfohlen, Heaps in Hintergrundthreads zu erstellen, um eine Störung des Renderthreads zu vermeiden. In D3D12 können mehrere Threads create-Routinen sicher gleichzeitig aufrufen.

D3D12 führt mehr Flexibilität und Orthogonalität in sein Ressourcenmodell ein, um mehr Optionen für Anwendungen zu ermöglichen. Es gibt drei arten von Ressourcen auf hoher Ebene in D3D12: Commit, Platzierung und Reserviert.

-   Ressourcen, für die ein Commit ausgeführt wurde, erstellen gleichzeitig eine Ressource und einen Heap. Der Heap ist implizit und kann nicht direkt aufgerufen werden. Der Heap ist entsprechend groß, um die gesamte Ressource innerhalb des Heaps zu finden.
-   Platzierte Ressourcen ermöglichen die Platzierung einer Ressource bei einem Offset ungleich 0 (null) innerhalb eines Heaps. Offsets müssen in der Regel auf 64 KB ausgerichtet werden. es gibt jedoch einige Ausnahmen in beide Richtungen. MSAA-Ressourcen erfordern eine Offsetausrichtung von 4 MB, und die Offsetausrichtung von 4 KB ist für kleine Texturen verfügbar. Platzierte Ressourcen können nicht direkt in einen anderen Heap verschoben oder neu zugeordnet werden. sie ermöglichen jedoch eine einfache Verschiebung der Ressourcendaten zwischen Heaps. Nachdem Sie eine neue platzierte Ressource in einem anderen Heap erstellt und die Ressourcendaten kopiert haben, müssen neue Ressourcendeskriptoren für den neuen Ressourcendatenspeicherort verwendet werden.
-   Reservierte Ressourcen sind nur verfügbar, wenn der Adapter gekachelte Ressourcen der Ebene 1 oder höher unterstützt. Wenn verfügbar, bieten sie die fortgeschrittensten verfügbaren Techniken für die Verwaltung von Residencys. aber nicht alle Adapter unterstützen sie derzeit. Sie ermöglichen die Neuzuordnung einer Ressource, ohne dass ressourcendeskriptoren, teilweise mip level residency, sparse texture scenarios usw. neu erstellt werden müssen. Nicht alle Ressourcentypen werden auch dann unterstützt, wenn reservierte Ressourcen verfügbar sind, sodass ein vollständig allgemeiner seitenbasierter Residency-Manager noch nicht möglich ist.

## <a name="residency-priorities"></a>Residencyprioritäten

Die Windows 10 Creators Update ermöglicht Entwicklern, zu beeinflussen, welche Heaps und Ressourcen bevorzugt bleiben sollen, wenn die Arbeitsspeicherauslastung erfordert, dass einige ihrer Ressourcen herabgestuft werden. Dies hilft Entwicklern, anwendungen mit besserer Leistung zu erstellen, indem sie wissen, dass die Runtime nicht von der API-Nutzung ableiten kann. Es wurde erwartet, dass Entwickler beim Übergang von der Verwendung von committeten Ressourcen zu ressourcenreserzielten und gekachelten Ressourcen komfortabler und in der Lage sind, Prioritäten anzugeben.

Das Anwenden dieser Prioritäten muss einfacher sein als das Verwalten von zwei dynamischen Speicherbudgets, das manuelle Herabsetzen und Heraufstaufen von Ressourcen, da anwendungen dies bereits tun können. Daher wird der Entwurf der Api für die Residencypriorität natürlich mit angemessenen Standardprioritäten abgestuft, die jedem Heap oder jeder Ressource beim Erstellen zugewiesen sind. Weitere Informationen finden Sie unter [**ID3D12Device1::SetResidencyPriority**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device1-setresidencypriority) und die [**D3D12 \_ RESIDENCY \_ PRIORITY-Enumeration.**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_residency_priority)

Bei Prioritäten wird von Entwicklern folgendes erwartet:

-   Erhöhen Sie die Priorität einiger Ausnahmeheaps, um die erfahrungsgemäßen Leistungsauswirkungen dieser Heaps früher oder häufiger zu verringern, als ihre natürlichen Zugriffsmuster erfordern würden. Dieser Ansatz wird von Anwendungen genutzt, die von Grafik-APIs wie Direct3D 11 oder OpenGL portiert werden. Das Ressourcenverwaltungsmodell unterscheidet sich erheblich von dem von Direct3D 12.
-   Überschreiben Sie fast alle Heapprioritäten mit dem eigenen Bucketisierungsschema der Anwendung, entweder fest, basierend auf dem Wissen des Programmierers über die Zugriffshäufigkeit oder dynamisch. Ein festes Schema ist einfacher zu verwalten als ein dynamisches Schema, kann aber weniger effektiv sein und eine Inteaktion des Programmierers erfordern, da sich Verwendungsmuster im Laufe der Entwicklung ändern. Dieser Ansatz sollte von Anwendungen genutzt werden, die unter Berücksichtigung der Ressourcenverwaltung im Direct3D 12-Stil erstellt werden, z. B. Anwendungen, die die Residencybibliothek verwenden (insbesondere dynamische Schemas).

### <a name="default-priority-algorithm"></a>Standardprioritätsalgorithmus

Eine Anwendung kann keine nützlichen Prioritäten für einen Heap angeben, den sie verwalten möchte, ohne zuvor den Standardprioritätsalgorithmus zu untergeben. Dies liegt daran, dass der Wert der Zuweisung einer bestimmten Priorität zu einem Heap von seiner relativen Priorität zu anderen priorisierten Heaps abgeleitet wird, die um denselben Arbeitsspeicher konkurrieren.

Die zum Generieren von Standardprioritäten gewählte Strategie besteht darin, Heaps in zwei Buckets zu kategorisieren, wobei Heaps bevorzugt werden (mit höherer Priorität), von denen angenommen wird, dass sie häufig von der GPU geschrieben werden, gegenüber Heaps, die nicht sind.

Der Bucket mit hoher Priorität enthält Heaps und Ressourcen, die mit Flags erstellt werden, die sie als Renderziele, Tiefenschablonenpuffer oder Unordered Access Views (UAVs) identifizieren. Diesen werden Prioritätswerte im Bereich zugewiesen, der bei **D3D12 \_ RESIDENCY \_ PRIORITY \_ HIGH** beginnt. Um diese Heaps und Ressourcen weiter zu priorisieren, werden die niedrigsten 16 Bits der Priorität auf die Größe des Heaps oder der Ressource geteilt durch 10 MB festgelegt (mit 0xFFFF für extrem große Heaps). Durch diese zusätzliche Priorisierung werden größere Heaps und Ressourcen bevorzugt.

Der Bucket mit niedriger Priorität enthält alle anderen Heaps und Ressourcen, denen der Prioritätswert **D3D12 \_ RESIDENCY \_ PRIORITY \_ NORMAL** zugewiesen ist. Es wird keine weitere Priorisierung zwischen diesen Heaps und Ressourcen versucht.

## <a name="programming-residency-management"></a>Programmieren der Residencyverwaltung

Einfache Anwendungen können dies erreichen, indem sie nur Ressourcen erstellen, für die ein Commit ausgeführt wurde, bis es zu Fehlern aufgrund von nicht genügend Arbeitsspeicher kommt. Bei einem Fehler kann die Anwendung andere Ressourcen oder API-Objekte, für die ein Commit ausgeführt wurde, zerstören, damit weitere Ressourcenerstellungen erfolgreich sind. Es wird jedoch dringend empfohlen, selbst einfache Anwendungen auf negative Budgetänderungen zu achten und nicht verwendete API-Objekte ungefähr einmal pro Frame zu zerstören.

Die Komplexität eines Entwurfs für die Residencyverwaltung steigt, wenn versucht wird, adapterarchitekturen zu optimieren oder Residencyprioritäten zu integrieren. Die diskrete Budgetierung und Verwaltung von zwei Speicherpools ist komplexer als die Verwaltung eines einzigen Speichers, und das Zuweisen fester Prioritäten in großem Umfang kann zu einer Wartungslast werden, wenn sich Verwendungsmuster weiterentwickeln. Das Überlaufen von Texturen in den Systemspeicher erhöht die Komplexität, da die falsche Ressource im Systemspeicher die Bildfrequenz erheblich beeinträchtigen kann. Und es gibt keine einfache Funktionalität, um die Ressourcen zu identifizieren, die entweder von einer höheren GPU-Bandbreite profitieren oder eine niedrigere GPU-Bandbreite tolerieren würden.

Noch kompliziertere Entwürfe fragen die Features des aktuellen Adapters ab. Diese Informationen sind unter [**\_ \_ \_ \_ \_ \_ D3D12 FEATURE DATA GPU VIRTUAL ADDRESS SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_gpu_virtual_address_support), [**D3D12 \_ FEATURE DATA \_ \_ ARCHITECTURE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_architecture), [**D3D12 \_ TILED RESOURCES \_ \_ TIER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier)und [**D3D12 \_ RESOURCE HEAP \_ \_ TIER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_heap_tier)verfügbar.

Mehrere Teile einer Anwendung werden wahrscheinlich mit unterschiedlichen Techniken aufwickelt. Beispielsweise können einige große Texturen und selten trainierte Codepfade Commitressourcen verwenden, während viele Texturen mit einer Streamingeigenschaft festgelegt werden können und eine allgemeine Methode für platzierte Ressourcen verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**ID3D12Heap**](/windows/desktop/api/d3d12/nn-d3d12-id3d12heap)
</dt> <dt>

[Speicherverwaltung](memory-management.md)
</dt> </dl>

 

 