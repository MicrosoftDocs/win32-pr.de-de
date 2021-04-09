---
description: Die Windows Installer-Datenbank besteht aus vielen miteinander verknüpften Tabellen, die zusammen eine relationale Datenbank mit den für die Installation einer Gruppe von Anwendungen erforderlichen Informationen bilden.
ms.assetid: 3352dd8f-c082-4c4b-98be-5823c8b28f07
title: Informationen zur Installer-Datenbank
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7f0ee2cc326f85d964ac3d845b97751a48fbb91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864535"
---
# <a name="about-the-installer-database"></a>Informationen zur Installer-Datenbank

Die Windows Installer-Datenbank besteht aus vielen miteinander verknüpften Tabellen, die zusammen eine relationale Datenbank mit den für die Installation einer Gruppe von Anwendungen erforderlichen Informationen bilden. Da die Datenbank relational ist, werden die Tabellen über die Daten in den Primär-und Fremdschlüssel Werten verknüpft. Dies stellt eine effiziente Methode zum Ändern des Installationsvorgangs dar und bedeutet, dass Benutzer eine große Anwendung oder Anwendungs Gruppe leichter anpassen können. Die Datenbanktabellen spiegeln das allgemeine Layout der gesamten Gruppe von Anwendungen wider, einschließlich:

-   Verfügbare Features
-   Komponenten
-   Beziehung zwischen Features und Komponenten
-   Erforderliche Registrierungs Einstellungen
-   Benutzeroberfläche für die Anwendung

Zum Erstellen einer Installations Datenbank müssen Sie die Tabellen mit allen Informationen über die Anwendungen und den Installationsvorgang auffüllen. Das manuelle Erstellen dieser Tabellen wird zu einer großen Aufgabe, auch bei einer mittleren Größen Installation. Daher stehen einige Tools von Drittanbietern zur Verfügung, die Sie beim Aufbau der Installer-Datenbank unterstützen. In den folgenden Abschnitten werden Gruppen verwandter Datenbanktabellen beschrieben.

[Kern Tabellen Gruppe](core-tables-group.md)

[Datei Tabellen Gruppe](file-tables-group.md)

[Registrierungs Tabellen Gruppe](registry-tables-group.md)

[System Tabellen Gruppe](system-tables-group.md)

[Locator-Tabellen Gruppe](locator-tables-group.md)

[Gruppe "Programm Informationstabellen"](program-information-tables-group.md)

[Gruppe "Installationsprozedur Tabellen"](installation-procedure-tables-group.md)

[Legende des Entitäts Beziehungs Diagramms](entity-relationship-diagram-legend.md)

[Text Archivdateien](text-archive-files.md)

Eine vollständige Liste aller Tabellen in einer-Installations Datenbank finden Sie unter [Datenbanktabellen](database-tables.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Veröffentlichte Versionen, Tools und verteilbare Dateien](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



