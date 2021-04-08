---
description: Die VBScript-Datei WiFilVer.vbs wird in den Windows SDK Komponenten für Windows Installer Entwickler bereitgestellt. Das Beispiel zeigt, wie Sie ein Skript zum melden oder Aktualisieren der Dateiversion, der Größe und der Sprachinformationen verwenden können.
ms.assetid: 21550eea-c30b-4738-9201-ab500356fabf
title: Verwalten von Dateigrößen und-Versionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 426acf71956d87fe1458447119d79bc142f1ee75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752776"
---
# <a name="manage-file-sizes-and-versions"></a>Verwalten von Dateigrößen und-Versionen

Die VBScript-Datei WiFilVer.vbs wird in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md)bereitgestellt. Das Beispiel zeigt, wie Sie ein Skript zum melden oder Aktualisieren der Dateiversion, der Größe und der Sprachinformationen verwenden können.

Das Beispiel zeigt auch Windows Installer Aktionen, den Zugriff auf eine Windows Installer Datenbank und die Verwendung der folgenden Informationen:

-   [**Installer. OpenDatabase**](installer-opendatabase.md) -Methode des [ **Installer-Objekts**](installer-object.md)
-   [**Installer. File Attribute**](installer-fileattributes.md) (Eigenschaft)
-   [**Installer. flehash**](installer-filehash.md) -Methode
-   [**Installer. FileVersion**](installer-fileversion.md) -Methode
-   [**Installer. lasterrorrecord**](installer-lasterrorrecord.md) -Methode des [ **Installer-Objekts**](installer-object.md)
-   [**Database. OpenView**](database-openview.md) -Methode
-   [**Database. SummaryInformation**](database-summaryinformation.md) -Eigenschaft des [ **Database-Objekts**](database-object.md)
-   [**Session. doaction**](session-doaction.md) -Methode
-   [**Session. Property**](session-session.md)
-   [**Session. SourcePath**](session-sourcepath.md) (Eigenschaft)
-   [**Session. Mode**](session-mode.md) -Eigenschaft des [ **Session-Objekts**](session-object.md)
-   [**Record. StringData**](record-stringdata.md) (Eigenschaft)
-   [**Record. IntegerData**](record-integerdata.md) -Eigenschaft des [ **Datensatz-Objekts**](record-object.md)

Zum Verwenden dieses Beispiels ist die CScript.exe oder WScript.exe Version von Windows Script Host erforderlich. Wenn Sie CScript.exe verwenden möchten, um dieses Beispiel auszuführen, geben Sie einen Befehl an der Eingabeaufforderung ein, indem Sie die folgende Syntax verwenden:

**cscript-WiFilVer.vbs \[ Pfad zu \] \[ optionalen Quell Speicherorten der Datenbank\]**

Beachten Sie auch Folgendes:

-   Hilfe wird angezeigt, wenn das erste Argument/? oder, wenn zu wenige Argumente angegeben werden.
-   Um die Ausgabe in eine Datei umzuleiten, beenden Sie die Befehlszeile mit VSB > \[ *Pfad zur Datei* \] .
-   Im Beispiel wird der Wert 0 (null) für Erfolg zurückgegeben, 1 (eins), wenn die Hilfe aufgerufen wird, und 2 (zwei), wenn das Skript fehlschlägt.

Geben Sie die Windows Installer Datenbank an, die Sie aktualisieren möchten. diese muss sich im Stammverzeichnis der Quelldatei befinden. Sie können jedoch Datenquellen für die Datenbank an separaten Speicherorten angeben. Wenn die Quelle komprimiert ist, werden alle Dateien im Stamm geöffnet.

Die folgenden Optionen können an beliebiger Stelle in der Befehlszeile angegeben werden.



| Option                | BESCHREIBUNG                                                                              |
|-----------------------|------------------------------------------------------------------------------------------|
| *keine Option angegeben.* | Zeigen Sie die Dateiinformationen der Datenbank an.                                            |
| /U                    | Aktualisieren Sie die Dateigröße, die Version und die Sprachinformationen in der Datenbank aus der Quelle. |



 

Weitere Informationen finden Sie unter [Windows Installer von Skript Beispielen](windows-installer-scripting-examples.md) und [Windows Installer Entwicklungs Tools](windows-installer-development-tools.md).

 

 



