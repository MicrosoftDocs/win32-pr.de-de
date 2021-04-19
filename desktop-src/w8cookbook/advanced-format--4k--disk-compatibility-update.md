---
title: Update der Datenträger Kompatibilität im erweiterten Format (4K)
description: Update der Datenträger Kompatibilität im erweiterten Format (4K)
ms.assetid: 2C9EB0CF-D27B-457A-8FE6-24824BCC084C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbad505575c4479bd750f09ccd83bc4da4c39667
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314973"
---
# <a name="advanced-format-4k-disk-compatibility-update"></a>Update der Datenträger Kompatibilität im erweiterten Format (4K)

## <a name="platforms"></a>Plattformen

**Clients**   Windows XP, Windows Vista, Windows 7, Windows 7 SP1, Windows 8  
**Server**   Windows Server 2003, Windows Server 2008, Windows Server 2008 R2, Windows Server 2008 R2 SP1, Windows Server 2012, Windows Server 2012 R2, Windows Server 2016  


## <a name="description"></a>Beschreibung

Dieser Artikel ist eine aktualisierte Version des Artikels mit dem Titel 512-Byte Emulation (512 e) Disk Compatibility Update, das für Windows 7 SP1 und Windows Server 2008 R2 SP1 veröffentlicht wurde. Dieses Update enthält viele neue Informationen, von denen einige nur für Windows 8 und Windows Server 2012 anwendbar sind.

Die Raum dichten werden jährlich gesteigert, und bei der letzten Einführung von 3 TB-Datenträgern werden die Fehlerkorrektur Mechanismen, die für den Umgang mit dem abnehmenden Signal-zu-Rauschen-Verhältnis (SNR) verwendet wurden, zu einem ineffizienten Raum. Dies bedeutet, dass ein erhöhter mehr Aufwand erforderlich ist, um sicherzustellen, dass die Medien verwendbar sind. Eine der Speicher-Branchenlösungen zum verbessern dieses Fehlerkorrektur Mechanismus besteht darin, ein anderes physisches Medienformat einzuführen, das eine größere physische Sektorgröße umfasst. Dieses neue Format für physische Medien wird als erweitertes Format bezeichnet. Daher ist es nicht mehr sicher, jegliche Annahmen hinsichtlich der Sektorgröße moderner Speichergeräte zu treffen, und Entwickler müssen die Annahmen, die Ihrem Code zugrunde liegen, untersuchen, um zu ermitteln, ob eine Auswirkung vorliegt.

In diesem Thema wird erläutert, wie sich das erweiterte Formatieren von Speichergeräten in Software unterstützt. Außerdem wird erläutert, welche Aktionen Apps zur Unterstützung dieser Art von Medien ausführen können. Außerdem wird die Infrastruktur erläutert, die Microsoft mit Windows Vista, Windows 7 und Windows 8 eingeführt hat, damit Entwickler diese Gerätetypen unterstützen können. Obwohl das in diesem Thema gezeigte Material Richtlinien zur Verbesserung der Kompatibilität mit erweiterten Format Datenträgern enthält, gelten die Informationen im Allgemeinen für alle Systeme mit erweiterten Format Datenträgern, auf denen Windows Vista, Windows 7 und Windows 8 ausgeführt werden.

**Zusammenfassung der neuen großen sektorbezogenen Features**

In der folgenden Liste werden die neuen Features, die als Teil von Windows 8 und Windows Server 2012 bereitgestellt werden, zusammengefasst, um die Kunden-und Entwickler Freundlichkeit bei Datenträgern mit großen Sektoren Eine ausführlichere Beschreibung der einzelnen Elemente folgt.

-   Basiert auf der Windows 7 SP1-Unterstützung für 4K-Datenträger mit Emulation (512 e) und bietet vollständige Eingangsbox Unterstützung für Datenträger mit einer Sektorgröße von 4 KB ohne Emulation (4K Native). Einige unterstützte apps und Szenarien umfassen Folgendes:
    -   Möglichkeit der Installation von Windows auf einem 4-KB-sektordatenträger ohne Emulation (4K Native Festplatte)
    -   VHD und das neue vhdx-Dateiformat
    -   Vollständige HyperV-Unterstützung
    -   Windows-Sicherung
    -   Vollständige Unterstützung im NT-Dateisystem (NTFS)
    -   Vollständige Unterstützung mit neuen Speicherplätzen und Pools (SSP)
    -   Vollständige Unterstützung mit Windows Defender
