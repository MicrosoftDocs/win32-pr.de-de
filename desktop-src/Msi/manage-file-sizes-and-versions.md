---
description: Die VBScript-WiFilVer.vbs wird in den sdk-Komponenten Windows für Windows Installer-Entwickler bereitgestellt. Das Beispiel zeigt, wie Sie mithilfe eines Skripts Informationen zu Version, Größe und Sprache der Datei melden oder aktualisieren können.
ms.assetid: 21550eea-c30b-4738-9201-ab500356fabf
title: Verwalten von Dateigrößen und -versionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79dcb5bec9b7fd24d7171efed9295479e56d979a3f7aa69352f2231d409417f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118629041"
---
# <a name="manage-file-sizes-and-versions"></a>Verwalten von Dateigrößen und -versionen

Die VBScript-dateiWiFilVer.vbs wird in den Windows [SDK-Komponenten für Windows Installer-Entwickler bereitgestellt.](platform-sdk-components-for-windows-installer-developers.md) Das Beispiel zeigt, wie Sie mithilfe eines Skripts Informationen zu Version, Größe und Sprache der Datei melden oder aktualisieren können.

Das Beispiel zeigt ihnen auch Windows Installer-Aktionen, den Zugriff auf eine Windows Installer-Datenbank und die Verwendung der folgenden Aktionen:

-   [**Installer.OpenDatabase-Methode**](installer-opendatabase.md) des [ **Installer-Objekts**](installer-object.md)
-   [**Installer.FileAttributes(Eigenschaft)**](installer-fileattributes.md)
-   [**Installer.FileHash-Methode**](installer-filehash.md)
-   [**Installer.FileVersion-Methode**](installer-fileversion.md)
-   [**Installer.LastErrorRecord-Methode**](installer-lasterrorrecord.md) des [ **Installer-Objekts**](installer-object.md)
-   [**Database.OpenView-Methode**](database-openview.md)
-   [**Database.SummaryInformation-Eigenschaft**](database-summaryinformation.md) des [ **Datenbankobjekts**](database-object.md)
-   [**Session.DoAction-Methode**](session-doaction.md)
-   [**Session.Property**](session-session.md)
-   [**Session.SourcePath(Eigenschaft)**](session-sourcepath.md)
-   [**Session.Mode-Eigenschaft**](session-mode.md) des [ **Sitzungsobjekts**](session-object.md)
-   [**Record.StringData(Eigenschaft)**](record-stringdata.md)
-   [**Record.IntegerData-Eigenschaft**](record-integerdata.md) des [ **Datensatzobjekts**](record-object.md)

Die Verwendung dieses Beispiels erfordert die CScript.exe oder WScript.exe-Version Windows Skripthosts. Um dieses CScript.exe auszuführen, geben Sie an der Eingabeaufforderung mithilfe der folgenden Syntax einen Befehl ein:

**cscript WiFilVer.vbs \[ zu optionalen Quellpfaden \] \[ der Datenbank\]**

Beachten Sie außerdem Folgendes:

-   Hilfe wird angezeigt, wenn das erste Argument /? ist. oder , wenn zu wenige Argumente angegeben werden.
-   Um die Ausgabe an eine Datei umzuleiten, beenden Sie die Befehlszeile mit VBS > \[ *Pfad zur Datei* \] .
-   Das Beispiel gibt den Wert 0 (null) für den Erfolg zurück, 1 (eins), wenn Hilfe aufgerufen wird, und 2 (zwei), wenn das Skript fehlschlägt.

Geben Sie Windows Installer-Datenbank an, die Sie aktualisieren möchten, die sich im Stammverzeichnis der Quelldatei befinden muss. Sie können jedoch Quellen für die Datenbank an separaten Speicherorten angeben. Wenn die Quelle komprimiert ist, werden alle Dateien im Stamm geöffnet.

Die folgenden Optionen können an einem beliebigen Speicherort in der Befehlszeile angegeben werden.



| Option                | Beschreibung                                                                              |
|-----------------------|------------------------------------------------------------------------------------------|
| *Keine Option angegeben* | Zeigt die Dateiinformationen der Datenbank an.                                            |
| /U                    | Aktualisieren Sie die Dateigröße, Version und Sprachinformationen in der Datenbank aus der Quelle. |



 

Weitere Informationen finden Sie unter [Windows Installer Scripting Examples](windows-installer-scripting-examples.md) und Windows Installer Development [Tools](windows-installer-development-tools.md).

 

 



