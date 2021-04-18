---
description: Dynamische Diagramm Bildung
ms.assetid: 13fed430-979b-40f7-91ba-aff2d811bd92
title: Dynamische Diagramm Bildung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 710bf5f648fc91e8db6bf62d81b41327f874ddf7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106344327"
---
# <a name="dynamic-graph-building"></a>Dynamische Diagramm Bildung

Wenn Sie ein vorhandenes Filter Diagramm ändern müssen, können Sie das Diagramm beenden, die Änderungen vornehmen und das Diagramm neu starten. Dies ist normalerweise der beste Ansatz. Unter bestimmten Umständen möchten Sie jedoch möglicherweise einen Graphen ändern, während er noch ausgeführt wird. Beispiel:

-   Die Anwendung fügt während der Wiedergabe einen Videoeffekt Filter ein.
-   Ein Quell Filter schaltet die Medientypen "Mittel Strom" ein und erfordert ggf. einen neuen Dekomprimierungs Filter.
-   Die Anwendung fügt dem Diagramm einen neuen Videostream hinzu.

Dabei handelt es sich um Beispiele für das *dynamische Graph-Gebäude*, einen Begriff, der alle Arten von Änderungen an einem Filter Diagramm abdeckt, während der Graph weiterhin ausgeführt wird. Die dynamische Diagramm Bildung kann von einer Anwendung oder einem Filter im Diagramm initiiert werden. Drei verschiedene Szenarien sind möglich:

-   [Dynamische Format Änderungen](dynamic-format-changes.md): ein Filter kann die Formatierungen von mittlerer Stream ändern, ohne dass Filter entfernt oder ersetzt werden müssen.
-   [Dynamische erneute Verbindung](dynamic-reconnection.md): das Diagramm wird durch Hinzufügen oder Entfernen von Filtern geändert.
-   [Filter Ketten](filter-chains.md): Hinzufügen, entfernen und Steuern von Filtern von Filtern.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu DirectShow](about-directshow.md)
</dt> </dl>

 

 



