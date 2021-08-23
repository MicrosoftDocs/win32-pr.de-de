---
description: In diesem Thema werden die Auswirkungen von Speichergeräten im erweiterten Format auf Software vorgestellt, und es wird erläutert, welche Anwendungen diese Art von Medien unterstützen können. Außerdem wird die Infrastruktur erläutert, die Microsoft mit Windows 7 SP1 und Windows Server 2008 R2 SP1 eingeführt hat, um Entwicklern die Unterstützung dieser Gerätetypen zu ermöglichen.
ms.assetid: 1D2847A7-15E9-42E0-90EB-7F43E76D3E44
title: Datenträgerkompatibilitätsupdate für 512-Byte-Emulation (512e)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fd26cfe1b5417af75906431291a51650757c08464f0c1dc6966ef7f58223423
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134177"
---
# <a name="512-byte-emulation-512e-disk-compatibility-update"></a>Datenträgerkompatibilitätsupdate für 512-Byte-Emulation (512e)

## <a name="platform"></a>Plattform

 **Clients** – Windows Vista, Windows 7, Windows 7 SP1  
**Server** – Windows Server 2008, Windows Server 2008 R2, Windows Server 2008 R2 SP1  

## <a name="feature-impact"></a>Auswirkungen auf Features

**Schweregrad –** Hoch  
**Frequency** – High  









## <a name="description"></a>Beschreibung

Die Dichten der Areal-Daten nehmen jährlich zu, und mit der kürzlichen Einführung von 3 TB Datenträgern werden die Fehlerkorrekturmechanismen, die zum Umgang mit dem abnehmenden Signal-zu-Rausch-Verhältnis (Signal-to-Noise-Ratio, SNR) verwendet werden, ineffizient. Das heißt, es ist ein höherer Mehraufwand erforderlich, um sicherzustellen, dass die Medien verwendet werden können. Eine der Speicherbranchelösungen zur Verbesserung dieses Fehlerkorrekturmechanismus ist die Einführung eines anderen physischen Medienformats, das eine größere physische Sektorgröße umfasst. Dieses neue physische Medienformat heißt *Erweitertes Format.* Daher ist es nicht mehr sicher, Annahmen zur Sektorgröße moderner Speichergeräte zu treffen, und Entwickler müssen die Annahmen untersuchen, die ihrem Code zugrunde liegen, um festzustellen, ob es Auswirkungen gibt.

In diesem Thema werden die Auswirkungen von Speichergeräten im erweiterten Format auf Software vorgestellt, und es wird erläutert, welche Möglichkeiten Anwendungen zur Unterstützung dieser Art von Medien haben. Außerdem wird die Infrastruktur erläutert, mit der Entwickler diese Gerätetypen unterstützen können. Während das in diesem Thema vorgestellte Material Richtlinien zur Verbesserung der Kompatibilität mit Datenträgern im erweiterten Format enthält, gelten die Informationen im Allgemeinen für alle Systeme mit Datenträgern im erweiterten Format. Die folgenden Versionen von Windows unterstützen das Abfragen der physischen Sektorgröße:

-   Windows 7 mit Microsoft KB-982018
-   Windows 7 SP1
-   Windows Server 2008 R2 mit Microsoft KB 982018
-   Windows Server 2008 R2 SP1
-   Windows Vista mit Microsoft KB 2553708
-   Windows Server 2008 mit Microsoft KB 2553708

