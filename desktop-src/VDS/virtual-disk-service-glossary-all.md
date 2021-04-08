---
description: Dieser Abschnitt enthält ein Glossar der technischen Begriffe, die in der Dokumentation zu Virtual Disk Service (VDS) verwendet werden.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 1cf28cfb-ce96-4659-955d-0088bddcb9ce
title: Glossar zum Dienst für virtuelle Datenträger
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cc8804f1aea832f59fcbcab65423e92e134939f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959845"
---
# <a name="virtual-disk-service-glossary"></a>Glossar zum Dienst für virtuelle Datenträger

\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [virtuellen Festplatten Dienstanbieter](virtual-disk-service-portal.md) durch die [Windows-Speicherverwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)ersetzt.\]

Dieser Abschnitt enthält ein Glossar der technischen Begriffe, die in der Dokumentation zu Virtual Disk Service (VDS) verwendet werden.

<dl> <dt>

<span id="base.automagic_configuration"></span><span id="BASE.AUTOMAGIC_CONFIGURATION"></span>**automagationskonfiguration**
</dt> <dd>

Der Hardware-RAID-Anbieter, der eine Reihe von Regeln zur Auswahl eines logischen LUN-Blocks basierend auf einfachen Attributen bereitstellt. Automaginganbieter können die Zuordnung für die Leistung oder Fehler Verwaltung auch dynamisch ändern.

</dd> <dt>

<span id="base.binding_hints"></span><span id="BASE.BINDING_HINTS"></span>**automagandeutungen**
</dt> <dd>

Informationen, die für einen automischen Anbieter bereitgestellt werden, um die Konfiguration der logischen LUN-Blöcke zu steuern Hinweise enthalten Informationen zu der gewünschten Fehlertoleranz, der physischen Atomizität und dem beabsichtigten e/a-Zugriffsmuster.

</dd> <dt>

<span id="base.basic_disk"></span><span id="BASE.BASIC_DISK"></span>**Basis Festplatte**
</dt> <dd>

Ein Datenträger, der vom einfachsten möglichen Softwareanbieter verwaltet wird. Der Basic-Datenträger Anbieter unterstützt nur Volumes, die den Partitions Konfigurationsdaten Strukturen direkt zugeordnet werden.

</dd> <dt>

<span id="base.binding"></span><span id="BASE.BINDING"></span>**lichere**
</dt> <dd>

Auswählen eines Satzes von Zuordnungen zu physischen Ressourcen.

</dd> <dt>

<span id="base.convert"></span><span id="BASE.CONVERT"></span>**umgebaut**
</dt> <dd>

Der Prozess, bei dem ein Basis Datenträger in einen dynamischen Datenträger umwandelt.

</dd> <dt>

<span id="base.configuration"></span><span id="BASE.CONFIGURATION"></span>**konfiguri**
</dt> <dd>

Eine Auflistung der Betriebsparameter, die die Zuordnung von einem Volume oder einer LUN zu physischen Ressourcen bereitstellen.

</dd> <dt>

<span id="base.controller"></span><span id="BASE.CONTROLLER"></span>**ern**
</dt> <dd>

Ein Softwareprogramm, das die Lauf Zeit Intelligenz für einen Hardware Anbieter enthält.

</dd> <dt>

<span id="base.disk"></span><span id="BASE.DISK"></span>**Diskette**
</dt> <dd>

Ein physischer Datenträger oder eine Hardware-RAID-LUN. Datenträger sind Ziele für die Laufzeitspeicher-e/a-Last. Plug & Play (PNP) unterscheidet nicht zwischen JBOD und LUNs.

</dd> <dt>

<span id="base.disk_platter"></span><span id="BASE.DISK_PLATTER"></span>**Datenträger Platte**
</dt> <dd>

Eine Teilmenge eines Pakets, das zum Exportieren oder Importieren von Volumes aus einem Paket verwendet wird.

</dd> <dt>

<span id="base.disk_pack"></span><span id="BASE.DISK_PACK"></span>**Disk Pack**
</dt> <dd>

Siehe *Paket*.

</dd> <dt>

<span id="base.drive"></span><span id="BASE.DRIVE"></span>**Antrie**
</dt> <dd>

Eine physische Datenträger Spindel innerhalb eines Hardware-RAID-Subsystems. Laufwerke werden vom-Subsystem an LUNs gebunden.

</dd> <dt>

<span id="base.dynamic_disk"></span><span id="BASE.DYNAMIC_DISK"></span>**dynamischer Datenträger**
</dt> <dd>

Ein von einem Software-RAID-Anbieter verwalteter Datenträger mit Unterstützung für eine flexible Neukonfiguration von Volumes. Ein dynamischer Datenträger verwendet eine Partition als Container für Volumes. Es ist keine garantierte Zuordnung vorhanden.

