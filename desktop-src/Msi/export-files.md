---
description: Die VBScript-Datei WiExport.vbs wird in den Windows SDK Komponenten für Windows Installer Entwickler bereitgestellt.
ms.assetid: 3ff7bd48-cb22-4d5b-a607-39eaeb67c55b
title: Dateien exportieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1512650ee144fc00c2de851051b9bbb4d98a21e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343401"
---
# <a name="export-files"></a>Dateien exportieren

Die VBScript-Datei WiExport.vbs wird in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md)bereitgestellt. Dieses Beispiel zeigt, wie Sie ein Skript schreiben, um Tabellen in eine Windows Installer Datenbank zu exportieren. Das Skript Beispiel stellt eine Verbindung mit einem [**Installer**](installer-object.md) -Objekt her, öffnet eine Datenbank und exportiert Tabellen in Archivdateien.

Das Beispiel veranschaulicht die Verwendung von:

-   [**OpenDatabase-Methode (Installer-Objekt)**](installer-opendatabase.md)
-   [**Lasterrorrecord-Methode**](installer-lasterrorrecord.md) des [ **Installer-Objekts**](installer-object.md)
-   [**Export Methode**](database-export.md)
-   [**OpenView-Methode**](database-openview.md) des [ **Datenbankobjekts**](database-object.md)
-   [**Fetch-Methode**](view-fetch.md) des [ **View-Objekts**](view-object.md)
-   [**StringData-Eigenschaft**](record-stringdata.md) des [ **Datensatz-Objekts**](record-object.md)

Sie benötigen die CScript.exe oder WScript.exe Version von Windows Script Host, um dieses Beispiel zu verwenden. Wenn Sie CScript.exe verwenden möchten, um dieses Beispiel auszuführen, geben Sie mithilfe der folgenden Syntax eine Befehlszeile an der Eingabeaufforderung ein. Hilfe wird angezeigt, wenn das erste Argument/? oder, wenn zu wenige Argumente angegeben werden. Um die Ausgabe in eine Datei umzuleiten, beenden Sie die Befehlszeile mit VSB > \[ *Pfad zur Datei* \] . Das Beispiel gibt den Wert 0 für Erfolg zurück, 1, wenn Hilfe aufgerufen wird, und 2, wenn das Skript fehlschlägt.

**cscript WiExport.vbs \[ Pfad zur \] \[ \] \[ \] \[ Liste der Tabellennamen der Ordneroptionen\]**

Geben Sie den Pfad zur Installer-Datenbank an, aus der die Tabellen exportiert werden. Geben Sie den Pfad zu dem Ordner an, in den die exportierten Archivdateien kopiert werden sollen. Listet die Namen der zu exportierenden [Datenbanktabellen](database-tables.md) auf. Geben \* Sie "" an, um alle Tabellen einschließlich " \_ SummaryInformation" zu exportieren.

Die folgenden Optionen können an beliebiger Stelle in der Befehlszeile vor der Liste der Tabellennamen angegeben werden.



| Option              | BESCHREIBUNG                                            |
|---------------------|--------------------------------------------------------|
| keine Option angegeben. | Exportierte Archivdateien haben möglicherweise einen langen Dateinamen.      |
| /s                  | Erzwingen Sie, dass exportierte Archivdateien kurze Dateinamen haben. |



 

Weitere Skript Beispiele finden Sie unter [Windows Installer Skript Beispiele](windows-installer-scripting-examples.md). Beispiel Hilfsprogramme, die keinen Windows Script Host erfordern, finden Sie unter [Windows Installer-Entwicklungs Tools](windows-installer-development-tools.md).

 

 



