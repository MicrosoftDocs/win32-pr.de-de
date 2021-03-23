---
title: Systeme mit mehreren Adaptern
description: Beschreibt die Unterstützung in Direct3D 12 für Systeme, die mehrere Adapter installiert haben, und umfasst Szenarien, in denen Ihre Anwendung explizit mehrere GPU-Adapter als Ziel verwendet, und Szenarios, in denen Treiber implizit mehrere GPU-Adapter im Auftrag der Anwendung verwenden.
ms.assetid: CC4C6594-D48F-40C1-93EE-9F98532BC038
ms.localizationpriority: high
ms.topic: article
ms.date: 09/25/2019
ms.openlocfilehash: d7d3985c880c4d1732a96b98ac6d3c6579dab8e6
ms.sourcegitcommit: 9d530b0a2396f2274e9ed693c1f5f10556aadebb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/09/2020
ms.locfileid: "104548647"
---
# <a name="multi-adapter-systems"></a>Systeme mit mehreren Adaptern

Beschreibt die Unterstützung in Direct3D 12 für Systeme, die mehrere Adapter installiert haben, und umfasst Szenarien, in denen Ihre Anwendung explizit mehrere GPU-Adapter als Ziel verwendet, und Szenarios, in denen Treiber implizit mehrere GPU-Adapter im Auftrag der Anwendung verwenden.

## <a name="multi-adapter-overview"></a>Übersicht über mehrere Adapter

Bei einem GPU-Adapter kann es sich um einen beliebigen Adapter (Grafiken oder COMPUTE, diskret oder integriert) von jedem Hersteller handeln, der Direct3D 12 unterstützt.

Mehrere Adapter werden als *Knoten* referenziert. Eine Reihe von Elementen, z. b. die Warteschlangen, gelten für jeden Knoten. Wenn also zwei Knoten vorhanden sind, gibt es zwei 3D-Standard Warteschlangen. Andere Elemente, wie z. b. der Pipeline Status und Stamm-und Befehls Signaturen, können auf einen oder mehrere der Knoten verweisen, wie im Diagramm dargestellt.

![Warteschlangen gelten für jeden Grafikadapter.](images/multigpu.png)

## <a name="sharing-heaps-across-adapters"></a>Freigeben von Heaps über Adapter hinweg

Weitere Informationen finden Sie im Thema frei [gegebene Heaps](shared-heaps.md) .

## <a name="multi-adapter-apis-and-node-masks"></a>APIs mit mehreren Adaptern und Knoten Masken

Ähnlich wie bei früheren Direct3D-APIs wird jeder Satz von verknüpften Adaptern als einzelnes [**IDXGIAdapter3**](/windows/win32/api/dxgi1_4/nn-dxgi1_4-idxgiadapter3) -Objekt aufgezählt. Alle Ausgaben, die an einen beliebigen Adapter in der Verknüpfung angefügt sind, werden als angefügt an das einzelne **IDXGIAdapter3** -Objekt aufgezählt.

Die Anwendung kann die Anzahl von physischen Adaptern ermitteln, die einem bestimmten Gerät zugeordnet sind, indem [**ID3D12Device:: getnodecount**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getnodecount)aufgerufen wird.

Viele APIs in Direct3D 12 akzeptieren eine *Knoten Maske* (eine Bitmaske), die die Gruppe von Knoten angibt, auf die der API-Befehl verweist. Jeder Knoten verfügt über einen NULL basierten Index. In der Knoten Maske wird jedoch 0 (null) in Bit 1 übersetzt. 1 übersetzt in Bit 2; Und so weiter.

### <a name="single-nodes"></a>Einzelne Knoten

Beim Aufrufen der folgenden (einzelnen Knoten) APIs gibt Ihre Anwendung einen einzelnen Knoten an, dem der API-Aufruf zugeordnet wird. In den meisten Fällen wird dies durch eine Knoten Maske angegeben. Jedes Bit in der Maske entspricht einem einzelnen Knoten. Für alle in diesem Abschnitt beschriebenen APIs muss in der Knoten Maske genau ein Bit festgelegt werden.

-   [**D3D12 \_ \_ \_ DESC der Befehls Warteschlange**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_queue_desc) : weist einen *nodemask* -Member auf.
-   [**Kreatecommandqueue**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandqueue) : erstellt eine Warteschlange aus einer [**D3D12-Befehls \_ Warteschlange \_ \_**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_queue_desc) -Struktur.
-   " [**Kreatecommandlist**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist) ": nimmt einen *nodemask* -Parameter an.
-   [**D3D12 \_ \_Deskriptorheap- \_ DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc) : weist einen *nodemask* -Member auf.
-   [**Kreatedescriptorheap**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createdescriptorheap) : erstellt einen deskriptorheap aus einer [**D3D12 \_ Deskriptor \_ - \_ Heap**](/windows/win32/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc) -Struktur.
-   [**D3D12 \_ \_Abfrageheap- \_ DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_query_heap_desc) : weist einen *nodemask* -Member auf.
-   " [**Kreatequeryheap**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createqueryheap) ": erstellt einen Abfrage Heap aus einer [**D3D12- \_ Abfrage Heap- \_ \_ debustruktur**](/windows/win32/api/d3d12/ns-d3d12-d3d12_query_heap_desc) .

