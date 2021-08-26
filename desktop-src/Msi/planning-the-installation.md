---
description: Wenn die Installation einer vorhandenen Anwendung von einer anderen Setuptechnologie in den Windows-Installer verschoben wird, kann der Setupentwickler mit der Erstellung eines Windows Installer-Pakets beginnen, indem er die Quell- und Zieldateiabbilder der vorhandenen Installation verwendet.
ms.assetid: 8b0fb473-e19f-4427-b2a1-d0721cde9d38
title: Planen der Installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d406ec97fd5edb34468586eb9f707eff32b289df3dc88b803b8c55d4aad10cd1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042360"
---
# <a name="planning-the-installation"></a>Planen der Installation

Wenn die Installation einer vorhandenen Anwendung von einer anderen Setuptechnologie in den Windows-Installer verschoben wird, kann der Setupentwickler mit der Erstellung eines Windows Installer-Pakets beginnen, indem er die Quell- und Zieldateiabbilder der vorhandenen Installation verwendet. Ein detaillierter Plan für die Organisation der Dateien und anderen Ressourcen an Quelle und Ziel ist auch ein guter Ausgangspunkt für die Entwicklung eines Pakets für eine neue Anwendung.

Das Beispielinstallationspaket verwendet die folgenden Dateien, die am Quellspeicherort für die Anwendung gespeichert sind, und installiert sie auf dem Ziel auf dem Computer des Benutzers.



| Datei         | BESCHREIBUNG                               | Pfad zur Quelle                                    | Pfad zum Ziel                                          |
|--------------|-------------------------------------------|---------------------------------------------------|---------------------------------------------------------|
| Redpark.exe  | Ausführbare Text-Editor-Datei.              | C: \\ \\ Beispiel Editor \\Redpark.exe                  | \[ProgramFilesFolder \] \\ Red Park \_ \\Redpark.exe          |
| Readme.txt   | Eine Informationsdatei.                    | C: \\ \\ Beispiel Editor \\Readme.txt                   | \[ProgramFilesFolder \] \\ Red Park \_ \\Readme.txt           |
| Help.txt     | Hilfehandbuch                               | C: \\ \\ Beispiel Editor \\Help.txt                     | Nicht installiert. Führen Sie immer aus der Quelle aus.                  |
| Baseball.txt | Baseballspielzeitplan für jahr 2000.     | C: \\ Beispiel für Editor Ereignisse \\ \\ \\Baseball.txt         | \[ProgramFilesFolder \] \\ Red Park Sports \_ \\ \\Baseball.txt |
| Football.txt | Spielzeitplan für das Jahr 2000.     | C: \\ Beispiel für Editor Ereignisse \\ \\ \\Football.txt         | \[ProgramFilesFolder \] \\ Red Park Sports \_ \\ \\Football.txt |
| Dance.txt    | Musikvorführung für das Jahr 2000.         | C: \\ Beispiel für Editor Ereignisse \\ \\ \\Dance.txt            | \[ProgramFilesFolder \] \\ Red \_ \\ Park- und \\Dance.txt      |
| Concert.txt  | Musik Jahr 2000.         | C: \\ Beispiel für Editor Ereignisse \\ \\ \\Concert.txt          | \[ProgramFilesFolder \] \\ Red \_ \\ Park- und \\Concert.txt    |
| January.txt  | Zulassungen im Januar des Jahres 2000.       | C: \\ Beispiel für Editor \\ \\ \\ GateJanuary.txt            | \[ProgramFilesFolder \] \\ Red Park Gate \_ \\ \\January.txt    |
| NewYears.txt | Zulassungen am Neujahrstag des Jahres 2000. | C: \\ Beispiel für Editor \\ \\ \\ \\ Gate-FeiertageNewYears.txt | \[ProgramFilesFolder \] \\ Red Park Gate \_ \\ \\NewYears.txt   |



 

Das Beispiel schreibt die folgenden Werte in die Registrierung des Benutzers unter **HKEY \_ LOCAL MACHINE SOFTWARE Microsoft Editor \_ \\ \\ \\ Sample**.



| Name             | Wert    |
|------------------|----------|
| lfCharSet        | 0        |
| lfClipPrecision  | 2        |
| lfFaceName       | FixedSys |
| lfItalic         | 0        |
| lfOrientation    | 0        |
| lfOutPrecision   | 1        |
| fSavePageSetting | 0        |
| lfPitchAndFamily | 49       |
| iPointSize       | 120      |
| lfQuality        | 2        |
| lfStrikeOut      | 0        |
| lfWeight         | 400      |
| fWrap            | 0        |



 

Im Beispiel werden die folgenden Tastenkombinationen installiert. Eine dieser Tastenkombinationen kann während des Setups als angekündigte Verknüpfung ausgewählt werden, damit der Benutzer das Baseball-Feature bei Bedarf installieren kann.



| Name      | Verknüpfungsposition                         | Verknüpfungsziel                                         |
|-----------|-------------------------------------------|---------------------------------------------------------|
| sNotepad  | \[ProgramFilesFolder \] \\ Red \_ Park \\ Menu\\ | \[ProgramFilesFolder \] \\ Red Park \_ \\Redpark.exe          |
| sReadme   | \[ProgramFilesFolder \] \\ Red \_ Park \\ Menu\\ | \[ProgramFilesFolder \] \\ Red Park \_ \\Readme.txt           |
| sHelp     | \[ProgramFilesFolder \] \\ Red \_ Park \\ Menu\\ | \[ProgramFilesFolder-Editor \] \\ \\ \\Help.txt       |
| sBaseball | \[ProgramFilesFolder \] \\ Red \_ Park \\ Menu\\ | \[ProgramFilesFolder \] \\ Red Park Sports \_ \\ \\Baseball.txt |
| sFootball | \[ProgramFilesFolder \] \\ Red \_ Park \\ Menu\\ | \[ProgramFilesFolder \] \\ Red Park Sports \_ \\ \\Football.txt |
| sDance    | \[ProgramFilesFolder \] \\ Red \_ Park \\ Menu\\ | \[ProgramFilesFolder \] \\ Red \_ \\ Park- und \\Dance.txt      |
| sConcert  | \[ProgramFilesFolder \] \\ Red \_ Park \\ Menu\\ | \[ProgramFilesFolder \] \\ Red Park \_ \\Concert.txt \\    |
| sJanuary  | \[ProgramFilesFolder \] \\ Red \_ Park \\ Menu\\ | \[ProgramFilesFolder \] \\ Red Park Gate \_ \\ \\January.txt    |
| sNewYears | \[ProgramFilesFolder \] \\ Red \_ Park \\ Menu\\ | \[ProgramFilesFolder \] \\ Red Park Gate \_ \\ \\NewYears.txt   |



 

Um das Beispiel zu reproduzieren, erstellen Sie zunächst die Quellverzeichnisstruktur, die in der ersten Tabelle angegeben ist. Sie können eine Kopie der Notepad.exe-Datei Ihres Systems erstellen und diese Kopie dann Redpark.exe umbenennen. Verwenden Sie den Editor Editor, um die verbleibenden Textdateien zu erstellen. Die Verzeichnisstruktur des Ziels, die Registrierungswerte und die Verknüpfungen werden durch Erstellen der Installationsdatenbank hinzugefügt.

[Fortsetzen](importing-a-blank-database.md)

 

 



