---
description: Die VBScript-Datei WiMakCab.vbs wird in den Windows SDK Komponenten für Windows Installer Entwickler bereitgestellt. Dieses Beispiel zeigt, wie das Skript zum Generieren von Datei Schränken aus einer Windows Installer Datenbank verwendet wird.
ms.assetid: 26671cb9-a200-4520-8b52-4cff3f71a2f2
title: Datei CAB-Datei generieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3df2355c247ff602d644d2865ec3b9d9a8447ca4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960051"
---
# <a name="generate-file-cabinet"></a>Datei CAB-Datei generieren

Die VBScript-Datei WiMakCab.vbs wird in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md)bereitgestellt. Dieses Beispiel zeigt, wie das Skript zum Generieren von Datei Schränken aus einer Windows Installer Datenbank verwendet wird.

In diesem Beispiel wird Folgendes veranschaulicht:

-   [**OpenDatabase-Methode (Installer-Objekt)**](installer-opendatabase.md) und die [**lasterrorrecord-Methode**](installer-lasterrorrecord.md) des [**Installer-Objekts**](installer-object.md)
-   [**Commit-Methode**](database-commit.md), [**die OpenView-Methode**](database-openview.md) und die [**SummaryInformation-Eigenschaft (Datenbankobjekt)**](database-summaryinformation.md) des [**Datenbankobjekts**](database-object.md)
-   [**Fetch-Methode**](view-fetch.md), [**Execute-Methode**](view-execute.md) und Modify- [**Methode**](view-modify.md) des View- [**Objekts**](view-object.md)
-   [**StringData-Eigenschaft**](record-stringdata.md) und [**IntegerData-Eigenschaft**](record-integerdata.md) des Datensatz- [**Objekts**](record-object.md)
-   [**Doaction-Methode**](session-doaction.md), die Property-Eigenschaft [**(Session-Objekt)**](session-session.md)und die [**Mode-Eigenschaft**](session-mode.md) des Session- [**Objekts**](session-object.md)

Sie benötigen die CScript.exe oder WScript.exe Version von Windows Script Host, um dieses Beispiel zu verwenden. Wenn Sie CScript.exe verwenden möchten, um dieses Beispiel auszuführen, geben Sie einen Befehl an der Eingabeaufforderung ein, indem Sie die folgende Syntax verwenden. Hilfe wird angezeigt, wenn das erste Argument/? oder, wenn zu wenige Argumente angegeben werden. Um die Ausgabe in eine Datei umzuleiten, beenden Sie die Befehlszeile mit VSB > \[ *Pfad zur Datei* \] . Das Beispiel gibt den Wert 0 für Erfolg zurück, 1, wenn Hilfe aufgerufen wird, und 2, wenn das Skript fehlschlägt.

**cscript WiMakCab.vbs \[ Pfad zu Datenbank- \] \[ Basisname \] \[ optionale Quell Speicherorte\]**

Um eine CAB-Makecab.exe zu generieren, müssen sich auf dem Pfad befinden. Das Makecab.exe-Hilfsprogramm ist in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md)enthalten. Beachten Sie, dass das Beispiel die [Medien Tabelle](media-table.md) nicht so aktualisiert, dass mehrere Schränke behandelt werden. Zum Ersetzen einer eingebetteten CAB-Installation schließen Sie die folgenden Optionen ein:/R/C/U/E.

Geben Sie den Pfad zur Installer-Datenbank an. Diese muss sich im Stammverzeichnis der Quell Struktur befinden. Geben Sie die Groß-/Kleinschreibung für die generierten CAB-Dateien an. Wenn der Quelltyp komprimiert ist, werden alle Dateien im Stamm geöffnet. Die folgenden Optionen können an einem beliebigen Punkt in der Befehlszeile angegeben werden.



| Option              | BESCHREIBUNG                                                                                                                               |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| keine Option angegeben. |                                                                                                                                           |
| /C                  | Komprimierung ausführen. Wenn/C nicht angegeben ist, generiert WiMakCab.vbs nur die DDF-Datei.                                                        |
| /L                  | Verwenden Sie die LZX-Komprimierung anstelle von mszip.                                                                                                      |
| /F                  | Schränken Sie die CAB-Größe auf die Größe von 1,44 MB anstelle von CD-ROM ein.                                                                              |
| /U                  | Aktualisieren der Datenbank auf die generierte CAB-Datenbank                                                                                    |
| /E                  | Einbetten der CAB-Datei in das Installer-Paket als Stream                                                                               |
| /S                  | Verwenden von Sequenznummern in der Dateitabelle geordnet nach Verzeichnissen                                                                             |
| /R                  | Auf nicht-CAB-Installation zurücksetzen, CAB entfernen, wenn/E angegeben ist (die/R-Option entfernt die komprimierte Bit-SummaryInfo-Eigenschaft 15 & 2) |



 

Weitere Skript Beispiele finden Sie unter [Windows Installer Skript Beispiele](windows-installer-scripting-examples.md). Beispiel Hilfsprogramme, die keinen Windows Script Host erfordern, finden Sie unter [Windows Installer-Entwicklungs Tools](windows-installer-development-tools.md).

 

 