### <a name="multiple-nodes"></a>Mehrere Knoten

Wenn Sie die folgenden APIs (mehrere Knoten) aufrufen, gibt Ihre Anwendung eine Gruppe von Knoten an, der der API-Aufruf zugeordnet wird. Sie geben die Knoten Affinität als Knoten Maske an, bei der möglicherweise mehrere Bits festgelegt sind. Wenn die Anwendung 0 für diese Bitmaske übergibt, konvertiert der Direct3D 12-Treiber diese in die Bitmaske 1 (gibt an, dass das Objekt mit Knoten 0 verknüpft ist).

-   [**D3D12 \_ \_Knoten übergreifende \_ Freigabe \_ Ebene**](/windows/win32/api/d3d12/ne-d3d12-d3d12_cross_node_sharing_tier) : bestimmt die Unterstützung für die Knoten übergreifende Freigabe.
-   [**D3D12 \_ Feature \_ Data \_ D3D12 \_ Optionen**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) : Struktur, die [**auf \_ D3D12 \_ Knoten übergreifende \_ Freigabe \_ Ebene**](/windows/win32/api/d3d12/ne-d3d12-d3d12_cross_node_sharing_tier)verweist.
-   [**D3D12 \_ \_ \_ Architektur von Featuredaten**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_architecture) : enthält ein *nodeindex* -Element.
-   [**D3D12 \_ \_ \_ Status \_ DESC der Grafik Pipeline**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) : weist einen *nodemask* -Member auf.
-   [**Kreategraphicspipelinestate**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) : erstellt ein Grafik Pipeline-Zustands Objekt aus einer [**D3D12- \_ Grafik \_ Pipeline State- \_ \_ DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) -Struktur.
-   [**D3D12 \_ Der COMPUTE- \_ Pipeline \_ Status \_ DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc) : weist einen *nodemask* -Member auf.
-   [**Kreatecomputepipelinestate**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate) : erstellt ein Compute Pipeline State-Objekt aus einer [**D3D12 \_ Compute \_ Pipeline \_ State \_**](/windows/win32/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc) -Struktur Struktur.
-   " [**Kreaterootsignature**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrootsignature)": nimmt einen *nodemask* -Parameter an.
-   [**D3D12 \_ Befehls \_ Signatur \_ DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_signature_desc): weist einen *nodemask* -Member auf.
-   [**Kreatecommandsignature**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandsignature) : erstellt ein Befehls Signatur Objekt aus einer [**D3D12- \_ Befehls \_ Signatur- \_ DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_signature_desc) -Struktur.

### <a name="resource-creation-apis"></a>APIs zum Erstellen von Ressourcen

Die folgenden APIs verweisen auf Knoten Masken.

-   [**D3D12 \_ Heap \_ Eigenschaften**](/windows/win32/api/d3d12/ns-d3d12-d3d12_heap_properties) : verfügt sowohl über die Member " *kreationnodemask* " als auch " *visiblenodemask* ".
-   [**Getresourcezucationinfo**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getresourceallocationinfo) : verfügt über einen *visiblemask* -Parameter.
-   [**Getcustomheapproperties**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getcustomheapproperties) : weist einen *nodemask* -Parameter auf.

Wenn Sie eine reservierte Ressource erstellen, wird kein Knoten Index oder keine Maske angegeben. Die reservierte Ressource kann einem Heap auf einem beliebigen Knoten zugeordnet werden (nach den Knoten übergreifenden Freigabe Regeln).

Die Methode " [**makeresident**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-makeresident) " funktioniert intern mit Adapter Warteschlangen, es ist nicht erforderlich, dass Ihre Anwendung für diese Angabe etwas angibt.

Wenn Sie die folgenden [**ID3D12Device**](/windows/win32/api/d3d12/nn-d3d12-id3d12device) -APIs aufrufen, muss Ihre Anwendung keinen Satz von Knoten angeben, mit denen der API-Aufruf verknüpft wird, da der API-Aufruf für alle Knoten gilt.

-   [**Erschluss**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createfence)
-   [**GetDescriptor handleinkrementsize**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize)
-   [**Setstablepowerstate**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-setstablepowerstate)
-   [**Checkfeaturesupport**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport)
-   [**"Kreatesampler"**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createsampler)
-   [**Copydescriptors**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-copydescriptors)
-   [**Copydescriptor ssimple**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple)
-   [**"Kreatesharedhandle"**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createsharedhandle)
-   [**Opensharedlenker byname**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-opensharedhandlebyname)
-   [**Opensharedhandle**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-opensharedhandle) : mit einem *Fence* als Parameter. Bei einer *Ressource* oder einem *Heap* als Parameter akzeptiert diese Methode keine Knoten als Parameter, da Knoten Masken von zuvor erstellten Objekten geerbt werden.
-   [**"Kreatecommandzucator"**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandallocator)
-   [**"Kreateconstantbufferview"**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createconstantbufferview)
-   [**"Kreaterendertargetview"**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrendertargetview)
-   [**"Kreateunorderedaccessview"**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview)
-   [**"Kreatedepthstencilview"**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createdepthstencilview)
-   [**"Kreateshaderresourceview"**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview)

## <a name="related-topics"></a>Verwandte Themen

[Direct3D 12-Programmier Handbuch](directx-12-programming-guide.md)