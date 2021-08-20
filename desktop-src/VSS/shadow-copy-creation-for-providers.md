---
description: Erstellung von Schattenkopien für Anbieter
ms.assetid: d5042945-ba81-40d0-b204-1f08d153a788
title: Erstellung von Schattenkopien für Anbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 953f9b5556b8cf0a35117d8df6756fdd52bdf033d390f0b08a7e018d1eaf5410
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118121847"
---
# <a name="shadow-copy-creation-for-providers"></a>Erstellung von Schattenkopien für Anbieter

## <a name="the-shadow-copy-creation-process"></a>Erstellungsprozess für Schattenkopien

Eine Anfordernde ist die Anwendung, die die Anforderung zum Erstellen einer Schattenkopie initiiert. In der Regel ist der Anfordernde eine Sicherungsanwendung. Bei Bedarf wird VSS die beteiligten Anbieter aufrufen. Die meisten Anbieter sind an drei spezifischen Anforderungen des Anfordernden interessiert.

1.  Der Anfordernde beginnt die Erstellungsaktivität für Schattenkopien mit einem Aufruf von [**IVssBackupComponents::StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset). Dadurch wird eine **GUID** vom Typ **\_ VSS-ID** generiert, die diesen bestimmten Schattenkopiesatz eindeutig identifiziert: die SnapshotSetId. Der Anbieter ist an diesem Schritt nicht beteiligt, aber die SnapshotSetId wird in allen nachfolgenden Schritten umfassend verwendet.
2.  Für jedes Volume, das in diesen Schattenkopiesatz enthalten sein soll, ruft die Anfordernde [**IVssBackupComponents::AddToSnapshotSet auf.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset) VSS bestimmt, welcher Anbieter zum Kopieren des Volumes als Schatten verwendet wird.
    -   Mehrere Anbieter können an einem Schattenkopiesatz teilnehmen. Wenn beispielsweise das Systemvolumen und ein Datenvolumen Teil desselben Schattenkopiesets sind, kann der Systemanbieter als Schattenkopieanbieter für das Systemvolumen dienen, während ein Hardwareanbieter als Schattenkopieanbieter für das Datenvolumen dienen kann. Beide Anbieter sind Teil desselben Schattenkopiesets, und der Benutzer erwartet dieselbe Zeitpunktkonsistenz auf beiden Volumes.
    -   Damit ein Hardwareanbieter ausgewählt werden kann, muss der Hardwareanbieter alle LUNs unterstützen können, die zum angegebenen Volume beitragen.
    -   Alle registrierten Anbieter erhalten die Möglichkeit, die Unterstützung für ein bestimmtes Volume während der Erstellung von Schattenkopien anzugeben. Wenn mehr als ein Anbieter unterstützung angibt, verwendet VSS standardmäßig Hardwareanbieter, dann Softwareanbieter und schließlich den Systemanbieter (wenn kein anderer Anbieter die Unterstützung für dieses Volume angibt).
    -   Ein Anforderer kann diese Standard reihenfolge außer Kraft setzen, indem er explizit den Anbieter angibt, der zum Erstellen der Schattenkopie erforderlich ist.
    -   Wenn mehrere Hardwareanbieter ein bestimmtes Volume unterstützen, gibt es keine Garantie für die Reihenfolge, in der die Hardwareanbieter aufgerufen werden.
3.  Nach mindestens einem Aufruf von [**AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset)kann der Anfordernde mithilfe der [**IVssBackupComponents::D oSnapshotSet-Methode**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) anfordern, dass die Schattenkopie erstellt wird. VSS arbeitet dann mit dem System zusammen, um die Schattenkopie zu erstellen. Die **DoSnapshotSet-Methode** führt diese Arbeit asynchron aus, und der Anfordernde kann entweder den Erstellungsprozess für Schattenkopien ab- oder warten.

Dieses Diagramm zeigt die Interaktionen zwischen dem Anfordernden, dem VSS-Dienst, der VSS-Kernelunterstützung, allen beteiligten VSS-Writern und allen VSS-Hardwareanbietern. Eine [ausführliche Beschreibung dieser Interaktionen finden Sie](the-shadow-copy-creation-process.md) unter Der Erstellungsprozess für Schattenkopien.

![Interaktionen zwischen Anfordernden, Sicherungskomponenten, Writern und Anbietern](images/vssimpl.png)

Wenn der Erstellungsprozess für Schattenkopien abgeschlossen ist, kann der An anfordernde Benutzer ermitteln, ob die Erstellung der Schattenkopie erfolgreich war, und falls nicht, kann er die Fehlerquelle bestimmen.

