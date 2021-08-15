---
description: Die VBScript-WiUseXfm.vbs wird in den Windows SDK-Komponenten für Windows Installer-Entwickler bereitgestellt. In diesem Beispiel wird gezeigt, wie sie mit einem Skript eine Transformation auf eine Windows Installer-Datenbank anwenden können.
ms.assetid: e647388e-5211-463d-9e3e-b502af01fc0c
title: Anwenden einer Transformation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 001737b1a08ea33ce233fa0aad90e96e23a1079f2c28f9d6308219cba270f6ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118381609"
---
# <a name="apply-a-transform"></a>Anwenden einer Transformation

Die VBScript-WiUseXfm.vbs wird in den Windows [SDK-Komponenten für Windows Installer-Entwickler bereitgestellt.](platform-sdk-components-for-windows-installer-developers.md) In diesem Beispiel wird gezeigt, wie sie mit einem Skript eine Transformation auf eine Windows Installer-Datenbank anwenden können.

Das Beispiel veranschaulicht die Verwendung von

-   [**OpenDatabase-Methode (Installer-Objekt)**](installer-opendatabase.md)
-   [**LastErrorRecord-Methode**](installer-lasterrorrecord.md) des [ **Installer-Objekts**](installer-object.md)
-   [**ApplyTransform-Methode**](database-applytransform.md)
-   [**Commit-Methode**](database-commit.md) des [ **Datenbankobjekts**](database-object.md)

Sie benötigen die CScript.exe oder WScript.exe von Windows Script Host, um dieses Beispiel verwenden zu können. Um dieses CScript.exe auszuführen, geben Sie an der Eingabeaufforderung eine Befehlszeile mit der folgenden Syntax ein. Hilfe wird angezeigt, wenn das erste Argument /? ist. oder , wenn zu wenige Argumente angegeben werden. Um die Ausgabe an eine Datei umzuleiten, beenden Sie die Befehlszeile mit VBS > \[ *Pfad zur Datei* \] . Das Beispiel gibt den Wert 0 für den Erfolg zurück, 1, wenn Hilfe aufgerufen wird, und 2, wenn das Skript fehlschlägt.

**cscript WiUseXfm.vbs \[ pfad zum ursprünglichen Datenbankpfad \] \[ zum Transformieren von \] \[ Dateioptionen\]**

Geben Sie den Pfad zur Windows Installer-Datenbank an. Geben Sie den Pfad zur Transformationsdatei an. Wenn der Pfad zur Transformationsdatei weggelassen wird, werden nur die beiden Datenbanken verglichen. Das dritte Argument ist ein optionaler numerischer Wert, der einen Satz von Fehlerbedingungen angibt, die unterdrückt werden sollen. Fügen Sie diese Werte zusammen hinzu, um mehrere Bedingungen zu unterdrücken.



| Wert | Zu unterdrückende Fehlerbedingung                   |
|-------|-----------------------------------------------|
| 1     | Hinzufügen einer zeile, die bereits vorhanden ist.             |
| 2     | Löschen einer Zeile, die nicht vorhanden ist.           |
| 4     | Hinzufügen einer tabelle, die bereits vorhanden ist.           |
| 8     | Löschen einer Tabelle, die nicht vorhanden ist.         |
| 16    | Aktualisieren einer Zeile, die nicht vorhanden ist.           |
| 256   | Nicht übereinstimmende Datenbank- und Transformationscodepages. |



 

Weitere Skriptbeispiele finden Sie unter [Windows Installer Scripting Examples](windows-installer-scripting-examples.md). Beispielprogramme, für die kein Skripthost Windows ist, finden Sie unter [Windows Installer Development Tools](windows-installer-development-tools.md).

 

 



