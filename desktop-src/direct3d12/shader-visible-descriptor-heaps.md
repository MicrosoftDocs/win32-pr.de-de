---
title: Shader sichtbare deskriptorheaps
description: Shader sichtbare deskriptorheaps, sind deskriptorheaps, auf die Shader durch deskriptortabellen verweisen können.
ms.assetid: 37691fd1-212d-4786-ac9c-861c1a6a4918
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e650d324f0826e00d8ffff08348597112f6d5cc4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103723"
---
# <a name="shader-visible-descriptor-heaps"></a>Shader sichtbare deskriptorheaps

Shader sichtbare deskriptorheaps, sind deskriptorheaps, auf die Shader durch deskriptortabellen verweisen können.

-   [Übersicht](#overview)
-   [Beispiel](#an-example)
-   [Verwandte Themen](#related-topics)

## <a name="overview"></a>Überblick

Deskriptorheaps, auf die durch Shader durch deskriptortabellen verwiesen werden kann, sind in einigen Varianten enthalten: ein heaptyp, der D3D12 \_ SRV \_ UAV \_ CBV- \_ \_ deskriptorheap, kann Shader-Ressourcen Sichten, ungeordnete Zugriffs Sichten und Konstante Puffer Ansichten enthalten, die alle gemischt sind. Jeder angegebene Speicherort im Heap kann einer der aufgelisteten deskriptortypen sein. Ein anderer heaptyp, D3D12 \_ Descriptor \_ Heap \_ Type \_ Sampler, speichert nur Samplern. Dies spiegelt die Tatsache wider, dass Samplern bei der Mehrzahl der Hardware getrennt von Srvs, UAVs, cbvs verwaltet werden.

Deskriptorheaps dieser Typen können als Shader angezeigt werden, oder nicht, wenn der Heap erstellt wird (der zweite – nicht-Shader, der für die stagingdeskriptoren auf der CPU sichtbar ist). Bei angeforderter Shader-Anforderung kann jeder der oben genannten Heap Typen eine Hardware Größenbeschränkung für jede einzelne deskriptorheap-Zuordnung aufweisen.

Anwendungen können eine beliebige Anzahl von deskriptorheaps erstellen, und nicht Shader sichtbare deskriptorheaps sind nicht in der Größe beschränkt. Wenn ein vom Shader sichtbarer deskriptorheap, der von der Anwendung erstellt wird, kleiner ist als das Limit für die Hardware Größe, kann der Treiber den deskriptorheap aus einem größeren zugrunde liegenden deskriptorheap unterzuordnen, sodass mehrere API-deskriptorheaps in einen Hardware deskriptorheap passen. Der Grund hierfür ist, dass für einige Hardware bei der Umstellung zwischen den Hardware Deskriptor-Heaps während der Ausführung eine GPU-Wartezeit für den Leerlauf erforderlich ist (um sicherzustellen, dass GPU-Verweise auf den zuvor deskriptorheap abgeschlossen sind). Wenn alle deskriptorheaps, die von einer Anwendung erstellt werden, in die maximalen Kapazitäten des betreffenden Hardware Heaps passen, werden beim Wechseln von API-deskriptorheaps während des Renderings keine solchen warte Vorgänge ausgeführt. Anwendungen müssen jedoch die Möglichkeit zulassen, dass durch das Wechseln des aktuellen deskriptorheaps eine Wartezeit auf den Leerlauf verursacht wird.

Um zu vermeiden, dass diese mögliche Wartezeit auf den deskriptorheap-Schalter beeinträchtigt wird, können Anwendungen die Unterbrechung beim Rendering ausnutzen, die dazu führen, dass sich die GPU aus anderen Gründen im Leerlauf befindet.

Der Mechanismus und die Semantik zum Identifizieren von deskriptorheaps für Shader während der Befehlsliste/Paket Aufzeichnung werden in der API-Referenz beschrieben.

## <a name="an-example"></a>Beispiel

Die folgende Abbildung zeigt zwei deskriptorheaps, die auf zwei separate 2D-Texturen verweisen, die in zwei Slots eines großen Standard Heaps gespeichert werden. Der deskriptorheap, der als Shader sichtbar ist, kann von der Grafik Pipeline (einschließlich der Shader) aufgerufen werden. Daher ist die 2D-Textur für die Pipeline verfügbar.

![sichtbare und nicht sichtbare deskriptorheaps](images/descriptor-heaps.png)

> [!Note]  
> Es gibt oftmals eine Beschränkung der GPU-Hardware, die von der CPU (als Schreib kombinierter Arbeitsspeicher bezeichnet) für deskriptorheaps beschreibbar ist. In der Regel beträgt dieser Grenzwert bei allen Prozessen etwa 96 MB. Ein 1 Million-Member-deskriptorheap mit 32-Byte-Deskriptoren verwendet beispielsweise bis zu 32 MB. Der Treiber wird bei Bedarf auf den System Arbeitsspeicher zurückgreifen, aber es wird empfohlen, keine große Anzahl von großen deskriptorheaps zu erstellen.

 

## <a name="related-topics"></a>Verwandte Themen

<dl> <dt>

[Deskriptorheaps](descriptor-heaps.md)
</dt> </dl>

 

 




