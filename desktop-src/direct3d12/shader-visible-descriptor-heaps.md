---
title: Für den Shader sichtbare Deskriptorheaps
description: Shader-sichtbare Deskriptor-Heaps sind Deskriptorhaps, auf die von Shadern über Deskriptortabellen verwiesen werden kann.
ms.assetid: 37691fd1-212d-4786-ac9c-861c1a6a4918
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96fbbb37f3337912780e5882918c0fcbc146c41f8dc60ddf3ba5d2a35c82c1bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045392"
---
# <a name="shader-visible-descriptor-heaps"></a>Für den Shader sichtbare Deskriptorheaps

Shader-sichtbare Deskriptor-Heaps sind Deskriptorhaps, auf die von Shadern über Deskriptortabellen verwiesen werden kann.

-   [Übersicht](#overview)
-   [Beispiel](#an-example)
-   [Zugehörige Themen](#related-topics)

## <a name="overview"></a>Übersicht

Deskriptor-Heaps, auf die von Shadern über Deskriptortabellen verwiesen werden kann, haben eine Reihe von Varianten: Ein Heaptyp, D3D12 \_ SRV \_ UAV \_ CBV \_ DESCRIPTOR \_ HEAP, kann Shaderressourcenansichten, ungeordnete Zugriffsansichten und konstante Pufferansichten enthalten, die alle miteinander vermischen. Jeder speicherort im Heap kann einer der aufgeführten Typen von Deskriptoren sein. Ein anderer Heaptyp, D3D12 DESCRIPTOR HEAP TYPE SAMPLER, speichert nur Sampler, was die Tatsache zeigt, dass Sampler für den Großteil der Hardware getrennt von \_ \_ \_ \_ SRVs, UAVs und CBVs verwaltet werden.

Deskriptor-Heaps dieser Typen können angefordert werden, dass sie beim Erstellen des Heaps shader sichtbar sind oder nicht (letzteres – nicht shader sichtbar – kann für Stagingdeskriptoren auf der CPU nützlich sein). Wenn angefordert wird, dass der Shader sichtbar ist, kann jeder der oben genannten Heaptypen eine Hardwaregrößenbeschränkung für jede einzelne Deskriptor-Heapzuordnung haben.

Anwendungen können eine beliebige Anzahl von Deskriptor-Heaps erstellen, und nicht im Shader sichtbare Deskriptor-Heaps sind nicht in der Größe eingeschränkt. Wenn ein von der Anwendung erstellter sichtbarer Shaderdeskriptor-Heap kleiner als das Hardwaregrößenlimit ist, kann der Treiber den Deskriptorhap aus einem größeren zugrunde liegenden Deskriptorhap unterteilen, damit mehrere API-Deskriptorhaps in einen Hardwaredeskriptor-Heap passen. Dies kann der Grund dafür sein, dass für einige Hardware das Wechseln zwischen Hardwaredeskriptor-Heaps während der Ausführung eine GPU-Wartezeit für den Leerlauf erfordert (um sicherzustellen, dass GPU-Verweise auf den vorherigen Deskriptor-Heap beendet sind). Wenn alle deskriptor heaps, die eine Anwendung erstellt, in die maximalen Kapazitäten des entsprechenden Hardwarehaps passen, treten keine solchen Wartevorgänge auf, wenn api-Deskriptorhaps während des Renderings umgestellt werden. Anwendungen müssen jedoch die Möglichkeit zulassen, dass das Wechseln des aktuellen Deskriptorhaps zu einer Wartezeit im Leerlauf werden kann.

Um zu vermeiden, dass diese mögliche Wartezeit auf den Leerlauf auf dem Deskriptor-Heapschalter negativ ist, können Anwendungen Unterbrechungen beim Rendering nutzen, die dazu führen würden, dass sich die GPU aus anderen Gründen im Leerlauf befindet, da die Zeit zum Ausführen von Deskriptor-Heaps wechselt, da das Warten auf den Leerlauf trotzdem stattfindet.

Der Mechanismus und die Semantik zum Identifizieren von Deskriptorhaps für Shader während der Befehlslisten-/Bündelaufzeichnung werden in der API-Referenz beschrieben.

## <a name="an-example"></a>Beispiel

Die folgende Abbildung zeigt zwei Deskriptorhaps, die auf zwei separate 2D-Texturen verweisen, die in zwei Slots eines großen Standardhaps gespeichert werden. Auf den deskriptor-Heap, der im Shader sichtbar ist, kann von der Grafikpipeline (einschließlich der Shader) zugegriffen werden. Daher ist die 2D-Textur für die Pipeline verfügbar.

![Sichtbare und nicht sichtbare Deskriptorhaps](images/descriptor-heaps.png)

> [!Note]  
> Für Deskriptor-Heaps gilt häufig eine Beschränkung der GPU-Hardware für die Menge des lokalen GPU-Arbeitsspeichers, der von der CPU geschrieben werden kann (als kombinierter Speicher mit Schreibzugriff bezeichnet). In der Regel beträgt dieser Grenzwert für alle Prozesse etwa 96 MB. Ein 1 Million Memberdeskriptor-Heap mit 32-Byte-Deskriptoren würde z. B. bis zu 32 MB verwenden. Der Treiber wird bei Bedarf auf den Systemspeicher zurückfallen. Es ist jedoch eine bewährte Methode, keine große Anzahl von Deskriptor-Heaps zu erstellen.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Deskriptorheaps](descriptor-heaps.md)
</dt> </dl>

 

 




