---
description: Die VBScript-Datei WiMakCab.vbs wird in den Windows SDK-Komponenten für Windows Installer-Entwickler bereitgestellt. Dieses Beispiel zeigt, wie skript verwendet wird, um Dateischränke aus einer Windows Installer-Datenbank zu generieren.
ms.assetid: 26671cb9-a200-4520-8b52-4cff3f71a2f2
title: Generieren eines Dateischränks
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2ca9e30822d0683aa09dc015ec2fd98d1f598c70e0fd63fd00f66a6bcdf3edf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119581490"
---
# <a name="generate-file-cabinet"></a>Generieren eines Dateischränks

Die VBScript-Datei WiMakCab.vbs wird in den [Windows SDK-Komponenten für Windows Installer-Entwickler](platform-sdk-components-for-windows-installer-developers.md)bereitgestellt. Dieses Beispiel zeigt, wie skript verwendet wird, um Dateischränke aus einer Windows Installer-Datenbank zu generieren.

In diesem Beispiel wird Folgendes veranschaulicht:

-   [**OpenDatabase-Methode (Installer-Objekt)**](installer-opendatabase.md) und [**LastErrorRecord-Methode**](installer-lasterrorrecord.md) des [**Installer-Objekts**](installer-object.md)
-   [**Commit-Methode,**](database-commit.md) [**openView-Methode**](database-openview.md) und [**SummaryInformation-Eigenschaft (Datenbankobjekt)**](database-summaryinformation.md) des [**Datenbankobjekts**](database-object.md)
-   [**Fetch-Methode,**](view-fetch.md) [**Execute-Methode**](view-execute.md) und [**Modify-Methode**](view-modify.md) des [**View-Objekts**](view-object.md)
-   [**StringData-Eigenschaft**](record-stringdata.md) und [**IntegerData-Eigenschaft**](record-integerdata.md) des [**Record-Objekts**](record-object.md)
-   [**DoAction-Methode,**](session-doaction.md) [**Eigenschaftseigenschaft (Sitzungsobjekt)**](session-session.md)und [**Mode-Eigenschaft**](session-mode.md) des [**Sitzungsobjekts**](session-object.md)

Sie benötigen die CScript.exe oder WScript.exe Version von Windows Script Host, um dieses Beispiel zu verwenden. Um CScript.exe zum Ausführen dieses Beispiels zu verwenden, geben Sie einen Befehl an der Eingabeaufforderung mit der folgenden Syntax ein. Hilfe wird angezeigt, wenn das erste Argument /? ist. oder , wenn zu wenige Argumente angegeben werden. Um die Ausgabe an eine Datei umzuleiten, beenden Sie die Befehlszeile mit VBS > \[ *Pfad zur Datei* \] . Das Beispiel gibt den Wert 0 für den Erfolg zurück, 1, wenn die Hilfe aufgerufen wird, und 2, wenn das Skript fehlschlägt.

**cscript WiMakCab.vbs \[ Pfad zum \] \[ \] \[ Datenbankbasisnamen optionale Quellspeicherorte\]**

Um einen Schränk zu generieren, müssen Makecab.exe sich auf path befinden. Das hilfsprogramm Makecab.exe ist in den [Windows SDK-Komponenten für Windows Installer-Entwickler](platform-sdk-components-for-windows-installer-developers.md)enthalten. Beachten Sie, dass die [Media-Tabelle](media-table.md) im Beispiel nicht aktualisiert wird, um mehrere Schränke zu verarbeiten. Um ein eingebettetes Gehäuse zu ersetzen, schließen Sie die Folgenden ein: /R /C /U /E.

Geben Sie den Pfad zur Installationsdatenbank an. Dieser muss sich im Stammverzeichnis der Quellstruktur befinden. Geben Sie den Basisnamen für die generierten Cab-Dateien an, bei dem die Groß-/Kleinschreibung beachtet wird. Wenn der Quelltyp komprimiert ist, werden alle Dateien im Stammverzeichnis geöffnet. Die folgenden Optionen können jederzeit in der Befehlszeile angegeben werden.



| Option              | Beschreibung                                                                                                                               |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| Keine Option angegeben |                                                                                                                                           |
| /C                  | Führen Sie die Komprimierung aus. Wenn /C nicht angegeben ist, generiert WiMakCab.vbs nur die DDF-Datei.                                                        |
| /L                  | Verwenden der LZX-Komprimierung anstelle von MSZIP                                                                                                      |
| /F                  | Schränken Sie die Größe des Gehäuses auf 1,44 MB und nicht auf CD-ROM ein.                                                                              |
| /U                  | Aktualisieren der Datenbank, um auf den generierten Schränk zu verweisen                                                                                    |
| /E                  | Einbetten der Cab-Datei in das Installationspaket als Stream                                                                               |
| /S                  | Verwenden von Sequenznummern in der Dateitabelle sortiert nach Verzeichnissen                                                                             |
| /R                  | Kehren Sie zur Installation ohne Schränke zurück, entfernen Sie die Schränke, wenn /E angegeben ist (die Option /R entfernt das komprimierte Bit – SummaryInfo-Eigenschaft 15 & 2) |



 

Weitere Skriptbeispiele finden Sie unter [Windows Installer Scripting Examples](windows-installer-scripting-examples.md). Beispielhilfsprogramme, die Windows Script Host nicht benötigen, finden Sie unter [Windows Installer Development Tools](windows-installer-development-tools.md).

 

 



