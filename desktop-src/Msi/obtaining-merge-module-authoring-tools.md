---
description: Um ein Mergemodul zu generieren, müssen Sie ein Softwaretool abrufen, mit dem Sie eine MSM-Datei bearbeiten können.
ms.assetid: bc14d36a-b299-4c61-ade2-43fad142d21d
title: Abrufen der Erstellungstools für Mergemodule
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a85fb75c0317a6737393e67f12a7a03cd8b76c68a8261c9d26d10d06cbe484c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119327880"
---
# <a name="obtaining-merge-module-authoring-tools"></a>Abrufen der Erstellungstools für Mergemodule

Um ein Mergemodul zu generieren, müssen Sie ein Softwaretool abrufen, mit dem Sie eine MSM-Datei bearbeiten können. Da eine MSM-Datei im Grunde eine vereinfachte .msi ist, können Sie möglicherweise die gleichen Tools verwenden, die zum Erstellen einer Installationsdatenbank verwendet werden. Beispielsweise wird die Anwendung Orca.exe mit dem Windows Installer SDK bereitgestellt.

Alternativ können Sie eines der Installationspakettools erwerben, das von unabhängigen Softwareherstellern zur Verfügung gestellt werden kann. Es gibt mehrere Drittanbietertools in der Entwicklung, die zum Erstellen von Mergemodulen verwendet werden können. Wenn Sie sich für die Verwendung eines Drittanbietertools entscheiden, sollten Sie überprüfen, ob Mergemodule generiert werden, die mit dem in diesem Dokument beschriebenen Standard übereinstimmen. Insbesondere sollten Sie feststellen, dass die Bearbeitungstools keine der folgenden Schritte für das Mergemodul durchgeführt haben.

-   Dem Mergemodul wurden zusätzliche Tabellen hinzugefügt, auf die in der [ModuleIgnoreTable-Tabelle](moduleignoretable-table.md)nicht verwiesen wird.

    Löschen Sie diese Tabellen, oder fügen Sie sie der Tabelle ModuleIgnoreTable hinzu.

-   Dem Mergemodul wurde [eine unnötige TextStyle-Tabelle](textstyle-table.md) hinzugefügt.

    Wenn Ihr Mergemodul über keine Benutzeroberfläche verfügt (und dies im Allgemeinen nicht der Fall sein sollte), können Sie diese Tabelle problemlos löschen.

-   Unnötige Einträge zur [Verzeichnistabelle hinzugefügt.](directory-table.md)

    Entfernen Sie unnötige Einträge aus der Directory-Tabelle.

-   Informationen wurden aus der Validierungstabelle des \_ Mergemoduls verlassen.

    Dadurch wird die Überprüfung des Mergemoduls verhindert. Fügen Sie eine vollständige \_ Validierungstabelle hinzu.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen von Benutzeroberflächen in Mergemodulen](authoring-user-interfaces-in-merge-modules.md)
</dt> <dt>

[Erstellen von Verzeichnistabellen für Mergemodule](authoring-merge-module-directory-tables.md)
</dt> <dt>

[Überprüfen von Mergemodulen](validating-merge-modules.md)
</dt> </dl>

 

 



