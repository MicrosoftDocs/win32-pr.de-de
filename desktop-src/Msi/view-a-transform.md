---
description: Die VBScript-Datei WiLstXfm.vbs wird in den Windows SDK-Komponenten für Windows Installer-Entwickler bereitgestellt. Dieses Skriptbeispiel kann verwendet werden, um eine Transformationsdatei anzuzeigen.
ms.assetid: c2e3dd56-b0e5-481a-b7b8-5000fa686850
title: Anzeigen einer Transformation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f599099ff858275f3b0c75df9b265129adfe0659a5c3c35d285417a8e295f58
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995630"
---
# <a name="view-a-transform"></a>Anzeigen einer Transformation

Die VBScript-Datei WiLstXfm.vbs wird in den [Windows SDK-Komponenten für Windows Installer-Entwickler](platform-sdk-components-for-windows-installer-developers.md)bereitgestellt. Dieses Skriptbeispiel kann verwendet werden, um eine Transformationsdatei anzuzeigen.

Das Beispiel veranschaulicht die Verwendung von:

-   [\_TransformView-Tabelle](-transformview-table.md)
-   [**OpenDatabase-Methode (Installer-Objekt)**](installer-opendatabase.md)
-   [**LastErrorRecord-Methode**](installer-lasterrorrecord.md) des [ **Installer-Objekts**](installer-object.md)
-   [**ApplyTransform-Methode**](database-applytransform.md)
-   [**OpenView-Methode**](database-openview.md)
-   [**Commit-Methode**](database-commit.md) des [ **Datenbankobjekts**](database-object.md)
-   [**IsNull-Eigenschaft**](record-isnull.md)
-   [**StringData-Eigenschaft**](record-stringdata.md) des [ **Record-Objekts**](record-object.md)

Für die Verwendung dieses Beispiels ist die CScript.exe Version von Windows Script Host erforderlich. Um CScript.exe zum Ausführen dieses Beispiels zu verwenden, geben Sie einen Befehl an der Eingabeaufforderung mit der folgenden Syntax ein. Hilfe wird angezeigt, wenn das erste Argument /? ist. oder , wenn zu wenige Argumente angegeben werden. Um die Ausgabe an eine Datei umzuleiten, beenden Sie die Befehlszeile mit VBS > \[ *Pfad zur Datei* \] . Das Beispiel gibt den Wert 0 für den Erfolg zurück, 1, wenn die Hilfe aufgerufen wird, und 2, wenn das Skript fehlschlägt.

**cscript WiLstXfm.vbs** *\[ Pfad zum Referenzdatenbankoptionspfad, \] \[ der zur \] \[ Anzeige transformiert \] werden soll*

Geben Sie den Pfad zum Verweis Windows Installer-Datenbank an. Geben Sie eine Liste der Pfade zum Transformieren von Dateien an, die angezeigt werden. Jedem Pfad in der Liste kann ein optionaler numerischer Wert vorangestellt werden. Dieser Wert gibt eine Reihe von Fehlerbedingungen an, die unterdrückt werden sollen. Sie können diese Werte zusammen hinzufügen, um mehrere Bedingungen zu unterdrücken. Wenn keine numerische Option angegeben ist, werden alle Fehlerbedingungen unterdrückt. Die Argumente in dieser Liste werden in der Reihenfolge von links nach rechts ausgeführt, in der sie in der Befehlszeile angezeigt werden.



| Wert | Zu unterdrückende Fehlerbedingung                   |
|-------|-----------------------------------------------|
| 1     | Hinzufügen einer Zeile, die bereits vorhanden ist.             |
| 2     | Löschen einer Zeile, die nicht vorhanden ist.           |
| 4     | Hinzufügen einer Tabelle, die bereits vorhanden ist.           |
| 8     | Löschen einer tabelle, die nicht vorhanden ist.         |
| 16    | Aktualisieren einer Zeile, die nicht vorhanden ist.           |
| 256   | Konflikt zwischen Datenbank- und Transformationscodepages. |



 

Weitere Skriptbeispiele finden Sie unter [Windows Installer Scripting Examples](windows-installer-scripting-examples.md). Beispielhilfsprogramme, die Windows Script Host nicht benötigen, finden Sie unter [Windows Installer Development Tools](windows-installer-development-tools.md).

 

 



