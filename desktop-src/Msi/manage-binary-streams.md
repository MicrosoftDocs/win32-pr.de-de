---
description: Die VBScript-Datei WiStream.vbs wird in den Windows SDK Komponenten für Windows Installer Entwickler bereitgestellt.
ms.assetid: f96d1fdd-81c8-4fb2-a23e-fda49ace8bef
title: Binäre Streams verwalten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 877631a40157a5d286ef0c2575732a6d561eefb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360737"
---
# <a name="manage-binary-streams"></a>Binäre Streams verwalten

Die VBScript-Datei WiStream.vbs wird in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md)bereitgestellt. Dieses Beispiel zeigt, wie mithilfe von Skripts binäre Datenströme in einer Windows Installer Datenbank verwaltet werden können. Das Beispiel kann verwendet werden, um komprimierte Datei Schränke in eine Datenbank einzugeben. Dieses Beispiel veranschaulicht den Betrieb der [ \_ Streams-Tabelle](-streams-table.md) in der Windows Installer-Datenbank.

Im Beispiel wird auch die Verwendung von veranschaulicht:

-   [**OpenDatabase-Methode (Installer-Objekt)**](installer-opendatabase.md)
-   [**Methode "kreaterecord"**](installer-createrecord.md)
-   [**Lasterrorrecord-Methode**](installer-lasterrorrecord.md) des [ **Installer-Objekts**](installer-object.md)
-   [**OpenView-Methode**](database-openview.md)
-   [**Commit-Methode**](database-commit.md) des [ **Datenbankobjekts**](database-object.md)
-   [**FETCH-Methode**](view-fetch.md)
-   [**Modify-Methode**](view-modify.md)
-   [**Execute-Methode**](view-execute.md) des [ **View-Objekts**](view-object.md)
-   [**StringData (Eigenschaft)**](record-stringdata.md)
-   [**SetStream-Methode**](record-setstream.md) des [ **Datensatz-Objekts**](record-object.md)

Sie benötigen die CScript.exe oder WScript.exe Version von Windows Script Host, um dieses Beispiel zu verwenden. Wenn Sie CScript.exe verwenden möchten, um dieses Beispiel auszuführen, geben Sie mithilfe der folgenden Syntax eine Befehlszeile an der Eingabeaufforderung ein. Hilfe wird angezeigt, wenn das erste Argument/? oder, wenn zu wenige Argumente angegeben werden. Um die Ausgabe in eine Datei umzuleiten, beenden Sie die Befehlszeile mit VSB > \[ *Pfad zur Datei* \] . Das Beispiel gibt den Wert 0 für Erfolg zurück, 1, wenn Hilfe aufgerufen wird, und 2, wenn das Skript fehlschlägt.

**cscript WiStream.vbs \[ Pfad zum Daten Bank \] \[ Pfad zu Datei \] \[ Optionen Daten \] \[ Strom Name\]**

Geben Sie den Pfad zur Windows Installer Datenbank an, die den Datenstrom empfangen soll. Geben Sie einen Pfad zu der Binärdatei an, die die Streamdaten enthält. Um die Datenströme in der Installerdatenbank aufzulisten, lassen Sie diesen Pfad Weg. Sie können einen optionalen Datenstrom Namen angeben. Wenn dieser Wert weggelassen wird, wird standardmäßig der Dateiname verwendet.

Die folgende Option kann angegeben werden.



| Option              | BESCHREIBUNG                                                                                     |
|---------------------|-------------------------------------------------------------------------------------------------|
| keine Option angegeben. | Fügen Sie der Windows Installer Datenbank einen Stream hinzu.                                                 |
| /d                  | Entfernen Sie einen Datenstrom. Auf dieses Optionsflag muss der Name des zu entfernenden subspeichers folgen. |



 

Weitere Skript Beispiele finden Sie unter [Windows Installer Skript Beispiele](windows-installer-scripting-examples.md). Beispiel Hilfsprogramme, die keinen Windows Script Host erfordern, finden Sie unter [Windows Installer-Entwicklungs Tools](windows-installer-development-tools.md).

 

 



