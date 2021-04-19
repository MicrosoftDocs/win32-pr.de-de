---
description: Die VBScript-Datei WiImport.vbs wird in den Windows SDK Komponenten für Windows Installer Entwickler bereitgestellt. Dieses Beispiel zeigt, wie Sie ein Skript schreiben, um Tabellen in eine Windows Installer Datenbank zu importieren.
ms.assetid: 37580bd6-30c7-4239-9717-223a381ba021
title: Dateien importieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8508ee4e385e3edc737515f1b524de074489fb2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343762"
---
# <a name="import-files"></a>Dateien importieren

Die VBScript-Datei WiImport.vbs wird in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md)bereitgestellt. Dieses Beispiel zeigt, wie Sie ein Skript schreiben, um Tabellen in eine Windows Installer Datenbank zu importieren.

Das Skript stellt eine Verbindung mit einem [**Installerobjekt**](installer-object.md) her, öffnet eine Datenbank, verarbeitet eine Liste von Dateien und führt einen Commit für die Änderungen aus, bevor die Datenbank geschlossen wird.

Das Beispiel veranschaulicht die Verwendung von:

-   [**OpenDatabase-Methode (Installer-Objekt)**](installer-opendatabase.md)
-   [**Lasterrorrecord-Methode**](installer-lasterrorrecord.md) des [ **Installer-Objekts**](installer-object.md)
-   [**Import-Methode**](database-import.md)
-   [**Commit-Methode**](database-commit.md) des [ **Datenbankobjekts**](database-object.md)

Sie benötigen die CScript.exe oder WScript.exe Version von Windows Script Host, um dieses Beispiel zu verwenden. Um CScript.exe zum Ausführen dieses Beispiels zu verwenden, verwenden Sie die folgende Syntax an der Eingabeaufforderung.

**cscript WiImport.vbs \[ Pfad zu Daten Bank \] \[ Pfad zu Ordner \] \[ Optionen \] \[ Archivdatei Liste**\]

Hilfe wird angezeigt, wenn das erste Argument/? oder, wenn zu wenige Argumente angegeben werden. Um die Ausgabe in eine Datei umzuleiten, beenden Sie die Befehlszeile mit VSB > \[ Pfad zur Datei \] . Das Beispiel gibt den Wert 0 für Erfolg zurück, 1, wenn Hilfe aufgerufen wird, und 2, wenn das Skript fehlschlägt.

Geben Sie den Pfad zu einer Windows Installer-Datenbank an, die erstellt werden soll oder die importierten Tabellen empfangen soll. Geben Sie den Pfad zum Ordner an, in dem die Archivdateien der zu importierenden Tabellen enthalten sind. Listet die Namen der Archivdateien auf, die importiert werden. Platzhalter Dateinamen, wie z \* . b. IDT, können verwendet werden, um mehrere Dateien zu importieren.

Die folgenden Optionen können an beliebiger Stelle in der Befehlszeile vor der Datei Liste angegeben werden.



| Option              | BESCHREIBUNG                                                                                                                          |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| keine Option angegeben. | Importieren Sie die Liste der Tabellen Archivdateien aus dem angegebenen Ordner in die Windows Installer Datenbank.                                |
| /c                  | Erstellen Sie eine Windows Installer Datenbank, und importieren Sie dann die Liste der Tabellen Archivdateien aus dem angegebenen Ordner in die neue Datenbank. |



 

Weitere Informationen finden Sie unter [Windows Installer Skript Beispiele](windows-installer-scripting-examples.md) für weitere Skript Beispiele. Beispiel Hilfsprogramme, die keinen Windows Script Host erfordern, finden Sie unter [Windows Installer-Entwicklungs Tools](windows-installer-development-tools.md).

Beachten Sie, dass [ein Lokalisierungs Beispiel](a-localization-example.md) auch das [importieren lokalisierter Fehler-und Aktions Text Tabellen](importing-localized-error-and-actiontext-tables.md)veranschaulicht.

 

 



