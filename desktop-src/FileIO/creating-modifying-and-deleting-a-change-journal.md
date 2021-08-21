---
description: Administratoren können Änderungsjournale erstellen, löschen und neu erstellen.
ms.assetid: 26cbacc2-d26b-434b-91b5-31aedc96da13
title: Erstellen, Ändern und Löschen eines Änderungsjournals
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3d4cf9a597baa14fc929028eab262479da30797a2e423b779083f028927ce50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118150866"
---
# <a name="creating-modifying-and-deleting-a-change-journal"></a>Erstellen, Ändern und Löschen eines Änderungsjournals

Administratoren können Änderungsjournale nach Be wunsch erstellen, löschen und neu erstellen. Ein Administrator sollte ein Journal löschen, wenn sich der aktuelle Wert der Updatesequenznummer (USN) dem maximal möglichen USN-Wert nähert, wie vom **MaxUsn-Element** der [**USN \_ JOURNAL \_ DATA-Struktur**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_journal_data_v0) angegeben. Ein Administrator kann auch ein Änderungsjournal löschen und neu erstellen, um Speicherplatz frei zu machen. Um diese und alle anderen nicht programmgesteuerten Änderungsjournalvorgänge ausführen zu können, benötigen Sie Systemadministratorberechtigungen. Das heißt, Sie müssen Mitglied der Gruppe Administratoren sein.

Verwenden Sie den [**FSCTL \_ CREATE \_ USN JOURNAL-Steuerungscode, \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_create_usn_journal) um ein Änderungsjournal auf einem angegebenen Volume programmgesteuert zu erstellen oder zu ändern.

Wenn Sie ein neues Änderungsjournal erstellen oder ein vorhandenes ändern, legt das NTFS-Dateisystem Informationen für dieses Änderungsjournal aus Informationen in der [**CREATE \_ USN \_ JOURNAL \_ DATA-Struktur**](/windows/desktop/api/WinIoCtl/ns-winioctl-create_usn_journal_data) fest, die [**FSCTL CREATE \_ \_ USN \_ JOURNAL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_create_usn_journal) als Eingabe übernimmt. **CREATE \_ USN \_ JOURNAL \_ DATA** verfügt über die Member **MaximumSize** und **AllocationDelta**.

**MaximumSize** ist die maximale Zielgröße für das Änderungsjournal in Bytes. Das Änderungsjournal kann größer als dieser Wert werden, aber bei NTFS-Dateisystemprüfpunkten untersucht das NTFS-Dateisystem das Journal und kürzet es, wenn seine Größe den Wert von **MaximumSize** plus den Wert von **AllocationDelta** überschreitet. (Bei NTFS-Dateisystemprüfpunkten schreibt das Betriebssystem Datensätze in die NTFS-Dateisystemprotokolldatei, mit denen das NTFS-Dateisystem bestimmen kann, welche Verarbeitung für die Wiederherstellung nach einem Fehler erforderlich ist.)

**AllocationDelta** ist die Anzahl der Bytes, die am Ende hinzugefügt und jedes Mal am Anfang des Änderungsjournals entfernt werden, wenn Arbeitsspeicher zugeordnet oder die Zuordnung aufgehoben wird. Anders ausgedrückt: Die Zuordnung und Freigabe erfolgt in Einheiten dieser Größe. Ein ganzzahliges Vielfaches einer Clustergröße ist ein sinnvoller Wert für diesen Member.

Wenn ein Administrator ein vorhandenes Änderungsjournal ändert, um einen größeren **MaximumSize-Wert** zu erhalten, z. B. wenn ein Volume zu oft neu indiziert wird, empfängt das Änderungsjournal einfach neue Einträge, bis es die neue maximale Größe überschreitet.

Um ein Änderungsjournal zu löschen, verwenden Sie den [**FSCTL \_ DELETE \_ USN JOURNAL-Steuerungscode. \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_usn_journal) Wenn Sie diesen Vorgang verwenden, werden alle Dateien auf dem Volume durchlaufen und die USN für jede Datei auf 0 (null) zurückgesetzt. Der Vorgang löscht dann das vorhandene Änderungsjournal. Dieser Vorgang wird bei Systemneustarts beibehalten, bis er abgeschlossen ist. Jeder Versuch, das Änderungsjournal während dieses Vorgangs zu lesen, zu erstellen oder zu ändern, schlägt mit dem Fehlercode **ERROR JOURNAL DELETE IN PROGRESS \_ \_ \_ \_ fehl.**

Sie können auch den [**FSCTL \_ DELETE \_ USN JOURNAL-Steuerungscode \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_usn_journal) verwenden, um zu bestimmen, ob ein von einem anderen Prozess gestarteter Löschvorgang ausgeführt wird. Beispielsweise kann Ihre Anwendung beim Starten ermitteln, ob ein Löschvorgang ausgeführt wird. Da Journallöschungen über Systemneustarts hinweg beibehalten werden, sollten Dienste und Anwendungen, die beim Systemneustart gestartet werden, nach einem laufenden Löschvorgang suchen.

Änderungsjournale werden nicht unbedingt beim Start erstellt. Um ein Änderungsjournal zu erstellen, kann ein Administrator dies explizit tun oder einen anderen Dienst starten, der ein Änderungsjournal erfordert.

 

 