-   Bietet eine neue API zum Abfragen der Größe des physischen Sektors ("flefssectorsizeinformation"):
    -   Verfügbar für Netzwerkvolumes
    -   Kann für ein beliebiges Datei Handle ausgestellt werden.
    -   Verfügbar für nicht privilegierte apps
    -   Friendlier-Verwendungs Modell
-   Umfasst das Erweiterte Befehlszeilen-Hilfsprogramm fsutil zum Abfragen der logischen und physischen Sektorgröße von Volumes mit Ausrichtungs Informationen (grundlegende Version des Hilfsprogramms ohne Ausrichtungs Informationen ist für Windows 7 mit Microsoft KB 982018 und Windows Server 2008 R2 mit Microsoft KB 982018 verfügbar)

**Einführung in erweiterte Format Datenträger (4K)**

Eines der Probleme bei der Einführung dieser Änderung im Medienformat ist das Potenzial, Kompatibilitätsprobleme mit vorhandener Software und Hardware einzuführen. Als temporäre Kompatibilitäts Lösung führt die Speicher Branche anfänglich Datenträger ein, die einen regulären 512-Byte-sektordatenträger emulieren, aber über standardmäßige ATA-und SCSI-Befehle Informationen über die tatsächliche Sektorgröße bereitstellen. Infolge dieser Emulation gibt es im Wesentlichen zwei Sektorgrößen:

**Logischer Sektor:** Die Einheit, die für die logische Block Adressierung für das Medium verwendet wird. Wir können uns dies auch als kleinste Schreibeinheit vorstellen, die der Speicher annehmen kann. Dies ist die Emulation.   
**Physischer Sektor:** Die Einheit, für die Lese-und Schreibvorgänge auf dem Gerät in einem einzelnen Vorgang abgeschlossen werden. Dies ist die Einheit des atomaren Schreibzugriffs.  
 Die meisten aktuellen Windows-APIs, wie z. b. IOCTL \_ Disk \_ get \_ Drive \_ Geometry, geben die logische Sektorgröße zurück, aber die physische Sektorgröße kann über den <a href="/windows-hardware/drivers/ddi/content/ntddstor/ni-ntddstor-ioctl_storage_query_property">IOCTL \_ Storage \_ Query- \_ Eigenschaften</a> Steuerungs Code abgerufen werden, wobei die relevanten Informationen im Feld bytesperphysicalsektorin der <a href="/windows/desktop/api/winioctl/ns-winioctl-storage_access_alignment_descriptor"> \_ \_ \_ deskriptorstruktur der Speicherzugriffs Ausrichtung</a> enthalten sind. Dies wird weiter unten in diesem Artikel ausführlicher erläutert.

**Anfängliche Typen von Medien im großen Sektor**

Die Speicher Branche beschleunigt rasch den Umstieg auf diesen neuen erweiterten Formattyp von Speicher für Medien mit einer physischen Sektorgröße von 4 KB. Zwei Arten von Medien werden auf dem Markt veröffentlicht:

**4 KB** System eigen: Dieses Medium hat keine Emulations Schicht und macht 4 KB direkt als logische und physische Sektorgröße verfügbar. Das Gesamtproblem bei dieser neuen Art von Medien besteht darin, dass die meisten apps und Betriebssysteme keine e/a-Vorgängen für die physische Sektorgröße Abfragen und ausrichten, was zu unerwarteten fehlgeschlagenen e/a-Vorgängen führen kann.  
**512-Byte-Emulation (512 e):** Dieses Medium verfügt über eine Emulations Schicht, wie im vorherigen Abschnitt erläutert wurde, und macht 512-Bytes als logische Sektorgröße verfügbar (ähnlich wie bei einem regulären Datenträger), stellt jedoch die Größe der physischen Sektoren (4 KB) zur Verfügung. Das Gesamtproblem bei diesem neuen Medientyp besteht darin, dass die Mehrzahl der APP und der Betriebssysteme nicht das vorhanden sein der physischen Sektorgröße verstehen, was zu einer Reihe von Problemen führen kann, die im folgenden erläutert werden.  
**Allgemeine Windows-Unterstützung für Medien im großen Sektor**

