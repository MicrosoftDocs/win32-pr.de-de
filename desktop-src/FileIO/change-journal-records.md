---
description: Beim Hinzufügen, löschen und Ändern von Dateien, Verzeichnissen und anderen NTFS-Dateisystemobjekten werden vom NTFS-Dateisystem Datensätze für Änderungs Journal in Streams eingegeben, eine für jedes Volume auf dem Computer.
ms.assetid: c41aa3a8-c8d8-4bf2-9bbb-d6a6a556c5e4
title: Journal Datensätze ändern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56580a28c01ca164af4598cb290a37c8e36828f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363721"
---
# <a name="change-journal-records"></a>Journal Datensätze ändern

Beim Hinzufügen, löschen und Ändern von Dateien, Verzeichnissen und anderen NTFS-Dateisystemobjekten werden vom NTFS-Dateisystem Datensätze für Änderungs Journal in Streams eingegeben, eine für jedes Volume auf dem Computer. Jeder Datensatz gibt den Änderungstyp und das geänderte Objekt an. Der Offset vom Anfang des Streams für einen bestimmten Datensatz wird als Update Sequenznummer (Update Sequence Number, US-v) für den jeweiligen Datensatz bezeichnet. Neue Datensätze werden am Ende des Streams angefügt.

Das NTFS-Dateisystem kann alte Datensätze löschen, um Speicherplatz zu sparen. Wenn erforderliche Datensätze gelöscht wurden, wird der Indizierungs Dienst durch Erneutes Indizieren des Volumes wieder hergestellt. Dies ist auch dann der Fall, wenn kein Änderungs Journal vorhanden ist.

Im Änderungs Journal wird nur die Tatsache protokolliert, dass eine Datei geändert wurde, und der Grund für die Änderung (z. b. Schreibvorgänge, abschneiden, verlängern, löschen usw.). Es werden nicht genügend Informationen aufgezeichnet, um das Umkehren der Änderung zuzulassen.

Darüber hinaus können mehrere Änderungen an derselben Datei dazu führen, dass dem aktuellen Datensatz nur ein Reason-Flag hinzugefügt wird. Wenn die gleiche Art von Änderung mehrmals auftritt, schreibt das NTFS-Dateisystem keinen neuen Datensatz für die Änderungen nach dem ersten. Beispielsweise führen mehrere Schreibvorgänge ohne zwischengeschaltete Vorgänge zum Schließen und wieder öffnen zu nur einem Änderungs Daten Satz mit dem Grund Flag "USN-Grund für die \_ \_ Daten \_ Überschreibung".

Um zu veranschaulichen, wie das Änderungs Journal funktioniert, wird angenommen, dass ein Benutzer in der folgenden Reihenfolge auf eine Datei zugreift:

1.  Schreibt in die Datei.
2.  Legt den Zeitstempel für die Datei fest.
3.  Schreibt in die Datei.
4.  Die Datei wird abgeschnitten.
5.  Schreibt in die Datei.
6.  Schließt die Datei.

In diesem Fall führt das NTFS-Dateisystem die folgenden Aktionen im Änderungs Journal aus (wobei \| eine bitweise OR-Operation angibt).



| Ereignis                                 | NTFS-Dateisystem Aktion                                                                                                                                                                                                                                                    |
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Anfangs Schreibvorgang<br/>    | Das NTFS-Dateisystem schreibt einen neuen USN-Datensatz mit dem \_ Grund Flag "USN Reason \_ Data \_ Überschreibungs Grund". Weitere Informationen zu möglichen Reason Flags finden Sie in der Struktur der Struktur des Daten [**\_ Satzes**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) .<br/>                                                     |
| Einstellung des Datei Zeitstempels<br/> | Das NTFS-Dateisystem schreibt einen neuen USN-Datensatz mit dem Flag Setting USN \_ reason \_ Data \_ Überschreibungs- \| USN Grund \_ \_ grundlegende \_ Informationen \_ ändern.<br/>                                                                                                                            |
| Zweiter Schreibvorgang<br/>     | Das NTFS-Dateisystem schreibt keinen neuen US-Daten Satz. Da \_ \_ \_ das Überschreiben von Daten aus der Datenbank für den vorhandenen Datensatz bereits festgelegt wurde, werden keine Änderungen am Datensatz vorgenommen.<br/>                                                                                           |
| Dateitrunzierung<br/>            | Das NTFS-Dateisystem schreibt einen neuen USN-Datensatz mit dem Flag "USN \_ reason \_ Data Überschreibung USN Reason Data Überschreibung USN Reason \_ \| \_ \_ Basic \_ Info \_ Change \| USN \_ reason \_ Data \_ trunation".<br/>                                                                                           |
| Dritter Schreibvorgang<br/>      | Das NTFS-Dateisystem schreibt keinen neuen US-Daten Satz. Da \_ \_ \_ das Überschreiben von Daten aus der Datenbank für den vorhandenen Datensatz bereits festgelegt wurde, werden keine Änderungen am Datensatz vorgenommen.<br/>                                                                                           |
| Vorgang schließen<br/>            | Wenn der Benutzer, der Änderungen vornimmt, der einzige Benutzer der Datei ist, schreibt das NTFS-Dateisystem einen neuen USN-Datensatz mit der folgenden Flag-Einstellung: USN \_ reason \_ Data \_ Überschreibung \| USN \_ reason \_ grundlegende \_ Informationen ändern USN \_ \| \_ Ursache \_ Daten \_ Abschneiden \| USN \_ reason \_ Close.<br/> |



 

Das Änderungs Journal sammelt eine Reihe von Datensätzen zwischen dem ersten öffnenden und dem letzten Schließen einer Datei. Für jeden Datensatz wurde ein neues Reason-Flag festgelegt, das angibt, dass eine neue Art von Änderung aufgetreten ist. Die Reihenfolge der Datensätze ergibt einen partiellen Verlauf der Datei. Der endgültige Datensatz, der beim Schließen der Datei erstellt wird, fügt das Flag "USN \_ reason Close" hinzu \_ . Dieser Datensatz stellt eine Zusammenfassung der Änderungen an der Datei dar. im Gegensatz zu den vorherigen Datensätzen gibt es jedoch keinen Hinweis auf die Reihenfolge der Änderungen.

Der nächste Benutzer, der auf die Datei zugreifen und diese ändern möchte, generiert einen neuen USN-Datensatz mit einem einzelnen Reason-Flag.

 

 




