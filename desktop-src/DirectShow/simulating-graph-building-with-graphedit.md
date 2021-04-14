---
description: Simulieren der Diagramm Erstellung mit GraphEdit
ms.assetid: 3f7d3079-3d3d-4b93-9ab7-4c03def7c4be
title: Simulieren der Diagramm Erstellung mit GraphEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f76878997c873c74d454979ccda689a9c241489d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481966"
---
# <a name="simulating-graph-building-with-graphedit"></a>Simulieren der Diagramm Erstellung mit GraphEdit

DirectShow bietet ein debughilfsprogramm mit dem Namen GraphEdit, das Sie zum Erstellen und Testen von Filter Diagrammen verwenden können.

GraphEdit ist ein visuelles Tool zum Entwickeln von Filter Diagrammen. Mit GraphEdit können Sie mit einem Filter Diagramm experimentieren, bevor Sie Anwendungscode schreiben. Sie können auch ein Filter Diagramm laden, das von der Anwendung erstellt wird, um zu überprüfen, ob die Anwendung das richtige Diagramm erstellt. Wenn Sie einen benutzerdefinierten Filter entwickeln, bietet GraphEdit eine schnelle Möglichkeit, Sie zu testen: Laden Sie einfach ein Diagramm mit Ihrem benutzerdefinierten Filter, und führen Sie das Diagramm aus. Wenn Sie mit DirectShow noch nicht vertraut sind, ist GraphEdit eine gute Möglichkeit, sich mit Filter Diagrammen und der DirectShow-Architektur vertraut zu machen.

Die folgende Abbildung zeigt, wie GraphEdit ein einfaches Filter Diagramm darstellt.

![einfaches Filter Diagramm in GraphEdit](images/gedit09.png)

Jeder Filter wird als Rechteck dargestellt. Kleinere Quadrate entlang der Kanten der Filter stellen Pins dar. Eingabe Pins befinden sich auf der linken Seite des Filters, und die Ausgabe Pins befinden sich auf der rechten Seite. Die Pfeile stellen die Verbindungen zwischen Pins dar.

Mit GraphEdit können Sie folgende Aktionen ausführen:

-   Erstellen und Ändern von Filter Diagrammen mithilfe einer visuellen Drag & amp; Drop-Schnittstelle.
-   Simulieren Sie programmgesteuerte Aufrufe, um ein Diagramm zu erstellen.
-   Ausführen, anhalten, anhalten und Suchen eines Diagramms.
-   Sehen Sie sich an, welche Filter auf Ihrem Computer registriert sind, und zeigen Sie Registrierungsinformationen für die einzelnen Filter an.
-   Filtereigenschaften Seiten anzeigen.
-   Zeigen Sie die Medientypen der PIN-Verbindungen an.

Dieser Abschnitt enthält die folgenden Themen:

-   [Verwenden von GraphEdit](using-graphedit.md)
-   [Laden eines Diagramms aus einem externen Prozess](loading-a-graph-from-an-external-process.md)
-   [Speichern eines Filter Diagramms in einer GraphEdit-Datei](saving-a-filter-graph-to-a-graphedit-file.md)
-   [Programm gesteuertes Laden einer GraphEdit-Datei](loading-a-graphedit-file-programmatically.md)
-   [GraphEdit-Datei Format](graphedit-file-format.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von DirectShow](using-directshow.md)
</dt> </dl>

 

 



