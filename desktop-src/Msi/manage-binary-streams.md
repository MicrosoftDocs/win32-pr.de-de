---
description: Die VBScript-WiStream.vbs wird in den sdk-Komponenten Windows für Windows Installer-Entwickler bereitgestellt.
ms.assetid: f96d1fdd-81c8-4fb2-a23e-fda49ace8bef
title: Verwalten von binären Streams
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32de268cc42a6dbb806d6f3c1503d8bb0cdf32aba037bf48da678ecb86fe2775
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118945625"
---
# <a name="manage-binary-streams"></a>Verwalten von binären Streams

Die VBScript-WiStream.vbs wird in den Windows [SDK-Komponenten für Windows Installer-Entwickler bereitgestellt.](platform-sdk-components-for-windows-installer-developers.md) In diesem Beispiel wird gezeigt, wie skript zum Verwalten von binären Streams in einer Windows Installer-Datenbank verwendet werden kann. Das Beispiel kann verwendet werden, um komprimierte Dateischränke in eine Datenbank zu geben. In diesem Beispiel wird der Vorgang der Streams [ \_ in](-streams-table.md) der Windows Installer-Datenbank veranschaulicht.

Das Beispiel veranschaulicht auch die Verwendung von:

-   [**OpenDatabase-Methode (Installer-Objekt)**](installer-opendatabase.md)
-   [**CreateRecord-Methode**](installer-createrecord.md)
-   [**LastErrorRecord-Methode**](installer-lasterrorrecord.md) des [ **Installer-Objekts**](installer-object.md)
-   [**OpenView-Methode**](database-openview.md)
-   [**Commit-Methode**](database-commit.md) des [ **Database-Objekts**](database-object.md)
-   [**Fetch-Methode**](view-fetch.md)
-   [**Modify-Methode**](view-modify.md)
-   [**Execute-Methode**](view-execute.md) des [ **View-Objekts**](view-object.md)
-   [**StringData-Eigenschaft**](record-stringdata.md)
-   [**SetStream-Methode**](record-setstream.md) des [ **Record-Objekts**](record-object.md)

Sie benötigen die CScript.exe oder WScript.exe version of Windows Script Host (Skripthost), um dieses Beispiel verwenden zu können. Um dieses CScript.exe ausführen zu können, geben Sie an der Eingabeaufforderung eine Befehlszeile mit der folgenden Syntax ein. Hilfe wird angezeigt, wenn das erste Argument /? ist. oder , wenn zu wenige Argumente angegeben werden. Um die Ausgabe an eine Datei umzuleiten, beenden Sie die Befehlszeile mit VBS > \[ *Pfad zur Datei* \] . Das Beispiel gibt den Wert 0 für den Erfolg zurück, 1, wenn Hilfe aufgerufen wird, und 2, wenn das Skript fehlschlägt.

**cscript WiStream.vbs \[ pfad zum Datenbankpfad zum \] \[ \] Dateioptionen-Streamnamen \[ \] \[\]**

Geben Sie den Pfad zur Windows Installer-Datenbank an, die den Stream empfangen soll. Geben Sie einen Pfad zur Binärdatei an, die die Datenstromdaten enthält. Um die Streams in der Installer-Datenbank auflisten zu können, weglassen Sie diesen Pfad. Sie können einen optionalen Streamnamen angeben. Wenn dieser nicht angegeben wird, wird standardmäßig der Dateiname verwendet.

Die folgende Option kann angegeben werden.



| Option              | BESCHREIBUNG                                                                                     |
|---------------------|-------------------------------------------------------------------------------------------------|
| keine Option angegeben | Fügen Sie der Datenbank des Windows-Installers einen Stream hinzu.                                                 |
| /d                  | Entfernen Sie einen Stream. Auf dieses Optionsflag muss der Name des zu entfernenden Unterstorages folgen. |



 

Weitere Skriptbeispiele finden Sie unter [Windows Installer Scripting Examples](windows-installer-scripting-examples.md). Beispielprogramme, für die kein Skripthost Windows ist, finden Sie unter [Windows Installer Development Tools](windows-installer-development-tools.md).

 

 



