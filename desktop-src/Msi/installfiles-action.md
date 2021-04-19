---
description: Mit der Aktion "InstallFiles" werden die in der Dateitabelle angegebenen Dateien aus dem Quellverzeichnis in das Zielverzeichnis kopiert.
ms.assetid: 187ad82f-13f5-4ea3-913c-2ae7561a6ee6
title: InstallFiles-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c2a0206ec5a64974f27375e175f25ce1888b430
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348839"
---
# <a name="installfiles-action"></a>InstallFiles-Aktion

Mit der Aktion "InstallFiles" werden die in der Dateitabelle angegebenen Dateien aus dem Quellverzeichnis in das Zielverzeichnis kopiert.

## <a name="sequence-restrictions"></a>Sequenz Einschränkungen

Die InstallFiles-Aktion muss nach der [InstallValidate](installvalidate-action.md) -Aktion und vor allen Datei abhängigen Aktionen erfolgen.

## <a name="actiondata-messages"></a>Aktions Daten Meldungen



| Feld | Beschreibung der Aktions Daten                      |
|-------|-------------------------------------------------|
| \[1\] | Der Bezeichner der installierten Datei.                   |
| \[6\] | Größe der installierten Datei in Bytes.                |
| \[9\] | Der Bezeichner des Verzeichnisses, das die installierte Datei enthält. |



 

## <a name="remarks"></a>Bemerkungen

Die InstallFiles-Aktion wird für Dateien ausgeführt, die in der [Dateitabelle](file-table.md)angegeben sind. Jede Datei wird auf Grundlage des Installationsstatus der zugeordneten Komponente der Datei in der [Komponenten Tabelle](component-table.md)installiert. Nur die Dateien, deren Komponenten in den Zustand **msiinstallstatelocal** aufgelöst werden, sind zum Kopieren berechtigt.

Die Aktion "InstallFiles" implementiert die folgenden Spalten der Dateitabelle.

-   Die FileName-Spalte gibt den Ziel Dateinamen an.
-   In der Spalte Version ist die Dateiversion angegeben.
-   In der Spalte Attribute werden die Bits des Datei-und Installations Attributs angegeben.
-   Die Datei Spalte gibt das eindeutige Datei Token an.
-   In der Filesize-Spalte wird die nicht komprimierte Dateigröße in Bytes angegeben.
-   In der Spalte Sprache wird der Bezeichner der Datei Sprache angegeben.
-   Die Sequenz Spalte gibt die Sequenznummer auf dem Medium an.

Die Aktion InstallFiles implementiert die folgenden Spalten der Component-Tabelle.

-   Die \_ Spalte Verzeichnis gibt einen Verweis auf ein [Verzeichnis Tabellen](directory-table.md) Element an.
-   Die Spalte Komponente gibt einen eindeutigen Namen für das Komponenten Element an.

Die angegebene Datei wird nur kopiert, wenn einer der folgenden Punkte zutrifft:

-   Die Datei ist zurzeit nicht auf dem lokalen Computer installiert.
-   Die Datei befindet sich auf dem lokalen Computer, hat jedoch eine niedrigere Versionsnummer als die Datei in der [Dateitabelle](file-table.md).
-   Die Datei befindet sich auf dem lokalen Computer, aber es ist keine zugehörige Versionsnummer vorhanden.

Das Quellverzeichnis für jede zu kopierende Datei wird vom sourcemode bestimmt, das wiederum von dem Wert in der CAB-Spalte der Medien Tabelle abhängt. Eine vollständige Erläuterung des Quell Modus finden Sie in der [Media-Tabelle](media-table.md).

Wenn sich das Quellverzeichnis für eine zu kopierende Datei auf einem Wechsel Datenträger (z. b. eine Diskette oder CD-ROM) befindet, wird durch die InstallFiles-Aktion überprüft, ob die richtigen Quell Medien eingefügt werden, bevor versucht wird, die Datei zu kopieren InstallFiles sucht nach Medien desselben Wechsel Datentyps mit einer [*Volumebezeichnung*](v-gly.md) , die mit dem in der Spalte VolumeLabel der Medien Tabelle angegebenen Wert übereinstimmt. Wenn ein entsprechendes bereitgestelltes Volume gefunden wird, wird der Datei Kopiervorgang fortgesetzt. Wenn keine Entsprechung gefunden wird, fordert ein Dialogfeld an, dass der Benutzer die richtigen Medien einfügt. In diesem Fall wird im Dialogfeld der Medien Name verwendet, der in der Spalte diskprompt der Medien Tabelle als Teil der Eingabeaufforderung gefunden wurde.

Vorsicht muss ausgeführt werden, da die InstallFiles-Aktion eine ursprüngliche Datei löschen und nicht ersetzen kann. Dies tritt auf, wenn bei der InstallFiles-Aktion ein Fehler auftritt, während eine ältere Datei ersetzt wird und der Benutzer die Fehlermeldung ignoriert. Das Standardverhalten des Installers besteht darin, eine alte Datei zu löschen, bevor sichergestellt wird, dass die neue Datei ordnungsgemäß kopiert wird.

Informationen zu den vom Installer verwendeten Regeln für die Datei Versionsverwaltung finden Sie unter Regeln für die [Datei Versions](file-versioning-rules.md)Verwaltung.

 

 



