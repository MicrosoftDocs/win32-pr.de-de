---
description: Dieses Thema enthält eine Einführung in die Auswirkungen erweiterter Formate von Speichergeräten auf Software, erläutert, welche Anwendungen diese Art von Medien unterstützen können und erläutert die Infrastruktur, die Microsoft mit Windows 7 SP1 und Windows Server 2008 R2 SP1 eingeführt hat, damit Entwickler diese Gerätetypen unterstützen können.
ms.assetid: 1D2847A7-15E9-42E0-90EB-7F43E76D3E44
title: Datenträgerkompatibilitätsupdate für 512-Byte-Emulation (512e)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94fbdce2937e2d121d892d8566755dfcb7f20f01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050555"
---
# <a name="512-byte-emulation-512e-disk-compatibility-update"></a>Datenträgerkompatibilitätsupdate für 512-Byte-Emulation (512e)

## <a name="platform"></a>Plattform

 **Clients** -Windows Vista \| Windows 7 \| Windows 7 SP1  
**Server** -Windows Server 2008 \| Windows Server 2008 R2 \| Windows Server 2008 R2 SP1  

## <a name="feature-impact"></a>Auswirkungen von Features

**Schweregrad** -hoch  
**Häufigkeit** -hoch  









## <a name="description"></a>BESCHREIBUNG

Die Raum dichten werden jährlich gesteigert, und bei der letzten Einführung von 3 TB-Datenträgern werden die Fehlerkorrektur Mechanismen, die für die absteigende Signal-zu-Rauschen-Quote (SNR) verwendet wurden, zu nicht ineffizient – das bedeutet, dass ein erhöhter Aufwand erforderlich ist, um sicherzustellen, dass die Medien verwendbar sind. Eine der Speicher-Branchenlösungen zum verbessern dieses Fehlerkorrektur Mechanismus besteht darin, ein anderes physisches Medienformat einzuführen, das eine größere physische Sektorgröße umfasst. Dieses neue Format für physische Medien wird als erweitertes *Format* bezeichnet. Daher ist es nicht mehr sicher, jegliche Annahmen hinsichtlich der Sektorgröße moderner Speichergeräte zu treffen, und Entwickler müssen die Annahmen, die Ihrem Code zugrunde liegen, untersuchen, um zu ermitteln, ob eine Auswirkung vorliegt.

In diesem Thema werden die Auswirkungen von erweiterten Formaten von Speichergeräten auf Software erläutert. Außerdem wird erläutert, welche Aktionen Anwendungen zur Unterstützung dieser Art von Medien ausführen können, und es wird die Infrastruktur erläutert, mit der Entwickler diese Gerätetypen unterstützen können. Obwohl das in diesem Thema gezeigte Material Richtlinien zur Verbesserung der Kompatibilität mit erweiterten Format Datenträgern enthält, gelten die Informationen in der Regel für alle Systeme mit erweiterten Format Datenträgern. Die folgenden Versionen von Windows unterstützen die Abfrage der physischen Sektorgröße:

-   Windows 7 mit Microsoft KB 982018
-   Windows 7 SP1
-   Windows Server 2008 R2 mit Microsoft KB 982018
-   Windows Server 2008 R2 SP1
-   Windows Vista mit Microsoft KB 2553708
-   Windows Server 2008 mit Microsoft KB 2553708