In dieser Tabelle wird die offizielle Microsoft-Support Richtlinie für verschiedene Medien und die resultierenden gemeldeten Sektorgrößen dokumentiert. Weitere Informationen finden Sie in diesem [KB-Artikel](https://support.microsoft.com/kb/2510009) .



| Allgemeine Namen                                  | Gemeldete logische Sektorgröße | Gemeldete physische Sektorgröße | Windows-Version mit Unterstützung                                                                                                                                                                                                                                                                             |
|-----------------------------------------------|------------------------------|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 512-Byte Native, 512 n                         | 512 Bytes                    | 512 Bytes                     | Alle Windows-Versionen                                                                                                                                                                                                                                                                                     |
| Erweitertes Format, 512 e, AF, 512-Byte-Emulation | 512 Bytes                    | 4 KB                          | Windows Vista w/MS KB 2553708 <br/> Windows Server 2008 \* w/MS KB 2553708 <br/> Windows 7 w/MS KB 982018 <br/> Windows Server 2008 R2 * w/MS KB 982018 <br/> Alle Windows-Versionen von Windows 7 SP1 und darüber hinaus. <br/> Alle Serverversionen von Server 2008 R2 SP1 und darüber hinaus. <br/> <br/> \*Mit Ausnahme von Hyper-V. Weitere Informationen finden Sie im Abschnitt ["Anforderungen für die Anwendungsunterstützung für große sektorlaufwerke"](https://support.microsoft.com/help/2510009/microsoft-support-policy-for-4k-sector-hard-drives-in-windows) . |
| Vorab Format, AF, 4K Native, 4kN            | 4 KB                         | 4 KB                          | Alle Windows-Versionen von Windows 8 und darüber hinaus <br/> Alle Server Versionen von Windows Server 2012 und darüber hinaus <br/>                                                                                                                                                                                                                                                      |
| Andere                                         | Nicht 4 KB oder 512 Bytes        | Nicht 4 KB oder 512 Bytes         | Nicht unterstützt                                                                                                                                                                                                                                                                                            |



 

> [!Note]  
> Obwohl es in der obigen Tabelle nicht hervorgehoben ist, unterstützen Windows XP, Windows Server 2003 und Windows Server 2003 R2 nicht die Medien 512 e oder 4kN. Obwohl das System gestartet werden kann und in der Lage sein kann, minimal zu arbeiten, gibt es möglicherweise unbekannte Szenarios mit Funktions Problemen, Datenverlusten oder suboptimaler Leistung. Daher unterliegt Microsoft stark der Verwendung von 512 e-Medien mit Windows XP oder anderen Produkten, die auf der Windows XP-Codebasis basieren (z. b. Windows Home Server 1,0, Windows Server 2003, Windows Server 2003 R2, Windows XP 64-Bit Edition, Windows XP Embedded, Windows Small Business Server 2003 und Windows Small Business Server 2003 R2).

 

## <a name="how-emulation-works-read-modify-write-rmw"></a>Funktionsweise der Emulation: Read-Modify-Write (RMW)

Ein Speichermedium verfügt über eine bestimmte Einheit, in der das physische Medium geändert werden kann. Das heißt, die Medien können nur in Einheiten der physischen Sektorgröße geschrieben oder umgeschrieben werden. Folglich erfordern Schreibvorgänge, die nicht auf dieser Einheits Ebene ausgeführt werden, zusätzliche Schritte, die wir im folgenden Beispiel durchgehen werden.

In diesem Szenario muss eine APP den Inhalt eines dataStor-Datensatzes innerhalb eines logischen 512-Byte-Sektors aktualisieren. Dieses Diagramm veranschaulicht die Schritte, die erforderlich sind, damit das Speichergerät den Schreibvorgang beendet:

![Schritte für ein Speichergerät zum Abschluss eines Schreibvorgangs](images/512ermwsteps.png)

Wie oben gezeigt, umfasst dieser Prozess etwas Arbeit vom Speichergerät, das zu einem Leistungsverlust führen kann. Um diese zusätzliche Arbeit zu vermeiden, müssen apps wie folgt aktualisiert werden:

-   Abfragen der physischen Sektorgröße
-   Sicherstellen, dass Schreibvorgänge an der Größe des gemeldeten physischen Sektors ausgerichtet sind

Obwohl dies anfänglich scheinbar nur ein Leistungsproblem sein kann, kann es zu einem schwerwiegenderen Problem kommen. Dies wird im nächsten Abschnitt erläutert.

**Resilienz: die ausgeblendeten Kosten für Lese-und Schreibvorgänge**

Resilienz spricht von der Fähigkeit einer APP, den Status zwischen den Sitzungen wiederherzustellen. Wir haben gesehen, was erforderlich ist, damit ein 512E-Speichergerät einen 512-Byte-Sektor durchführen kann, um den Lese-und Schreibvorgang zu schreiben. Sehen Sie sich an, was passiert, wenn der Prozess der Überschreibung des vorherigen physischen Sektors auf dem Medium unterbrochen wurde. Wie lauten die Konsequenzen?

-   Da die meisten Festplattenlaufwerke direkt aktualisiert werden, ist der physische Sektor, d. h. der Teil des Mediums, auf dem sich der physische Sektor befand, möglicherweise aufgrund einer partiellen Überschreibung mit unvollständigen Informationen beschädigt worden. Anders ausgedrückt, Sie können sich davon vorstellen, dass alle acht logischen Sektoren verloren gegangen sind (was der physische Sektor logisch enthält).
-   Obwohl die meisten apps mit einem Datenspeicher mit der Funktion zur Wiederherstellung nach Medien Fehlern, dem Verlust von acht Sektoren oder einem anderen Weg, dem Verlust von acht Commit-Datensätzen, entworfen wurden, kann es möglicherweise unmöglich machen, dass der Datenspeicher ordnungsgemäß wieder hergestellt wird. Ein Administrator muss die Datenbank möglicherweise manuell aus einer Sicherung wiederherstellen oder sogar eine langwierige Neuerstellung durchführen.
-   Eine weitere wichtige Auswirkung besteht darin, dass der Act einer anderen APP, der einen Lese-/Änderungs-Vorgang verursacht, möglicherweise dazu führen kann, dass Ihre Daten verloren gehen, auch wenn Ihre APP nicht ausgeführt wird. Dies liegt einfach daran, dass sich die Daten und die anderen APP-Daten innerhalb desselben physischen Sektors befinden könnten.

Vor diesem Hintergrund ist es wichtig, dass die APP-Software alle Annahmen, die im Code vorgenommen wurden, neu bewertet und die Unterscheidung der logischen Sektorgröße sowie einige interessante Kunden Szenarios beachten, die später in diesem Artikel erläutert werden.

**Alles tun (vermeiden von Lese-und Schreibzugriff)**

Während einige Speicher Anbieter einige Stufen der Entschärfung innerhalb bestimmter 512 e-Speichergeräte einführen, um die Leistungs-und resilienzprobleme des Lese-/Änderungs-Schreibzyklen zu vereinfachen, gibt es nur so viele Entschärfungs Maßnahmen in Bezug auf die Arbeitsauslastung. Daher sollten sich apps nicht auf diese Entschärfung als langfristige Lösung verlassen. Außerdem gibt es keine Garantie dafür, dass für alle Klassen von Datenträgern diese Entschärfung vorhanden ist, und es gibt auch keine Garantie dafür, dass die Entschärfung gut entworfen wurde.

Dabei handelt es sich nicht um eine nicht-Laufwerke-Lösung, sondern um die Entwicklung von Apps für den richtigen Satz von Medien, um diese Art von Medien zu unterstützen. In diesem Abschnitt werden häufige Szenarien erläutert, in denen apps Probleme mit großen sektordatenträgern haben können, und es wird eine Untersuchungs Möglichkeit vorgeschlagen, um die einzelnen Probleme zu beheben.

**Problem 1: die Partition ist nicht an einer physischen Sektorgrenze ausgerichtet.**

Wenn der Administrator/Benutzer den Datenträger partitioniert, wurde die erste Partition möglicherweise nicht an einer ausgerichteten Grenze erstellt. Dies kann dazu führen, dass alle nachfolgenden Schreibvorgänge an den physischen Sektorgrenzen nicht ausgerichtet werden. Ab Windows Vista SP1 und Windows Server 2008 wird die erste Partition auf den ersten 1024 KB des Datenträgers platziert (für Datenträger mit einer Größe von 4 GB oder größer, andernfalls ist die Ausrichtung auf 64 KB), die an einer physischen Sektorgrenze von 4 KB ausgerichtet ist. Wenn jedoch die Standard Partitionierung in Windows XP, ein Drittanbieter-Partitionierungsprogramm oder eine falsche Verwendung von Windows-APIs vorhanden ist, sind erstellte Partitionen möglicherweise nicht an einer physischen Sektorgrenze ausgerichtet. Entwickler müssen sicherstellen, dass die richtigen APIs verwendet werden, um die Ausrichtung sicherzustellen. Die empfohlenen APIs, um sicherzustellen, dass die Partitions Ausrichtung nachfolgend beschrieben wird.

Die ivdspack:: anatevolume-und IVdsPack2:: CreateVolume2-APIs verwenden den angegebenen Ausrichtungs Parameter nicht, wenn ein neues Volume erstellt wird, sondern verwenden stattdessen den Standardwert für die Ausrichtung des Betriebssystems (Pre-Windows Vista SP1 verwendet 63 Bytes, und nach Windows Vista SP1 werden die oben genannten Standardeinstellungen verwendet). Verwenden Sie stattdessen die ivdscreatepartitionex:: | atepartitionex-oder ivdsadvanceddisk:: up-Partition-APIs, die den angegebenen Ausrichtungs Parameter für die apps verwenden, die Partitionen erstellen müssen.

Die beste Möglichkeit, um sicherzustellen, dass die Ausrichtung korrekt ist, ist das Recht, wenn Sie die Partition erstmalig erstellen. Andernfalls muss Ihre APP beim Ausführen von Schreibvorgängen oder bei der Initialisierung, bei der es sich um einen sehr komplexen Prozess handeln kann, eine Ausrichtung berücksichtigen.

**Problem 2: nicht gepufferte Schreibvorgänge, die nicht an der physischen Sektorgröße ausgerichtet sind**

Das einfachste Problem ist, dass nicht gepufferte Schreibvorgänge nicht an der gemeldeten physischen Sektorgröße des Speichermediums ausgerichtet werden. Gepufferte Schreibvorgänge werden hingegen auf die Seitengröße 4 KB ausgerichtet, was zufälligerweise die physische Sektorgröße der ersten Generation von Medien mit großen Sektoren ist. Bei den meisten apps mit einem Datenspeicher werden jedoch nicht gepufferte Schreibvorgänge ausgeführt. Daher muss sichergestellt werden, dass diese Schreibvorgänge in Einheiten der physischen Sektorgröße durchgeführt werden.

Einige Beispiele für Szenarien, in denen die resultierende App-e/a nicht ausgerichtet ist:

**Commit-Datensätze werden in 512-Byte-Sektoren aufgefüllt:** Apps mit einem Datenspeicher verfügen in der Regel über eine Art Commit-Datensatz, der entweder Informationen über Metadatenänderungen verwaltet oder die Struktur des Datenspeicher beibehält. Um sicherzustellen, dass sich der Verlust eines Sektors nicht auf mehrere Datensätze auswirkt, wird dieser Commit-Datensatz in der Regel in einer Sektorgröße aufgefüllt. Bei einem Datenträger mit einer größeren physischen Sektorgröße muss die APP die physische Sektorgröße Abfragen, wie im vorherigen Abschnitt gezeigt, und sicherstellen, dass jeder Commit-Datensatz in dieser Größe aufgefüllt wird. Bei einem 4K-Datenträger wird dadurch sichergestellt, dass e/a-Vorgänge nicht ausgeführt werden. Mit einem 512 e-Datenträger wird nicht nur der Lese-und Schreibvorgang vermieden, sondern es wird sichergestellt, dass nur ein Commit-Datensatz verloren geht, wenn ein physischer Sektor verloren gegangen ist.  
**Protokolldateien werden in nicht ausgerichtete Blöcke in geschrieben:** Nicht gepufferte e/a-Vorgänge werden in der Regel beim Aktualisieren oder Anhängen an eine Protokolldatei verwendet. Apps können entweder zu gepufferter e/a-Vorgänge wechseln oder die Protokoll Aktualisierungen intern auf Einheiten der physischen Sektorgröße Puffern, um fehlerhafte e/As zu vermeiden oder einen Lese-/Änderungs-Schreibvorgang auszulösen.  
 Wenn Sie ermitteln möchten, ob Ihre APP nicht gepufferte e/a-Vorgänge ausgibt, stellen Sie sicher, dass Sie das Flag für die \_ Dateiflag " \_ keine \_ Pufferung" in den Parameter " *dwflagsandattributs* " einschließen, wenn Sie die Funktion "

Wenn Sie derzeit die Schreibvorgänge an der Sektorgröße ausrichten, ist diese Sektorgröße wahrscheinlich nur die logische Sektorgröße, da die meisten vorhandenen APIs, die die Sektorgröße der Medien Abfragen, nur die Einheit der Adressierung Abfragen, d. h. die Größe des logischen Sektors. Die Sektorgröße, die hier von Interesse ist, ist die physische Sektorgröße, bei der es sich um die reale Einheit der Atomizität handelt. Einige Beispiele für APIs, die die logische Sektorgröße abrufen, sind:

-   GetDiskFreeSpace, GetDiskFreeSpaceEx
-   "Flefsvolumeinformation"
-   ioctl-Datenträger \_ \_ get- \_ Laufwerk \_ Geometrie, IOCTL \_ Disk \_ get \_ Drive \_ Geometry \_ Ex
-   Ivdsdisk:: GetProperties, IVdsDisk3:: GetProperties2

Hier erfahren Sie, wie Sie die physische Sektorgröße Abfragen können:

**Bevorzugte Methode für Windows 8**

Mit Windows 8 hat Microsoft eine neue API eingeführt, die es Entwicklern ermöglicht, 4K-Unterstützung problemlos in Ihre apps zu integrieren. Diese neue API unterstützt eine noch größere Anzahl von Szenarien als die ältere Methode für Windows Vista und Windows 7, die im folgenden erläutert wird. Diese API ermöglicht folgende Aufruf Szenarien:

-   Aufrufen von einer nicht privilegierten App
-   Aufrufen eines beliebigen gültigen Datei Handles
-   Aufrufen eines Datei Handles auf einem Remote Volume über SMB2
-   Vereinfachtes Programmiermodell

Die API verfügt über die neue Info-Klasse "flefssectorsizeinformation" mit zugeordneten Informationen zu den \_ Sektorgrößen für Struktur Datei FS \_ , die \_ \_ wie folgt definiert werden:


```
typedef struct _FILE_FS_SECTOR_SIZE_INFORMATION {  
    ULONG LogicalBytesPerSector;  
    ULONG PhysicalBytesPerSectorForAtomicity;  
    ULONG PhysicalBytesPerSectorForPerformance;  
    ULONG FileSystemEffectivePhysicalBytesPerSectorForAtomicity;  
    ULONG Flags;  
    ULONG ByteOffsetForSectorAlignment;  
    ULONG ByteOffsetForPartitionAlignment;  
} FILE_FS_SECTOR_SIZE_INFORMATION, *PFILE_FS_SECTOR_SIZE_INFORMATION;
```



**Legacy Methode für Windows 7 und Windows Vista**

Mit Windows Vista und Windows Server 2008 wurden APIs eingeführt, um die physische Sektorgröße des angefügten Speichergeräts für AHCI-basierte Speichercontroller abzufragen. Mit Windows 7 und Windows Server 2008 R2, ab SP1 (oder Microsoft Knowledge Base 982018), wird diese Unterstützung auf Storport-basierte Speichercontroller erweitert. Microsoft hat in MSDN ein [Codebeispiel](/windows/desktop/api/winioctl/ns-winioctl-storage_access_alignment_descriptor) bereitgestellt, in dem erläutert wird, wie eine APP die physische Sektorgröße des Volumes Abfragen kann.

Im obigen Codebeispiel können Sie die physische Sektorgröße des Volumes abrufen. Sie sollten jedoch einige grundlegende integritätprüfungen der gemeldeten physischen Sektorgröße durchführen, bevor Sie Sie verwenden, da festgestellt wurde, dass einige Treiber möglicherweise nicht ordnungsgemäß formatierte Daten zurückgeben:

-   Stellen Sie sicher, dass die gemeldete physische Sektorgröße >= der gemeldeten logischen Sektorgröße ist. Wenn dies nicht der Fall ist, sollte Ihre APP eine physische Sektorgröße verwenden, die der gemeldeten logischen Sektorgröße entspricht.
-   Stellen Sie sicher, dass die gemeldete physische Sektorgröße eine Potenz von zwei ist. Wenn dies nicht der Fall ist, sollte Ihre APP eine physische Sektorgröße verwenden, die der gemeldeten logischen Sektorgröße entspricht.
-   Wenn die physische Sektorgröße einen zweidimensionalen Wert zwischen 512-Byte und 4 KB beträgt, sollten Sie die Verwendung einer physischen Sektorgröße in Erwägung nehmen, die auf die gemeldete logische Sektorgröße gerundet ist.
-   Wenn es sich bei der physischen Sektorgröße um einen zweidimensionalen Wert als 4 KB handelt, sollten Sie die Fähigkeit Ihrer APP auswerten, dieses Szenario zu verarbeiten, bevor Sie diesen Wert verwenden. Andernfalls sollten Sie die Verwendung einer physischen Sektorgröße in Erwägung gezogen, die auf 4 KB gerundet ist.

Die Verwendung dieser ioctl zum erzielen der physischen Sektorgröße hat mehrere Einschränkungen. Sie hat folgende Aufgaben:

-   Erfordert erweiterte Berechtigungen. Wenn Ihre APP nicht mit Berechtigungen ausgeführt wird, müssen Sie möglicherweise wie oben beschrieben eine Windows-Dienst Anwendung schreiben.
-   SMB-Volumes werden von nicht unterstützt. Sie müssen möglicherweise auch eine Windows-Dienst Anwendung schreiben, um die Abfragen physischer Sektorgröße auf diesen Volumes zu unterstützen.
-   Kann nicht an ein Datei Handle ausgegeben werden (die IOCTL muss für ein volumehandle ausgestellt werden)

**Problem 3: Dateiformate, die sich auf 512-Byte-Sektoren verlassen**

Für einige apps mit Standarddatei Formaten (z. b. VHD 1,0) können diese Dateien hart codiert werden, um die Sektorgröße von 512 Bytes anzunehmen. Daher führen Updates und Schreibvorgänge für diese Datei zu einem Lese-/Schreib-Schreibvorgang auf dem Gerät, was potenziell zu Leistungs-und resilienzproblemen für Ihre Kunden führen kann. Es gibt jedoch Möglichkeiten, wie eine APP Unterstützung für diese Art von Medien bietet, z. b.:

-   Verwenden Sie Pufferung, um sicherzustellen, dass Schreibvorgänge in Einheiten der physischen Sektorgröße durchgeführt werden.
-   Implementieren Sie einen internen Lese-und Schreibzugriff, mit dem sichergestellt werden kann, dass Updates in Einheiten der gemeldeten physischen Sektorgröße durchgeführt werden.
-   Füllen Sie nach Möglichkeit Datensätze in einem physischen Sektor auf, so dass die Auffüllung als leerer Raum interpretiert werden würde.
-   Sie sollten eine Version der APP-Datenstruktur mit Unterstützung für größere Sektoren umgestalten.

**Problem 4: die gemeldete physische Sektorgröße kann sich zwischen den Sitzungen ändern.**

Es gibt viele Szenarien, in denen die gemeldete physische Sektorgröße des zugrunde liegenden Speichers, der den dataStor hostet, geändert werden kann. Der häufigste Fall ist, wenn Sie den dataStor zu einem anderen Volume oder sogar über das Netzwerk migrieren. Eine Änderung in der gemeldeten physischen Sektorgröße kann ein unerwartetes Ereignis für viele apps sein und möglicherweise dazu führen, dass einige apps nicht erneut initialisiert werden.

Dies ist nicht das einfachste Szenario für die Unterstützung von und wird hier als Empfehlung erwähnt. Berücksichtigen Sie die Mobilitätsanforderungen ihrer Kunden, und passen Sie Ihren Support entsprechend an, um sicherzustellen, dass die Kunden nicht durch die Verwendung von 4K Native oder 512 e-Medien beeinträchtigt werden.

**Wie ein Benutzer die logische und physische Sektorgröße für ein Volume abrufen kann**

In-Box mit Windows ist ein Hilfsprogramm zum Anzeigen der Sektorgrößen Informationen für ein Volume. Windows-Versionen mit unterstützter Unterstützung:

-   Windows 8
-   Windows Server 2012
-   Windows 7 SP1 mit Microsoft KB 982018
-   Windows 7 mit Microsoft KB 982018
-   Windows Server 2008 R2 SP1 mit Microsoft KB 982018 (v3)
-   Windows Server 2008 R2 mit Microsoft KB 982018 (v3)
-   Windows Vista mit Microsoft KB 2553708
-   Windows Server 2008 mit Microsoft KB 2553708

Um die Sektorgrößen Informationen abzurufen, nennen Sie das-Hilfsprogramm an einer Eingabeaufforderung mit erhöhten Rechten wie folgt:


```
fsutil fsinfo ntfsinfo <drive letter>
```



Ein 4K-sektordatenträger mit 512-Byte-Emulation hat das Feld Bytes pro Sektor auf 512 festgelegt, und das Feld Bytes pro physischem Sektor ist wie folgt auf 4096 festgelegt:

![Bytes pro Sektor und pro physischem Sektor eines 4K-sektordatenträgers mit 512-Byte-Emulation](images/4ksectordiskwith512emulation.png)

Ein 4K-Datenträger mit einer Größe von 4 KB weist die Felder Bytes pro Sektor und Bytes pro physischem Sektor auf 4096, wie im folgenden dargestellt:

![Bytes pro Sektor und pro physischem Sektor eines 4K-Datenträgers](images/4knativedisk.png)

> [!Note]  
> Wenn das Feld Byte pro physischem Sektor nicht unterstützt angezeigt wird, unterstützt der Speicher Treiber die IOCTL- \_ Speicher \_ Abfrage \_ Eigenschaft nicht, oder es ist ein Fehler beim Abrufen der Informationen aufgetreten.

 

## <a name="resources"></a>Ressourcen

-   [Allgemeine Windows-Support-Anweisung](https://support.microsoft.com/kb/2510009)
-   [Microsoft KB 982018](https://support.microsoft.com/kb/982018)
-   [Microsoft KB 2553708](https://support.microsoft.com/kb/2553708)
-   [Hotfix für Windows 7 und Windows Server 2008 R2](https://support.microsoft.com/kb/982018)
-   [Hotfix für Windows Vista und Windows Server 2008](https://support.microsoft.com/kb/2553708)
-   [HyperV-Unterstützungs Anweisung](https://support.microsoft.com/kb/2515143)
-   [Allgemeine Informationen über den Steuerungs Code der IOCTL- \_ Speicher \_ Abfrage \_ Eigenschaft](/windows-hardware/drivers/ddi/ntddstor/ni-ntddstor-ioctl_storage_query_property)
-   [Steuerungs Code der IOCTL- \_ Speicher \_ Abfrage \_ Eigenschaft](/windows/win32/api/winioctl/ni-winioctl-ioctl_storage_query_property)
-   [Allgemeine Informationen zur \_ \_ deskriptorstruktur der Speicherzugriffs Ausrichtung \_](/windows-hardware/drivers/ddi/ntddstor/ns-ntddstor-_storage_access_alignment_descriptor)
-   [Beschreibung der Standard Terminologie, die zum Beschreiben von Microsoft-Software Updates verwendet wird.](https://support.microsoft.com/kb/824684/)
-   [WDK-Beispielcode mit Details zum Extrahieren der gemeldeten Informationen zur Speicherzugriffs Ausrichtung aus der Speicher \_ Zugriffs- \_ Ausrichtungs \_ deskriptorstruktur beim Aufrufen des \_ \_ Steuercodes der IOCTL Storage Query- \_ Eigenschaft](/windows/win32/api/winioctl/ns-winioctl-storage_access_alignment_descriptor)
-   [Allgemeine Informationen zu ImageX-Command-Line Optionen](/previous-versions/windows/it-pro/windows-7/dd799302(v=ws.10))
-   [Anforderungen an den Intel Chip Set-Treiber zur Unterstützung von 4-KB](https://www.intel.com/support/chipsets/imsm/sb/CS-031502.htm)

 