</dd> <dt>

<span id="base.explicit_configuration"></span><span id="BASE.EXPLICIT_CONFIGURATION"></span>**explizite Konfiguration**
</dt> <dd>

Eine Konfiguration mit den Parametern, einschließlich des Volumetyps und dem exakten Layout, für eine Auflistung von Zielvolumes.

</dd> <dt>

<span id="base.export"></span><span id="BASE.EXPORT"></span>**Exports**
</dt> <dd>

Das Verschieben einer Datenträger Platte und aller Volumes, die auf dieser Platte enthalten sind, aus einem Paket.

</dd> <dt>

<span id="base.extent"></span><span id="BASE.EXTENT"></span>**Ausdehnung**
</dt> <dd>

Ein zusammenhängender Bereich logischer Sektoren, die zu einem einzelnen Volume oder Datenträger beitragen. Ein Block kann auch der Bereich nicht zugeordneter Sektoren sein. Häufig werden einem Endbenutzer in einem Dateisystem Details zu den Details angezeigt.

</dd> <dt>

<span id="base.guid_partition_table_gpt"></span><span id="BASE.GUID_PARTITION_TABLE_GPT"></span>**GUID-Partitionstabelle (GPT)**
</dt> <dd>

Von EFI-Firmware verwendete Strukturen. GPT ist eines von zwei Datenformaten für die Softwarekonfiguration auf niedrigster Ebene, die von der Platt Form Firmware verwendet werden, um ein Start fähiges Betriebssystem oder ein anderes ausführbares Image

</dd> <dt>

<span id="base.hardware_provider"></span><span id="BASE.HARDWARE_PROVIDER"></span>**Hardware Anbieter**
</dt> <dd>

Eine Sammlung von Software, die auf dem Host ausgeführt wird, ein Busadapter und möglicherweise ein externes Speichersubsystem, das zusammenarbeitet, um RAID-LUNs zu verwalten und zu verwalten. Hardware Anbieter für die meisten externen Speicher Subsysteme enthalten nur Host basierte Software im Benutzermodus.

</dd> <dt>

<span id="base.health"></span><span id="BASE.HEALTH"></span>**gesundheitliche**
</dt> <dd>

Der aktuelle Fehler Verwaltungsstatus eines Volumes oder einer LUN.

</dd> <dt>

<span id="base.hot_spotting"></span><span id="BASE.HOT_SPOTTING"></span>**heiß sparsam**
</dt> <dd>

Temporäres Hinzufügen eines volumeplex zu einem Volume.

</dd> <dt>

<span id="base.import"></span><span id="BASE.IMPORT"></span>**Importieren**
</dt> <dd>

Das Verschieben einer Datenträger Platte und sämtlicher Volumes in ein vorhandenes Paket.

</dd> <dt>

<span id="base.JBOD"></span><span id="base.jbod"></span><span id="BASE.JBOD"></span>**nur eine Reihe von Datenträgern (JBOD)**
</dt> <dd>

Eine Auflistung physischer Spindeln ohne das koordinierte Steuerelement, das von einem Hardware-RAID-Gerät bereitgestellt wird.

</dd> <dt>

<span id="base.logical_block_number_LBN"></span><span id="base.logical_block_number_lbn"></span><span id="BASE.LOGICAL_BLOCK_NUMBER_LBN"></span>**logische Block Nummer (LBN)**
</dt> <dd>

Die kleinste adressierbare Einheit von Speicherdaten. LBN wird mit e/a-Befehls Protokollen verwendet.

</dd> <dt>

<span id="base.logical_block_mapping"></span><span id="BASE.LOGICAL_BLOCK_MAPPING"></span>**logische Block Zuordnung**
</dt> <dd>

Die Transformation der logischen Blöcke, die einem Anbieter für die vom Anbieter bereitgestellten logischen Blöcke angezeigt werden.

</dd> <dt>

<span id="base.logical_Unit_Number_LUN"></span><span id="base.logical_unit_number_lun"></span><span id="BASE.LOGICAL_UNIT_NUMBER_LUN"></span>**logische Gerätenummer (LUN)**
</dt> <dd>

Eine physisch adressierbare Speichereinheit, die von einem Hardware-RAID-Subsystem bereitgestellt wird. Dieser Begriff kann sich auch auf den SCSI-Bezeichner für die Speichereinheit beziehen.

</dd> <dt>

<span id="base.LUN_number"></span><span id="base.lun_number"></span><span id="BASE.LUN_NUMBER"></span>**LUN-Nummer**
</dt> <dd>

Eine Zahl, die ein VDS-Hardware Anbieter einer LUN in einem Array zuweist. Dies entspricht nicht der "logischen Gerätenummer" in der SCSI-Adresse des Datenträgers.

</dd> <dt>

