---
description: Beschreibt zwei Datenträgerspeichertypen und erläutert Partitionsstile.
ms.assetid: 5d511654-92e0-4236-80e7-bb2417403186
title: Basisdatenträger und dynamische Datenträger
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f134f0dd7c8d81522733d26a6c5efb433d0e425978e1cbffd7edf3b0937b949
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119582629"
---
# <a name="basic-and-dynamic-disks"></a>Basisdatenträger und dynamische Datenträger

Bevor Sie ein Laufwerk partitionieren oder Informationen über das Partitionslayout eines Laufwerks abrufen, müssen Sie zunächst die Features und Einschränkungen von grundlegenden und dynamischen Datenträgerspeichertypen verstehen.

Für die Zwecke dieses Themas wird der Begriff *Volume* verwendet, um auf das Konzept einer Datenträgerpartition zu verweisen, die mit einem gültigen Dateisystem formatiert ist( am häufigsten NTFS), das vom Windows Betriebssystem zum Speichern von Dateien verwendet wird. Ein Volume hat einen Win32-Pfadnamen, kann von den Funktionen [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew) und [**FindNextVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew) aufzählen und verfügt in der Regel über einen Laufwerkbuchstaben, z.B. C:. Weitere Informationen zu Volumes und Dateisystemen finden Sie unter [Dateisysteme.](file-systems.md)

In diesem Thema:

-   [Basisdatenträger](#basic-disks)
-   [Dynamische Datenträger](#dynamic-disks)
-   [Partitionsstile](#partition-styles)
    -   [Master Boot Record](#master-boot-record)
    -   [GUID-Partitionstabelle](#guid-partition-table)
-   [Erkennen des Datenträgertyps](#detecting-the-type-of-disk)
-   [Zugehörige Themen](#related-topics)

Beim Verweisen auf Speichertypen in diesem Kontext gibt es zwei Arten von *Datenträgern: Basisdatenträger* und *dynamische Datenträger.* Beachten Sie, dass die hier beschriebenen Speichertypen nicht mit physischen Datenträgern oder Partitionsstilen identisch sind, bei denen es sich um verwandte, aber separate Konzepte handelt. Beispielsweise impliziert der Verweis auf einen Basisdatenträger keinen bestimmten Partitionsstil. Der Partitionsstil, der für den datenträger in der Diskussion verwendet wird, muss ebenfalls angegeben werden. Eine vereinfachte Beschreibung der Beziehung eines grundlegenden Datenträgerspeichertyps zu einer physischen Festplatte finden Sie unter [Datenträgergeräte und Partitionen.](disk-devices-and-partitions.md)

## <a name="basic-disks"></a>Basisdatenträger

*Basisdatenträger* sind die Speichertypen, die am häufigsten mit Windows verwendet werden. Der Begriff *Basisdatenträger* bezieht sich auf einen Datenträger, der Partitionen enthält, z. B. primäre Partitionen und logische Laufwerke, und diese wiederum werden in der Regel mit einem Dateisystem formatiert, um ein Volume für den Dateispeicher zu werden. Basisdatenträger bieten eine einfache Speicherlösung, die ein nützliches Array von Szenarien mit sich ändernden Speicheranforderungen aufnehmen kann. Basic-Datenträger unterstützen auch Clusterdatenträger, IEEE 1394-Datenträger (Institute of Electrical and Electronics Engineers) und USB-Wechseldatenträger (Universal Serial Bus). Aus Gründen der Abwärtskompatibilität verwenden Basisdatenträger in der Regel den gleichen Master Boot Record (MBR)-Partitionsstil wie die Datenträger, die vom Microsoft MS-DOS-Betriebssystem und allen Versionen von Windows verwendet werden, können aber auch GPT-Partitionen **(GUID** Partition Table) auf Systemen unterstützen, die dies unterstützen. Weitere Informationen zu MBR- und GPT-Partitionsstilen finden Sie im Abschnitt [Partitionsstile.](#partition-styles)

Sie können vorhandenen primären Partitionen und logischen Laufwerken mehr Platz hinzufügen, indem sie diese auf den angrenzenden, zusammenhängenden und nicht zugewiesenen Speicherplatz auf dem gleichen Datenträger erweitern. Um ein Basisvolume zu erweitern, muss es mit dem NTFS-Dateisystem formatiert sein. Ein logisches Laufwerk kann innerhalb des zusammenhängenden freien Speicherplatzes in der erweiterten Partition erweitert werden, die es enthält. Wenn Sie ein logisches Laufwerk über den in der erweiterten Partition verfügbaren freien Speicherplatz hinaus erweitern, erhöht die erweiterte Partition die Größe, um das logische Laufwerk zu beinhalten, solange sich an die erweiterte Partition zusammenhängender, nicht zugewiesener Speicherplatz anschließt. Weitere Informationen finden Sie unter [Funktionsweise von Basisdatenträgern und Volumes.](/previous-versions/windows/it-pro/windows-server-2003/cc739412(v=ws.10))

Die folgenden Vorgänge können nur auf Basisdatenträgern ausgeführt werden:

-   Erstellen und Löschen von primären und erweiterten Partitionen.
-   Erstellen und Löschen logischer Laufwerke innerhalb einer erweiterten Partition
-   Formatieren Sie eine Partition, und markieren Sie sie als aktiv.

## <a name="dynamic-disks"></a>Dynamische Datenträger

> [!NOTE]
> Für alle Verwendungen mit Ausnahme von Spiegelstartvolumes (mit einem Spiegelvolume zum Hosten des Betriebssystems) sind dynamische Datenträger veraltet. Verwenden Sie für Daten, die Resilienz bei Laufwerkausfällen erfordern, Speicherplätze, eine robuste Speichervirtualisierungslösung. Weitere Informationen finden Sie unter [Speicherplätze Übersicht.](/windows-server/storage/storage-spaces/overview)

*Dynamische Datenträger* bieten Features, die grundlegende Datenträger nicht bieten, z. B. die Möglichkeit, Volumes zu erstellen, die mehrere Datenträger (übergreifend und Stripesetvolumes) umfassen, und die Möglichkeit, fehlertolerante Volumes (gespiegelte volumes und RAID-5-Volumes) zu erstellen. Wie Basisdatenträger können dynamische Datenträger die MBR- oder GPT-Partitionsstile auf Systemen verwenden, die beide unterstützen. Alle Volumes auf dynamischen Datenträgern werden als dynamische Volumes bezeichnet. Dynamische Datenträger bieten mehr Flexibilität für die Volumeverwaltung, da sie eine Datenbank verwenden, um Informationen zu dynamischen Volumes auf dem Datenträger und zu anderen dynamischen Datenträgern auf dem Computer nachzuverfolgen. Da jeder dynamische Datenträger auf einem Computer beispielsweise ein Replikat der Dynamischen Datenträgerdatenbank speichert, kann eine beschädigte Datenbank für dynamische Datenträger einen dynamischen Datenträger reparieren, indem die Datenbank auf einem anderen dynamischen Datenträger verwendet wird. Der Speicherort der Datenbank wird durch den Partitionsstil des Datenträgers bestimmt. Auf MBR-Partitionen ist die Datenbank in den letzten 1 Megabyte (MB) des Datenträgers enthalten. Auf GPT-Partitionen ist die Datenbank in einer reservierten (ausgeblendeten) Partition mit 1 MB enthalten.

Dynamische Datenträger sind eine separate Form der Volumeverwaltung, die es Volumes ermöglicht, nicht zusammenhängende Erweiterungen auf einem oder mehreren physischen Datenträgern zu haben. Dynamische Datenträger und Volumes basieren auf dem Logical Disk Manager (LDM) und Virtual Disk Service (VDS) und den zugehörigen Features. Mit diesen Features können Sie Aufgaben wie das Konvertieren von Basisdatenträgern in dynamische Datenträger und das Erstellen fehlertoleranter Volumes ausführen. Um die Verwendung dynamischer Datenträger zu fördern, wurde die Volumeunterstützung mit mehreren Partitionen von den Basisdatenträgern entfernt und wird jetzt ausschließlich auf dynamischen Datenträgern unterstützt.

Die folgenden Vorgänge können nur auf dynamischen Datenträgern ausgeführt werden:

-   Erstellen und löschen Sie einfache Volumes, übergreifende Volumes, Stripesetvolumes, gespiegelte Volumes und RAID-5-Volumes.
-   Erweitern sie ein einfaches volume oder ein übergreifendes Volume.
-   Entfernen Sie einen Spiegel von einem gespiegelten Volume, oder unterlegen Sie das gespiegelte Volume in zwei Volumes.
-   Reparieren gespiegelter Volumes oder RAID-5-Volumes.
-   Reaktivieren sie einen fehlenden oder Offlinedatenträger.

Ein weiterer Unterschied zwischen basisigen und dynamischen Datenträgern besteht darin, dass dynamische Datenträgervolumes aus einer Reihe von nicht zusammenhängenden Erweiterungen auf einem oder mehreren physischen Datenträgern bestehen können. Im Gegensatz dazu besteht ein Volume auf einem Basisdatenträger aus einem Satz zusammenhängender Erweiterungen auf einem einzelnen Datenträger. Aufgrund des Speicherorts und der Größe des Speicherplatzes, der von der LDM-Datenbank benötigt wird, können Windows einen Basisdatenträger nicht in einen dynamischen Datenträger konvertieren, es sei denn, es ist mindestens 1 MB ungenutzter Speicherplatz auf dem Datenträger vorhanden.

Unabhängig davon, ob die dynamischen Datenträger auf einem System den MBR- oder GPT-Partitionsstil verwenden, können Sie bis zu 2.000 dynamische Volumes auf einem System erstellen, obwohl die empfohlene Anzahl dynamischer Volumes 32 oder weniger beträgt. Ausführliche Informationen und andere Überlegungen zur Verwendung dynamischer Datenträger und Volumes finden Sie unter [Dynamische Datenträger und Volumes.](/previous-versions/windows/it-pro/windows-server-2003/cc757696(v=ws.10))

Weitere Features von und Verwendungsszenarien für dynamische Datenträger finden Sie unter [Was sind dynamische Datenträger und Volumes?](/previous-versions/windows/it-pro/windows-server-2003/cc737048(v=ws.10)).

Grundlegende und dynamische Datenträger haben folgende Vorgänge:

-   Unterstützt sowohl MBR- als auch GPT-Partitionsstile.
-   Überprüfen Sie die Datenträgereigenschaften, z. B. Kapazität, verfügbaren freien Speicherplatz und aktuellen Status.
-   Zeigen Sie Partitionseigenschaften wie Offset, Länge, Typ und an, ob die Partition beim Start als Systemvolume verwendet werden kann.
-   Anzeigen von Volumeeigenschaften, z. B. Größe, Laufwerkbuchstabenzuweisung, Bezeichnung, Typ, Win32-Pfadname, Partitionstyp und Dateisystem.
-   Richten Sie Laufwerkbuchstabenzuweisungen für Datenträgervolumes oder Partitionen sowie für CD-ROM-Geräte ein.
-   Konvertieren eines Basisdatenträgers in einen dynamischen Datenträger oder eines dynamischen Datenträgers in einen Basisdatenträger.

Sofern nicht anders angegeben, partitioniert Windows ein Laufwerk standardmäßig als Basisdatenträger. Sie müssen einen Basisdatenträger explizit in einen dynamischen Datenträger konvertieren. Es gibt jedoch Überlegungen zum Speicherplatz, die berücksichtigt werden müssen, bevor Sie dies versuchen. Weitere Informationen finden Sie unter [How To Convert to Basic and Dynamic Disks in Windows XP Professional](https://support.microsoft.com/kb/309044).

## <a name="partition-styles"></a>Partitionsstile

*Partitionsstile*, auch als *Partitionsschemas* bezeichnet, sind ein Begriff, der sich auf die spezifische zugrunde liegende Struktur des Datenträgerlayouts bezieht und wie die Partitionierung tatsächlich angeordnet wird, was die Funktionen sind und welche Einschränkungen gelten. Zum Starten Windows benötigen die BIOS-Implementierungen auf x86- und x64-basierten Computern einen Basisdatenträger, der mindestens eine MBR-Partition (Master Boot Record) enthalten muss, die als aktiv markiert ist, wobei Informationen zum Windows Betriebssystem (aber nicht notwendigerweise die gesamte Betriebssysteminstallation) und wo Informationen zu den Partitionen auf dem Datenträger gespeichert werden. Diese Informationen werden an separaten Stellen platziert, und diese beiden Stellen können sich in separaten Partitionen oder in einer einzelnen Partition befinden. Alle anderen physischen Datenträgerspeicher können als verschiedene Kombinationen der beiden verfügbaren Partitionsstile eingerichtet werden, die in den folgenden Abschnitten beschrieben werden. Weitere Informationen zu anderen Systemtypen finden Sie im TechNet-Thema zu [Partitionsstilen.](/previous-versions/windows/it-pro/windows-server-2003/cc738081(v=ws.10))

Dynamische Datenträger folgen etwas unterschiedlichen Verwendungsszenarien, wie zuvor beschrieben, und die Art und Weise, wie sie die beiden Partitionsstile verwenden, wird von dieser Verwendung beeinflusst. Da dynamische Datenträger im Allgemeinen nicht verwendet werden, um Systemstartvolumes zu enthalten, wird diese Erläuterung vereinfacht, um Sonderszenarien auszuschließen. Ausführlichere Informationen zu Partitionsdatenblocklayouts und grundlegenden oder dynamischen Datenträgerverwendungsszenarien im Zusammenhang mit Partitionsstilen finden Sie unter [Funktionsweise von Basisdatenträgern und Volumes](/previous-versions/windows/it-pro/windows-server-2003/cc739412(v=ws.10)) und Funktionsweise dynamischer Datenträger und [Volumes.](/previous-versions/windows/it-pro/windows-server-2003/cc758035(v=ws.10))

### <a name="master-boot-record"></a>Master Boot Record

Alle x86- und x64-basierten Computer, auf denen Windows ausgeführt wird, können den Partitionsstil verwenden, der als *Master Boot Record* (MBR) bezeichnet wird. Der MBR-Partitionsstil enthält eine Partitionstabelle, die beschreibt, wo sich die Partitionen auf dem Datenträger befinden. Da MBR das einzige Partitionsformat ist, das auf x86-basierten Computern vor Windows Server 2003 mit Service Pack 1 (SP1) verfügbar ist, müssen Sie diesen Stil nicht auswählen. Sie wird automatisch verwendet.

Sie können bis zu vier Partitionen auf einem Basisdatenträger mithilfe des MBR-Partitionsschemas erstellen: entweder vier primäre Partitionen oder drei primäre und eine erweiterte Partition. Die erweiterte Partition kann ein oder mehrere logische Laufwerke enthalten. Die folgende Abbildung veranschaulicht ein Beispiellayout von drei primären Partitionen und einer erweiterten Partition auf einem Basisdatenträger mit MBR. Die erweiterte Partition enthält vier erweiterte logische Laufwerke darin. Die erweiterte Partition kann sich am Ende des Datenträgers befinden oder nicht, aber sie ist immer ein einzelner zusammenhängender Speicherplatz für logische Laufwerke 1-n.

![drei primäre Partitionen und eine erweiterte Partition auf einem Basisdatenträger mit mbr](images/basic-mbr.png)

Jede Partition ( primär oder erweitert) kann als Windows Volume mit einer 1:1-Korrelation von Volume zu Partition formatiert werden. Anders ausgedrückt: Eine einzelne Partition darf nicht mehr als ein einzelnes Volume enthalten. In diesem Beispiel stehen insgesamt sieben Volumes für Windows für den Dateispeicher zur Verfügung. Eine nicht formatierte Partition ist für die Dateispeicherung in Windows nicht verfügbar.

Das MBR-Layout für dynamische Datenträger ähnelt dem MBR-Layout des Basisdatenträgers, mit der Ausnahme, dass nur eine primäre Partition zulässig ist (als LDM-Partition bezeichnet), keine erweiterte Partitionierung zulässig ist und am Ende des Datenträgers eine ausgeblendete Partition für die LDM-Datenbank vorhanden ist. Weitere Informationen zum LDM finden Sie im Abschnitt [Dynamische Datenträger.](#basic-and-dynamic-disks)

### <a name="guid-partition-table"></a>GUID-Partitionstabelle

Systeme, auf denen Windows Server 2003 mit SP1 und höher ausgeführt wird, können zusätzlich zum MBR-Partitionsstil einen Partitionsstil verwenden, der als global eindeutiger Bezeichner **(GUID)** partition table (GPT) bezeichnet wird. Ein Basisdatenträger, der den GPT-Partitionsstil verwendet, kann bis zu 128 primäre Partitionen enthalten, während dynamische Datenträger wie bei der MBR-Partitionierung über eine einzelne LDM-Partition verfügen. Da Basisdatenträger mit GPT-Partitionierung Sie nicht auf vier Partitionen beschränken, müssen Sie keine erweiterten Partitionen oder logischen Laufwerke erstellen.

Der GPT-Partitionsstil verfügt auch über die folgenden Eigenschaften:

-   Ermöglicht Partitionen, die größer als 2 Terabyte sind.
-   Zuverlässigkeit durch Replikation und crC-Schutz (cyclic redundancy check) der Partitionstabelle wurde hinzugefügt.
-   Unterstützung für zusätzliche **Partitionstyp-GUIDs,** die von Originalgeräteherstellern (OEMs), unabhängigen Softwareherstellern (INDEPENDENT Software Vendors, ISVs) und anderen Betriebssystemen definiert werden.

Das GPT-Partitionierungslayout für einen Basisdatenträger ist in der folgenden Abbildung dargestellt.

![GPT-Layout](images/basic-gpt.png)

Der mbr-Schutzbereich ist in einem GPT-Partitionslayout vorhanden, um Abwärtskompatibilität mit Datenträgerverwaltungs-Hilfsprogrammen zu gewährleisten, die mit MBR arbeiten. Der GPT-Header definiert den Bereich logischer Blockadressen, die von Partitionseinträgen verwendet werden können. Der GPT-Header definiert auch seinen Speicherort auf dem Datenträger, die **GUID** und eine CRC32-Prüfsumme (32-Bit cyclic redundancy check), mit der die Integrität des GPT-Headers überprüft wird. Jeder **GUID-Partitionseintrag** beginnt mit einer Partitionstyp-GUID. Die 16-Byte-Partitionstyp-GUID, die einer System-ID in der Partitionstabelle eines MBR-Datenträgers ähnelt, identifiziert den Typ der Daten, die die Partition enthält, und gibt an, wie die Partition verwendet wird, z. B. wenn es sich um einen Basisdatenträger oder einen dynamischen Datenträger handelt.  Beachten Sie, dass **jeder GUID-Partitionseintrag** über eine Sicherungskopie verfügt.

Dynamische **GPT-Partitionslayouts** für Datenträger ähneln diesem einfachen Datenträgerbeispiel, verfügen jedoch wie bereits erwähnt nur über einen LDM-Partitionseintrag anstelle von 1-n primären Partitionen, wie auf Basisdatenträgern zulässig. Es gibt auch eine ausgeblendete LDM-Datenbankpartition mit einem entsprechenden **GUID-Partitionseintrag** dafür. Weitere Informationen zur LDM finden Sie im Abschnitt [Dynamische Datenträger.](#basic-and-dynamic-disks)

## <a name="detecting-the-type-of-disk"></a>Erkennen des Datenträgertyps

Es gibt keine bestimmte Funktion zum programmgesteuerten Erkennen des Datenträgertyps, auf dem sich eine bestimmte Datei oder ein bestimmtes Verzeichnis befindet. Es gibt eine indirekte Methode.

* Übergeben Sie den Datei- oder Verzeichnispfad [**an GetVolumePathName,**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumepathnamew) um den Bereitstellungspunkt zu erhalten.
* Übergeben Sie den Bereitstellungspunkt [**an GetVolumeNameForVolumeMountPoint,**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) um den Volumenamen zu erhalten.
* Entfernen Sie den nachdenkenden schrägen Schrägstrich aus dem Volumenamen.
* Übergeben Sie den Volumenamen ohne den hinteren schrägen Schrägstrich an [**CreateFile,**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) um das Volume zu öffnen.
* Verwenden [**Sie IOCTL \_ VOLUME GET VOLUME DISK \_ \_ \_ \_ EXTENTS**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_volume_get_volume_disk_extents) mit dem Volumehandles, um die Datenträgernummern zu erhalten.
* Verwenden Sie die Datenträgernummern, um die Datenträgerpfade zu erstellen, z. B. " \\ \\ ? \\ PhysicalDrive *X*".
* Übergeben Sie jeden Datenträgerpfad an [**CreateFile,**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) um den Datenträger zu öffnen.
* Verwenden [**Sie IOCTL \_ DISK GET DRIVE LAYOUT \_ \_ \_ \_ EX,**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_disk_get_drive_layout_ex) um die Partitionsliste zu erhalten.
* Überprüfen Sie **partitionType** für jeden Eintrag in der Partitionsliste.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zur Volumeverwaltung](about-volume-management.md)
</dt> <dt>

[Basic Disks and Volumes Technical Reference](/previous-versions/windows/it-pro/windows-server-2003/cc784732(v=ws.10))
</dt> <dt>

[Dynamic Disks and Volumes Technical Reference](/previous-versions/windows/it-pro/windows-server-2003/cc785638(v=ws.10))
</dt> <dt>

[Grundlegende Storage im Vergleich zu dynamischen Storage in Windows XP]( https://support.microsoft.com/kb/314343/)
</dt> </dl>

 

 
