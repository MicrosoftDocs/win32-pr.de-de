---
description: Wenn eine Änderung an einer Datei oder einem Verzeichnis in einem Volume vorgenommen wird, wird das Änderungs Journal für die Aktualisierung des Volumes mit einer Beschreibung der Änderung und des Datei-oder Verzeichnis namens aktualisiert.
ms.assetid: 9a158c2b-da8e-4ca9-b3c1-2185cf41eb7d
title: Ändern von Journalen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb5052ec87830a822270071a6ee00f1c3f7cffdd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868255"
---
# <a name="change-journals"></a>Ändern von Journalen

Eine automatische Sicherungs Anwendung ist ein Beispiel für ein Programm, das eine Überprüfung auf Änderungen am Status eines Volumes durchführen muss, um seine Aufgabe auszuführen. Die Brute-Force-Methode zum Überprüfen von Änderungen in Verzeichnissen oder Dateien besteht darin, das gesamte Volume zu scannen. Dies ist jedoch häufig keine akzeptable Vorgehensweise, da die Systemleistung beeinträchtigt wird. Eine andere Methode besteht darin, dass die Anwendung eine Verzeichnis Benachrichtigung (durch Aufrufen der Funktionen [**findfirstchangenotifior**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstchangenotificationa) [**leaddirectorychangesw**](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw) ) für die zu sichernden Verzeichnisse registriert. Dies ist effizienter als die erste Methode, erfordert jedoch, dass eine Anwendung immer ausgeführt wird. Wenn eine große Anzahl von Verzeichnissen und Dateien gesichert werden muss, kann die Leistung des Betriebssystems durch die Menge an Verarbeitung und den Arbeitsspeicher Aufwand für eine solche Anwendung ebenfalls beeinträchtigt werden.

Um diese Nachteile zu vermeiden, verwaltet das NTFS-Dateisystem ein Änderungs Journal für eine Aktualisierungs Sequenznummer (Update Sequence Number, n). Wenn eine Änderung an einer Datei oder einem Verzeichnis in einem Volume vorgenommen wird, wird das Änderungs Journal für die Aktualisierung des Volumes mit einer Beschreibung der Änderung und des Datei-oder Verzeichnis namens aktualisiert.

Änderungs Journale sind auch erforderlich, um die Dateisystem Indizierung nach einem Computer-oder Volumefehler wiederherzustellen. Die Möglichkeit, die Indizierung wiederherzustellen, bedeutet, dass das Dateisystem den zeitaufwändigen Prozess der Neuindizierung des gesamten Volumes in solchen Fällen vermeiden kann.

In den folgenden Themen werden Änderungs Journale erörtert.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                                             | BESCHREIBUNG                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Journal Datensätze ändern](change-journal-records.md)<br/>                                                                   | Beim Hinzufügen, löschen und Ändern von Dateien, Verzeichnissen und anderen NTFS-Dateisystemobjekten werden vom NTFS-Dateisystem Datensätze für Änderungs Journal in Streams eingegeben, eine für jedes Volume auf dem Computer.<br/>                                           |
| [Verwenden des Änderungs Journal Bezeichners](using-the-change-journal-identifier.md)<br/>                                         | Das NTFS-Dateisystem ordnet jedem Änderungs Journal einen 64-Bit-Bezeichner ohne Vorzeichen zu.<br/>                                                                                                                                                   |
| [Erstellen, ändern und Löschen eines Änderungs Journals](creating-modifying-and-deleting-a-change-journal.md)<br/>             | Administratoren können Änderungs Journale erstellen, löschen und neu erstellen.<br/>                                                                                                                                                                         |
| [Abrufen eines Volumehandles für Änderungs Journal Vorgänge](obtaining-a-volume-handle-for-change-journal-operations.md)<br/> | Rufen Sie zum Abrufen eines Handles für ein Volume zur Verwendung mit Aktualisierungs Zeichenfolgenvorgängen (Update Sequence Number, Aktualisierungs Sequenznummer) die Funktion "| [**atefile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) " mit dem Parameter " *lpFileName* " auf, die auf eine Zeichenfolge in der folgenden Form \\ \\ \\ *X*.<br/> |
| [Ändern von Journal Vorgängen](change-journal-operations.md)<br/>                                                             | Steuern Sie Codes und Strukturen, die mit dem Änderungs Journal für die NTFS-Dateisystem-Aktualisierungs Sequenznummer verwendet werden sollen.<br/>                                                                                                                                |



 

 

 




