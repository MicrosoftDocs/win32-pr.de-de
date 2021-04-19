---
description: Die VBScript-Datei WiLstXfm.vbs wird in den Windows SDK Komponenten für Windows Installer Entwickler bereitgestellt. Dieses Skript Beispiel kann verwendet werden, um eine Transformations Datei anzuzeigen.
ms.assetid: c2e3dd56-b0e5-481a-b7b8-5000fa686850
title: Anzeigen einer Transformation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69f4a858f8deb115de967da3b4d485b596f85cee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345688"
---
# <a name="view-a-transform"></a>Anzeigen einer Transformation

Die VBScript-Datei WiLstXfm.vbs wird in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md)bereitgestellt. Dieses Skript Beispiel kann verwendet werden, um eine Transformations Datei anzuzeigen.

Das Beispiel veranschaulicht die Verwendung von:

-   [\_Transformview-Tabelle](-transformview-table.md)
-   [**OpenDatabase-Methode (Installer-Objekt)**](installer-opendatabase.md)
-   [**Lasterrorrecord-Methode**](installer-lasterrorrecord.md) des [ **Installer-Objekts**](installer-object.md)
-   [**Applytransform-Methode**](database-applytransform.md)
-   [**OpenView-Methode**](database-openview.md)
-   [**Commit-Methode**](database-commit.md) des [ **Datenbankobjekts**](database-object.md)
-   [**IsNull-Eigenschaft**](record-isnull.md)
-   [**StringData-Eigenschaft**](record-stringdata.md) des [ **Datensatz-Objekts**](record-object.md)

Zum Verwenden dieses Beispiels ist die CScript.exe Version von Windows Script Host erforderlich. Wenn Sie CScript.exe verwenden möchten, um dieses Beispiel auszuführen, geben Sie einen Befehl an der Eingabeaufforderung ein, indem Sie die folgende Syntax verwenden. Hilfe wird angezeigt, wenn das erste Argument/? oder, wenn zu wenige Argumente angegeben werden. Um die Ausgabe in eine Datei umzuleiten, beenden Sie die Befehlszeile mit VSB > \[ *Pfad zur Datei* \] . Das Beispiel gibt den Wert 0 für Erfolg zurück, 1, wenn Hilfe aufgerufen wird, und 2, wenn das Skript fehlschlägt.

**cscript WiLstXfm.vbs** Pfad zum Verweis auf die *\[ Daten Bank \] \[ Option \] \[ , die angezeigt \] werden* soll.

Geben Sie den Pfad zum Verweis Windows Installer-Datenbank an. Geben Sie eine Liste mit Pfaden zum Transformieren von Dateien an, die angezeigt werden. Jedem Pfad in der Liste kann ein optionaler numerischer Wert vorangestellt werden. Dieser Wert gibt eine Reihe von Fehlerbedingungen an, die unterdrückt werden sollen. Sie können diese Werte hinzufügen, um mehrere Bedingungen zu unterdrücken. Wenn keine numerische Option angegeben wird, werden alle Fehlerbedingungen unterdrückt. Die Argumente in dieser Liste werden in der Reihenfolge von links nach rechts ausgeführt, in der Sie in der Befehlszeile angezeigt werden.



| Wert | Zu unterdrückenden Fehlerzustand                   |
|-------|-----------------------------------------------|
| 1     | Hinzufügen einer Zeile, die bereits vorhanden ist.             |
| 2     | Löschen einer Zeile, die nicht vorhanden ist.           |
| 4     | Eine Tabelle, die bereits vorhanden ist, wird hinzugefügt.           |
| 8     | Löschen einer Tabelle, die nicht vorhanden ist.         |
| 16    | Aktualisieren einer Zeile, die nicht vorhanden ist.           |
| 256   | Nicht übereinstimmende Datenbank-und Transformations-Codepages. |



 

Weitere Skript Beispiele finden Sie unter [Windows Installer Skript Beispiele](windows-installer-scripting-examples.md). Beispiel Hilfsprogramme, die keinen Windows Script Host erfordern, finden Sie unter [Windows Installer-Entwicklungs Tools](windows-installer-development-tools.md).

 

 



