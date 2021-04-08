---
description: Die VBScript-Datei WiUseXfm.vbs wird in den Windows SDK Komponenten für Windows Installer Entwickler bereitgestellt. In diesem Beispiel wird gezeigt, wie mithilfe eines Skripts eine Transformation auf eine Windows Installer Datenbank angewendet werden kann.
ms.assetid: e647388e-5211-463d-9e3e-b502af01fc0c
title: Anwenden einer Transformation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9e86acc495fc2a0bb8dff562832e58d29483256
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864487"
---
# <a name="apply-a-transform"></a>Anwenden einer Transformation

Die VBScript-Datei WiUseXfm.vbs wird in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md)bereitgestellt. In diesem Beispiel wird gezeigt, wie mithilfe eines Skripts eine Transformation auf eine Windows Installer Datenbank angewendet werden kann.

Im Beispiel wird die Verwendung von veranschaulicht.

-   [**OpenDatabase-Methode (Installer-Objekt)**](installer-opendatabase.md)
-   [**Lasterrorrecord-Methode**](installer-lasterrorrecord.md) des [ **Installer-Objekts**](installer-object.md)
-   [**Applytransform-Methode**](database-applytransform.md)
-   [**Commit-Methode**](database-commit.md) des [ **Datenbankobjekts**](database-object.md)

Sie benötigen die CScript.exe oder WScript.exe Version von Windows Script Host, um dieses Beispiel zu verwenden. Wenn Sie CScript.exe verwenden möchten, um dieses Beispiel auszuführen, geben Sie mithilfe der folgenden Syntax eine Befehlszeile an der Eingabeaufforderung ein. Hilfe wird angezeigt, wenn das erste Argument/? oder, wenn zu wenige Argumente angegeben werden. Um die Ausgabe in eine Datei umzuleiten, beenden Sie die Befehlszeile mit VSB > \[ *Pfad zur Datei* \] . Das Beispiel gibt den Wert 0 für Erfolg zurück, 1, wenn Hilfe aufgerufen wird, und 2, wenn das Skript fehlschlägt.

**cscript WiUseXfm.vbs \[ Pfad zum ursprünglichen Daten Bank \] \[ Pfad zum Transformieren von Datei \] \[ Optionen\]**

Geben Sie den Pfad für die Windows Installer-Datenbank an. Geben Sie den Pfad zur Transformations Datei an. Wenn der Pfad zur Transformations Datei weggelassen wird, werden die beiden Datenbanken nur verglichen. Das dritte Argument ist ein optionaler numerischer Wert, der einen Satz von Fehlerbedingungen angibt, die unterdrückt werden sollen. Fügen Sie diese Werte hinzu, um mehrere Bedingungen zu unterdrücken.



| Wert | Zu unterdrückenden Fehlerzustand                   |
|-------|-----------------------------------------------|
| 1     | Hinzufügen einer Zeile, die bereits vorhanden ist.             |
| 2     | Löschen einer Zeile, die nicht vorhanden ist.           |
| 4     | Eine Tabelle, die bereits vorhanden ist, wird hinzugefügt.           |
| 8     | Löschen einer Tabelle, die nicht vorhanden ist.         |
| 16    | Aktualisieren einer Zeile, die nicht vorhanden ist.           |
| 256   | Nicht übereinstimmende Datenbank-und Transformations-Codepages. |



 

Weitere Skript Beispiele finden Sie unter [Windows Installer Skript Beispiele](windows-installer-scripting-examples.md). Beispiel Hilfsprogramme, die keinen Windows Script Host erfordern, finden Sie unter [Windows Installer-Entwicklungs Tools](windows-installer-development-tools.md).

 

 



