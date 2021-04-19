---
description: Wenn Windows Installer für die Installation und Einrichtung einer Anwendung verwendet wird, können spätere Upgrades dieser Anwendung durch die Installation eines upgradepakets durchgeführt werden.
ms.assetid: 69ad4928-e750-47c2-8668-c9e3deff8066
title: Planen eines größeren Upgrades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88ca6b82e53a38dde8131525eb885a5f17603ac6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348683"
---
# <a name="planning-a-major-upgrade"></a>Planen eines größeren Upgrades

Wenn Windows Installer für die Installation und Einrichtung einer Anwendung verwendet wird, können spätere Upgrades dieser Anwendung durch die Installation eines upgradepakets durchgeführt werden. Setup Entwickler können ein Upgradepaket erstellen, indem Sie das ursprüngliche Installationspaket ändern. Diese Vorgehensweise wird im folgenden upgradebeispiel veranschaulicht.

Bei der Installation des ursprünglichen Produkts, MNP2000, gefolgt von der Installation des upgradepakets, werden dem Benutzer die folgenden Dateien für das Produkt MNP2001 zur Verfügung stehen.



| Datei          | BESCHREIBUNG                                                    | Pfad zur Quelle                                    | Pfad zum Ziel                                          |
|---------------|----------------------------------------------------------------|---------------------------------------------------|---------------------------------------------------------|
| Redpark.exe   | Ausführbare Datei des Text-Editors. Unverändert gegenüber vorherigen Produkten. | C: \\ Beispiel für \\ Notepad \\Redpark.exe                  | \[Ordner "ProgramFilesFolder \] \\ Red \_ Park \\Redpark.exe"          |
| Readme.txt    | Eine Informationsdatei. Unverändert gegenüber vorherigen Produkten.         | C: \\ Beispiel für \\ Notepad \\Readme.txt                   | \[Ordner "ProgramFilesFolder \] \\ Red \_ Park \\Readme.txt"           |
| Help.txt      | Hilfe manuell. Unverändert gegenüber vorherigen Produkten.                 | C: \\ Beispiel für \\ Notepad \\Help.txt                     | Nicht installiert. Immer aus Quelle ausführen.                  |
| Baseba01.txt  | Der Plan für das Baseball Spiel für Jahr 2001.                          | C: \\ Beispiel für \\ Notepad- \\ Ereignisse \\Baseba01.txt         | \[ProgramFilesFolder \] \\ Red \_ Park \\ Sport \\Baseball.txt |
| Footba01.txt  | Zeitplan für Fußballspiel für Jahr 2001.                          | C: \\ Beispiel für \\ Notepad- \\ Ereignisse \\Footba01.txt         | \[ProgramFilesFolder \] \\ Red \_ Park \\ Sport \\Football.txt |
| Basket01.txt  | Kalender Spiel Zeitplan für Jahr 2001.                        | C: \\ Beispiel für \\ Notepad- \\ Ereignisse \\Basket01.txt         | \[ProgramFilesFolder \] \\ Red \_ Park \\ Sport \\Basket01.txt |
| Dance01.txt   | Tanzaufführungen für Jahr 2001.                              | C: \\ Beispiel für \\ Notepad- \\ Ereignisse \\Dance01.txt          | \[ProgramFilesFolder \] \\ Red \_ Park \\ Arts \\Dance.txt      |
| Concert01.txt | Musik Aufführungen für Jahr 2001.                              | C: \\ Beispiel für \\ Notepad- \\ Ereignisse \\Concer01.txt         | \[ProgramFilesFolder \] \\ Red \_ Park \\ Arts \\Concert.txt    |
| Opera01.txt   | Opernaufführungen für Jahr 2001.                              | C: \\ Beispiel für \\ Notepad- \\ Ereignisse \\Opera01.txt          | \[ProgramFilesFolder \] \\ Red \_ Park \\ Arts \\Opera01.txt    |
| Januar01.txt  | Zuweisungen im Januar des Jahres 2001.                            | C: \\ Beispiel für \\ Notepad- \\ Gate \\Januar01.txt           | \[ProgramFilesFolder \] \\ rotes \_ Park \\ Gate \\January.txt    |
| NewYea01.txt  | Eintritte an den neuen Jahren Jahr 2001.                      | C: \\ Beispiel für \\ Notepad \\ Gate \\ Holidays \\NewYea01.txt | \[ProgramFilesFolder \] \\ rotes \_ Park \\ Gate \\NewYears.txt   |
| Memori01.txt  | Eintritte am Gedenktag des Jahres 2001.                       | C: \\ Beispiel für \\ Notepad \\ Gate \\ Holidays \\Memori01.txt | \[ProgramFilesFolder \] \\ rotes \_ Park \\ Gate \\Memori01.txt   |



 

Bei der Installation des upgradepakets werden alle mit dem ursprünglichen Produkt installierten Features entfernt, die nicht vom aktualisierten Produkt verwendet werden.

Wenn Sie z. b. ein Upgrade von MNP2000 ausführen, werden die folgenden Dateien vom Computer des Benutzers entfernt:

-   Baseball.txt
-   Football.txt
-   Dance.txt
-   Concert.txt
-   January.txt
-   NewYears.txt

Bei der Installation des upgradepakets werden folgende Werte in die Registrierung des Benutzers geschrieben:

**HKEY \_ Beispiel für lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **Notepad**



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



 

Das Upgrade aktualisiert alte Verknüpfungen zu den folgenden Tastenkombinationen. Eine dieser Verknüpfungen kann während des Setups als angekündigte Verknüpfung ausgewählt werden, damit der Benutzer die-on-Demand-Baseball Funktion installieren kann.



| Name        | Verknüpfungs Position                         | Verknüpfungs Ziel                                           |
|-------------|-------------------------------------------|-----------------------------------------------------------|
| SNotepad    | \[Menü "ProgramFilesFolder \] \\ Red \_ Park" \\\\ | \[Ordner "ProgramFilesFolder \] \\ Red \_ Park \\Redpark.exe"            |
| sInfo     | \[Menü "ProgramFilesFolder \] \\ Red \_ Park" \\\\ | \[Ordner "ProgramFilesFolder \] \\ Red \_ Park \\Readme.txt"             |
| sHelp       | \[Menü "ProgramFilesFolder \] \\ Red \_ Park" \\\\ | \[Editor für ProgramFilesFolder- \] \\ Beispiel \\ \\Help.txt         |
| sbaseball   | \[Menü "ProgramFilesFolder \] \\ Red \_ Park" \\\\ | \[ProgramFilesFolder \] \\ Red \_ Park \\ Sport \\Baseba01.txt   |
| sfußball   | \[Menü "ProgramFilesFolder \] \\ Red \_ Park" \\\\ | \[ProgramFilesFolder \] \\ Red \_ Park \\ Sport \\Footba01.txt   |
| sbasketball | \[Menü "ProgramFilesFolder \] \\ Red \_ Park" \\\\ | \[ProgramFilesFolder \] \\ Red \_ Park \\ Sport \\Basketba01.txt |
| sdance      | \[Menü "ProgramFilesFolder \] \\ Red \_ Park" \\\\ | \[ProgramFilesFolder \] \\ Red \_ Park \\ Arts \\Dance01.txt      |
| sconcert    | \[Menü "ProgramFilesFolder \] \\ Red \_ Park" \\\\ | \[ProgramFilesFolder \] \\ Red \_ Park \\ Arts \\Concer01.txt     |
| SOPERA      | \[Menü "ProgramFilesFolder \] \\ Red \_ Park" \\\\ | \[ProgramFilesFolder \] \\ Red \_ Park \\ Arts \\Opera01.txt      |
| sjanuar    | \[Menü "ProgramFilesFolder \] \\ Red \_ Park" \\\\ | \[ProgramFilesFolder \] \\ rotes \_ Park \\ Gate \\Januar01.txt     |
| snewyears   | \[Menü "ProgramFilesFolder \] \\ Red \_ Park" \\\\ | \[ProgramFilesFolder \] \\ rotes \_ Park \\ Gate \\NewYea01.txt     |
| smemorial   | \[Menü "ProgramFilesFolder \] \\ Red \_ Park" \\\\ | \[ProgramFilesFolder \] \\ rotes \_ Park \\ Gate \\Memori01.txt     |



 

Wenn ein Benutzer das Upgradepaket deinstalliert, entfernt Windows Installer alle Versionen des Produkts vollständig auf dem Computer des Benutzers. Der Benutzer hat keine Teile von MNP2000 oder MNP2001.

[Fortsetzen](importing-original-installation-database.md)

 

 



