---
description: Wenn Windows Installer für die Installation und Einrichtung einer Anwendung verwendet wird, können spätere Upgrades dieser Anwendung durch Installieren eines Upgradepakets durchgeführt werden.
ms.assetid: 69ad4928-e750-47c2-8668-c9e3deff8066
title: Planen eines größeren Upgrades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a07ece8acf0dbc37ecdfddaa3505e5e54a283a8e8efd7b4eb0dc1a0a365a461e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118377371"
---
# <a name="planning-a-major-upgrade"></a>Planen eines größeren Upgrades

Wenn Windows Installer für die Installation und Einrichtung einer Anwendung verwendet wird, können spätere Upgrades dieser Anwendung durch Installieren eines Upgradepakets durchgeführt werden. Setupentwickler können ein Upgradepaket erstellen, indem sie das ursprüngliche Installationspaket ändern. Dieser Ansatz wird im folgenden Upgradebeispiel veranschaulicht.

Die Installation des originalen Produkts MNP2000, gefolgt von der Installation des Upgradepakets, stellt dem Benutzer die folgenden Dateien bereit, die für das Produkt MNP2001 erforderlich sind.



| Datei          | BESCHREIBUNG                                                    | Pfad zur Quelle                                    | Pfad zum Ziel                                          |
|---------------|----------------------------------------------------------------|---------------------------------------------------|---------------------------------------------------------|
| Redpark.exe   | Ausführbare Datei des Text-Editors. Unverändert von vorherigen Produkten. | C: \\ Beispiel \\ Editor \\Redpark.exe                  | \[ProgramFilesFolder \] \\ Red Park \_ \\Redpark.exe          |
| Readme.txt    | Eine Informationsdatei. Unverändert von vorherigen Produkten.         | C: \\ Beispiel \\ Editor \\Readme.txt                   | \[ProgramFilesFolder \] \\ Red Park \_ \\Readme.txt           |
| Help.txt      | Hilfehandbuch. Unverändert von vorherigen Produkten.                 | C: \\ Beispiel \\ Editor \\Help.txt                     | Nicht installiert. Immer aus der Quelle ausführen.                  |
| Baseba01.txt  | Baseballspielzeitplan für das Jahr 2001.                          | C: \\ Beispiel für Editor Ereignisse \\ \\ \\Baseba01.txt         | \[ProgramFilesFolder \] \\ Red Park Sports \_ \\ \\Baseball.txt |
| Footba01.txt  | Zeitplan für Das Footballspiel für das Jahr 2001.                          | C: \\ Beispiel für Editor Ereignisse \\ \\ \\Footba01.txt         | \[ProgramFilesFolder \] \\ Red Park Sports \_ \\ \\Football.txt |
| Basket01.txt  | Gameplan für Das Jahr 2001.                        | C: \\ Beispiel für Editor Ereignisse \\ \\ \\Basket01.txt         | \[ProgramFilesFolder \] \\ Red Park Sports \_ \\ \\Basket01.txt |
| Dance01.txt   | Musikleistungen für das Jahr 2001.                              | C: \\ Beispiel für Editor Ereignisse \\ \\ \\Dance01.txt          | \[ProgramFilesFolder \] \\ Red Park \_ \\Dance.txt \\      |
| Concert01.txt | Musik Leistungen für das Jahr 2001.                              | C: \\ Beispiel für Editor Ereignisse \\ \\ \\Concer01.txt         | \[ProgramFilesFolder \] \\ Red Park \_ \\Concert.txt \\    |
| Opera01.txt   | Opera-Leistungen für das Jahr 2001.                              | C: \\ Beispiel für Editor Ereignisse \\ \\ \\Opera01.txt          | \[ProgramFilesFolder \] \\ Red Park \_ \\Opera01.txt \\    |
| Januar01.txt  | Zulassungen im Januar des Jahres 2001.                            | C: \\ Beispiel für Editor \\ \\ \\ Gate-Januar01.txt           | \[ProgramFilesFolder \] \\ Red Park Gate \_ \\ \\January.txt    |
| NewYea01.txt  | Eintritte am Neujahrstag des Jahres 2001.                      | C: \\ Beispiel für Editor \\ \\ \\ \\ Gate-NewYea01.txt | \[ProgramFilesFolder \] \\ Red Park Gate \_ \\ \\NewYears.txt   |
| Memori01.txt  | Eintritte am Tag des Jahres 2001.                       | C: \\ Beispiel für Editor \\ \\ \\ \\ Gate-Memori01.txt | \[ProgramFilesFolder \] \\ Red Park Gate \_ \\ \\Memori01.txt   |



 

