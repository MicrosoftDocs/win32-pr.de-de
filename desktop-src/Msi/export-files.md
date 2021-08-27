---
description: Die VBScript-Datei WiExport.vbs wird in den Windows SDK-Komponenten für Windows Installer-Entwickler bereitgestellt.
ms.assetid: 3ff7bd48-cb22-4d5b-a607-39eaeb67c55b
title: Exportieren von Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de7cab882778bce6d84412f53987c65211f70f4a8a10b52836ad993d8e813304
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044440"
---
# <a name="export-files"></a>Exportieren von Dateien

Die VBScript-Datei WiExport.vbs wird in den [Windows SDK-Komponenten für Windows Installer-Entwickler](platform-sdk-components-for-windows-installer-developers.md)bereitgestellt. In diesem Beispiel wird gezeigt, wie Skripts zum Exportieren von Tabellen in eine Windows Installer-Datenbank geschrieben werden. Das Skriptbeispiel stellt eine Verbindung mit einem [**Installer-Objekt**](installer-object.md) her, öffnet eine Datenbank und exportiert Tabellen in Archivdateien.

Das Beispiel veranschaulicht die Verwendung von:

-   [**OpenDatabase-Methode (Installer-Objekt)**](installer-opendatabase.md)
-   [**LastErrorRecord-Methode**](installer-lasterrorrecord.md) des [ **Installer-Objekts**](installer-object.md)
-   [**Exportmethode**](database-export.md)
-   [**OpenView-Methode**](database-openview.md) des [ **Database-Objekts**](database-object.md)
-   [**Fetch-Methode**](view-fetch.md) des [ **View-Objekts**](view-object.md)
-   [**StringData-Eigenschaft**](record-stringdata.md) des [ **Record-Objekts**](record-object.md)

Sie benötigen die CScript.exe oder WScript.exe Version von Windows Script Host, um dieses Beispiel zu verwenden. Um CScript.exe zum Ausführen dieses Beispiels zu verwenden, geben Sie eine Befehlszeile an der Eingabeaufforderung mit der folgenden Syntax ein. Hilfe wird angezeigt, wenn das erste Argument /? ist. oder , wenn zu wenige Argumente angegeben werden. Um die Ausgabe an eine Datei umzuleiten, beenden Sie die Befehlszeile mit VBS > \[ *Pfad zur Datei* \] . Das Beispiel gibt den Wert 0 für den Erfolg zurück, 1, wenn die Hilfe aufgerufen wird, und 2, wenn das Skript fehlschlägt.

**cscript WiExport.vbs \[ Pfad zum \] \[ Datenbankpfad zur Liste der \] \[ \] Tabellennamen der Ordneroptionen \[\]**

Geben Sie den Pfad zur Installationsdatenbank an, aus der die Tabellen exportiert werden. Geben Sie den Pfad zum Ordner an, in den die exportierten Archivdateien kopiert werden sollen. Listen Sie die Namen der zu exportierenden [Datenbanktabellen](database-tables.md) auf, bei der die Groß-/Kleinschreibung beachtet wird. Geben Sie " \* " an, um alle Tabellen einschließlich \_ SummaryInformation zu exportieren.

Die folgenden Optionen können an einer beliebigen Stelle in der Befehlszeile vor der Tabellennamenliste angegeben werden.



| Option              | BESCHREIBUNG                                            |
|---------------------|--------------------------------------------------------|
| Keine Option angegeben | Exportierte Archivdateien können einen langen Dateinamen aufweisen.      |
| /s                  | Erzwingen Sie, dass exportierte Archivdateien kurze Dateinamen aufweisen. |



 

Weitere Skriptbeispiele finden Sie unter [Windows Installer Scripting Examples](windows-installer-scripting-examples.md). Beispielhilfsprogramme, die Windows Script Host nicht benötigen, finden Sie unter [Windows Installer Development Tools](windows-installer-development-tools.md).

 

 



