---
description: Die VBScript-WiImport.vbs wird in den sdk-Komponenten Windows für Windows Installer-Entwickler bereitgestellt. In diesem Beispiel wird gezeigt, wie Sie ein Skript schreiben, um Tabellen in eine Windows Installer-Datenbank zu importieren.
ms.assetid: 37580bd6-30c7-4239-9717-223a381ba021
title: Importieren von Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dc67cc3f698d1268a5ce08fe1e4c76b86a425216396fa168b0e8e6dc8a3f91f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043860"
---
# <a name="import-files"></a>Importieren von Dateien

Die VBScript-WiImport.vbs wird in den Windows [SDK-Komponenten für Windows Installer-Entwickler bereitgestellt.](platform-sdk-components-for-windows-installer-developers.md) In diesem Beispiel wird gezeigt, wie Sie ein Skript schreiben, um Tabellen in eine Windows Installer-Datenbank zu importieren.

Das Skript stellt eine Verbindung mit einem [**Installer-Objekt**](installer-object.md) auf, öffnet eine Datenbank, verarbeitet eine Liste von Dateien und führt vor dem Schließen der Datenbank einen Commit für die Änderungen aus.

Das Beispiel veranschaulicht die Verwendung von:

-   [**OpenDatabase-Methode (Installer-Objekt)**](installer-opendatabase.md)
-   [**LastErrorRecord-Methode**](installer-lasterrorrecord.md) des [ **Installer-Objekts**](installer-object.md)
-   [**Import-Methode**](database-import.md)
-   [**Commit-Methode**](database-commit.md) des [ **Database-Objekts**](database-object.md)

Sie benötigen die CScript.exe oder WScript.exe von Windows Script Host, um dieses Beispiel verwenden zu können. Verwenden Sie CScript.exe Syntax an der Eingabeaufforderung, um dieses Beispiel mithilfe von CScript.exe auszuführen.

**cscript WiImport.vbs \[ zum Datenbankpfad zu \] \[ Ordneroptionen \] \[ \] \[ Archivdateiliste**\]

Hilfe wird angezeigt, wenn das erste Argument /? ist. oder , wenn zu wenige Argumente angegeben werden. Um die Ausgabe an eine Datei umzuleiten, beenden Sie die Befehlszeile mit VBS > \[ Pfad zur Datei \] . Das Beispiel gibt den Wert 0 für den Erfolg zurück, 1, wenn Hilfe aufgerufen wird, und 2, wenn das Skript fehlschlägt.

Geben Sie den Pfad zu einer Windows Installer-Datenbank an, die erstellt oder die importierten Tabellen empfangen soll. Geben Sie den Pfad zu dem Ordner an, der die Archivdateien der zu importierenden Tabellen enthält. Listen Sie die Namen der Archivdateien auf, die importiert werden. Platzhalterdateinamen, \* z. B. IDT, können verwendet werden, um mehrere Dateien zu importieren.

Die folgenden Optionen können an einer beliebigen Stelle in der Befehlszeile vor der Dateiliste angegeben werden.



| Option              | BESCHREIBUNG                                                                                                                          |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| keine Option angegeben | Importieren Sie die Liste der Tabellenarchivdateien aus dem angegebenen Ordner in die Windows Installer-Datenbank.                                |
| /c                  | Erstellen Sie Windows Installer-Datenbank, und importieren Sie dann die Liste der Tabellenarchivdateien aus dem angegebenen Ordner in die neue Datenbank. |



 

Weitere Informationen finden Sie unter [Windows Installer Scripting Examples](windows-installer-scripting-examples.md) für zusätzliche Skriptbeispiele. Beispielprogramme, für die kein Skripthost Windows ist, finden Sie unter [Windows Installer Development Tools](windows-installer-development-tools.md).

Beachten [Sie, dass ein Lokalisierungsbeispiel](a-localization-example.md) auch [das Importieren lokalisierter Fehler- und ActionText-Tabellen veranschaulicht.](importing-localized-error-and-actiontext-tables.md)

 

 