<span id="base.management_service"></span><span id="BASE.MANAGEMENT_SERVICE"></span>**Verwaltungsdienst**
</dt> <dd>

Ein Softwareprogramm, das nach Bedarf ausgeführt wird, um die Volumekonfiguration, Überwachung oder Fehlerbehandlung auszuführen.

</dd> <dt>

<span id="base.mapping"></span><span id="BASE.MAPPING"></span>**Mapping**
</dt> <dd>

Ein Volume, das für das Betriebssystem verfügbar gemacht wird und über einen zugeordneten Volumenamen (Laufwerk Buchstabe) verfügt. Ein Dateisystem kann auf ein Volume zugreifen.

</dd> <dt>

<span id="base.masking"></span><span id="BASE.MASKING"></span>**maskiert**
</dt> <dd>

Ein Datenträger, der vom Betriebssystem nicht erkannt wird. Ein Datenträger kann mit dem Hardware-RAID-Subsystem, dem Switch, der SCSI-Reserve eines anderen Computer Hosts oder der Software im Datenträger Stapel maskiert werden.

</dd> <dt>

<span id="base.master_Boot_Record_partitioning_MBR"></span><span id="base.master_boot_record_partitioning_mbr"></span><span id="BASE.MASTER_BOOT_RECORD_PARTITIONING_MBR"></span>**Master Boot Record Partitionierung (MBR)**
</dt> <dd>

MBR ist eines von zwei Datenformaten für die Softwarekonfiguration auf niedrigster Ebene und wird von der BIOS-Firmware verwendet, um ein Start fähiges Betriebssystem Abbild zu suchen.

</dd> <dt>

<span id="base.member"></span><span id="BASE.MEMBER"></span>**Kollege**
</dt> <dd>

Eine Auflistung verketter Datenträger Blöcke, die auf einem oder mehreren Datenträgern enthalten sind. Ein Datenträger kann nur zu einem Mitglied eines Volumes beitragen.

</dd> <dt>

<span id="base.mirror"></span><span id="BASE.MIRROR"></span>**OL**
</dt> <dd>

Ein Volume oder eine Datenträger Zuordnung, das mindestens zwei identische Datenkopien verwaltet. Der Typ der Zuordnung wird auch als RAID-Stufe 1 bezeichnet.

</dd> <dt>

<span id="base.pack"></span><span id="BASE.PACK"></span>**ru**
</dt> <dd>

Eine Auflistung logischer Volumes und zugrunde liegender Datenträger. Ein Paket ist die Einheit des transitiven Abschlusses für ein Volume. Dynamische Festplatten Pakete und Datenträger Gruppen sind Begriffe für dasselbe Element.

</dd> <dt>

<span id="base.parity_stripe"></span><span id="BASE.PARITY_STRIPE"></span>**Paritäts Streifen**
</dt> <dd>

Ein Volume oder eine Datenträger Zuordnung, das Informationen zur Paritäts Überprüfung sowie Daten verwaltet. Jeder Lieferant liefert das genaue Mapping-und Schutzschema. Umfasst RAID 3, 4, 5 und 6.

</dd> <dt>

<span id="base.partially_directed_configuration"></span><span id="BASE.PARTIALLY_DIRECTED_CONFIGURATION"></span>**teilweise gesteuerte Konfiguration**
</dt> <dd>

Ein Volume oder eine Datenträger Konfiguration, das nicht vollständig explizit ist. Der Bindungstyp und eine Auflistung von Ziel Ressourcen werden angegeben. das tatsächliche Layout ist nicht. Die teilweise gesteuerte Konfiguration ist die gängigste Volumekonfiguration.

</dd> <dt>

<span id="base.partition"></span><span id="BASE.PARTITION"></span>**spaltet**
</dt> <dd>

Ein zusammenhängender Bereich logischer Sektoren, der durch einen einzelnen Eintrag in der MBR-oder GPT-Struktur beschrieben wird. Auf Basis Datenträgern entsprechen Partitionen direkt einfachen Volumes. Partitions Strukturen werden von der BIOS-oder EFI-Platt Form Firmware und einem Betriebssystem oder einem anderen Start baren Image gemeinsam genutzt.

</dd> <dt>

<span id="base.path"></span><span id="BASE.PATH"></span>**ADS**
</dt> <dd>

Der Zugriffs Pfad von einem Computer auf einen Datenträger oder eine externe Hardware-LUN.

</dd> <dt>

<span id="base.plex"></span><span id="BASE.PLEX"></span>**Plex**
</dt> <dd>

Ein Member eines gespiegelten Volumes oder einer gespiegelten LUN.

</dd> <dt>

<span id="base.port"></span><span id="BASE.PORT"></span>**Port**
</dt> <dd>

Der Endpunkt eines Pfads auf einem Datenträger.

</dd> <dt>

