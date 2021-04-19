---
description: Die Datei Gruppe der Tabellen enthält alle Windows Installer Tabellen, die sich auf Dateien beziehen.
ms.assetid: 8f56328e-ed58-41a1-94b6-266e9c117246
title: Datei Tabellen Gruppe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2667a1b9fe2bd9d2f8260523e2386bf7751dce8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355593"
---
# <a name="file-tables-group"></a>Datei Tabellen Gruppe

![Datei Tabellen Gruppe](images/filegrp.png)

Weitere Informationen zu diesem Diagramm finden Sie unter [Entity Relationship Diagram-Legende](entity-relationship-diagram-legend.md).

Ein Installer-Paket Entwickler sollte die Datei Tabellen Gruppe von Tabellen auffüllen, nachdem die Anwendung in [Komponenten und Funktionen](components-and-features.md) und nach dem Auffüllen der [Gruppe "Core Tables](core-tables-group.md)" unterteilt wurde. Die Datei Tabellen Gruppe enthält alle Dateien, die zur Installation gehören, und die meisten dieser Dateien sind in der [Dateitabelle](file-table.md)aufgeführt. Die [Verzeichnis Tabelle](directory-table.md) wird in der Abbildung nicht angezeigt, ist jedoch eng mit der Datei Tabellen Gruppe verknüpft. Die Verzeichnis Tabelle enthält die Verzeichnisstruktur der-Installation.

Die Datei Gruppe der Tabellen enthält alle Tabellen, die sich auf Dateien beziehen.

-   In der [Dateitabelle](file-table.md) sind die Dateien aufgelistet, die zur Installation gehören. Dateien, die nicht in der Dateitabelle aufgeführt sind, enthalten Datenträger Dateien, die in der Medien Tabelle aufgeführt sind. Da jede Datei zu einer Komponente gehört, weist die Dateitabelle einen externen Schlüssel in die Komponenten Tabelle auf.
-   Die [Tabelle RemoveFile](removefile-table.md) enthält eine Liste der Dateien, die von der [RemoveFiles-Aktion](removefiles-action.md)entfernt werden sollen.
-   In der [Schriftart Tabelle](font-table.md) sind die Schriftart Dateien aufgelistet, die beim System registriert werden sollen.
-   In der [Tabelle selfreg](selfreg-table.md) sind die Moduldateien der Installation aufgeführt, die selbst registriert sind.
-   In der [Medien Tabelle](media-table.md) werden die Quell Medien und die Datenträger aufgelistet, die zur Installation gehören.
-   In der [Tabelle BindImage](bindimage-table.md) sind Dateien aufgelistet, die an DLLs gebunden sind, die von ausführbaren Dateien importiert wurden.
-   In der [Tabelle "muvefile](movefile-table.md) " wird angegeben, welche Dateien während der Installation verschoben werden.
-   Die [duplicatefile-Tabelle](duplicatefile-table.md) gibt an, welche Dateien während der Installation dupliziert werden.
-   In der [Tabelle IniFile](inifile-table.md) werden die INI-Dateien und die Informationen aufgelistet, die von der Anwendung in der Datei festgelegt werden müssen.
-   Die [removeinifile-Tabelle](removeinifile-table.md) enthält die Informationen, die eine Anwendung aus einer INI-Datei löschen muss.
-   Die [Umgebungs Tabelle](environment-table.md) wird verwendet, um die Werte von Umgebungsvariablen festzulegen.
-   Die [Symboltabelle](icon-table.md) enthält Symbol Informationen, die als Teil der Produktankündigung in eine Datei kopiert werden.
-   In der [filesfpcatalog-Tabelle](filesfpcatalog-table.md) werden angegebene Dateien mit Katalogdateien für den Systemdatei Schutz verknüpft.

    **Windows Vista, Windows Server 2003 und Windows XP:** Nicht unterstützt.

-   Die [sfpcatalog-Tabelle](sfpcatalog-table.md) enthält Kataloge zum Systemdatei Schutz.

    **Windows Vista, Windows Server 2003 und Windows XP:** Nicht unterstützt.

-   Die [msiflehash-Tabelle](msifilehash-table.md) wird zum Speichern eines 128-Bit-Hashs einer Quelldatei verwendet, die vom Windows Installer Paket bereitgestellt wird.

 

 



