---
title: Update der Datenträgerkompatibilität im erweiterten Format (4K)
description: Update der Datenträgerkompatibilität im erweiterten Format (4K)
ms.assetid: 2C9EB0CF-D27B-457A-8FE6-24824BCC084C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99cf89345dfc33826c4eb1f155083793726de7d70bc95c1dcdda96644d5d1173
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117672202"
---
# <a name="advanced-format-4k-disk-compatibility-update"></a>Update der Datenträgerkompatibilität im erweiterten Format (4K)

## <a name="platforms"></a>Plattformen

**Clients** Windows XP, Windows Vista, Windows 7, Windows 7 SP1, Windows 8     
**Server** Windows Server 2003, Windows Server 2008, Windows Server 2008 R2, Windows Server 2008 R2 SP1, Windows Server 2012, Windows Server 2012 R2, Windows Server 2016     


## <a name="description"></a>Beschreibung

Dieser Artikel ist eine aktualisierte Version des Artikels mit dem Titel 512-Byte Emulation (512e) Disk Compatibility Update, das für Windows 7 SP1 und Windows Server 2008 R2 SP1 veröffentlicht wurde. Dieses Update enthält viele neue Informationen, von denen einige nur für Windows 8 und Windows Server 2012 gelten.

Die Arealdichten nehmen jährlich zu, und mit dem aktuellen Aufkommen von 3 TB Datenträgern werden die Fehlerkorrekturmechanismen, die zum Umgang mit dem abnehmenden Signal-Rausch-Verhältnis (Signal-to-Noise-Ratio, SNR) verwendet werden, ineffizient. Das heißt, es ist ein höherer Mehraufwand erforderlich, um sicherzustellen, dass die Medien verwendbar sind. Eine der Speicherbranchelösungen zur Verbesserung dieses Fehlerkorrekturmechanismus ist die Einführung eines anderen physischen Medienformats, das eine größere physische Sektorgröße umfasst. Dieses neue physische Medienformat heißt Erweitertes Format. Daher ist es nicht mehr sicher, Annahmen zur Sektorgröße moderner Speichergeräte zu treffen, und Entwickler müssen die Annahmen untersuchen, die ihrem Code zugrunde liegen, um festzustellen, ob es Auswirkungen gibt.

In diesem Thema werden die Auswirkungen von Speichergeräten im erweiterten Format auf Software vorgestellt, und es wird erläutert, welche Möglichkeiten Apps zur Unterstützung dieser Art von Medien haben. Außerdem wird die Infrastruktur erläutert, die Microsoft mit Windows Vista, Windows 7 und Windows 8 eingeführt hat, um Entwicklern die Unterstützung dieser Gerätetypen zu ermöglichen. Während das in diesem Thema vorgestellte Material Richtlinien zur Verbesserung der Kompatibilität mit Datenträgern im erweiterten Format enthält, gelten die Informationen im Allgemeinen für alle Systeme mit Datenträgern im erweiterten Format, die Windows Vista, Windows 7 und Windows 8 ausgeführt werden.

**Zusammenfassung der neuen Features im Zusammenhang mit großen Sektoren**

In der folgenden Liste sind die neuen Features zusammengefasst, die als Teil der Windows 8 und Windows Server 2012 bereitgestellt werden, um die Kunden- und Entwicklererfahrung mit großen Sektordatenträgern zu verbessern. Eine ausführlichere Beschreibung der einzelnen Elemente finden Sie hier.

-   Baut auf der Windows 7 SP1-Unterstützung für 4K-Datenträger mit Emulation (512e) auf und bietet vollständige Posteingangsunterstützung für Datenträger mit einer Sektorgröße von 4K ohne Emulation (4K nativ). Zu den unterstützten Apps und Szenarien gehören:
    -   Möglichkeit zum Installieren Windows und Starten von einem 4K-Sektordatenträger ohne Emulation (nativer 4K-Datenträger)
    -   VHD und neues VHDX-Dateiformat
    -   Vollständige HyperV-Unterstützung
    -   Windows Sicherung
    -   Vollständige Unterstützung im NT-Dateisystem (NTFS)
    -   Vollständige Unterstützung mit neuen Speicherplätze und Pools (SSP)
    -   Vollständige Unterstützung mit Windows Defender