Das Zeitintervall zwischen dem Einfrieren und dem Auftauen der Writeranwendungen muss minimiert werden. Der Anbieter muss alle Vorbereitungen im Zusammenhang mit der Schattenkopie (z. B. ein Hardwareanbieter, der Plexes zum Starten der Synchronisierung verwendet) in der [**IVssHardwareSnapshotProvider::BeginPrepareSnapshot-Methode**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotprovider-beginpreparesnapshot) asynchron starten und dann auf die Vervollständigungen in der [**IVssProviderCreateSnapshotSet::EndPrepareSnapshots-Methode**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-endpreparesnapshots) warten.

Es gibt mehrere Zeitlimitfenster, denen Anbieter folgen müssen. Daher führen anbieter mit gutem Verhalten vor [**IVssProviderCreateSnapshotSet::P reCommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-precommitsnapshots) und nach [**IVssProviderCreateSnapshotSet::P ostCommitSnapshots alle unnötigen Verarbeitungen durch.**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-postcommitsnapshots)

Der Schattenkopiesatz wird korrigiert, wenn [**DoSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) aufgerufen wird. Zusätzliche Volumes können später nicht hinzugefügt werden, da die zusätzlichen Volumes nicht denselben Zeitpunkt gemeinsam haben.

Der Schattenkopiesatz ist auf 64 Volumes festgelegt. Ein bestimmtes Volume kann einer gesamten LUN, einem Teil einer LUN oder Teilen mehrerer LUNs zuordnen. Die meisten Konfigurationen verfügen über ein Volume pro LUN, obwohl beliebige Zuordnungen möglich sind.

Es gibt keine Beschränkung für die Anzahl der Schattenkopiesätze oder die Anzahl der Schattenkopiesätze eines ursprünglichen Volumes. Ein Anbieter kann bestimmte Grenzwerte definieren oder basierend auf verfügbaren Hardwareressourcen dynamisch einschränken.

### <a name="point-in-time-for-writerless-applications"></a>Zeitpunkt für writerlose Anwendungen

VSS bietet spezielle Unterstützung, die den Zeitpunkt definiert, der für alle Volumes in einem Schattenkopiesatz üblich ist. Hardwareanbieter müssen nicht direkt mit diesen Kerneltechnologien verbunden werden, da sie im Rahmen der normalen Schattenkopie-Commitverarbeitung aufgerufen werden. Es ist jedoch hilfreich, die verwendeten Mechanismen zu verstehen, da sie die Definition von "Zeitpunkt" für schreiblose Anwendungen (Anwendungen, die keine VSS Writer-Schnittstelle verfügbar gemacht haben und daher nicht am Erstellungsprozess für Volumeschattenkopien teilnehmen) erläutert.

Diese VSS-Kernelunterstützung für allgemeine Zeitpunkte wird zwischen dem VolSnap.sys, den Dateisystemen und VSS verteilt.

1.  Bevor die VSS-Kernelunterstützung aufgerufen wird, hat VSS bereits:
    1.  Ermittelt, welche Volumes an der Schattenkopie beteiligt sein sollen.
    2.  Bestimmt, welcher Anbieter auf jedem Volume verwendet werden soll.
    3.  Eingefrorene Anwendungen, die Frierungs-/Thaw-Nachrichten akzeptieren.
    4.  Die Anbieter für die Schattenkopie wurden durch Aufrufen der [**PreCommitSnapshots-Methoden**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-precommitsnapshots) vorbereitet. Alle Anbieter warten nun auf die erstellung der eigentlichen Schattenkopie.
2.  Der Zeitpunkt wird dann erstellt. VSS leert gleichzeitig die Dateisysteme auf allen Volumes, die schattenkopiert werden sollen.
    1.  VSS gibt einen IOCTL \_ VOLSNAP \_ FLUSH AND HOLD \_ \_ WRITES-Steuerungsbefehl auf jedem Volume aus, \_ das die Dateisysteme leert. Diese IOCTL wird an den Speicherstapel übergeben, um VolSnap.sys. VolSnap.sys enthält dann alle Schreib-IRPs bis schritt 4 unten. Jedes Dateisystem (z. B. RAW) ohne Unterstützung für diese neue IOCTL übergibt die unbekannte IOCTL nach unten, wo sie wieder von der VolSnap.sys. Auf NTFS-Volumes wird beim Leeren auch ein Commit für das NTFS-Protokoll verwendet.
    2.  Dadurch werden alle NTFS-/FAT-Metadatenaktivitäten angehalten. für die Dateisystemmetadaten wird ein cleanly-Committed verwendet.
    3.  Der Schattenkopie-Moment: VolSnap.sys bewirkt, dass alle nachfolgenden Schreib-IRPs auf allen Volumes, die schattenkopiert werden sollen, in die Warteschlange gestellt werden.
    4.  VolSnap.sys wartet, bis alle ausstehenden Schreibvorgänge auf den Schattenkopievolumes abgeschlossen sind. Die Volumes sind nun in Bezug auf Schreibvorgänge ins Ruhen und auf jedem Volume genau zur gleichen Zeit ins Ruhen. Es gibt keine Garantie für Schreibvorgänge in vom Benutzer zugeordnete Abschnitte oder Schreibvorgänge, die zwischen (a) und (b) auf Dateisystemen ausgegeben werden, die die Leerungs-IOCTL (z. B. RAW) nicht implementieren.
