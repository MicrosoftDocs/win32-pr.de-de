---
description: Die Dateigruppe der Tabellen enthält alle tabellenbezogenen Windows Installer-Tabellen, die mit Dateien verknüpft sind.
ms.assetid: 8f56328e-ed58-41a1-94b6-266e9c117246
title: Dateitabellengruppe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3f8a73aa46b202d184356c14ff12da9ce9ce9880b009418e922b252cc35bc54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118142904"
---
# <a name="file-tables-group"></a>Dateitabellengruppe

![Dateitabellengruppe](images/filegrp.png)

Weitere Informationen zu diesem Diagramm finden Sie in der Legende [des Entitätsbeziehungsdiagramms.](entity-relationship-diagram-legend.md)

Ein Installer-Paketentwickler sollte erwägen, die Dateitabellengruppe von [](components-and-features.md) Tabellen nach dem Aufteilen der Anwendung in Komponenten und Features und nach dem Aufpopulieren der Kerntabellengruppe [aufpopulieren.](core-tables-group.md) Die Dateitabellengruppe enthält alle Dateien, die zur Installation gehören, und die meisten dieser Dateien sind in der [Dateitabelle aufgeführt.](file-table.md) Die [Tabelle Directory](directory-table.md) wird in der Abbildung nicht angezeigt, ist aber eng mit der Dateitabellengruppe verknüpft. Die Tabelle Directory gibt die Verzeichnisstruktur der Installation an.

Die Dateigruppe der Tabellen enthält alle Tabellen, die mit Dateien verknüpft sind.

-   In [der Tabelle Datei](file-table.md) werden dateien aufgeführt, die zur Installation gehören. Dateien, die nicht in der Tabelle Datei aufgeführt sind, enthalten Datenträgerdateien, die in der Medientabelle aufgeführt sind. Da jede Datei zu einer Komponente gehört, verfügt die Dateitabelle über einen externen Schlüssel in der Component-Tabelle.
-   Die [RemoveFile-Tabelle](removefile-table.md) enthält eine Liste der Dateien, die von der [RemoveFiles-Aktion entfernt werden sollen.](removefiles-action.md)
-   In [der Tabelle Schriftart](font-table.md) werden Schriftartdateien aufgeführt, die beim System registriert werden sollen.
-   In [der Tabelle SelfReg sind](selfreg-table.md) die Moduldateien der Installation aufgeführt, die selbst registriert sind.
-   In [der Tabelle Medien](media-table.md) werden die Quellmedien und Datenträger aufgeführt, die zur Installation gehören.
-   In [der Tabelle BindImage werden](bindimage-table.md) Dateien aufgeführt, die an von ausführbaren Dateien importierte DLLs gebunden sind.
-   Die [Tabelle MoveFile gibt](movefile-table.md) an, welche Dateien während der Installation verschoben werden.
-   Die [Tabelle DuplicateFile gibt](duplicatefile-table.md) an, welche Dateien während der Installation dupliziert werden.
-   In [der Tabelle IniFile sind](inifile-table.md) die .ini dateien und die Informationen aufgeführt, die die Anwendung in der Datei festlegen muss.
-   Die [RemoveIniFile-Tabelle](removeinifile-table.md) enthält die Informationen, die eine Anwendung aus einer .ini löschen muss.
-   Die [Tabelle Umgebung](environment-table.md) wird zum Festlegen der Werte von Umgebungsvariablen verwendet.
-   Die [Tabelle Symbol enthält](icon-table.md) Symbolinformationen, die als Teil der Produktanzeige in eine Datei kopiert werden.
-   Die [Tabelle FileSFPCatalog ordnet](filesfpcatalog-table.md) angegebene Dateien den Katalogdateien des Systemdateischutzes zu.

    **Windows Vista, Windows Server 2003 und Windows XP:** Nicht unterstützt.

-   Die [Tabelle SFPCatalog enthält](sfpcatalog-table.md) Systemdateischutzkataloge.

    **Windows Vista, Windows Server 2003 und Windows XP:** Nicht unterstützt.

-   Die [MsiFileHash-Tabelle](msifilehash-table.md) wird verwendet, um einen 128-Bit-Hash einer Quelldatei zu speichern, die vom Paket Windows Installer bereitgestellt wird.

 

 