-   Stellt eine neue API zum Abfragen der physischen Sektorgröße (FileFsSectorSizeInformation) bereit:
    -   Verfügbar für Netzwerkvolumes
    -   Kann für jedes Dateihandle ausgegeben werden
    -   Verfügbar für nicht privilegierte Apps
    -   Benutzerfreundlicheres Nutzungsmodell
-   Enthält ein erweitertes Fsutil-Befehlszeilenprogramm zum Abfragen der logischen und physischen Sektorgröße des Volumes mit Ausrichtungsinformationen (grundlegende Version des Hilfsprogramms ohne Ausrichtungsinformationen ist für Windows 7 mit Microsoft KB 982018 und Windows Server 2008 R2 mit Microsoft KB 982018 verfügbar).

**Einführung in Datenträger im erweiterten Format (4K)**

Eines der Probleme bei der Einführung dieser Änderung im Medienformat besteht darin, dass Kompatibilitätsprobleme mit vorhandener Software und Hardware auftreten können. Als temporäre Kompatibilitätslösung führt die Speicherbranche anfänglich Datenträger ein, die einen regulären 512-Byte-Sektordatenträger emulieren, aber Informationen zur tatsächlichen Sektorgröße über ATA- und SCSI-Standardbefehle zur Verfügung stellen. Aufgrund dieser Emulation gibt es im Wesentlichen zwei Sektorgrößen:

**Logischer Sektor:** Die Einheit, die für die Adressierung logischer Blöcke für die Medien verwendet wird. Wir können uns dies auch als die kleinste Schreibeinheit vorstellen, die der Speicher akzeptieren kann. Dies ist die Emulation.   
**Physischer Sektor:** Die Einheit, für die Lese- und Schreibvorgänge auf dem Gerät in einem einzigen Vorgang abgeschlossen werden. Dies ist die Einheit des atomaren Schreibzugriffs.  
 Die meisten aktuellen Windows-APIs, z. B. IOCTL \_ DISK \_ GET DRIVE \_ \_ GEOMETRY, geben die größe des logischen Sektor zurück. Die physische Sektorgröße kann jedoch über den <a href="/windows-hardware/drivers/ddi/content/ntddstor/ni-ntddstor-ioctl_storage_query_property">IOCTL \_ STORAGE QUERY \_ PROPERTY-Steuerungscode \_ </a> abgerufen werden, wobei die relevanten Informationen im Feld BytesPerPhysicalSector in der <a href="/windows/desktop/api/winioctl/ns-winioctl-storage_access_alignment_descriptor"> \_ \_ \_ DESCRIPTOR-Struktur für DIE AUSRICHTUNG DES SPEICHERZUGRIFFs</a> enthalten sind. Dies wird weiter unten in diesem Artikel ausführlicher erläutert.

**Anfängliche Typen großer Sektormedien**

Die Speicherbranche setzt die Umstellung auf diesen neuen Speichertyp im erweiterten Format für Medien mit einer physischen Sektorgröße von 4 KB schnell fort. Zwei Medientypen werden auf dem Markt veröffentlicht:

**4 KB nativ:** Dieses Medium verfügt über keine Emulationsebene und macht 4 KB direkt als logische und physische Sektorgröße verfügbar. Das Gesamtproblem bei diesem neuen Medientyp besteht darin, dass die Meisten Apps und Betriebssysteme keine E/A-Abfragen durchführen und die E/A-Daten nicht an die Größe des physischen Sektor ausrichten, was zu unerwarteten E/A-Fehlern führen kann.  
**512-Byte-Emulation (512e):** Dieses Medium verfügt über eine Emulationsebene, wie im vorherigen Abschnitt erläutert, und macht 512 Bytes als logische Sektorgröße verfügbar (ähnlich wie ein regulärer Datenträger heute), stellt aber informationen zur physischen Sektorgröße (4 KB) zur Verfügung. Das Allgemeine Problem bei diesem neuen Medientyp besteht darin, dass die Mehrheit der App- und Betriebssysteme das Vorhandensein der physischen Sektorgröße nicht versteht, was zu einer Reihe von Problemen führen kann, wie unten erläutert.  
**Allgemeine Windows Unterstützung für große Sektormedien**