3.  VSS weist jeden Anbieter an, die Schattenkopie zu übernehmen, indem die [**IVssProviderCreateSnapshotSet::CommitSnapshots-Methoden aufgerufen**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots) werden. Die Anbieter sollten alle Vorbereitungen durchgeführt haben, damit dies ein schneller Vorgang ist.

    Beachten Sie, dass das E/A-System nur während der Ausführung dieser [**CommitSnapshots-Methoden**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots) ins Ruhen kommt. Wenn ein Anbieter eine Synchronisierung der Quell- und Schattenkopie-LUNs ausführt, muss diese Synchronisierung abgeschlossen werden, bevor die **CommitSnapshots-Methode** des Anbieters zurückgegeben wird. Sie kann nicht asynchron ausgeführt werden.

4.  Unmittelbar nachdem die [**CommitSnapshots-Methode**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots) des letzten Anbieters zurückgegeben wurde, gibt VSS alle ausstehenden Schreib-IRPs frei (einschließlich der IRPs, die die Dateisysteme nach Abschluss ihrer Commitpfade blockiert haben), indem ein anderer an VolSnap.sys übergebener IRP-Aufruf VolSnap.sys.
5.  Wenn der Schattenkopievorgang erfolgreich war, dann ist VSS jetzt:
    1.  Ruft [**PostCommitSnapshots für**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-postcommitsnapshots) die beteiligten Anbieter auf.
    2.  Ruft [**CVssWriter::OnThaw**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onthaw) für die beteiligten Writer auf.
    3.  Informiert den Anfordernden darüber, dass der Schattenkopieprozess abgeschlossen wurde.

[**PreCommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-precommitsnapshots), [**CommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots)und [**PostCommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-postcommitsnapshots) sind alle zeitkritisch. Alle E/A-Aktivitäten von Anwendungen mit Writern werden von **PreCommitSnapshots** zu **PostCommitSnapshots eingefroren.** Verzögerungen wirken sich auf die Anwendungsverfügbarkeit aus. Alle Datei-E/A,einschließlich schreibloser Anwendungs-E/A, werden während **CommitSnapshots angehalten.**

Anbieter sollten alle zeitkritischen Arbeiten vor der Rückgabe von [**EndPrepareSnapshots abschließen.**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-endpreparesnapshots)

-   [**CommitSnapshots sollten**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots) innerhalb von Sekunden zurückgegeben werden. Die **CommitSnapshots-Phase** befindet sich im Fenster Leeren und Halten. Die VSS-Kernelunterstützung bricht das Leeren und Halten ab, das die E/A enthält, wenn die nachfolgende Version nicht innerhalb von 10 Sekunden empfangen wird, und VSS kann den Erstellungsprozess für Schattenkopien nicht ausführen. Andere Aktivitäten werden auf dem System stattfinden, sodass sich ein Anbieter nicht auf die vollen 10 Sekunden verlassen sollte. Der Anbieter sollte win32-APIs während des Commits nicht aufrufen, da viele zu unerwarteten Schreib- und Blockvorgängen führen. Wenn der Anbieter mehr als einige Sekunden zum Abschließen des Aufrufs benötigt, ist die Wahrscheinlichkeit hoch, dass dies fehlschlägt.
-   Die vollständige Sequenz von [**PreCommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-precommitsnapshots) bis zur Rückgabe von [**PostCommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-postcommitsnapshots) wird dem Fenster zwischen Writern, die die Freeze- und Thaw-Ereignisse empfangen, angezeigt. Der Writer-Standardwert für dieses Fenster beträgt 60 Sekunden, aber ein Writer kann diesen Wert mit einem kleineren Timeout überschreiben. Beispielsweise ändert der Microsoft Exchange Server Writer das Timeout in 20 Sekunden. Anbieter sollten in dieser Methode nicht mehr als ein oder zwei Sekunden ausgeben.

Während [**CommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots) muss der Anbieter keine Datei-E/A ohne Auslagerung vermeiden. solche E/A-Daten haben eine sehr hohe Wahrscheinlichkeit für Deadlocks. Insbesondere sollte der Anbieter keine Debug- oder Ablaufverfolgungsprotokolle synchron schreiben.

 

 



