---
description: Beschreibt zwei Datenträger-Speichertypen und erläutert Partitions Stile.
ms.assetid: 5d511654-92e0-4236-80e7-bb2417403186
title: Basis-und dynamische Datenträger
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd3b52767983c7707f619b83c93e987b51879fdd
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "103961232"
---
# <a name="basic-and-dynamic-disks"></a>Basis-und dynamische Datenträger

Vor dem Partitionieren eines Laufwerks oder dem erhalten von Informationen zum Partitionslayout eines Laufwerks müssen Sie zunächst die Features und Einschränkungen der grundlegenden und dynamischen Datenträger Speichertypen verstehen.

Im Rahmen dieses Themas wird der Begriff *Volume* verwendet, um auf das Konzept einer Datenträger Partition zu verweisen, die mit einem gültigen Dateisystem formatiert ist (am häufigsten NTFS), das vom Windows-Betriebssystem zum Speichern von Dateien verwendet wird. Ein Volume weist einen Win32-Pfadnamen auf, kann durch die Funktionen " [**findfirstvolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew) " und " [**findnextvolume**](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew) " aufgezählt werden, und es wird normalerweise ein Laufwerksbuchstabe zugewiesen, z. b. "c:". Weitere Informationen zu Volumes und Dateisystemen finden Sie unter [Dateisysteme](file-systems.md).

In diesem Thema:

-   [Grundlegende Datenträger](#basic-disks)
-   [Dynamische Datenträger](#dynamic-disks)
-   [Partitions Stile](#partition-styles)
    -   [Master Boot Record](#master-boot-record)
    -   [GUID-Partitionstabelle](#guid-partition-table)
-   [Erkennen der Art des Datenträgers](#detecting-the-type-of-disk)
-   [Zugehörige Themen](#related-topics)

Beim Verweisen auf Speichertypen in diesem Kontext gibt es zwei Arten von Datenträgern: *Basis* Datenträger und *dynamische* Datenträger. Beachten Sie, dass die hier erläuterten Speichertypen nicht mit physischen Datenträgern oder Partitions Formaten identisch sind, die miteinander verknüpft sind, aber separate Konzepte haben. Beispielsweise impliziert das verweisen auf einen Basis Datenträger keinen bestimmten Partitions Stil – der für den Datenträger in der Diskussion verwendete Partitions Stil muss ebenfalls angegeben werden. Eine vereinfachte Beschreibung der Beziehung zwischen einem einfachen Datenträger Speichertyp und einer physischen Festplatte finden Sie unter Datenträger [Geräte und Partitionen](disk-devices-and-partitions.md).

## <a name="basic-disks"></a>Grundlegende Datenträger

*Basis* Datenträger sind die Speichertypen, die am häufigsten mit Windows verwendet werden. Der Begriff " *Basis* Datenträger" bezieht sich auf einen Datenträger, der Partitionen (z. b. primäre Partitionen und logische Laufwerke) enthält. Diese werden normalerweise mit einem Dateisystem formatiert, um ein Volume für den Dateispeicher zu werden Basis Datenträger stellen eine einfache Speicherlösung dar, die ein nützliches Array von veränderlichen Szenarien für Speicheranforderungen bereitstellen kann. Basis Datenträger unterstützen auch Cluster Datenträger, IEEE (Institute of Electrical and Electronics Engineers) 1394-Datenträger und USB-Wechsel Datenträger. Aus Gründen der Abwärtskompatibilität verwenden Basis Datenträger normalerweise denselben MBR-Partitions Stil (Master Boot Record) wie die vom MS-DOS-Betriebssystem verwendeten Datenträger und alle Versionen von Windows, können aber auch GPT-Partitionen ( **GUID** -Partitionstabelle) auf Systemen unterstützen, die diese unterstützen. Weitere Informationen zu MBR-und GPT-Partitions Stilen finden Sie im Abschnitt [Partitions Stile](#partition-styles) .

Sie können vorhandenen primären Partitionen und logischen Laufwerken mehr Platz hinzufügen, indem sie diese auf den angrenzenden, zusammenhängenden und nicht zugewiesenen Speicherplatz auf dem gleichen Datenträger erweitern. Um ein Basisvolume zu erweitern, muss es mit dem NTFS-Dateisystem formatiert sein. Ein logisches Laufwerk kann innerhalb des zusammenhängenden freien Speicherplatzes in der erweiterten Partition erweitert werden, die es enthält. Wenn Sie ein logisches Laufwerk über den in der erweiterten Partition verfügbaren freien Speicherplatz hinaus erweitern, erhöht die erweiterte Partition die Größe, um das logische Laufwerk zu beinhalten, solange sich an die erweiterte Partition zusammenhängender, nicht zugewiesener Speicherplatz anschließt. Weitere Informationen finden Sie unter [Funktionsweise von Basis](/previous-versions/windows/it-pro/windows-server-2003/cc739412(v=ws.10))Datenträgern und Volumes.

Die folgenden Vorgänge können nur auf Basis Datenträgern ausgeführt werden:

-   Erstellen und löschen primärer und erweiterter Partitionen.
-   Erstellen und Löschen von logischen Laufwerken innerhalb einer erweiterten Partition.
-   Formatieren Sie eine Partition, und markieren Sie Sie als aktiv.

## <a name="dynamic-disks"></a>Dynamische Datenträger

> [!NOTE]
> Für alle Verwendungen mit Ausnahme von Spiegelungs Start Volumes (mit einem Spiegelungs Volume zum Hosten des Betriebssystems) sind dynamische Datenträger veraltet. Verwenden Sie für Daten, die Resilienz vor Laufwerks Fehlern erfordern, Speicherplätze, eine robuste Lösung für die Speichervirtualisierung. Weitere Informationen finden Sie unter [Übersicht über Speicherplätze](/windows-server/storage/storage-spaces/overview).

*Dynamische* Datenträger bieten Funktionen, die für Basis Datenträger nicht gelten, wie z. b. die Möglichkeit zum Erstellen von Volumes, die mehrere Datenträger umfassen (übergreifende Volumes und Stripesetvolumes), sowie die Möglichkeit, fehlertolerante Volumes zu erstellen (gespiegelte und RAID Ebenso wie Basis Datenträger können dynamische Datenträger die MBR-oder GPT-Partitions Stile auf Systemen verwenden, die beide unterstützen. Alle Volumes auf dynamischen Datenträgern werden als dynamische Volumes bezeichnet. Dynamische Datenträger bieten mehr Flexibilität bei der Volumeverwaltung, da Sie eine Datenbank zum Nachverfolgen von Informationen zu dynamischen Volumes auf dem Datenträger und zu anderen dynamischen Datenträgern auf dem Computer verwenden. Da jeder dynamische Datenträger auf einem Computer ein Replikat der Datenbank für dynamische Datenträger speichert, kann beispielsweise eine beschädigte dynamische Datenträger Datenbank einen dynamischen Datenträger reparieren, indem er die Datenbank auf einem anderen dynamischen Datenträger verwendet. Der Speicherort der Datenbank wird durch den Partitions Stil des Datenträgers bestimmt. Bei MBR-Partitionen ist die Datenbank in den letzten 1 Megabyte (MB) des Datenträgers enthalten. Bei GPT-Partitionen ist die Datenbank in einer reservierten (verborgenen) 1-MB-Partition enthalten.

Dynamische Datenträger sind eine separate Form der Volumeverwaltung, mit der Volumes auf einem oder mehreren physischen Datenträgern nicht zusammenhängende Blöcke aufweisen können. Dynamische Datenträger und Volumes basieren auf dem LDM (Logical Disk Manager) und den virtuellen Datenträger Diensten (Virtual Disk Service, VDS) und den zugehörigen Features. Diese Funktionen ermöglichen Ihnen das Ausführen von Aufgaben wie z. b. das Umstellen von Basis Datenträgern in dynamische Datenträger und das Erstellen von fehlertoleranten Um die Verwendung dynamischer Datenträger zu fördern, wurde die Volumen Unterstützung für mehrere Partitionen von Basis Datenträgern entfernt und wird jetzt exklusiv auf dynamischen Datenträgern unterstützt.

Die folgenden Vorgänge können nur auf dynamischen Datenträgern ausgeführt werden:

-   Erstellen und löschen Sie einfache, übergreifende, Stripesets, gespiegelte und RAID-5-Volumes.
-   Erweitern Sie ein einfaches oder übergreifendes Volume.
-   Entfernen Sie eine Spiegelung von einem gespiegelten Volume, oder unterbrechen Sie das gespiegelte Volume in zwei Volumes.
-   Reparieren von gespiegelten oder RAID-5-Volumes.
-   Reaktivieren Sie einen fehlenden oder Offline Datenträger.

Ein weiterer Unterschied zwischen Basis Datenträgern und dynamischen Datenträgern besteht darin, dass dynamische Datenträgervolumes aus einer Reihe nicht zusammenhängender Blöcke auf einem oder mehreren physischen Datenträgern bestehen können. Im Gegensatz dazu besteht ein Volume auf einem Basis Datenträger aus einem Satz zusammenhängender Blöcke auf einem einzelnen Datenträger. Aufgrund der Position und Größe des Speicherplatzes, der von der LDM-Datenbank benötigt wird, kann Windows einen Basis Datenträger nur dann in einen dynamischen Datenträger konvertieren, wenn mindestens 1 MB nicht verwendeter Speicherplatz auf dem Datenträger vorhanden ist.

Unabhängig davon, ob die dynamischen Datenträger in einem System das MBR-oder GPT-Partitionsformat verwenden, können Sie bis zu 2.000 dynamische Volumes auf einem System erstellen, obwohl die empfohlene Anzahl dynamischer Volumes 32 oder weniger beträgt. Weitere Informationen und weitere Überlegungen zur Verwendung dynamischer Datenträger und Volumes finden Sie unter dynamische Datenträger [und Volumes](/previous-versions/windows/it-pro/windows-server-2003/cc757696(v=ws.10)).

Weitere Funktionen von und Verwendungs Szenarien für dynamische Datenträger finden Sie unter [Was sind dynamische Datenträger und Volumes?](/previous-versions/windows/it-pro/windows-server-2003/cc737048(v=ws.10)).

Die folgenden Vorgänge sind für Basic-und dynamische Datenträger üblich:

-   Unterstützung von MBR-und GPT-Partitions Stilen.
-   Überprüfen Sie die Datenträger Eigenschaften, z. b. Kapazität, verfügbarer freier Speicherplatz und aktueller Status.
-   Anzeigen von Partitions Eigenschaften, z. b. Offset, Länge, Typ und, wenn die Partition beim Start als System Volume verwendet werden kann.
-   Anzeigen von Volumeeigenschaften, z. b. Größe, Laufwerk Buchstaben Zuweisung, Bezeichnung, Typ, Win32-Pfadname, Partitionstyp und Dateisystem.
-   Richten Sie Laufwerk Buchstaben Zuweisungen für Datenträgervolumes oder Partitionen und für CD-ROM-Geräte ein.
-   Konvertieren eines Basis Datenträgers in einen dynamischen Datenträger oder einen dynamischen Datenträger in einen Basis Datenträger.

Sofern nicht anders angegeben, partitioniert Windows zunächst ein Laufwerk standardmäßig als Basis Datenträger. Sie müssen einen Basis Datenträger explizit in einen dynamischen Datenträger konvertieren. Es müssen jedoch Speicherplatz Überlegungen beachtet werden, die berücksichtigt werden müssen, bevor Sie versuchen, dies zu tun. Weitere Informationen finden Sie unter [Konvertieren in einfache und dynamische Datenträger in Windows XP Professional](https://support.microsoft.com/kb/309044).

## <a name="partition-styles"></a>Partitions Stile

*Partitions Stile*, auch mitunter als *Partitions Schemas* bezeichnet, sind ein Begriff, der sich auf die jeweilige zugrunde liegende Struktur des Datenträger Layouts bezieht, und wie die Partitionierung tatsächlich angeordnet ist, welche Funktionen es gibt und welche Einschränkungen es gibt. Zum Starten von Fenstern benötigen die BIOS-Implementierungen in x86-basierten und x64-basierten Computern einen Basis Datenträger, der mindestens eine Master Boot Record MBR-Partition () enthalten muss, die als aktiv gekennzeichnet ist und Informationen zum Windows-Betriebssystem (aber nicht unbedingt zur gesamten Betriebssystem Installation) und zum Speicherort von Informationen zu den Partitionen auf dem Datenträger enthält. Diese Informationen werden an separaten Stellen platziert, und diese beiden Orte können sich in separaten Partitionen oder in einer einzelnen Partition befinden. Alle anderen physischen Datenträger Speicher können als verschiedene Kombinationen der beiden verfügbaren Partitions Stile eingerichtet werden, die in den folgenden Abschnitten beschrieben werden. Weitere Informationen zu anderen Systemtypen finden Sie im TechNet-Thema zu [Partitions Stilen](/previous-versions/windows/it-pro/windows-server-2003/cc738081(v=ws.10)).

Dynamische Datenträger folgen etwas anderen Verwendungs Szenarien, wie zuvor beschrieben, und die Art und Weise, wie Sie die beiden Partitions Stile verwenden, ist von dieser Verwendung betroffen. Da dynamische Datenträger in der Regel nicht für systemstartvolumes verwendet werden, wird diese Erörterung vereinfacht, um spezielle Szenarien auszuschließen. Ausführlichere Informationen zu Partitions Datenblock Layouts und grundlegenden oder dynamischen Datenträger Verwendungs Szenarien im Zusammenhang mit Partitions Formaten finden Sie unter [Funktionsweise von grundlegenden Datenträgern und Volumes](/previous-versions/windows/it-pro/windows-server-2003/cc739412(v=ws.10)) und [Funktionsweise dynamischer Datenträger und Volumes](/previous-versions/windows/it-pro/windows-server-2003/cc758035(v=ws.10)).

### <a name="master-boot-record"></a>Master Boot Record

Alle x86-und x64-basierten Computer, auf denen Windows ausgeführt wird, können den als *Master Boot Record* (MBR) bezeichneten Partitions Stil verwenden. Der MBR-Partitions Stil enthält eine Partitionstabelle, in der beschrieben wird, wo sich die Partitionen auf dem Datenträger befinden. Da MBR der einzige Partitions Stil ist, der auf x86-basierten Computern vor Windows Server 2003 mit Service Pack 1 (SP1) verfügbar ist, müssen Sie diesen Stil nicht auswählen. Sie wird automatisch verwendet.

Sie können bis zu vier Partitionen auf einem Basis Datenträger mithilfe des MBR-Partitions Schemas erstellen: entweder vier primäre Partitionen oder drei primäre Partitionen und eine erweiterte. Die erweiterte Partition kann ein oder mehrere logische Laufwerke enthalten. In der folgenden Abbildung wird ein Beispiel Layout für drei primäre Partitionen und eine erweiterte Partition auf einem Basis Datenträger mithilfe von MBR veranschaulicht. Die erweiterte Partition enthält vier erweiterte logische Laufwerke darin. Die erweiterte Partition befindet sich möglicherweise am Ende des Datenträgers, ist jedoch immer ein einzelner zusammenhängender Speicherplatz für logische Laufwerke 1-n.

![drei primäre Partitionen und eine erweiterte Partition auf einem Basis Datenträger mit MBR](images/basic-mbr.png)

Jede Partition, egal ob primär oder erweitert, kann als Windows-Volume mit einer eins-zu-Eins-Korrelation von Volume zu Partition formatiert werden. Anders ausgedrückt: eine einzelne Partition darf nicht mehr als ein einzelnes Volume enthalten. In diesem Beispiel gibt es insgesamt sieben Volumes, die für die Dateispeicherung für Windows verfügbar sind. Eine nicht formatierte Partition ist für den Dateispeicher in Windows nicht verfügbar.

Das Dynamic Disk MBR-Layout ähnelt dem grundlegenden Disk MBR-Layout, mit dem Unterschied, dass nur eine primäre Partition zulässig ist (als LDM-Partition bezeichnet), keine Erweiterte Partitionierung zulässig ist und am Ende des Datenträgers eine versteckte Partition für die LDM-Datenbank vorhanden ist. Weitere Informationen zum LDM finden Sie im Abschnitt [dynamische](#basic-and-dynamic-disks) Datenträger.

### <a name="guid-partition-table"></a>GUID-Partitionstabelle

Systeme, auf denen Windows Server 2003 mit SP1 und höher ausgeführt wird, können zusätzlich zum MBR-Partitions Stil einen Partitions Stil verwenden, der als Globally Unique Identifier (**GUID**)-Partitionstabelle (GPT) bezeichnet wird. Ein Basis Datenträger mit dem GPT-Partitions Stil kann bis zu 128 primäre Partitionen aufweisen, während dynamische Datenträger über eine einzelne LDM-Partition verfügen, wie bei der MBR-Partitionierung. Da Basis Datenträger mit GPT-Partitionierung nicht auf vier Partitionen beschränkt sind, müssen Sie keine erweiterten Partitionen oder logischen Laufwerke erstellen.

Der GPT-Partitions Stil verfügt auch über die folgenden Eigenschaften:

-   Ermöglicht Partitionen, die größer als 2 Terabyte sind.
-   Hinzugefügte Zuverlässigkeit der Replikation und des CRC-Schutzes (zyklische Redundanz Überprüfung) der Partitionstabelle.
-   Unterstützung für zusätzliche **GUID** s des Partitions Typs, die von Originalgeräte Herstellern (OEMs), unabhängigen Softwareanbietern (ISVs) und anderen Betriebssystemen definiert werden.

Das GPT-Partitionierungs Layout für einen Basis Datenträger wird in der folgenden Abbildung veranschaulicht.

![GPT-Layout](images/basic-gpt.png)

Der schutzmbr-Bereich ist in einem GPT-Partitionslayout für die Abwärtskompatibilität mit Datenträger Verwaltungs Dienstprogrammen vorhanden, die auf MBR arbeiten. Der GPT-Header definiert den Bereich der logischen Block Adressen, die von Partitions Einträgen verwendet werden können. Der GPT-Header definiert auch seinen Speicherort auf dem Datenträger, seine **GUID** und eine 32-Bit-CRC32-Prüfsumme (zyklische Redundanz Überprüfung), die zum Überprüfen der Integrität des GPT-Headers verwendet wird. Jeder **GUID** -Partitionseintrag beginnt mit einer GUID des Partitions Typs. Die 16-Byte-Partitionstyp- **GUID**, die einer System-ID in der Partitionstabelle eines MBR-Datenträgers ähnelt, identifiziert den Datentyp, den die Partition enthält, und gibt an, wie die Partition verwendet wird, z. b. wenn es sich um einen einfachen Datenträger oder einen dynamischen Datenträger handelt. Beachten Sie, dass jeder **GUID** -Partitionseintrag über eine Sicherungskopie verfügt.

Dynamische Datenträger- **GPT** -Partitionslayouts ähneln diesem einfachen Datenträger Beispiel. wie bereits erwähnt, gibt es jedoch nur einen LDM-Partitionseintrag anstelle von 1-n primären Partitionen, der auf Basis Datenträgern zulässig ist. Außerdem gibt es eine versteckte LDM-Daten Bank Partition mit einem entsprechenden **GUID** -Partitionseintrag. Weitere Informationen zum LDM finden Sie im Abschnitt [dynamische](#basic-and-dynamic-disks) Datenträger.

## <a name="detecting-the-type-of-disk"></a>Erkennen der Art des Datenträgers

Es gibt keine bestimmte Funktion, um den Typ des Datenträgers, auf dem sich eine bestimmte Datei oder ein bestimmtes Verzeichnis befindet, Programm gesteuert zu erkennen. Es gibt eine indirekte Methode.

* Übergeben Sie den Datei-oder Verzeichnispfad an [**getvolumepathname**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumepathnamew) , um den Einfügepunkt abzurufen.
* Übergeben Sie den Bereitstellungspunkt an [**getvolumenameforvolumemountpoint, um den Volumenamen**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) abzurufen.
* Entfernen Sie den nachfolgenden umgekehrten Schrägstrich aus dem Volumenamen.
* Übergeben Sie den Volumenamen ohne den nachfolgenden umgekehrten Schrägstrich an die [**Datei**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) "up", um das Volume zu öffnen
* Verwenden Sie [**IOCTL \_ Volume \_ get \_ Volume \_ Disk \_ Blöcke**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_volume_get_volume_disk_extents) mit dem volumehandle, um die Datenträger Nummern zu erhalten.
* Verwenden Sie die Datenträger Nummern zum Erstellen der Datenträger Pfade, z. b. " \\ \\ ? \\ Physicaldrive *X*".
* Übergeben Sie jeden Datenträger Pfad an " [**foratefile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) ", um den Datenträger zu öffnen
* Verwenden Sie [**IOCTL \_ Disk \_ get \_ Drive \_ Layout \_ Ex**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_disk_get_drive_layout_ex) zum Abrufen der Partitionsliste.
* Überprüfen Sie den **PartitionType** für jeden Eintrag in der Partitionsliste.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zur Volumeverwaltung](about-volume-management.md)
</dt> <dt>

[Technische Referenz zu einfachen Datenträgern und Volumes](/previous-versions/windows/it-pro/windows-server-2003/cc784732(v=ws.10))
</dt> <dt>

[Technische Referenz zu dynamischen Datenträgern und Volumes](/previous-versions/windows/it-pro/windows-server-2003/cc785638(v=ws.10))
</dt> <dt>

[Storage Basic im Vergleich zu dynamischem Speicher in Windows XP]( https://support.microsoft.com/kb/314343/)
</dt> </dl>

 

 