In dieser Tabelle werden die offizielle Microsoft-Supportrichtlinie für verschiedene Medien und die daraus resultierenden gemeldeten Sektorgrößen dokumentiert. Weitere Informationen finden Sie in diesem [KB-Artikel.](https://support.microsoft.com/kb/2510009)



| Allgemeine Namen                                  | Gemeldete Größe des logischen Sektor | Gemeldete Größe des physischen Sektor | Windows Version mit Support                                                                                                                                                                                                                                                                             |
|-----------------------------------------------|------------------------------|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 512 Byte nativ, 512n                         | 512 Bytes                    | 512 Bytes                     | Alle Windows-Versionen                                                                                                                                                                                                                                                                                     |
| Erweitertes Format, 512e, AF, 512-Byte-Emulation | 512 Bytes                    | 4 KB                          | Windows Vista w/MS KB 2553708 <br/> Windows Server 2008 \* w/MS KB 2553708 <br/> Windows 7 w/MS KB 982018 <br/> Windows Server 2008 R2* mit MS KB 982018 <br/> Alle Windows Versionen von Windows 7 SP1 und höher. <br/> Alle Serverversionen ab Server 2008 R2 SP1. <br/> <br/> \*Mit Ausnahme von Hyper-V. Weitere Informationen finden Sie im Abschnitt "Anforderungen an die [Anwendungsunterstützung für Große Sektorlaufwerke".](https://support.microsoft.com/help/2510009/microsoft-support-policy-for-4k-sector-hard-drives-in-windows) |
| Advance Format, AF, 4K Native, 4Kn            | 4 KB                         | 4 KB                          | Alle Windows Versionen von Windows 8 und darüber hinaus <br/> Alle Serverversionen von Windows Server 2012 und höher <br/>                                                                                                                                                                                                                                                      |
| Andere                                         | Nicht 4 KB oder 512 Bytes        | Nicht 4 KB oder 512 Bytes         | Nicht unterstützt                                                                                                                                                                                                                                                                                            |



 

> [!Note]  
> Obwohl in der obigen Tabelle nicht enthalten, unterstützen Windows XP, Windows Server 2003 und Windows Server 2003 R2 keine 512e- oder 4Kn-Medien. Obwohl das System möglicherweise gestartet wird und minimal betrieben werden kann, gibt es möglicherweise unbekannte Szenarien mit Funktionalitätsproblemen, Datenverlust oder suboptimaler Leistung. Daher warnt Microsoft dringend davor, 512e-Medien mit Windows XP oder anderen Produkten zu verwenden, die auf der Windows XP-Codebasis basieren (z. B. Windows Home Server 1.0, Windows Server 2003, Windows Server 2003 R2, Windows XP 64-Bit Edition, Windows XP Embedded, Windows Small Business Server 2003 und Windows Small Business Server 2003 R2).

 

## <a name="how-emulation-works-read-modify-write-rmw"></a>Funktionsweise der Emulation: Read-Modify-Write (RMW)

Ein Speichermedium verfügt über eine bestimmte Einheit, in der das physische Medium geändert werden kann. Das heißt, die Medien können nur in Einheiten der physischen Sektorgröße geschrieben oder umgeschrieben werden. Daher sind für Schreibvorgänge, die nicht auf dieser Einheitenebene ausgeführt werden, zusätzliche Schritte erforderlich. Dies wird im folgenden Beispiel erläutert.

In diesem Szenario muss eine App den Inhalt eines Datastor-Datensatzes aktualisieren, der sich in einem logischen 512-Byte-Sektor befindet. Dieses Diagramm veranschaulicht die Schritte, die für das Speichergerät erforderlich sind, um den Schreibvorgang abzuschließen:

![Schritte für ein Speichergerät zum Abschließen eines Schreibzugriffs](images/512ermwsteps.png)

Wie oben gezeigt, umfasst dieser Prozess einige Arbeit des Speichergeräts, die zu leistungseinbußen führen kann. Um diese zusätzliche Arbeit zu vermeiden, müssen Apps aktualisiert werden auf:

-   Abfrage der physischen Sektorgröße
-   Stellen Sie sicher, dass Schreibvorgänge an der gemeldeten physischen Sektorgröße ausgerichtet sind.

Obwohl dies anfänglich nur ein Leistungsproblem zu sein scheint, kann es zu einem schwerwiegenderen Problem kommen. Dies wird im nächsten Abschnitt erläutert.

**Resilienz: die verborgenen Kosten für Lese-/Änderungs-/Schreibzugriff**

Resilienz bezeichnet die Fähigkeit einer App, den Zustand zwischen Sitzungen wiederherzustellen. Wir haben gesehen, was erforderlich ist, damit ein 512e-Speichergerät einen 512-Byte-Sektor ausführen kann, um den Lese-/Änderungs-/Schreibzyklus zu schreiben. Sehen wir uns an, was passieren würde, wenn der Prozess des Überschreibens des vorherigen physischen Sektor auf den Medien unterbrochen würde. Was wären die Konsequenzen?

-   Da die meisten Festplattenlaufwerke direkt aktualisiert werden, könnte der physische Sektor, d. h. der Teil der Medien, in dem sich der physische Sektor befand, aufgrund eines partiellen Überschreibens mit unvollständigen Informationen beschädigt worden sein. Anders ausgedrückt: Sie können sich vorstellen, dass möglicherweise alle acht logischen Sektoren verloren gegangen sind (die der physische Sektor logisch enthält).
-   Während die meisten Apps mit einem Datenspeicher mit der Möglichkeit zur Wiederherstellung nach Medienfehlern, dem Verlust von acht Sektoren oder einem anderen Weg, dem Verlust von acht Commitdatensätzen, entworfen wurden, kann es für den Datenspeicher möglicherweise unmöglich sein, ordnungsgemäß wiederhergestellt zu werden. Ein Administrator muss die Datenbank möglicherweise manuell aus einer Sicherung wiederherstellen oder sogar eine lange Neuerstellung durchführen.
-   Ein weiterer wichtiger Einfluss ist, dass der Vorgang einer anderen App, die einen Lese-/Änderungs-/Schreibzyklus verursacht, dazu führen kann, dass Ihre Daten verloren gehen, auch wenn Ihre App nicht ausgeführt wird! Dies liegt einfach daran, dass sich Ihre Daten und die Daten der anderen App im selben physischen Sektor befinden können.

Vor diesem Hintergrund ist es wichtig, dass App-Software alle Annahmen im Code neu bewertet und sich der Unterscheidung zwischen logisch und physisch nach Sektorgröße sowie einigen interessanten Kundenszenarien bewusst ist, die weiter unten in diesem Artikel erläutert werden.

**Richtiges Tun (Vermeiden von Lese-/Änderungs-/Schreibzugriff)**

Während einige Speicheranbieter auf bestimmten 512e-Speichergeräten möglicherweise ein gewisses Maß an Entschärfung einführen, um zu versuchen, die Leistungs- und Resilienzprobleme des Lese-/Änderungs-/Schreibzyklus zu reduzieren, gibt es nur so viele Entschärfungen in Bezug auf die Workload. Daher sollten Sich Apps nicht auf diese Lösung als langfristige Lösung verlassen. Darüber hinaus gibt es keine Garantie dafür, dass diese Entschärfung für alle Klassen von Datenträgern vorhanden ist, und es gibt auch keine Garantie dafür, dass die Entschärfung gut konzipiert ist.

Die Lösung hierfür besteht nicht in der vermeidungsorientierten Risikominderung, sondern darin, Apps so zu entwerfen, dass sie die richtigen Maßnahmen zur Unterstützung dieser Art von Medien durchführen. In diesem Abschnitt werden häufige Szenarien erläutert, in denen Apps Probleme mit großen Sektordatenträgern haben können, und es wird eine Möglichkeit zur Untersuchung vorgeschlagen, um die einzelnen Probleme zu beheben.

**Problem 1: Die Partition ist nicht an einer physischen Sektorgrenze ausgerichtet.**

Wenn der Administrator/Benutzer den Datenträger partitioniert, wurde die erste Partition möglicherweise nicht an einer ausgerichteten Grenze erstellt. Dies kann dazu führen, dass alle nachfolgenden Schreibvorgänge nicht mehr an physischen Sektorgrenzen ausgerichtet werden. Ab Windows Vista SP1 und Windows Server 2008 wird die erste Partition auf den ersten 1024 KB des Datenträgers platziert (bei Datenträgern mit 4 GB oder höher, andernfalls 64 KB), die an einer physischen Sektorgrenze von 4 KB ausgerichtet sind. Angesichts der Standardpartitionierung in Windows XP, einem Partitionierungshilfsprogramm eines Drittanbieters oder einer falschen Verwendung Windows APIs werden erstellte Partitionen möglicherweise nicht an einer physischen Sektorgrenze ausgerichtet. Entwickler müssen sicherstellen, dass die richtigen APIs verwendet werden, um die Ausrichtung sicherzustellen. Die empfohlenen APIs zur Sicherstellung der Partitionsausrichtung sind unten beschrieben.

Die APIs IVdsPack::CreateVolume und IVdsPack2::CreateVolume2 verwenden beim Erstellen eines neuen Volumes nicht den angegebenen Ausrichtungsparameter, sondern den Standardwert für die Ausrichtung für das Betriebssystem (Vor Windows Vista SP1 verwendet 63 Bytes, und nach Windows Vista SP1 werden die oben angegebenen Standardwerte verwendet). Verwenden Sie stattdessen die IVdsCreatePartitionEx::CreatePartitionEx- oder IVdsAdvancedDisk::CreatePartition-APIs, die den angegebenen Ausrichtungsparameter für die Apps verwenden, die Partitionen erstellen müssen.

Die beste Möglichkeit, um sicherzustellen, dass die Ausrichtung richtig ist, besteht darin, dies beim ersten Erstellen der Partition richtig zu tun. Andernfalls muss Ihre App die Ausrichtung beim Ausführen von Schreibvorgängen oder bei der Initialisierung berücksichtigen, was ein sehr komplexer Prozess sein kann.

**Problem 2: Nicht gepufferte Schreibvorgänge, die nicht an der physischen Sektorgröße ausgerichtet sind**

Das einfachste Problem besteht darin, dass nicht gepufferte Schreibvorgänge nicht an der gemeldeten physischen Sektorgröße des Speichermediums ausgerichtet sind. Gepufferte Schreibvorgänge werden dagegen an der Seitengröße von 4 KB ausgerichtet, was zufällig der physischen Sektorgröße der ersten Generation großer Sektormedien entspricht. Die meisten Apps mit einem Datenspeicher führen jedoch nicht gepufferte Schreibvorgänge durch und müssen daher sicherstellen, dass diese Schreibvorgänge in Einheiten der physischen Sektorgröße ausgeführt werden.

Einige Beispiele für Szenarien, in denen die resultierende App-E/A nicht ausgerichtet ist:

**Commitdatensätze werden auf 512-Byte-Sektoren aufgefüllt:** Apps mit einem Datenspeicher verfügen in der Regel über einen Commitdatensatz, der entweder Informationen zu Metadatenänderungen oder die Struktur des Datenspeichers beibehält. Um sicherzustellen, dass sich der Verlust eines Sektor nicht auf mehrere Datensätze auswirkt, wird dieser Commitdatensatz in der Regel auf eine Sektorgröße aufgefüllt. Bei einem Datenträger mit einer größeren physischen Sektorgröße muss die App die Größe des physischen Sektor wie im vorherigen Abschnitt gezeigt abfragen und sicherstellen, dass jeder Commitdatensatz auf diese Größe aufgefüllt ist. Bei einem 4K-Datenträger wird dadurch sichergestellt, dass E/A-Fehler nicht fehlschlagen. Bei einem 512e-Datenträger vermeidet dies nicht nur den Lese-/Änderungs-/Schreibzyklus, sondern stellt auch sicher, dass bei einem Verlust eines physischen Sektor nur ein Commitdatensatz verloren geht.  
**Protokolldateien werden in nicht ausgerichtete Blöcke geschrieben:** Nicht gepufferte E/A wird in der Regel beim Aktualisieren oder Anfügen an eine Protokolldatei verwendet. Apps können entweder zu gepufferten E/A-Blöcken wechseln oder die Protokollaktualisierungen intern auf Einheiten der physischen Sektorgröße puffern, um E/A-Fehler zu vermeiden oder Lese-/Änderungs-/Schreibzugriff auszulösen.  
 Um zu ermitteln, ob Ihre App ungepufferte E/A-Aufgaben ausgibt, stellen Sie sicher, dass Sie das FLAG FILE \_ FLAG \_ NO \_ BUFFERING in den *dwFlagsAndAttributes-Parameter* einschließen, wenn Sie die CreateFile-Funktion aufrufen.

Wenn Sie die Schreibvorgänge derzeit an der Sektorgröße ausrichten, entspricht diese Sektorgröße wahrscheinlich nur der größe des logischen Sektor, da die meisten vorhandenen APIs, die die Sektorgröße der Medien abfragen, nur die Adressierungseinheit abfragen, d. h. die Größe des logischen Sektor. Die Sektorgröße, die hier von Interesse ist, ist die physische Sektorgröße, die die tatsächliche Einheit der Atomarität ist. Einige Beispiele für APIs, die die logische Sektorgröße abrufen, sind:

-   GetDiskFreeSpace, GetDiskFreeSpaceEx
-   FileFsVolumeInformation
-   IOCTL \_ DISK \_ GET \_ DRIVE \_ GEOMETRY, IOCTL \_ DISK \_ GET \_ DRIVE \_ GEOMETRY \_ EX
-   IVdsDisk::GetProperties, IVdsDisk3::GetProperties2

So können Sie die physische Sektorgröße abfragen:

**Bevorzugte Methode für Windows 8**

Mit Windows 8 hat Microsoft eine neue API eingeführt, mit der Entwickler 4K-Unterstützung problemlos in ihre Apps integrieren können. Diese neue API unterstützt eine noch größere Anzahl von Szenarien als die legacy-Methode für Windows Vista und Windows 7 weiter unten beschrieben. Diese API ermöglicht die folgenden Aufrufszenarien:

-   Aufrufen von einer nicht privilegierten App
-   Aufrufen eines gültigen Dateihandle
-   Aufrufen eines Dateihandle auf einem Remotevolume über SMB2
-   Vereinfachtes Programmiermodell

Die API hat die Form einer neuen Infoklasse, FileFsSectorSizeInformation, mit der zugeordneten Struktur FILE \_ FS \_ SECTOR SIZE \_ \_ INFORMATION, die wie folgt definiert ist:


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



**Legacymethode für Windows 7 und Windows Vista**

Windows Vista und Windows Server 2008 haben APIs eingeführt, um die physische Sektorgröße des angeschlossenen Speichergeräts für AHCI-basierte Speichercontroller abzufragen. Mit Windows 7 und Windows Server 2008 R2 ab SP1 (oder Microsoft Knowledge Base 982018) wird diese Unterstützung auf Storport-basierte Speichercontroller erweitert. Microsoft hat auf MSDN ein [Codebeispiel](/windows/desktop/api/winioctl/ns-winioctl-storage_access_alignment_descriptor) bereitgestellt, in dem erläutert wird, wie eine App die physische Sektorgröße des Volumes abfragen kann.

Im obigen Codebeispiel können Sie zwar die Größe des physischen Sektor des Volumes abrufen, aber Sie sollten vor der Verwendung eine grundlegende Überprüfung der Gemeldeten physischen Sektorgröße durchführen, da festgestellt wurde, dass einige Treiber möglicherweise nicht ordnungsgemäß formatierte Daten zurückgeben:

-   Stellen Sie sicher, dass die gemeldete physische Sektorgröße >= die gemeldete größe des logischen Sektor ist. Andernfalls sollte Ihre App eine physische Sektorgröße verwenden, die der gemeldeten größe des logischen Sektor entspricht.
-   Stellen Sie sicher, dass die gemeldete physische Sektorgröße eine Potenz von zwei ist. Andernfalls sollte Ihre App eine physische Sektorgröße verwenden, die der gemeldeten größe des logischen Sektor entspricht.
-   Wenn die größe des physischen Sektor einen Wert von zwei Potenzen zwischen 512 Byte und 4 KB hat, sollten Sie erwägen, eine physische Sektorgröße zu verwenden, die auf die gemeldete logische Sektorgröße gerundet wird.
-   Wenn die Größe des physischen Sektor einen Wert von zwei Potenzen über 4 KB hat, sollten Sie die Fähigkeit Ihrer App auswerten, dieses Szenario zu verarbeiten, bevor Sie diesen Wert verwenden. Andernfalls sollten Sie erwägen, eine auf 4 KB aufgerundete physische Sektorgröße zu verwenden.

Die Verwendung dieser IOCTL zum Abrufen der physischen Sektorgröße hat mehrere Einschränkungen. Sie hat folgende Aufgaben:

-   Erfordert erhöhte Rechte. Wenn Ihre App nicht mit Berechtigungen ausgeführt wird, müssen Sie möglicherweise wie oben erwähnt eine Windows-Dienstanwendung schreiben.
-   Unterstützt keine SMB-Volumes. Möglicherweise müssen Sie auch eine Windows-Dienstanwendung schreiben, um Abfragen der physischen Sektorgröße für diese Volumes zu unterstützen.
-   Kann nicht für ein Dateihandle ausgegeben werden (die IOCTL muss für ein Volumehandle ausgegeben werden)

**Problem 3: Dateiformate, die auf 512-Byte-Sektoren basieren**

Bei einigen Apps mit Standarddateiformaten (z.B. VHD 1.0) sind diese Dateien möglicherweise hart codiert, um eine Sektorgröße von 512 Byte zu übernehmen. Daher führen Updates und Schreibvorgänge in dieser Datei zu einem Lese-/Änderungs-/Schreibzyklus auf dem Gerät, der möglicherweise zu Leistungs- und Resilienzproblemen für Ihre Kunden führt. Es gibt jedoch Möglichkeiten für eine App, unterstützung für den Betrieb auf dieser Art von Medien bereitzustellen, z. B.:

-   Verwenden Sie die Pufferung, um sicherzustellen, dass Schreibvorgänge in Einheiten der physischen Sektorgröße ausgeführt werden.
-   Implementieren Sie einen internen Lese-/Änderungs-/Schreibzugriff, mit dem sichergestellt werden kann, dass Updates in Einheiten der gemeldeten physischen Sektorgröße ausgeführt werden.
-   Auffüllen von Datensätzen in einem physischen Sektor nach Möglichkeit so, dass die Auffüllung als leerer Bereich interpretiert wird
-   Erwägen Sie das Umgestalten einer Version der App-Datenstruktur mit Unterstützung für größere Sektoren.

**Problem 4: Die gemeldete physische Sektorgröße kann sich zwischen sitzungen ändern.**

Es gibt viele Szenarien, in denen sich die gemeldete physische Sektorgröße des zugrunde liegenden Speichers, der den Datastor hostet, ändern kann. Die gängigste davon ist, wenn Sie den Datastor auf ein anderes Volume oder sogar über das Netzwerk migrieren. Eine Änderung der gemeldeten physischen Sektorgröße kann für viele Apps ein unerwartetes Ereignis sein und möglicherweise dazu führen, dass einige Apps nicht erneut initialisiert werden können.

Dies ist nicht das einfachste Szenario, das unterstützt werden kann, und wird hier als Empfehlung erwähnt. Sie sollten die Mobilitätsanforderungen Ihrer Kunden berücksichtigen und Ihren Support entsprechend anpassen, um sicherzustellen, dass Kunden nicht durch die Verwendung nativer 4K- oder 512e-Medien beeinträchtigt werden.

**Abrufen der logischen und physischen Sektorgröße für ein Volume durch einen Benutzer**

In-Box mit Windows ist ein Hilfsprogramm zum Anzeigen der Informationen zur Sektorgröße für ein Volume. Versionen von Windows mit unterstützten fsutil-Versionen sind:

-   Windows 8
-   Windows Server 2012
-   Windows 7 SP1 mit Microsoft KB-982018
-   Windows 7 mit Microsoft KB-982018
-   Windows Server 2008 R2 SP1 mit Microsoft KB 982018 (v3)
-   Windows Server 2008 R2 mit Microsoft KB 982018 (v3)
-   Windows Vista mit Microsoft KB 2553708
-   Windows Server 2008 mit Microsoft KB 2553708

Rufen Sie das Hilfsprogramm wie folgt an einer Eingabeaufforderung mit erhöhten Rechten auf, um informationen zur Sektorgröße abzurufen:


```
fsutil fsinfo ntfsinfo <drive letter>
```



Bei einem 4K-Sektordatenträger mit 512-Byte-Emulation ist das Feld Bytes pro Sektor auf 512 und das Feld Bytes pro physischem Sektor wie folgt auf 4096 festgelegt:

![Bytes pro Sektor und pro physischem Sektor eines 4K-Sektordatenträgers mit 512-Byte-Emulation](images/4ksectordiskwith512emulation.png)

Auf einem nativen 4K-Datenträger sind die Felder Bytes pro Sektor und Bytes pro physischem Sektor wie folgt auf 4096 festgelegt:

![Bytes pro Sektor und physischem Sektor eines nativen 4K-Datenträgers](images/4knativedisk.png)

> [!Note]  
> Wenn im Feld Byte pro physischem Sektor nicht unterstützt angezeigt wird, unterstützt der Speichertreiber IOCTL STORAGE QUERY PROPERTY nicht, oder es ist ein Fehler beim Abrufen der \_ \_ Informationen \_ aufgetreten.

 

## <a name="resources"></a>Ressourcen

-   [Windows Allgemeine Supportbestimmungen](https://support.microsoft.com/kb/2510009)
-   [Microsoft KB-982018](https://support.microsoft.com/kb/982018)
-   [Microsoft KB-2553708](https://support.microsoft.com/kb/2553708)
-   [Hotfix für Windows 7 und Windows Server 2008 R2](https://support.microsoft.com/kb/982018)
-   [Hotfix für Windows Vista und Windows Server 2008](https://support.microsoft.com/kb/2553708)
-   [HyperV-Support-Anweisung](https://support.microsoft.com/kb/2515143)
-   [Allgemeine Informationen zum IOCTL \_ STORAGE \_ QUERY \_ PROPERTY-Steuerungscode](/windows-hardware/drivers/ddi/ntddstor/ni-ntddstor-ioctl_storage_query_property)
-   [IOCTL \_ STORAGE \_ QUERY \_ PROPERTY Control Code](/windows/win32/api/winioctl/ni-winioctl-ioctl_storage_query_property)
-   [Allgemeine Informationen zur \_ \_ SPEICHERZUGRIFFSAUSRICHTUNGSDESCRIPTOR-Struktur \_](/windows-hardware/drivers/ddi/ntddstor/ns-ntddstor-_storage_access_alignment_descriptor)
-   [Beschreibung der Standardterminologie zur Beschreibung von Microsoft-Softwareupdates](https://support.microsoft.com/kb/824684/)
-   [WDK-Beispielcode mit Details zum Extrahieren der gemeldeten Informationen zur Speicherzugriffsausrichtung aus der STORAGE ACCESS ALIGNMENT DESCRIPTOR-Struktur beim Aufrufen des \_ \_ \_ IOCTL \_ STORAGE \_ QUERY PROPERTY-Steuerungscodes \_](/windows/win32/api/winioctl/ns-winioctl-storage_access_alignment_descriptor)
-   [Allgemeine Informationen zu ImageX Command-Line Optionen](/previous-versions/windows/it-pro/windows-7/dd799302(v=ws.10))
-   [Intel-Chipsatztreiberanforderungen zur Unterstützung von 4-KB-Sektorlaufwerken](https://www.intel.com/support/chipsets/imsm/sb/CS-031502.htm)

 