Weitere Informationen finden Sie unter [Informationen zur Microsoft-Supportrichtlinie für große Laufwerke in Windows](https://support.microsoft.com/kb/2510009).

Weitere Informationen zu Datenträgern im erweiterten Format erhalten Sie von Ihrem Speicheranbieter.

## <a name="logical-vs-physical-sector-size"></a>Logische und physische Sektorgröße

Eines der Bedenken bei der Einführung dieser Änderung im Medienformat ist die Kompatibilität mit der Software und Hardware, die derzeit auf dem Markt verfügbar ist. Als temporäre Lösung führt die Speicherbranche zunächst Datenträger ein, die einen regulären 512-Byte-Sektordatenträger emulieren, aber Informationen zur tatsächlichen Sektorgröße über ATA- und SCSI-Standardbefehle verfügbar machen. Aufgrund dieser Emulation gibt es zwei Sektorgrößen:

-   **Logischer Sektor:** Die Einheit, die für die Adressierung logischer Blöcke für die Medien verwendet wird. Wir können uns dies auch als die kleinste Schreibeinheit vorstellen, die der Speicher akzeptieren kann. Dies ist die Emulation.

-   **Physischer Sektor:** Die Einheit, für die Lese- und Schreibvorgänge auf dem Gerät in einem einzigen Vorgang abgeschlossen werden. Dies ist die Einheit des atomaren Schreibzugriffs.

Die meisten aktuellen Windows-APIs, z. **B. IOCTL \_ DISK GET DRIVE \_ \_ \_ GEOMETRY,** geben die größe des logischen Sektor zurück. Die physische Sektorgröße kann jedoch über den [IOCTL \_ STORAGE QUERY \_ PROPERTY-Steuerungscode \_](/windows-hardware/drivers/ddi/content/ntddstor/ni-ntddstor-ioctl_storage_query_property) abgerufen werden, wobei die relevanten Informationen im Feld **BytesPerPhysicalSector** in der [ \_ \_ \_ DESCRIPTOR-Struktur STORAGE ACCESS ALIGNMENT](/windows/desktop/api/winioctl/ns-winioctl-storage_access_alignment_descriptor) enthalten sind. Dies wird weiter unten in diesem Artikel ausführlicher erläutert.

## <a name="initial-types-of-large-sector-media"></a>Anfängliche Typen großer Sektormedien

Die Speicherbranche setzt die Umstellung auf diesen neuen Speichertyp im erweiterten Format für Medien mit physischen Sektorgrößen von 4 KB schnell fort. Zwei Medientypen werden auf dem Markt veröffentlicht:

-   **4 KB nativ:** Dieses Medium verfügt über keine Emulationsebene und macht 4 KB direkt als logische und physische Sektorgröße verfügbar. Dieses Medium wird derzeit von Windows und den meisten anderen Betriebssystemen nicht unterstützt. Microsoft führt jedoch eine Untersuchung der Ierbarkeit durch, diese Art von Medien in einer zukünftigen Version von Windows zu unterstützen, und gibt ggf. einen Knowledge Base Artikel aus.
-   **512-Byte-Emulation (512e):** Dieses Medium verfügt über eine Emulationsebene, wie im vorherigen Abschnitt erläutert, und macht 512 Bytes als logische Sektorgröße verfügbar (ähnlich wie ein regulärer Datenträger heute), stellt aber informationen zur physischen Sektorgröße (4 KB) zur Verfügung. Dies ist das, was mehrere Speicheranbieter derzeit auf dem Markt einführen. Dieses allgemeine Problem mit dieser neuen Art von Medien besteht darin, dass die Mehrheit der Anwendung und betriebssysteme das Vorhandensein der physischen Sektorgröße nicht versteht, was zu einer Reihe von Problemen führen kann, wie im Folgenden erläutert wird.

## <a name="how-emulation-works-read-modify-write-rmw"></a>Funktionsweise der Emulation: Lesen/Ändern-Schreiben (RMW)

Ein Speichermedium verfügt über eine bestimmte Einheit, in der das physische Medium geändert werden kann. Das heißt, die Medien können nur in Einheiten der physischen Sektorgröße geschrieben oder umgeschrieben werden. Daher sind für Schreibvorgänge, die nicht auf dieser Einheitenebene ausgeführt werden, zusätzliche Schritte erforderlich. Dies wird im folgenden Beispiel beschrieben.

In diesem Szenario muss eine Anwendung den Inhalt eines Datastor-Datensatzes aktualisieren, der sich in einem logischen 512-Byte-Sektor befindet. Das folgende Diagramm veranschaulicht die Schritte, die für das Speichergerät erforderlich sind, um den Schreibvorgang abzuschließen:

![Erforderliche Schritte zum Aktualisieren des Datastor-Datensatzes in einem logischen 512-Byte-Sektor](images/512ermwsteps.png)

Wie oben gezeigt, umfasst dieser Prozess einige Arbeit des Speichergeräts, die zu leistungseinbußen führen kann. Um diese zusätzliche Arbeit zu vermeiden, müssen Anwendungen für folgende Schritte aktualisiert werden:

-   Abfrage der physischen Sektorgröße.
-   Stellen Sie sicher, dass Schreibvorgänge an der gemeldeten physischen Sektorgröße ausgerichtet sind.

## <a name="the-resiliency-impact-of-read-modify-write"></a>Auswirkungen der Resilienz von Lese-/Änderungs-/Schreibzugriff

Resilienz bezeichnet die Fähigkeit einer Anwendung, den Zustand zwischen Sitzungen wiederherzustellen. Wir haben gesehen, was erforderlich ist, damit ein 512e-Speichergerät einen 512-Byte-Sektorschreibvorgang ausführt – den Lese-/Änderungs-/Schreibzyklus. Sehen wir uns an, was passieren würde, wenn der Prozess des Überschreibens des vorherigen physischen Sektor auf den Medien unterbrochen würde. Was wären die Konsequenzen?

-   Da die meisten Festplattenlaufwerke direkt aktualisiert werden, könnte der physische Sektor , d. h. der Teil der Medien, in dem sich der physische Sektor befand, aufgrund eines partiellen Überschreibens mit unvollständigen Informationen beschädigt worden sein. Anders ausgedrückt: Sie können sich vorstellen, dass möglicherweise alle acht logischen Sektoren verloren gegangen sind (die der physische Sektor logisch enthält).

-   Die meisten Anwendungen mit einem Datenspeicher sind zwar so konzipiert, dass sie nach Medienfehlern wiederhergestellt werden können, aber der Verlust von acht Sektoren oder der Verlust von acht Commitdatensätzen kann es möglicherweise unmöglich machen, dass der Datenspeicher ordnungsgemäß wiederhergestellt wird. Ein Administrator muss die Datenbank möglicherweise manuell aus einer Sicherung wiederherstellen oder sogar eine lange Neuerstellung durchführen.

-   Ein weiterer wichtiger Einfluss ist, dass das Verhalten einer anderen Anwendung, die einen Lese-/Änderungs-/Schreibzyklus verursacht, möglicherweise dazu führen kann, dass Ihre Daten verloren gehen – auch wenn Ihre Anwendung nicht ausgeführt wird! Dies liegt einfach daran, dass sich Ihre Daten und die Daten der anderen Anwendung im selben physischen Sektor befinden können.

Vor diesem Hintergrund ist es wichtig, dass die Anwendungssoftware alle Annahmen im Code neu auswertet und sich der Unterscheidung zwischen logisch und physischer Sektorgröße sowie einigen interessanten Kundenszenarien bewusst ist, die weiter unten in diesem Artikel erläutert werden.

Dieses Problem tritt wahrscheinlicher auf, wenn Ihre Anwendung auf einem Datenspeicher für die Protokollstruktur basiert.

## <a name="avoiding-read-modify-write"></a>Vermeiden von Lese-/Änderungs-/Schreibzugriff

Während einige Speicheranbieter möglicherweise ein gewisses Maß an Entschärfung auf bestimmten 512e-Speichergeräten einführen, um zu versuchen, die Leistungs- und Resilienzprobleme des Lese-/Änderungs-/Schreibzyklus zu reduzieren, gibt es nur so viel, was eine Entschärfung in Bezug auf die Workload bewältigen kann. Daher sollten Sich Anwendungen nicht auf diese Lösung als langfristige Lösung verlassen.

Die Lösung hierfür ist keine laufwerksbasierte Risikominderung, sondern die Möglichkeit, dass Anwendungen die richtigen Maßnahmen durchführen, um den Lese-/Änderungs-/Schreibzyklus zu vermeiden. In diesem Abschnitt werden häufige Szenarien erläutert, in denen Anwendungen Probleme mit großen Sektordatenträgern haben können, und es wird eine Möglichkeit zur Untersuchung vorgeschlagen, um die einzelnen Probleme zu beheben.

### <a name="issue-1-the-partition-is-not-aligned-to-a-physical-sector-boundary"></a>Problem 1: Die Partition ist nicht an einer physischen Sektorgrenze ausgerichtet.

Wenn der Administrator/Benutzer den Datenträger partitioniert, wurde die erste Partition möglicherweise nicht an einer ausgerichteten Grenze erstellt. Dies kann dazu führen, dass alle nachfolgenden Schreibvorgänge nicht mehr an physischen Sektorgrenzen ausgerichtet werden. Ab Windows Vista SP1 und Windows Server 2008 wird die erste Partition auf den ersten 1024 KB des Datenträgers platziert (für Datenträger mit 4 GB oder höher, andernfalls beträgt die Ausrichtung 64 KB), die an einer physischen Sektorgrenze von 4 KB ausgerichtet ist. Angesichts der Standardpartitionierung in Windows XP, einem Partitionierungshilfsprogramm eines Drittanbieters oder einer falschen Verwendung Windows APIs werden erstellte Partitionen möglicherweise nicht an einer physischen Sektorgrenze ausgerichtet. Entwickler müssen sicherstellen, dass die richtigen APIs verwendet werden, um die Ausrichtung sicherzustellen. Die empfohlenen APIs zur Sicherstellung der Partitionsausrichtung sind unten beschrieben.

Die **APIs IVdsPack::CreateVolume** und **IVdsPack2::CreateVolume2** verwenden beim Erstellen eines neuen Volumes nicht den angegebenen Ausrichtungsparameter, sondern verwenden stattdessen den Standardausrichtungswert für das Betriebssystem (Pre-Windows Vista SP1 verwendet 63 Bytes, und nach Windows Vista SP1 werden die oben angegebenen Standardwerte verwendet). Daher wird empfohlen, dass Anwendungen, die Partitionen erstellen müssen, stattdessen die **APIs IVdsCreatePartitionEx::CreatePartitionEx** oder **IVdsAdvancedDisk::CreatePartition** verwenden, die den angegebenen Ausrichtungsparameter verwenden.

Die beste Möglichkeit, um sicherzustellen, dass die Ausrichtung richtig ist, besteht darin, dies beim ersten Erstellen der Partition richtig zu tun. Andernfalls muss Ihre Anwendung beim Ausführen von Schreibvorgängen oder bei der Initialisierung die Ausrichtung berücksichtigen . Dies kann eine sehr komplexe Aufgabe sein. Ab Windows Vista SP1 ist dies im Allgemeinen kein Problem. ältere Versionen von Windows können jedoch nicht ausgerichtete Partitionen erstellen, die bei einigen Datenträgern im erweiterten Format zu Leistungsproblemen führen können.

### <a name="issue-2-unbuffered-writes-not-aligned-to-physical-sector-size"></a>Problem 2: Nicht gepufferte Schreibvorgänge, die nicht an der Größe des physischen Sektor ausgerichtet sind

Das grundlegende Problem besteht darin, dass nicht gepufferte Schreibvorgänge nicht an der gemeldeten physischen Sektorgröße des Speichermediums ausgerichtet sind, wodurch ein Read-Modify-Write im Laufwerk ausgelöst wird, das zu Leistungsproblemen führen kann. Gepufferte Schreibvorgänge werden dagegen an der Seitengröße von 4 KB ausgerichtet, was zufällig der physischen Sektorgröße der ersten Generation großer Sektormedien entspricht. Die meisten Anwendungen mit einem Datenspeicher führen jedoch nicht gepufferte Schreibvorgänge durch und müssen daher sicherstellen, dass diese Schreibvorgänge in Einheiten der physischen Sektorgröße ausgeführt werden.

Um zu ermitteln, ob Ihre Anwendung ungepufferte E/A-Aufgaben ausgibt, überprüfen Sie, ob Sie das **FLAG FILE FLAG NO \_ \_ \_ BUFFERING** in den *parameter dwFlagsAndAttributes* einschließen, wenn Sie die **CreateFile-Funktion** aufrufen.

Wenn Sie die Schreibvorgänge derzeit an der Sektorgröße ausrichten, entspricht diese Sektorgröße wahrscheinlich nur der größe des *logischen* Sektor, da die meisten vorhandenen APIs, die die Sektorgröße der Medien abfragen, tatsächlich nur die Adressierungseinheit abfragen, d. h. die Größe des logischen Sektor. Die Sektorgröße, die hier von Interesse ist, ist die physische Sektorgröße, die die tatsächliche Einheit der Atomarität ist. Einige Beispiele für APIs, die die logische Sektorgröße abrufen, sind:

-   **GetDiskFreeSpace**, **GetDiskFreeSpaceEx**
-   **FileFsVolumeInformation**
-   **IOCTL \_ DISK \_ GET \_ DRIVE \_ GEOMETRY**, **IOCTL \_ DISK GET DRIVE \_ \_ \_ GEOMETRY \_ EX**
-   **IVdsDisk::GetProperties**, **IVdsDisk3::GetProperties2**

**Abfragen der Größe des physischen Sektor**

Microsoft hat auf MSDN ein Codebeispiel bereitgestellt, das detailliert erläutert, wie eine Anwendung die physische Sektorgröße des Volumes abfragen kann. Das Codebeispiel befindet sich unter <https://msdn.microsoft.com/library/ff800831.aspx> .

Im obigen Codebeispiel können Sie zwar die Größe des physischen Sektor des Volumes abrufen, aber Sie sollten vor der Verwendung einige grundlegende Überprüfungen der Sanität der gemeldeten physischen Sektorgröße durchführen, da festgestellt wurde, dass einige Treiber möglicherweise nicht ordnungsgemäß formatierte Daten zurückgeben:

-   Stellen Sie sicher, dass die gemeldete physische Sektorgröße >= der gemeldeten logischen Sektorgröße ist. Andernfalls sollte Ihre Anwendung eine physische Sektorgröße verwenden, die der gemeldeten logischen Sektorgröße entspricht.
-   Stellen Sie sicher, dass die gemeldete physische Sektorgröße eine Potenz von zwei ist. Andernfalls sollte Ihre Anwendung eine physische Sektorgröße verwenden, die der gemeldeten logischen Sektorgröße entspricht.
-   Wenn die größe des physischen Sektor ein Leistungswert von zwei Werten zwischen 512 Byte und 4 KB ist, sollten Sie erwägen, eine physische Sektorgröße zu verwenden, die auf die gemeldete logische Sektorgröße gerundet wird.
-   Wenn die physische Sektorgröße einen Wert von mehr als 4 KB auf zwei Leistungsstärken hat, sollten Sie die Fähigkeit Ihrer Anwendung auswerten, dieses Szenario zu verarbeiten, bevor Sie diesen Wert verwenden. Andernfalls sollten Sie erwägen, eine physische Sektorgröße zu verwenden, die auf 4 KB aufgerundet wird.

Die Verwendung dieser IOCTL zum Abrufen der physischen Sektorgröße hat mehrere Einschränkungen:

-   Erfordert erhöhte Rechte. Wenn Ihre Anwendung nicht mit Berechtigungen ausgeführt wird, müssen Sie möglicherweise wie oben erwähnt eine Windows-Dienstanwendung schreiben.

-   Unterstützt keine SMB-Volumes. Möglicherweise müssen Sie auch eine Windows-Dienstanwendung schreiben, um Abfragen der physischen Sektorgröße für diese Volumes zu unterstützen.

-   Kann nicht für ein Dateihandle ausgegeben werden (die IOCTL muss für ein Volumehandle ausgegeben werden).

-   Wird nur in Windows Versionen unterstützt, die am Anfang dieses Artikels aufgeführt sind.

**Commitdatensätze werden auf 512-Byte-Sektoren aufgefüllt.**

Anwendungen mit einem Datenspeicher verfügen in der Regel über eine Form von Commitdatensatz, der entweder Informationen zu Metadatenänderungen verwaltet oder die Struktur des Datenspeichers beibehält. Um sicherzustellen, dass sich der Verlust eines Sektor nicht auf mehrere Datensätze auswirkt, wird dieser Commitdatensatz in der Regel auf eine Sektorgröße aufgefüllt. Bei einem Datenträger mit einer größeren physischen Sektorgröße muss die Anwendung die Größe des physischen Sektor wie im vorherigen Abschnitt gezeigt abfragen und sicherstellen, dass jeder Commitdatensatz auf diese Größe aufgefüllt ist. Dadurch wird nicht nur der Lese-/Änderungs-/Schreibzyklus vermieden, sondern es wird sichergestellt, dass im Fall eines Verlusts eines physischen Sektor nur ein Commitdatensatz verloren geht.

**Protokolldateien werden in nicht ausgerichtete Blöcke geschrieben.**

Nicht gepufferte E/A wird in der Regel beim Aktualisieren oder Anfügen an eine Protokolldatei verwendet. Es gibt mehrere Möglichkeiten, sicherzustellen, dass diese Updates richtig ausgerichtet sind:

-   Protokollaktualisierungen der gemeldeten physischen Sektorgröße des Betriebsmediums intern puffern und Nur dann Protokollschreibungen ausstellen, wenn eine physische Sektoreinheit voll ist
-   Verwenden gepufferter E/A

### <a name="issue-3-file-formats-relying-on-512-byte-sectors"></a>Problem 3: Dateiformate, die auf 512-Byte-Sektoren basieren

Bei einigen Anwendungen mit Standarddateiformaten (z.B. VHD 1.0) sind diese Dateien möglicherweise hart codiert, um eine Sektorgröße von 512 Byte zu übernehmen. Daher führen Updates und Schreibvorgänge in dieser Datei zu einem Lese-/Änderungs-/Schreibzyklus auf dem Gerät. Dies kann zu Leistungs- und Resilienzproblemen für Ihre Kunden führen. Es gibt jedoch Möglichkeiten für eine Anwendung, Unterstützung für den Betrieb auf diesem Medientyp bereitzustellen, z. B.:

-   Verwenden Sie die Pufferung, um sicherzustellen, dass Schreibvorgänge in Einheiten der physischen Sektorgröße ausgeführt werden.
-   Implementieren Sie einen internen Lese-/Änderungs-/Schreibzugriff, mit dem sichergestellt werden kann, dass Updates in Einheiten der gemeldeten physischen Sektorgröße ausgeführt werden.
-   Auffüllen von Datensätzen in einem physischen Sektor nach Möglichkeit so, dass die Auffüllung als leerer Bereich interpretiert wird
-   Erwägen Sie das Umgestalten einer neuen Version der Anwendungsdatenstruktur mit Unterstützung für größere Sektoren.

### <a name="issue-4-the-reported-physical-sector-size-can-change-between-sessions"></a>Problem 4: Die gemeldete Größe des physischen Sektor kann sich zwischen Sitzungen ändern.

Es gibt viele Szenarien, in denen sich die gemeldete physische Sektorgröße des zugrunde liegenden Speichers, der den Datastor hostet, ändern kann. Die gängigste davon ist, wenn Sie den Datastor auf ein anderes Volume oder sogar über das Netzwerk migrieren. Eine Änderung der gemeldeten physischen Sektorgröße kann für viele Anwendungen ein unerwartetes Ereignis sein und möglicherweise dazu führen, dass einige Anwendungen sogar nicht erneut initialisiert werden können.

Dies ist nicht das einfachste Szenario, das unterstützt werden kann, und wird hier als Empfehlung erwähnt. Sie sollten die Mobilitätsanforderungen Ihrer Kunden berücksichtigen und Ihren Support entsprechend anpassen, um sicherzustellen, dass Kunden nicht durch die Verwendung von 512e-Medien beeinträchtigt werden.

## <a name="4-kb-native-media"></a>4 KB native Medien

512-Byte-Emulationsmedien sind als Übergangsschritt zwischen nativen 512-Byte- und 4-KB-nativen Medien gedacht, und es wird erwartet, dass 4 KB native Medien kurz nach 512e veröffentlicht werden. Es gibt mehrere wichtige Auswirkungen auf diese Medien, die zu beachten sind:

-   Die logische und physische Sektorgröße beträgt jeweils 4 KB.
-   Da keine Emulationsebene vorhanden ist, treten beim Speicher Fehler bei nicht ausgerichteten Schreibvorgängen auf.
-   Keine verborgene Resilienz: Anwendungen funktionieren entweder, oder sie funktionieren nicht.

Obwohl Microsoft derzeit die Unterstützung für diese Medientypen in einer zukünftigen Version von Windows untersucht und bei Bedarf einen KB-Artikel ausstellen wird, sollten Anwendungsentwickler erwägen, diese Medientypen präemptiv zu unterstützen.

## <a name="closing"></a>Schließen

In diesem Artikel haben wir die Auswirkungen erläutert, die große Sektormedien mit vielen gängigen Bereitstellungsszenarien einführen. Wir haben die Auswirkungen von Read-Modify-Write auf Leistung und Resilienz, einige der interessanten Szenarien, die dieses Medium einführen kann, und den Satz von Problemen gesehen, die sie möglicherweise mit Software verursachen können, was sich letztendlich auf den Endbenutzer auswirkt. Die Speicherbranche geht schnell zu Medien mit größeren Sektorgrößen über, und sehr bald können Kunden keine Datenträger mit herkömmlichen Sektorgrößen von 512 Byte erwerben.

Dies ist ein wichtiges Dokument und soll Entwicklern helfen, diesen Übergang zu verstehen. Sie sollten eine Konversation mit Ihren jeweiligen Organisationen, mit Kunden, IT-Spezialisten und Ihren Hardwareanbietern beginnen, um über den großen Sektorübergang und die Auswirkungen auf die szenarien zu sprechen, die für Sie wichtig sind.

## <a name="links-to-other-resources"></a>Links zu anderen Ressourcen

-   **Windows allgemeine Supporthinweis:**<https://support.microsoft.com/kb/2510009>
-   **Hotfix für Windows 7 und Windows Server 2008 R2:**<https://support.microsoft.com/kb/982018>
-   **Hotfix für Windows Vista und Windows Server 2008:**<https://support.microsoft.com/kb/2470478>
-   **HyperV-Supporthinweis:**<https://support.microsoft.com/kb/2515143>
-   **Allgemeine Informationen zur IOCTL \_ \_ \_ SPEICHERABFRAGEEIGENSCHAFTEN-Steuerelementcode:**[https://msdn.microsoft.com/library/ff560590.aspx](/windows-hardware/drivers/ddi/ntddstor/ni-ntddstor-ioctl_storage_query_property)
-   **IOCTL \_ STORAGE \_ QUERY PROPERTY Control \_ Code**: [https://msdn.microsoft.com/library/ff800830.aspx](/windows/win32/api/winioctl/ni-winioctl-ioctl_storage_query_property)
-   **Allgemeine Informationen zum SPEICHER \_ ACCESS \_ ALIGNMENT \_ DESCRIPTOR-Struktur:**[https://msdn.microsoft.com/library/ff566344.aspx](/windows-hardware/drivers/ddi/ntddstor/ns-ntddstor-_storage_access_alignment_descriptor)
-   **Beschreibung der Standardterminologie, die zur Beschreibung von Microsoft-Softwareupdates verwendet wird:**<https://support.microsoft.com/kb/824684/>
-   **WDK-Beispielcode** mit Details zum Extrahieren der gemeldeten Informationen zur Ausrichtung des Speicherzugriffs aus der **STORAGE ACCESS ALIGNMENT \_ \_ \_ DESCRIPTOR-Struktur** beim Aufrufen des **IOCTL \_ STORAGE QUERY \_ PROPERTY-Steuerungscodes: \_** [/windows/desktop/api/winioctl/ns-winioctl-storage_access_alignment_descriptor](/windows/desktop/api/winioctl/ns-winioctl-storage_access_alignment_descriptor)
-   **Allgemeine Informationen zu ImageX Command-Line Optionen:**<https://technet.microsoft.com/library/dd799302(WS.10).aspx>
-   **Intel-Chiptreiberanforderungen zur Unterstützung von 4-KB-Sektorlaufwerken:**<https://www.intel.com/support/chipsets/imsm/sb/CS-031502.htm>
-   Weitere Informationen zu Datenträgern im erweiterten Format finden Sie auf den folgenden IDEMA-Websites:
    -   <http://idema.org/?page_id=2172>
    -   <http://idema.org/?download=7926>

 

 
