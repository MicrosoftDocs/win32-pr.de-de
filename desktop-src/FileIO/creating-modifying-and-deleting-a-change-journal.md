---
description: Administratoren können Änderungs Journale erstellen, löschen und neu erstellen.
ms.assetid: 26cbacc2-d26b-434b-91b5-31aedc96da13
title: Erstellen, ändern und Löschen eines Änderungs Journals
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50c8cf7296f93549e7d9ec05f5d614131cc342ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355334"
---
# <a name="creating-modifying-and-deleting-a-change-journal"></a>Erstellen, ändern und Löschen eines Änderungs Journals

Administratoren können Änderungs Journale bei der Erstellung erstellen, löschen und neu erstellen. Ein Administrator sollte ein Journal löschen, wenn der aktuelle Wert für die Aktualisierungs Sequenznummer den maximal möglichen Wert für die Aktualisierungs Sequenznummer erreicht, wie vom **maxun** -Member der Datenstruktur des [**\_ Datenblatts " \_ Daten**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_journal_data_v0) " angezeigt. Ein Administrator kann auch ein Änderungs Journal löschen und neu erstellen, um Speicherplatz freizugeben. Um dies und alle anderen nicht programmatischen Änderungs Journal Vorgänge auszuführen, müssen Sie über Systemadministrator Rechte verfügen. Das heißt, Sie müssen Mitglied der Gruppe "Administratoren" sein.

Zum programmgesteuerten Erstellen oder Ändern eines Änderungs Journals auf einem angegebenen Volume verwenden Sie den [**FSCTL \_ Create \_ \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_create_usn_journal) -Steuerelement-Steuerelement Code.

Wenn Sie ein neues Änderungs Journal erstellen oder ein vorhandenes Änderungs Journal ändern, legt das NTFS-Dateisystem Informationen für dieses Änderungs Journal von den Informationen in der Datenstruktur des [**Create- \_ \_ Daten \_ Journal**](/windows/desktop/api/WinIoCtl/ns-winioctl-create_usn_journal_data) fest, die vom [**fisctl Create-Daten \_ \_ \_ Journal**](/windows/win32/api/winioctl/ni-winioctl-fsctl_create_usn_journal) als Eingabe benötigt wird. **Erstellen \_ Sie Die Daten für das \_ \_ Datenblatt des Datenblatts** haben die Mitglieder **MaximumSize** und **Zuweisung**.

**MaximumSize** ist die Ziel maximale Größe für das Änderungs Journal (in Bytes). Das Änderungs Journal kann größer als dieser Wert sein. bei Prüfpunkten des NTFS-Dateisystems prüft das NTFS-Dateisystem jedoch das Journal und schneidet es ab, wenn seine Größe den Wert von **MaximumSize** zuzüglich des Werts von " **Zustellungs Delta**" überschreitet. (Bei NTFS-Dateisystem Prüfpunkten schreibt das Betriebssystem Datensätze in die NTFS-Dateisystem-Protokolldatei, die es dem NTFS-Dateisystem ermöglicht, zu bestimmen, welche Verarbeitung bei einem Fehler wieder hergestellt werden muss.)

" **Zuordnende** Bytes" gibt die Anzahl der am Ende hinzugefügten Bytes an und wird jeweils am Anfang des Änderungs Journals entfernt, wenn der Arbeitsspeicher zugeordnet oder die Zuordnung aufgehoben wird. Anders ausgedrückt: die Zuordnung und die Aufhebung der Zuordnung erfolgt in Einheiten dieser Größe. Ein ganzzahliges Vielfache einer Clustergröße ist ein angemessener Wert für diesen Member.

Wenn ein Administrator ein vorhandenes Änderungs Journal geändert hat, sodass es einen größeren **MaximumSize** -Wert hat, z. b. Wenn ein Volume zu häufig neu indiziert wird, empfängt das Änderungs Journal einfach neue Einträge, bis die neue maximale Größe überschritten wird.

Zum Löschen eines Änderungs Journals verwenden Sie den [**FSCTL \_ Delete \_ \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_usn_journal) -Steuerelement Code für den Löschvorgang. Wenn Sie diesen Vorgang verwenden, werden alle Dateien auf dem Volume durchlaufen und die USN für jede Datei auf 0 (null) zurückgesetzt. Der Vorgang löscht dann das vorhandene Änderungs Journal. Dieser Vorgang wird über Systemneustarts hinweg fortgesetzt, bis er abgeschlossen ist. Bei jedem Versuch, das Änderungs Journal während dieses Prozesses zu lesen, zu erstellen oder zu ändern, tritt ein Fehler auf, dass das Fehler **\_ Journal \_ Delete \_ in \_** Bearbeitung ist.

Sie können auch den Code des [**FSCTL \_ Delete \_ USN \_ Journal**](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_usn_journal) -Steuer Elements verwenden, um zu bestimmen, ob ein Löschvorgang ausgeführt wird, der von einem anderen Prozess gestartet wird. Beispielsweise kann Ihre Anwendung, wenn Sie gestartet wird, ermitteln, ob ein Löschvorgang ausgeführt wird. Da Journal Löschungen über Systemneustarts hinweg beibehalten werden, sollten beim Systemneustart gestartete Dienste und Anwendungen nach einem laufenden Löschvorgang suchen.

Änderungs Journale werden nicht notwendigerweise beim Start erstellt. Zum Erstellen eines Änderungs Journals kann ein Administrator dies explizit durchführen oder einen anderen Dienst starten, für den ein Änderungs Journal erforderlich ist.

 

 
