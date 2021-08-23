---
description: Simulieren von Graph Building mit GraphEdit
ms.assetid: 3f7d3079-3d3d-4b93-9ab7-4c03def7c4be
title: Simulieren von Graph Building mit GraphEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff4f5bee201e2bd5b771348596b46caa513944aa148c7ec17a9e2974a360e60c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119583195"
---
# <a name="simulating-graph-building-with-graphedit"></a>Simulieren von Graph Building mit GraphEdit

DirectShow bietet ein Debug-Hilfsprogramm namens GraphEdit, mit dem Sie Filterdiagramme erstellen und testen können.

GraphEdit ist ein visuelles Tool zum Erstellen von Filterdiagrammen. Mit GraphEdit können Sie mit einem Filterdiagramm experimentieren, bevor Sie Anwendungscode schreiben. Sie können auch ein Von Ihrer Anwendung erstelltes Filterdiagramm laden, um zu überprüfen, ob ihre Anwendung das richtige Diagramm erstellt. Wenn Sie einen benutzerdefinierten Filter entwickeln, bietet GraphEdit eine schnelle Möglichkeit zum Testen: Laden Sie einfach ein Diagramm mit Ihrem benutzerdefinierten Filter, und versuchen Sie, das Diagramm zu verwenden. Wenn Sie noch nicht mit DirectShow vertraut sind, ist GraphEdit eine gute Möglichkeit, sich mit Filterdiagrammen und der DirectShow-Architektur vertraut zu machen.

Die folgende Abbildung zeigt, wie GraphEdit ein einfaches Filterdiagramm darstellt.

![Einfaches Filterdiagramm in graphedit](images/gedit09.png)

Jeder Filter wird als Rechteck dargestellt. Kleinere Quadrate entlang der Ränder der Filter stellen Stecknadeln dar. Eingabepins befinden sich auf der linken Seite des Filters, und Ausgabepins befinden sich auf der rechten Seite. Die Pfeile stellen die Verbindungen zwischen Stecknadeln dar.

Mit GraphEdit haben Sie folgende Folgendes:

-   Erstellen und Ändern von Filterdiagrammen mithilfe einer grafischen Drag & Drop-Schnittstelle.
-   Simulieren Sie programmgesteuerte Aufrufe, um ein Diagramm zu erstellen.
-   Ausführen, Anhalten, Beenden und Suchen eines Graphen.
-   Sehen Sie sich an, welche Filter auf Ihrem Computer registriert sind, und zeigen Sie Registrierungsinformationen für jeden Filter an.
-   Anzeigen von Filtereigenschaftsseiten.
-   Zeigen Sie die Medientypen von Pinverbindungen an.

Dieser Abschnitt enthält die folgenden Themen:

-   [Verwenden von GraphEdit](using-graphedit.md)
-   [Laden einer Graph aus einem externen Prozess](loading-a-graph-from-an-external-process.md)
-   [Speichern eines Filterfilters Graph in einer GraphEdit-Datei](saving-a-filter-graph-to-a-graphedit-file.md)
-   [Programmgesteuertes Laden einer GraphEdit-Datei](loading-a-graphedit-file-programmatically.md)
-   [GraphEdit-Dateiformat](graphedit-file-format.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von DirectShow](using-directshow.md)
</dt> </dl>

 

 