Weitere Informationen finden Sie unter [Informationen zur Microsoft-Support Richtlinie für Laufwerke mit großen Sektoren in Windows](https://support.microsoft.com/kb/2510009).

Weitere Informationen zu Datenträgern mit erweiterter Formatierung erhalten Sie von Ihrem Speicher Anbieter.

## <a name="logical-vs-physical-sector-size"></a>Logische und physische Sektorgröße

Eines der Probleme bei der Einführung dieser Änderung im Medienformat ist die Kompatibilität mit der Software und Hardware, die derzeit auf dem Markt verfügbar ist. Als temporäre Lösung führt die Speicher Branche anfänglich Datenträger ein, die einen regulären 512-Byte-sektordatenträger emulieren, aber über standardmäßige ATA-und SCSI-Befehle Informationen über die tatsächliche Sektorgröße bereitstellen. Infolge dieser Emulation gibt es zwei Sektorgrößen:

-   **Logischer Sektor**: die Einheit, die für die logische Block Adressierung für das Medium verwendet wird. Wir können uns dies auch als kleinste Schreibeinheit vorstellen, die der Speicher annehmen kann. Dies ist die Emulation.

-   **Physischer Sektor**: die Einheit, für die Lese-und Schreibvorgänge auf dem Gerät in einem einzelnen Vorgang abgeschlossen werden. Dies ist die Einheit des atomaren Schreibzugriffs.

Die meisten aktuellen Windows-APIs, wie z. b. **IOCTL \_ Disk \_ get \_ Drive \_ Geometry** , geben die logische Sektorgröße zurück, aber die physische Sektorgröße kann über den [IOCTL \_ Storage \_ Query- \_ Eigenschaften](/windows-hardware/drivers/ddi/content/ntddstor/ni-ntddstor-ioctl_storage_query_property) Steuerungs Code abgerufen werden, wobei die relevanten Informationen im Feld **bytesperphysicalsektorin** der [ \_ \_ \_ deskriptorstruktur der Speicherzugriffs Ausrichtung](/windows/desktop/api/winioctl/ns-winioctl-storage_access_alignment_descriptor) enthalten sind. Dies wird weiter unten in diesem Artikel ausführlicher erläutert.

## <a name="initial-types-of-large-sector-media"></a>Anfängliche Typen von Medien im großen Sektor

Die Speicher Branche beschleunigt rasch den Umstieg auf diesen neuen erweiterten Formattyp von Speicher für Medien mit einer physischen Sektorgröße von 4 KB. Zwei Arten von Medien werden auf dem Markt veröffentlicht:

-   **4-KB**-System eigen: dieses Medium hat keine Emulations Schicht und macht 4 KB direkt als logische und physische Sektorgröße verfügbar. Dieses Medium wird derzeit nicht von Windows und den meisten anderen Betriebssystemen unterstützt. Microsoft führt jedoch eine Untersuchung der Möglichkeit der Unterstützung dieser Art von Medien in einer zukünftigen Version von Windows durch und gibt ggf. einen Knowledge Base-Artikel aus.
-   **512-Byte-Emulation (512 e)**: dieses Medium verfügt über eine Emulations Schicht, wie im vorherigen Abschnitt erläutert wurde, und macht 512 Bytes als logische Sektorgröße verfügbar (ähnlich wie bei einem normalen Datenträger), stellt jedoch die Größe der physischen Sektoren (4 KB) zur Verfügung. Dies ist der Ort, an dem mehrere Speicher Anbieter zurzeit auf dem Markt eingeführt werden. Dieses allgemeine Problem bei diesem neuen Medientyp besteht darin, dass die Mehrzahl der Anwendungen und Betriebssysteme das vorhanden sein der physischen Sektorgröße nicht verstehen, was zu einer Reihe von Problemen führen kann, die im folgenden erläutert werden.

## <a name="how-emulation-works-read-modify-write-rmw"></a>Funktionsweise der Emulation: Read-Modify-Write (RMW)

Ein Speichermedium verfügt über eine bestimmte Einheit, in der das physische Medium geändert werden kann. Das heißt, die Medien können nur in Einheiten der physischen Sektorgröße geschrieben oder umgeschrieben werden. Daher erfordern Schreibvorgänge, die nicht auf dieser Einheits Ebene ausgeführt werden, zusätzliche Schritte, die wir im folgenden Beispiel durchgehen werden.

In diesem Szenario muss eine Anwendung den Inhalt eines dataStor-Datensatzes innerhalb eines logischen 512-Byte-Sektors aktualisieren. Das folgende Diagramm veranschaulicht die Schritte, die erforderlich sind, damit das Speichergerät den Schreibvorgang beendet:

![erforderliche Schritte zum Aktualisieren eines dataStor-Datensatzes innerhalb eines logischen 512-Byte-Sektors](images/512ermwsteps.png)

Wie oben gezeigt, umfasst dieser Prozess etwas Arbeit vom Speichergerät, das zu einem Leistungsverlust führen kann. Um diese zusätzliche Arbeit zu vermeiden, müssen Anwendungen aktualisiert werden, um Folgendes zu tun:

-   Fragen Sie die physische Sektorgröße ab.
-   Stellen Sie sicher, dass Schreibvorgänge an der Größe der gemeldeten physischen Sektoren ausgerichtet sind

## <a name="the-resiliency-impact-of-read-modify-write"></a>Die resilienzauswirkung von Read-Modify-Write

Resilienz spricht von der Fähigkeit einer Anwendung, den Zustand zwischen Sitzungen wiederherzustellen. Wir haben gesehen, was für ein 512E-Speichergerät notwendig ist, um einen 512-Byte-sektorschreib Vorgang durchzuführen – den Lese-und Schreibvorgang. Sehen wir uns an, was passiert, wenn der Prozess der Überschreibung des vorherigen physischen Sektors auf den Medien unterbrochen wurde. Wie lauten die Konsequenzen?

-   Da die meisten Festplattenlaufwerke direkt aktualisiert werden, ist der physische Sektor – d. h. der Teil des Mediums, auf dem sich der physische Sektor befand – möglicherweise aufgrund einer partiellen Überschreibung mit unvollständigen Informationen beschädigt worden. Anders ausgedrückt, Sie können sich davon vorstellen, dass alle acht logischen Sektoren verloren gegangen sind (was der physische Sektor logisch enthält).

-   Obwohl die meisten Anwendungen mit einem Datenspeicher mit der Funktion zur Wiederherstellung nach Medien Fehlern, dem Verlust von acht Sektoren oder einem anderen Weg, dem Verlust von acht Commit-Datensätzen, entworfen wurden, kann es möglicherweise unmöglich machen, dass der Datenspeicher ordnungsgemäß wieder hergestellt wird. Ein Administrator muss die Datenbank möglicherweise manuell aus einer Sicherung wiederherstellen oder sogar eine langwierige Neuerstellung durchführen.

-   Eine weitere wichtige Auswirkung besteht darin, dass das Vorgehen einer anderen Anwendung, die einen Lese-/Änderungs-Vorgang verursacht, möglicherweise dazu führen kann, dass Ihre Daten verloren gehen – auch wenn Ihre Anwendung nicht ausgeführt wird. Dies liegt einfach daran, dass sich die Daten und die Daten der anderen Anwendung innerhalb desselben physischen Sektors befinden können.

Vor diesem Hintergrund ist es wichtig, dass die Anwendungssoftware alle Annahmen, die im Code vorgenommen wurden, neu bewertet und die Unterscheidung zwischen logischer und physischer Sektorgröße sowie einige interessante Kunden Szenarios beachten, die weiter unten in diesem Artikel erläutert werden.

Dieses Problem tritt eher auf, wenn Ihre Anwendung auf einem Datenspeicher für die Protokoll Struktur basiert.

## <a name="avoiding-read-modify-write"></a>Vermeiden von Lese-/änderungschreibzugriff

Während einige Speicher Anbieter einige Stufen der Entschärfung innerhalb bestimmter 512-e-Speichergeräte einführen, um die Leistungs-und resilienzprobleme des Lese-/Änderungs-Schreibzyklen zu vereinfachen, können Sie in Bezug auf die Arbeitsauslastung nur so viele Schutzmaßnahmen bewältigen. Daher sollten sich Anwendungen nicht auf diese Entschärfung als langfristige Lösung verlassen.

Dabei handelt es sich nicht um eine Risikominderung, aber damit Anwendungen die richtigen Schritte ausführen können, um den Lese-und Schreibvorgang zu vermeiden. In diesem Abschnitt werden häufige Szenarien erläutert, in denen bei Anwendungen möglicherweise Probleme mit großen sektordatenträgern auftreten, und es wird eine Möglichkeit zum Beheben der einzelnen Probleme vorgeschlagen.

### <a name="issue-1-the-partition-is-not-aligned-to-a-physical-sector-boundary"></a>Problem 1: die Partition ist nicht an einer physischen Sektorgrenze ausgerichtet.

Wenn der Administrator/Benutzer den Datenträger partitioniert, wurde die erste Partition möglicherweise nicht an einer ausgerichteten Grenze erstellt. Dies kann dazu führen, dass alle nachfolgenden Schreibvorgänge an den physischen Sektorgrenzen nicht ausgerichtet werden. Ab Windows Vista SP1 und Windows Server 2008 wird die erste Partition auf den ersten 1024 KB des Datenträgers platziert (für Datenträger mit einer Größe von 4 GB oder größer, andernfalls ist die Ausrichtung auf 64 KB), die an einer physischen Sektorgrenze von 4 KB ausgerichtet ist. Wenn jedoch die Standard Partitionierung in Windows XP, ein Drittanbieter-Partitionierungsprogramm oder eine falsche Verwendung von Windows-APIs vorhanden ist, sind erstellte Partitionen möglicherweise nicht an einer physischen Sektorgrenze ausgerichtet. Entwickler müssen sicherstellen, dass die richtigen APIs verwendet werden, um die Ausrichtung sicherzustellen. Die empfohlenen APIs, um sicherzustellen, dass die Partitions Ausrichtung nachfolgend beschrieben wird.

Die **ivdspack:: anatevolume** -und **IVdsPack2:: CreateVolume2** -APIs verwenden den angegebenen Ausrichtungs Parameter nicht, wenn ein neues Volume erstellt wird, sondern verwenden stattdessen den Standardwert für die Ausrichtung des Betriebssystems (Pre-Windows Vista SP1 verwendet 63 Bytes, und nach Windows Vista SP1 werden die oben genannten Standardeinstellungen verwendet). Daher wird empfohlen, dass Anwendungen, die Partitionen erstellen müssen, stattdessen die **ivdscreatepartitionex::** up-oder **ivdsadvanceddisk::** up-API-APIs verwenden, die den angegebenen Alignment-Parameter verwenden.

Die beste Möglichkeit, um sicherzustellen, dass die Ausrichtung korrekt ist, ist das Recht, wenn Sie die Partition erstmalig erstellen. Andernfalls muss Ihre Anwendung bei der Ausführung von Schreibvorgängen oder bei der Initialisierung die Ausrichtung berücksichtigen – dies kann sehr komplex sein. Ab Windows Vista SP1 stellt dies im Allgemeinen kein Problem dar. Ältere Versionen von Windows können jedoch nicht ausgerichtete Partitionen erstellen, die potenziell zu Leistungsproblemen mit einigen erweiterten Format Datenträgern führen können.

### <a name="issue-2-unbuffered-writes-not-aligned-to-physical-sector-size"></a>Problem 2: nicht gepufferte Schreibvorgänge, die nicht an der physischen Sektorgröße ausgerichtet sind

Das grundlegende Problem besteht darin, dass nicht gepufferte Schreibvorgänge nicht an der gemeldeten physischen Sektorgröße des Speichermediums ausgerichtet sind, wodurch ein Lese-/Schreibzugriff auf das Laufwerk ausgelöst wird, das zu Leistungsproblemen führen kann. Gepufferte Schreibvorgänge werden hingegen an die Seitengröße – 4 KB ausgerichtet – was zufälligerweise die physische Sektorgröße der ersten Generation von Medien mit großen Sektoren ist. Bei den meisten Anwendungen mit einem Datenspeicher werden jedoch nicht gepufferte Schreibvorgänge ausgeführt. Daher muss sichergestellt werden, dass diese Schreibvorgänge in Einheiten der physischen Sektorgröße durchgeführt werden.

Wenn Sie ermitteln möchten, ob Ihre Anwendung nicht gepufferte e/a-Vorgänge ausgibt, prüfen Sie, ob Sie das **\_ Dateiflag \_ No \_ buffersflag** in den *dwflagsandattributs-Parameter* einschließen, wenn Sie die **CreateFile** -Funktion aufrufen.

Wenn Sie derzeit die Schreibvorgänge an der Sektorgröße ausrichten, ist diese Sektorgröße wahrscheinlich nur die *logische* Sektorgröße, da die meisten vorhandenen APIs, die die Sektorgröße der Medien Abfragen, tatsächlich nur die Einheit der Adressierung Abfragen, d. –. die Größe des logischen Sektors. Die Sektorgröße, die hier von Interesse ist, ist die physische Sektorgröße, bei der es sich um die reale Einheit der Atomizität handelt. Einige Beispiele für APIs, die die logische Sektorgröße abrufen, sind:

-   **GetDiskFreeSpace**, **GetDiskFreeSpaceEx**
-   **"Flefsvolumeinformation"**
-   **IOCTL \_ Datenträger \_ get- \_ Laufwerk \_ Geometrie**, **IOCTL \_ Disk \_ get \_ Drive \_ Geometry \_ Ex**
-   **Ivdsdisk:: GetProperties**, **IVdsDisk3:: GetProperties2**

**Abfragen der physischen Sektorgröße**

Microsoft hat in MSDN ein Codebeispiel bereitgestellt, in dem erläutert wird, wie eine Anwendung die physische Sektorgröße des Volumes Abfragen kann. Das Codebeispiel befindet sich unter <https://msdn.microsoft.com/library/ff800831.aspx> .

Im obigen Codebeispiel können Sie die physische Sektorgröße des Volumes abrufen. Sie sollten jedoch einige grundlegende integritätprüfungen für die gemeldete physische Sektorgröße ausführen, bevor Sie Sie verwenden, da festgestellt wurde, dass einige Treiber möglicherweise nicht ordnungsgemäß formatierte Daten zurückgeben:

-   Stellen Sie sicher, dass die gemeldete physische Sektorgröße >= der gemeldeten logischen Sektorgröße ist. Wenn dies nicht der Fall ist, sollte die Anwendung eine physische Sektorgröße verwenden, die der gemeldeten logischen Sektorgröße entspricht.
-   Stellen Sie sicher, dass die gemeldete physische Sektorgröße eine Potenz von zwei ist. Wenn dies nicht der Fall ist, sollte die Anwendung eine physische Sektorgröße verwenden, die der gemeldeten logischen Sektorgröße entspricht.
-   Wenn die physische Sektorgröße einen zweidimensionalen Wert zwischen 512-Byte und 4 KB beträgt, sollten Sie die Verwendung einer physischen Sektorgröße in Erwägung gezogen, die auf die gemeldete logische Sektorgröße gerundet wird.
-   Wenn es sich bei der physischen Sektorgröße um einen zweidimensionalen Wert von mehr als 4 KB handelt, sollten Sie die Fähigkeit Ihrer Anwendung auswerten, dieses Szenario zu verarbeiten, bevor Sie diesen Wert verwenden. Andernfalls sollten Sie die Verwendung einer physischen Sektorgröße in Erwägung gezogen, die auf 4 KB gerundet ist.

Die Verwendung dieser ioctl zum erzielen der physischen Sektorgröße hat mehrere Einschränkungen:

-   Erfordert erweiterte Berechtigungen. Wenn Ihre Anwendung nicht mit-Berechtigungen ausgeführt wird, müssen Sie möglicherweise wie oben beschrieben eine Windows-Dienst Anwendung schreiben.

-   SMB-Volumes werden von nicht unterstützt. Sie müssen möglicherweise auch eine Windows-Dienst Anwendung schreiben, um die Abfrage physischer Sektorgröße auf diesen Volumes zu unterstützen.

-   Kann nicht an ein Datei Handle ausgegeben werden (die IOCTL muss für ein volumehandle ausgestellt werden).

-   Wird nur in Windows-Versionen unterstützt, die am Anfang dieses Artikels aufgeführt sind.

**Commit-Datensätze werden in 512-Byte-Sektoren aufgefüllt**

Anwendungen mit einem Datenspeicher verfügen in der Regel über eine Art Commit-Datensatz, der entweder Informationen über Metadatenänderungen oder die Struktur des Datenspeicher beibehält. Um sicherzustellen, dass sich der Verlust eines Sektors nicht auf mehrere Datensätze auswirkt, wird dieser Commit-Datensatz in der Regel in einer Sektorgröße aufgefüllt. Bei einem Datenträger mit einer größeren physischen Sektorgröße muss die Anwendung die physische Sektorgröße Abfragen, wie im vorherigen Abschnitt gezeigt, und sicherstellen, dass jeder Commit-Datensatz in dieser Größe aufgefüllt wird. Dadurch wird nicht nur der Lese-und Schreibvorgang vermieden, sondern es wird sichergestellt, dass für den Fall, dass ein physischer Sektor verloren gegangen ist, nur ein Commit-Datensatz verloren geht.

**Protokolldateien werden in nicht ausgerichtete Blöcke in geschrieben.**

Nicht gepufferte e/a-Vorgänge werden in der Regel beim Aktualisieren oder Anhängen an eine Protokolldatei verwendet. Es gibt mehrere Möglichkeiten, um sicherzustellen, dass diese Updates ordnungsgemäß ausgerichtet sind:

-   Puffern Sie intern Protokoll Aktualisierungen der gemeldeten physischen Sektorgröße des betriebsmediums ab, und geben Sie Protokoll Schreibvorgänge nur dann aus, wenn eine physische sektoreinheit voll ist.
-   Gepufferte e/a verwenden

### <a name="issue-3-file-formats-relying-on-512-byte-sectors"></a>Problem 3: Dateiformate, die sich auf 512-Byte-Sektoren verlassen

Bei einigen Anwendungen mit Standarddatei Formaten (z. b. VHD 1,0) können diese Dateien hart codiert werden, um die Sektorgröße von 512 Bytes anzunehmen. Daher führen Updates und Schreibvorgänge für diese Datei zu einem Lese-/Schreib-Schreibvorgang auf dem Gerät – was potenziell zu Leistungs-und Resilienz für Ihre Kunden führen kann. Es gibt jedoch Möglichkeiten, wie eine Anwendung Unterstützung für diese Art von Medien bietet, z. b.:

-   Verwenden Sie Pufferung, um sicherzustellen, dass Schreibvorgänge in Einheiten der physischen Sektorgröße durchgeführt werden.
-   Implementieren Sie einen internen Lese-und Schreibzugriff, mit dem sichergestellt werden kann, dass Updates in Einheiten der gemeldeten physischen Sektorgröße durchgeführt werden.
-   Füllen Sie nach Möglichkeit Datensätze in einem physischen Sektor auf, so dass die Auffüllung als leerer Raum interpretiert werden würde.
-   Sie sollten eine neue Version der Anwendungsdaten Struktur mit Unterstützung für größere Sektoren umgestalten.

### <a name="issue-4-the-reported-physical-sector-size-can-change-between-sessions"></a>Problem 4: die gemeldete physische Sektorgröße kann sich zwischen den Sitzungen ändern.

Es gibt viele Szenarien, in denen die gemeldete physische Sektorgröße des zugrunde liegenden Speichers, der den dataStor hostet, geändert werden kann. Der häufigste Fall ist, wenn Sie den dataStor zu einem anderen Volume oder sogar über das Netzwerk migrieren. Eine Änderung in der gemeldeten physischen Sektorgröße ist möglicherweise ein unerwartetes Ereignis für viele Anwendungen und kann möglicherweise dazu führen, dass einige Anwendungen sogar nicht erneut initialisiert werden.

Dies ist nicht das einfachste Szenario für die Unterstützung von und wird hier als Empfehlung erwähnt. Berücksichtigen Sie die Mobilitätsanforderungen ihrer Kunden, und passen Sie Ihren Support entsprechend an, um sicherzustellen, dass Kunden durch die Verwendung von 512 e-Medien nicht beeinträchtigt werden.

## <a name="4-kb-native-media"></a>Native Medien mit 4 KB

512-Byte-Emulations Medien sind ein Übergangsschritt zwischen einem systemeigenen 512-Byte-und 4-KB-Medium, und es wird erwartet, dass systemeigene Medien mit 4 KB verfügbar sind, kurz nachdem 512 e verfügbar ist. Es gibt einige wichtige Implikationen für dieses Medium, die beachtet werden sollten:

-   Die Größe der logischen und physischen Sektoren beträgt 4 KB.
-   Da keine Emulations Ebene vorhanden ist, wird der Speicher bei nicht ausgerichteten Schreibvorgängen nicht ausgeführt.
-   Keine ausgeblendeten resilienztreffer – Anwendungen funktionieren entweder oder funktionieren nicht.

Obwohl Microsoft derzeit die Unterstützung für diese Medientypen in einer zukünftigen Version von Windows untersucht und bei Bedarf einen KB-Artikel ausgibt, sollten Anwendungsentwickler in Erwägung gezogen werden, dass diese Medientypen vorab unterstützt werden.

## <a name="closing"></a>Schließen

In diesem Artikel haben wir erläutert, welche Auswirkungen das große sektormedium mit vielen gängigen Bereitstellungs Szenarien bietet. Wir haben die Auswirkungen auf die Leistung und Resilienz von Lese-/Änderungs-Schreibzugriff, einige der interessanten Szenarien, die diese Medien einbringen können, und die Probleme, die Sie möglicherweise mit Software verursachen können, die letztendlich den Endbenutzer betreffen, gesehen. Die Speicher Branche wird schnell auf Medien mit größeren Sektorgrößen umgestellt, und in Kürze können Kunden keine Datenträger mit herkömmlichen Größen für 512-Byte-Sektoren erwerben.

Dieses Dokument ist ein lebendiges Dokument und soll Entwicklern helfen, diesen Übergang zu verstehen. Sie sollten eine Konversation mit ihren jeweiligen Organisationen, Kunden, IT-Experten und ihren Hardwareanbietern durchführen, um über den Übergang des großen Sektors und die Auswirkungen auf die für Sie wichtigen Szenarien zu sprechen.

## <a name="links-to-other-resources"></a>Links zu anderen Ressourcen

-   **Allgemeine Windows-Support-Anweisung**: <https://support.microsoft.com/kb/2510009>
-   **Hotfix für Windows 7 und Windows Server 2008 R2**: <https://support.microsoft.com/kb/982018>
-   **Hotfix für Windows Vista und Windows Server 2008**: <https://support.microsoft.com/kb/2470478>
-   **HyperV-Unterstützungs Anweisung**: <https://support.microsoft.com/kb/2515143>
-   **Allgemeine Informationen zu IOCTL \_ \_ \_ Steuerungs Code der Speicher Abfrage Eigenschaft**: [https://msdn.microsoft.com/library/ff560590.aspx](/windows-hardware/drivers/ddi/ntddstor/ni-ntddstor-ioctl_storage_query_property)
-   **IOCTL \_ \_ \_ Steuerungs Code der Speicher Abfrage Eigenschaft**: [https://msdn.microsoft.com/library/ff800830.aspx](/windows/win32/api/winioctl/ni-winioctl-ioctl_storage_query_property)
-   **Allgemeine Informationen zum Speicher \_ Struktur der Zugriffs \_ Ausrichtungs \_ Deskriptoren**: [https://msdn.microsoft.com/library/ff566344.aspx](/windows-hardware/drivers/ddi/ntddstor/ns-ntddstor-_storage_access_alignment_descriptor)
-   **Beschreibung der Standard Terminologie, die zum Beschreiben von Microsoft-Software Updates verwendet wird**: <https://support.microsoft.com/kb/824684/>
-   **WDK-Beispielcode** mit Details zum Extrahieren der gemeldeten Informationen zur Speicherzugriffs Ausrichtung aus der **Speicher \_ Zugriffs- \_ Ausrichtungs \_ deskriptorstruktur** beim Aufrufen des Steuercodes der **IOCTL \_ Storage \_ Query- \_ Eigenschaft** : [/Windows/Desktop/API/winioctl/NS-winioctl-storage_access_alignment_descriptor](/windows/desktop/api/winioctl/ns-winioctl-storage_access_alignment_descriptor)
-   **Allgemeine Informationen zu ImageX-Command-Line Optionen**: <https://technet.microsoft.com/library/dd799302(WS.10).aspx>
-   **Intel Chip Set Driver-Anforderungen zur Unterstützung von 4-KB-sektorlaufwerken**: <https://www.intel.com/support/chipsets/imsm/sb/CS-031502.htm>
-   Weitere Informationen zu erweiterten Format Datenträgern finden Sie auf den folgenden idema-Websites:
    -   <http://idema.org/?page_id=2172>
    -   <http://idema.org/?download=7926>

 

 
