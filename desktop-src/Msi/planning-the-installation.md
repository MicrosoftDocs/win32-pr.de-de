---
description: Wenn die Installation einer vorhandenen Anwendung aus einer anderen Setup Technologie in Windows Installer verschoben wird, startet der Setup Entwickler möglicherweise mit der Erstellung eines Windows Installer Pakets mithilfe der Quell-und Ziel Datei Images der vorhandenen-Installation.
ms.assetid: 8b0fb473-e19f-4427-b2a1-d0721cde9d38
title: Planen der Installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5eb98368c5c5c8e13a8f9b03a44805a8cff6e517
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866084"
---
# <a name="planning-the-installation"></a>Planen der Installation

Wenn die Installation einer vorhandenen Anwendung aus einer anderen Setup Technologie in Windows Installer verschoben wird, startet der Setup Entwickler möglicherweise mit der Erstellung eines Windows Installer Pakets mithilfe der Quell-und Ziel Datei Images der vorhandenen-Installation. Ein detaillierter Plan, wie die Dateien und anderen Ressourcen an Quelle und Ziel organisiert werden, ist ein guter Ausgangspunkt für die Entwicklung eines Pakets für eine neue Anwendung.

Das Beispiel Installationspaket übernimmt die folgenden Dateien, die am Quell Speicherort für die Anwendung gespeichert sind, und installiert Sie auf dem Computer des Benutzers.



| Datei         | BESCHREIBUNG                               | Pfad zur Quelle                                    | Pfad zum Ziel                                          |
|--------------|-------------------------------------------|---------------------------------------------------|---------------------------------------------------------|
| Redpark.exe  | Ausführbare Datei des Text-Editors.              | C: \\ Beispiel für \\ Notepad \\Redpark.exe                  | \[Ordner "ProgramFilesFolder \] \\ Red \_ Park \\Redpark.exe"          |
| Readme.txt   | Eine Informationsdatei.                    | C: \\ Beispiel für \\ Notepad \\Readme.txt                   | \[Ordner "ProgramFilesFolder \] \\ Red \_ Park \\Readme.txt"           |
| Help.txt     | Hilfe manuell                               | C: \\ Beispiel für \\ Notepad \\Help.txt                     | Nicht installiert. Immer aus Quelle ausführen.                  |
| Baseball.txt | Der Plan für das Baseball Spiel für Jahr 2000.     | C: \\ Beispiel für \\ Notepad- \\ Ereignisse \\Baseball.txt         | \[ProgramFilesFolder \] \\ Red \_ Park \\ Sport \\Baseball.txt |
| Football.txt | Zeitplan für Fußballspiel für Jahr 2000.     | C: \\ Beispiel für \\ Notepad- \\ Ereignisse \\Football.txt         | \[ProgramFilesFolder \] \\ Red \_ Park \\ Sport \\Football.txt |
| Dance.txt    | Tanzaufführungen für Jahr 2000.         | C: \\ Beispiel für \\ Notepad- \\ Ereignisse \\Dance.txt            | \[ProgramFilesFolder \] \\ Red \_ Park \\ Arts \\Dance.txt      |
| Concert.txt  | Musik Aufführungen für Jahr 2000.         | C: \\ Beispiel für \\ Notepad- \\ Ereignisse \\Concert.txt          | \[ProgramFilesFolder \] \\ Red \_ Park \\ Arts \\Concert.txt    |
| January.txt  | Zuweisungen im Januar des Jahres 2000.       | C: \\ Beispiel für \\ Notepad- \\ Gate \\January.txt            | \[ProgramFilesFolder \] \\ rotes \_ Park \\ Gate \\January.txt    |
| NewYears.txt | Eintritte an den neuen Jahren Jahr 2000. | C: \\ Beispiel für \\ Notepad \\ Gate \\ Holidays \\NewYears.txt | \[ProgramFilesFolder \] \\ rotes \_ Park \\ Gate \\NewYears.txt   |



 

Im Beispiel werden die folgenden Werte in der Registrierung des Benutzers unter **HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Notepad Sample** geschrieben.



| Name             | Wert    |
|------------------|----------|
| LF charset        | 0        |
| LF ClipPrecision  | 2        |
| lffacename       | Fixedsys |
| LFI         | 0        |
| lforientation    | 0        |
| LF OutPrecision   | 1        |
| fsavepgesete | 0        |
| LF PitchAndFamily | 49       |
| ipointsize       | 120      |
| LF-Qualität        | 2        |
| LF Strip-out      | 0        |
| LF Weight         | 400      |
| Umbruch            | 0        |



 

Im Beispiel werden die folgenden Tastenkombinationen installiert. Eine dieser Verknüpfungen kann während des Setups als angekündigte Verknüpfung ausgewählt werden, damit der Benutzer die-on-Demand-Baseball Funktion installieren kann.



| Name      | Verknüpfungs Position                         | Verknüpfungs Ziel                                         |
|-----------|-------------------------------------------|---------------------------------------------------------|
| SNotepad  | \[Menü "ProgramFilesFolder \] \\ Red \_ Park" \\\\ | \[Ordner "ProgramFilesFolder \] \\ Red \_ Park \\Redpark.exe"          |
| sInfo   | \[Menü "ProgramFilesFolder \] \\ Red \_ Park" \\\\ | \[Ordner "ProgramFilesFolder \] \\ Red \_ Park \\Readme.txt"           |
| sHelp     | \[Menü "ProgramFilesFolder \] \\ Red \_ Park" \\\\ | \[Editor für ProgramFilesFolder- \] \\ Beispiel \\ \\Help.txt       |
| sbaseball | \[Menü "ProgramFilesFolder \] \\ Red \_ Park" \\\\ | \[ProgramFilesFolder \] \\ Red \_ Park \\ Sport \\Baseball.txt |
| sfußball | \[Menü "ProgramFilesFolder \] \\ Red \_ Park" \\\\ | \[ProgramFilesFolder \] \\ Red \_ Park \\ Sport \\Football.txt |
| sdance    | \[Menü "ProgramFilesFolder \] \\ Red \_ Park" \\\\ | \[ProgramFilesFolder \] \\ Red \_ Park \\ Arts \\Dance.txt      |
| sconcert  | \[Menü "ProgramFilesFolder \] \\ Red \_ Park" \\\\ | \[ProgramFilesFolder \] \\ Red \_ Park \\ Arts \\Concert.txt    |
| sjanuar  | \[Menü "ProgramFilesFolder \] \\ Red \_ Park" \\\\ | \[ProgramFilesFolder \] \\ rotes \_ Park \\ Gate \\January.txt    |
| snewyears | \[Menü "ProgramFilesFolder \] \\ Red \_ Park" \\\\ | \[ProgramFilesFolder \] \\ rotes \_ Park \\ Gate \\NewYears.txt   |



 

Um das Beispiel zu reproduzieren, erstellen Sie zunächst die Quellverzeichnis Struktur, die in der ersten Tabelle angegeben ist. Sie können eine Kopie der Notepad.exe Datei Ihres Systems erstellen und diese Kopie dann Redpark.exe umbenennen. Verwenden Sie den Editor, um die verbleibenden Textdateien zu erstellen. Die Verzeichnisstruktur des Ziels, die Registrierungs Werte und die Verknüpfungen werden durch das Erstellen der Installations Datenbank hinzugefügt.

[Fortsetzen](importing-a-blank-database.md)

 

 



