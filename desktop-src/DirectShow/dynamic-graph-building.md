---
description: Erstellen dynamischer Graph
ms.assetid: 13fed430-979b-40f7-91ba-aff2d811bd92
title: Erstellen dynamischer Graph
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8c7296b95bc97461eb5a16ee577acb4bd267ee1a25f9be357a00fef7d4bdba5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118652790"
---
# <a name="dynamic-graph-building"></a>Erstellen dynamischer Graph

Wenn Sie ein vorhandenes Filterdiagramm ändern müssen, können Sie das Diagramm beenden, die Änderungen vornehmen und das Diagramm neu starten. Dies ist in der Regel der beste Ansatz. Unter bestimmten Umständen können Sie jedoch ein Diagramm ändern, während es noch ausgeführt wird. Beispiel:

-   Die Anwendung fügt während der Wiedergabe einen Filter für Videoeffekte ein.
-   Ein Quellfilter schaltet medientyps midstream um, sodass möglicherweise ein neuer Dekomprimierungsfilter erforderlich ist.
-   Die Anwendung fügt dem Diagramm einen neuen Videostream hinzu.

Dies sind alle Beispiele für die *dynamische Grapherstellung,* ein Begriff, der jede Art von Änderung an einem Filterdiagramm abdeckt, während der Graph weiterhin ausgeführt wird. Die dynamische Grapherstellung kann von einer Anwendung oder einem Filter im Diagramm initiiert werden. Es sind drei verschiedene Szenarien möglich:

-   [Dynamische Formatänderungen:](dynamic-format-changes.md)Ein Filter kann formate midstream ändern, ohne Filter entfernen oder ersetzen zu müssen.
-   [Dynamische Wiederherstellung der Verbindung:](dynamic-reconnection.md)Ändern des Diagramms durch Hinzufügen oder Entfernen von Filtern.
-   [Filterketten:](filter-chains.md)Hinzufügen, Entfernen und Steuern von Filterketten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu DirectShow](about-directshow.md)
</dt> </dl>

 

 



