---
description: Wenn Dateien, Verzeichnisse und andere NTFS-Dateisystemobjekte hinzugefügt, gelöscht und geändert werden, gibt das NTFS-Dateisystem Änderungsjournaldatensätze in Streams ein, einen für jedes Volume auf dem Computer.
ms.assetid: c41aa3a8-c8d8-4bf2-9bbb-d6a6a556c5e4
title: Ändern von Journaldatensätzen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2313dde6a71b36ed046a7086d39ce8e1a86b909cc7c815f295bb8a45c82ab92f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119765990"
---
# <a name="change-journal-records"></a>Ändern von Journaldatensätzen

Wenn Dateien, Verzeichnisse und andere NTFS-Dateisystemobjekte hinzugefügt, gelöscht und geändert werden, gibt das NTFS-Dateisystem Änderungsjournaldatensätze in Streams ein, einen für jedes Volume auf dem Computer. Jeder Datensatz gibt den Änderungstyp und das geänderte Objekt an. Der Offset vom Anfang des Streams für einen bestimmten Datensatz wird als Updatesequenznummer (USN) für den jeweiligen Datensatz bezeichnet. Neue Datensätze werden am Ende des Streams angefügt.

Das NTFS-Dateisystem kann alte Datensätze löschen, um Speicherplatz zu sparen. Wenn benötigte Datensätze gelöscht wurden, wird der Indizierungsdienst wiederhergestellt, indem das Volume neu indiziert wird, wie es auch bei nicht vorhandener Änderungsjournalindizierung der Grund ist.

Das Änderungsjournal protokolliert nur die Tatsache einer Änderung an einer Datei und den Grund für die Änderung (z. B. Schreibvorgänge, Kürzung, Verlängerung, Löschung und so weiter). Es werden nicht genügend Informationen zum Umkehren der Änderung aufzeichnen.

Darüber hinaus können mehrere Änderungen an derselben Datei dazu führen, dass dem aktuellen Datensatz nur ein Grundflag hinzugefügt wird. Wenn dieselbe Art von Änderung mehr als einmal auftritt, schreibt das NTFS-Dateisystem keinen neuen Datensatz für die Änderungen nach der ersten. Beispielsweise führen mehrere Schreibvorgänge ohne intervening schließende und erneut öffnende Vorgänge zu nur einem Änderungsdatensatz mit dem Grundflag USN \_ REASON \_ DATA \_ OVERWRITE.

Um die Funktionsweise des Änderungsjournals zu veranschaulichen, nehmen wir an, dass ein Benutzer in der folgenden Reihenfolge auf eine Datei zutritt:

1.  Schreibt in die Datei.
2.  Legt den Zeitstempel für die Datei fest.
3.  Schreibt in die Datei.
4.  Schneidt die Datei ab.
5.  Schreibt in die Datei.
6.  Schließt die Datei.

In diesem Fall führt das NTFS-Dateisystem die folgenden Aktionen im Änderungsjournal aus (wobei eine \| bitweise OR-Operation angibt).



| Ereignis                                 | NTFS-Dateisystemaktion                                                                                                                                                                                                                                                    |
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Erster Schreibvorgang<br/>    | Das NTFS-Dateisystem schreibt einen neuen USN-Eintrag, für den das Grundflag USN \_ REASON \_ DATA \_ OVERWRITE festgelegt ist. Weitere Informationen zu möglichen Grundflags finden Sie in der [**USN \_ RECORD-Struktur.**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2)<br/>                                                     |
| Festlegen des Dateizeitstempels<br/> | Das NTFS-Dateisystem schreibt einen neuen USN-Eintrag mit der Flageinstellung USN \_ REASON \_ DATA \_ OVERWRITE \| USN REASON BASIC INFO \_ \_ \_ \_ CHANGE.<br/>                                                                                                                            |
| Zweiter Schreibvorgang<br/>     | Das NTFS-Dateisystem schreibt keinen neuen USN-Eintrag. Da USN REASON DATA OVERWRITE bereits für den vorhandenen Datensatz festgelegt ist, werden keine \_ \_ Änderungen am Datensatz \_ vorgenommen.<br/>                                                                                           |
| Abschneiden von Dateien<br/>            | Das NTFS-Dateisystem schreibt einen neuen USN-Eintrag mit der Flageinstellung USN \_ REASON \_ DATA \_ OVERWRITE \| USN REASON BASIC INFO \_ CHANGE \_ \_ \_ \| USN REASON DATA \_ \_ \_ TRUNCATION.<br/>                                                                                           |
| Dritter Schreibvorgang<br/>      | Das NTFS-Dateisystem schreibt keinen neuen USN-Eintrag. Da USN REASON DATA OVERWRITE bereits für den vorhandenen Datensatz festgelegt ist, werden keine \_ \_ Änderungen am Datensatz \_ vorgenommen.<br/>                                                                                           |
| Vorgang zum Schließen<br/>            | Wenn der Benutzer, der Änderungen vorschreibt, der einzige Benutzer der Datei ist, schreibt das NTFS-Dateisystem einen neuen USN-Eintrag mit der folgenden Flageinstellung: USN \_ REASON \_ DATA \_ OVERWRITE \| USN REASON BASIC INFO \_ \_ CHANGE \_ \_ \| USN REASON DATA \_ \_ \_ \| TRUNCATION USN \_ REASON \_ CLOSE.<br/> |



 

Das Änderungsjournal sammelt eine Reihe von Datensätzen zwischen dem ersten Öffnen und dem letzten Schließen einer Datei. Für jeden Datensatz ist ein neues Grundflag festgelegt, das angibt, dass eine neue Art von Änderung aufgetreten ist. Die Sequenz von Datensätzen gibt einen Teilverlauf der Datei an. Der letzte Datensatz, der erstellt wird, wenn die Datei geschlossen wird, fügt das USN \_ REASON \_ CLOSE-Flag hinzu. Dieser Datensatz stellt eine Zusammenfassung der Änderungen an der Datei dar, gibt jedoch im Gegensatz zu den vorherigen Datensätzen keinen Hinweis auf die Reihenfolge der Änderungen.

Der nächste Benutzer, der auf die Datei zugreifen und diese ändern soll, generiert einen neuen USN-Eintrag mit einem Flag für einen einzelnen Grund.

 

 