Bei der Installation des Upgradepakets werden alle Features entfernt, die mit dem ursprünglichen Produkt installiert wurden und nicht vom aktualisierten Produkt verwendet werden.

Wenn Sie beispielsweise ein Upgrade von MNP2000 durchführen, werden bei der Installation des Upgrades die folgenden Dateien vom Computer des Benutzers entfernt:

-   Baseball.txt
-   Football.txt
-   Dance.txt
-   Concert.txt
-   January.txt
-   NewYears.txt

Bei der Installation des Upgradepakets werden die folgenden Werte in die Registrierung des Benutzers geschrieben:

**HKEY \_ Microsoft \_** \\  \\  \\ **Editor-Beispiel** für LOKALE COMPUTERSOFTWARE



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



 

Das Upgrade aktualisiert alte Verknüpfungen auf die folgenden Tastenkombinationen. Eine dieser Tastenkombinationen kann während des Setups als angekündigte Verknüpfung ausgewählt werden, damit der Benutzer das Baseball-Feature bei Bedarf installieren kann.



| Name        | Verknüpfungsposition                         | Kontextziel                                           |
|-------------|-------------------------------------------|-----------------------------------------------------------|
| sNotepad    | \[ProgramFilesFolder \] \\ Red \_ Park \\ Menu\\ | \[ProgramFilesFolder \] \\ Red Park \_ \\Redpark.exe            |
| sReadme     | \[ProgramFilesFolder \] \\ Red \_ Park \\ Menu\\ | \[ProgramFilesFolder \] \\ Red Park \_ \\Readme.txt             |
| sHelp       | \[ProgramFilesFolder \] \\ Red \_ Park \\ Menu\\ | \[ProgramFilesFolder-Beispiel \] \\ \\ Editor \\Help.txt         |
| sBaseball   | \[ProgramFilesFolder \] \\ Red \_ Park \\ Menu\\ | \[ProgramFilesFolder \] \\ Red Park Sports \_ \\ \\Baseba01.txt   |
| sFootball   | \[ProgramFilesFolder \] \\ Red \_ Park \\ Menu\\ | \[ProgramFilesFolder \] \\ Red Park Sports \_ \\ \\Footba01.txt   |
| sBasketball | \[ProgramFilesFolder \] \\ Red \_ Park \\ Menu\\ | \[ProgramFilesFolder \] \\ Red Park Sports \_ \\ \\Basketba01.txt |
| sDance      | \[ProgramFilesFolder \] \\ Red \_ Park \\ Menu\\ | \[ProgramFilesFolder \] \\ Red Park \_ \\Dance01.txt \\      |
| sConcert    | \[ProgramFilesFolder \] \\ Red \_ Park \\ Menu\\ | \[ProgramFilesFolder \] \\ Red Park \_ \\Concer01.txt \\     |
| Sopera      | \[ProgramFilesFolder \] \\ Red \_ Park \\ Menu\\ | \[ProgramFilesFolder \] \\ Red Park \_ \\Opera01.txt \\      |
| sJanuary    | \[ProgramFilesFolder \] \\ Red \_ Park \\ Menu\\ | \[ProgramFilesFolder \] \\ Red Park Gate \_ \\ \\Januar01.txt     |
| sNewYears   | \[ProgramFilesFolder \] \\ Red \_ Park \\ Menu\\ | \[ProgramFilesFolder \] \\ Red Park Gate \_ \\ \\NewYea01.txt     |
| sMeirial   | \[ProgramFilesFolder \] \\ Red \_ Park \\ Menu\\ | \[ProgramFilesFolder \] \\ Red Park Gate \_ \\ \\Memori01.txt     |



 

Wenn ein Benutzer das Upgradepaket deinstalliert, entfernt Windows Installer alle Versionen des Produkts vollständig vom Computer des Benutzers. Dem Benutzer werden keine Teile von MNP2000 oder MNP2001 überlassen.

[Fortsetzen](importing-original-installation-database.md)

 

 



