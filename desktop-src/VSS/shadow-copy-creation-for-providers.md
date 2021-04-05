---
description: Erstellen von Schatten Kopien für Anbieter
ms.assetid: d5042945-ba81-40d0-b204-1f08d153a788
title: Erstellen von Schatten Kopien für Anbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91cc7306e7a13ef8e96ab032016a922411a70f95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042088"
---
# <a name="shadow-copy-creation-for-providers"></a>Erstellen von Schatten Kopien für Anbieter

## <a name="the-shadow-copy-creation-process"></a>Der Erstellungs Vorgang für Schatten Kopien

Ein Anforderer ist die Anwendung, die die Anforderung initiiert, eine Schatten Kopie zu erstellen. In der Regel ist der Anforderer eine Sicherungs Anwendung. Bei Bedarf werden von VSS die beteiligten Anbieter aufgerufen. Die meisten Anbieter sind an drei speziellen Anforderungen von der anfordernden Person interessiert.

1.  Der Anforderer beginnt mit der Erstellung der Schattenkopieerstellung mit einem Befehl für [**IVssBackupComponents:: startnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset). Dadurch wird eine **GUID** des Typs "VSS-ID" generiert, die diesen speziellen **Schattenkopiesatz \_** eindeutig identifiziert: "snapshotsetid". Der Anbieter ist in diesem Schritt nicht beteiligt, aber die snapshotsetid wird in allen nachfolgenden Schritten ausgiebig verwendet.
2.  Für jedes Volume, das in diesen Schattenkopiesatz aufgenommen werden soll, ruft der Anforderer [**IVssBackupComponents:: addtosnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset)auf. VSS bestimmt, welcher Anbieter zum Schatten kopieren des Volumes verwendet wird.
    -   Mehrere Anbieter können an einem Schattenkopiesatz teilnehmen. Wenn z. b. das System Volume und ein Daten Volume Teil desselben schattenkopiesatzes sind, kann der Systemanbieter als Schattenkopieanbieter für das System Volume fungieren, während ein Hardware Anbieter als Schattenkopieanbieter für das Daten Volume fungieren kann. Beide Anbieter sind Teil desselben schattenkopiespeichersets, und der Benutzer erwartet für beide Volumes dieselbe Zeit Punkt Konsistenz.
    -   Damit ein Hardware Anbieter ausgewählt werden kann, muss der Hardware Anbieter in der Lage sein, alle LUNs zu unterstützen, die zum angegebenen Volume beitragen.
    -   Alle registrierten Anbieter haben die Möglichkeit, die Unterstützung für ein bestimmtes Volume während der Erstellung von Schatten Kopien anzugeben. Wenn mehr als ein Anbieter Unterstützung angibt, wird VSS zuerst standardmäßig Hardware Anbieter, dann Softwareanbieter und schließlich den Systemanbieter (wenn kein anderer Anbieter Unterstützung für dieses Volume anzeigt).
    -   Ein Anforderer kann diese Standard Reihenfolge überschreiben, indem er explizit den Anbieter angibt, der zum Erstellen der Schatten Kopie erforderlich ist.
    -   Wenn es mehrere Hardware Anbieter gibt, die ein bestimmtes Volume unterstützen, gibt es keine Garantie für die Reihenfolge, in der die Hardware Anbieter aufgerufen werden.
3.  Nach einem oder mehreren Aufrufen von [**addtosnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset)kann der Anforderer mithilfe der [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) -Methode zum Erstellen der Schatten Kopie aufgefordert werden. VSS arbeitet dann mit dem System zusammen, um die Schatten Kopie zu erstellen. Die **DoSnapshotSet** -Methode führt diese Aufgabe asynchron aus, und der Anforderer kann entweder Abfragen oder darauf warten, dass der Vorgang zum Erstellen von Schatten Kopien beendet wird.

Dieses Diagramm zeigt die Interaktionen zwischen dem Anforderer, dem VSS-Dienst, der VSS-Kernel Unterstützung, den beteiligten VSS-Writern und VSS-Hardwareanbietern. Eine ausführliche Beschreibung dieser Interaktionen finden Sie [unter Erstellen von Schatten Kopien](the-shadow-copy-creation-process.md) .

![Interaktionen zwischen Anforderer, Sicherungs Komponenten, Writern und Anbietern](images/vssimpl.png)

Wenn der Vorgang zum Erstellen von Schatten Kopien abgeschlossen ist, kann der Anforderer ermitteln, ob die Erstellung der Schatten Kopie erfolgreich war, und andernfalls die Fehlerquelle ermitteln.