<span id="base.redundant_array_of_independent_disks_RAID"></span><span id="base.redundant_array_of_independent_disks_raid"></span><span id="BASE.REDUNDANT_ARRAY_OF_INDEPENDENT_DISKS_RAID"></span>**redundantes Array von unabhängigen Datenträgern (RAID)**
</dt> <dd>

Eine Sammlung von Techniken zum Verwalten mehrerer Datenträger.

</dd> <dt>

<span id="base.runtime_service"></span><span id="BASE.RUNTIME_SERVICE"></span>**Lauf Zeit Dienst**
</dt> <dd>

Ein Softwareprogramm, das auf einer e/a-Anforderung ausgeführt wird.

</dd> <dt>

<span id="base.simple_disk"></span><span id="BASE.SIMPLE_DISK"></span>**einfache Festplatte**
</dt> <dd>

Eine Spindel, die nicht mit einem Hardware-RAID-Controller verbunden ist. Siehe auch nur eine Reihe von Datenträgern (JBOD).

</dd> <dt>

<span id="base.software_provider"></span><span id="BASE.SOFTWARE_PROVIDER"></span>**Softwareanbieter**
</dt> <dd>

Host basierte Software, die logische Volumes verfügbar macht und auf Datenträgern arbeitet. Ein Softwareanbieter umfasst Lauf Zeit Dienste im Kernel Modus, Konfigurationsdaten und benutzermodusverwaltungsdienste.

</dd> <dt>

<span id="base.span"></span><span id="BASE.SPAN"></span>**Spanne**
</dt> <dd>

Eine lineare Zuordnung von Volumes oder Datenträgern mehrerer diskontinuierlichen Datenträger-oder Laufwerks Blöcke. Die Blöcke können sich auf einem oder mehreren Spindeln oder LUNs befinden.

</dd> <dt>

<span id="base.spindle"></span><span id="BASE.SPINDLE"></span>**Maschinen**
</dt> <dd>

Eine physische Einheit von Datenträger Speicher.

</dd> <dt>

<span id="base.stacking"></span><span id="BASE.STACKING"></span>**Staffeln**
</dt> <dd>

Der Vorgang des Erstellens eines Volumes oder einer LUN durch Ausführen mehrerer logischer Block Mapping-Vorgänge. Ein Beispiel hierfür ist ein gespiegeltes Stripeset. Das häufigste Stapeln tritt auf, wenn Software-RAID für LUNs verwendet wird, die von Hardware-RAID erstellt wurden.

</dd> <dt>

<span id="base.stripe"></span><span id="BASE.STRIPE"></span>**Reifen**
</dt> <dd>

Ein Volume oder eine Datenträger Zuordnung, das zusammenhängende Blöcke über mehrere Volumes, Datenträger oder Laufwerke hinweg überlappt. Diese Zuordnung wird auch als RAID 0 bezeichnet.

</dd> <dt>

<span id="base.status"></span><span id="BASE.STATUS"></span>**Stands**
</dt> <dd>

Die aktuelle Verfügbarkeit eines Volumes, einer Festplatte oder eines Laufwerks.

</dd> <dt>

<span id="base.subsystem"></span><span id="BASE.SUBSYSTEM"></span>**System**
</dt> <dd>

Die Instanziierung von Hardware Anbieter Software. Ein Subsystem enthält mindestens einen Controller und ein Laufwerk. Wenn das Subsystem für den Computer extern ist, wird von einem oder mehreren Netzwerkpfaden das Subsystem mit dem Computer verbunden.

</dd> <dt>

<span id="base.jello"></span><span id="BASE.JELLO"></span>**Übergangsstatus**
</dt> <dd>

Der Status der logischen und physischen Zuordnung, die geändert wird.

</dd> <dt>

<span id="base.uninitialized_disk"></span><span id="BASE.UNINITIALIZED_DISK"></span>**nicht initialisierter Datenträger**
</dt> <dd>

Ein Datenträger, der kein Mitglied eines Pakets ist.

</dd> <dt>

<span id="base.unmasked_disk"></span><span id="BASE.UNMASKED_DISK"></span>**unmaskierte Festplatte**
</dt> <dd>

Ein Datenträger, der für das Betriebssystem sichtbar ist. Der Inhalt eines nicht maskierten Datenträgers ist für Softwareverteilungs-Manager, Dateisysteme usw. sichtbar.

</dd> <dt>

<span id="base.volume"></span><span id="BASE.VOLUME"></span>**Handels**
</dt> <dd>

Eine Reihe von Datenträger Blöcke, die an einen praktisch zusammenhängenden Bereich logischer Blöcke gebunden sind. Auf ein Volume kann über einen Laufwerk Buchstaben, einen bereitgestellten Ordner oder einen VolumeGuid-Pfad zugegriffen werden.

</dd> </dl>

 

 