Das Zeitintervall zwischen dem Einfrieren und dem Bereinigen der Writer-Anwendungen muss minimiert werden. Der Anbieter muss in der [**ivsshardwaresnapshotprovider:: beginpreparesnapshot**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotprovider-beginpreparesnapshot) -Methode asynchron alle Vorbereitungsarbeiten im Zusammenhang mit der Schatten Kopie (z. b. einen Hardware Anbieter, der die Synchronisierung startet) starten und dann auf die Vervollständigung in der [**ivssproviderkreatesnapshotset**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-endpreparesnapshots)

Es gibt mehrere Zeit Steuerungs Grenzen, die von Anbietern befolgt werden müssen. Daher führen wohl verhaltene Anbieter die gesamte unnötige Verarbeitung vor [**ivssproviderkreatesnapshotset aus::P recommitsnapshot**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-precommitsnapshots) und nach [**ivssproviderkreatesnapshotset::P ostcommitsnapshot**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-postcommitsnapshots).

Der Schattenkopiesatz wird korrigiert, wenn [**DoSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) aufgerufen wird. Zusätzliche Volumes können später nicht mehr hinzugefügt werden, da die zusätzlichen Volumes nicht denselben Zeitpunkt aufweisen würden.

Im Schattenkopiesatz ist ein Grenzwert von 64 Volumes vorhanden. Ein bestimmtes Volume kann einer ganzen LUN, einem Teil einer LUN oder Teilen mehrerer LUNs zugeordnet werden. Die meisten Konfigurationen verfügen über ein Volume pro LUN, obwohl beliebige Zuordnungen möglich sind.

Es gibt keine Beschränkung der Anzahl von schattenkopiesätzen oder der Anzahl von schattenkopiesätzen eines ursprünglichen Volumes. Ein Anbieter kann bestimmte Grenzwerte definieren oder basierend auf den verfügbaren Hardware Ressourcen eine dynamische Beschränkung festlegen.

### <a name="point-in-time-for-writerless-applications"></a>Zeitpunkt für Schreib lose Anwendungen

VSS umfasst besondere Unterstützung, die den Zeit Punkt definiert, der für alle Volumes in einem Schattenkopiesatz verwendet wird. Hardware Anbieter müssen sich nicht direkt mit diesen Kernel Technologien verbinden, da Sie im Rahmen der normalen Verarbeitung von schattenkopiercommit aufgerufen werden. Es ist jedoch sinnvoll, die verwendeten Mechanismen zu verstehen, da die Definition von "Point-in-Time" für Schreib lose Anwendungen (Anwendungen, die keine VSS Writer-Schnittstelle verfügbar gemacht haben und daher nicht am Erstellungs Prozess der Volumeschattenkopie beteiligt sind) erläutert wird.

Diese VSS-Kernel Unterstützung für allgemeine Zeitpunkte wird zwischen dem VolSnap.sys-Treiber, den Dateisystemen und VSS verteilt.

1.  Bevor die VSS-Kernel Unterstützung aufgerufen wird, hat VSS bereits Folgendes:
    1.  Bestimmt, welche Volumes an der Schatten Kopie beteiligt sein sollen.
    2.  Bestimmt, welcher Anbieter auf jedem Volume verwendet werden soll.
    3.  Fixierte Anwendungen, die Freeze/Thaw-Nachrichten akzeptieren.
    4.  Die Anbieter für die Schatten Kopie wurden durch Aufrufen der [**precommitshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-precommitsnapshots) -Methoden vorbereitet. Alle Anbieter warten nun, dass die tatsächliche Erstellung von Schatten Kopien durchzuführen ist.
2.  Der Zeitpunkt wird dann erstellt. VSS leert die Dateisysteme gleichzeitig auf allen Volumes, die als Schatten kopiert werden sollen.
    1.  VSS gibt \_ \_ \_ \_ \_ für jedes Volume, das die Dateisysteme leert, einen Befehl zum Steuern von IOCTL Volsnap-und Hold-Schreibvorgängen aus. Diese IOCTL wird an VolSnap.sys an den Speicher Stapel übermittelt. VolSnap.sys enthält dann alle Schreibvorgänge bis 4. Jedes Dateisystem (z. b. RAW) ohne Unterstützung dieser neuen ioctl übergibt die unbekannte IOCTL-–, wo Sie wieder von VolSnap.sys gehalten wird. Auf NTFS-Volumes führt das Flush auch ein Commit für das NTFS-Protokoll aus.
    2.  Dadurch werden alle NTFS/FAT-metadatenaktivitäten angehalten. für die Dateisystem Metadaten ist ein ordnungsgemäßes Commit ausgeführt worden.
    3.  Der Schatten Kopie-Instant: VolSnap.sys bewirkt, dass alle nachfolgenden Schreibvorgänge auf allen Volumes, die als Schatten kopiert werden sollen, in die Warteschlange eingereiht werden.
    4.  VolSnap.sys wartet auf den Abschluss aller ausstehenden Schreibvorgänge auf den schattenkopierten Volumes. Die Volumes sind nun in Bezug auf Schreibvorgänge inaktiv und wurden auf jedem Volume in genau demselben Moment inaktiv. Es gibt keine Garantie für Schreibzugriffe auf vom Benutzer zugeordnete Abschnitte oder Schreibvorgänge, die zwischen (a) und (b) auf Dateisystemen ausgegeben werden, die die leeren ioctl nicht implementieren (z. b. RAW).
3.  VSS weist jeden Anbieter an, die Schatten Kopie durch Aufrufen der [**ivssprovidercreatesnapshotset:: commitsnapshot**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots) -Methoden zu übernehmen. Die Anbieter sollten die gesamte Vorbereitung durchgeführt haben, damit dies ein schneller Vorgang ist.

    Beachten Sie, dass das e/a-System nur ineskalierend ist, während diese [**commitshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots) -Methoden ausgeführt werden. Wenn ein Anbieter eine Synchronisierung der Quell-und schattenkopieluns ausführt, muss diese Synchronisierung abgeschlossen werden, bevor die **commitshots** -Methode des Anbieters zurückgibt. Sie kann nicht asynchron ausgeführt werden.

4.  Unmittelbar nach dem Zurückgeben der [**commitshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots) -Methode des letzten Anbieters gibt VSS alle ausstehenden Schreibvorgänge (einschließlich der unps, die die Dateisysteme am Ende ihrer commitpfade blockieren) durch Aufrufen eines anderen, an VolSnap.sys übergeben.
5.  Wenn der Schattenkopievorgang erfolgreich war, wird jetzt VSS angezeigt:
    1.  Ruft [**postcommitmomentaufnahmen**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-postcommitsnapshots) für die beteiligten Anbieter auf.
    2.  Ruft [**CVssWriter:: OnThaw**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onthaw) für die beteiligten Writer auf.
    3.  Benachrichtigt den Anforderer, dass der schattenkopieprozess abgeschlossen wurde.

[**Precommitmomentaufnahmen**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-precommitsnapshots), [**commitmomentaufnahmen**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots)und [**postcommitmomentaufnahmen**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-postcommitsnapshots) sind Zeit kritisch. Alle e/a-Vorgänge von Anwendungen mit Writern werden von **präcommitmomentaufnahmen** zu **postcommitmomentaufnahmen** eingefroren. Verzögerungen wirken sich auf die Anwendungs Verfügbarkeit aus. Alle Datei-e/a-Vorgänge, einschließlich Schreib loser Anwendungs-e/a, werden während **commitmomentaufnahmen** angehalten.

Anbieter sollten vor der Rückgabe von [**EndPrepareSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-endpreparesnapshots)alle zeitkritischen Arbeiten ausführen.

-   [**Commitmomentaufnahmen**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots) sollten innerhalb von Sekunden zurückgegeben werden. Die **commitshots** -Phase befindet sich im Fenster "leeren" und "Speichern". Durch die VSS-Kernel Unterstützung wird die Leerung und die Aufbewahrung abgebrochen, die die e/a-Vorgänge enthält, wenn die nachfolgende Version nicht innerhalb von 10 Sekunden empfangen wird und VSS den Vorgang zum Erstellen von Schatten Kopien nicht besteht. Andere Aktivitäten werden auf dem System ausgeführt, sodass ein Anbieter nicht die vollen 10 Sekunden benötigen sollte. Der Anbieter sollte während des Commit keine Win32-APIs aufzurufen, da viele zu unerwarteten Schreib-und Blockierungs Vorgängen führen. Wenn der Anbieter mehr als einige Sekunden Zeit benötigt, um den-Vorgang abzuschließen, besteht eine hohe Wahrscheinlichkeit, dass dies fehlschlägt.
-   Die vollständige Sequenz von [**precommitmomentaufnahmen**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-precommitsnapshots) zur Rückgabe von [**postcommitmomentaufnahmen**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-postcommitsnapshots) wird dem Fenster zwischen den Writern zugeordnet, die die Ereignisse zum Einfrieren und zum Durchsetzen des Ereignisses empfangen. Der Writer-Standard für dieses Fenster ist 60 Sekunden, aber ein Writer kann diesen Wert mit einem kleineren Timeout überschreiben. Der Microsoft Exchange Server-Writer ändert z. b. den Timeout Wert auf 20 Sekunden. Anbieter sollten in dieser Methode nicht mehr als eine Sekunde oder zwei Sekunden aufwenden.

Während der [**commitmomentaufnahmen**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots) muss der Anbieter alle nicht Auslagerungs Datei-e/a-Vorgänge vermeiden. Diese e/a-Vorgänge haben eine sehr hohe Wahrscheinlichkeit für Deadlocks. Insbesondere sollte der Anbieter keine Debug-oder Ablauf Verfolgungs Protokolle synchron schreiben.

 

 



