---
description: Dieser Abschnitt enthält ein Glossar mit technischen Begriffen, die in der Dokumentation zu Virtual Disk Service (VDS) verwendet werden.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 1cf28cfb-ce96-4659-955d-0088bddcb9ce
title: Glossar zum Dienst für virtuelle Datenträger
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af7e73e9de8f6c30b69f2e39e78fae36e5c3ea547cccfed2f25f9a15327e3f8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118602993"
---
# <a name="virtual-disk-service-glossary"></a>Glossar zum Dienst für virtuelle Datenträger

\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [Virtual Disk Service](virtual-disk-service-portal.md) durch die [Windows Storage Verwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)ersetzt.\]

Dieser Abschnitt enthält ein Glossar mit technischen Begriffen, die in der Dokumentation zu Virtual Disk Service (VDS) verwendet werden.

<dl> <dt>

<span id="base.automagic_configuration"></span><span id="BASE.AUTOMAGIC_CONFIGURATION"></span>**Automagic-Konfiguration**
</dt> <dd>

Hardware-RAID-Anbieter, der eine Reihe von Regeln für die Auswahl der Neuzuordnung logischer LUN-Blöcke basierend auf einfachen Attributen bietet. Automagic-Anbieter können auch die Zuordnung für die Leistung oder Fehlerverwaltung dynamisch ändern.

</dd> <dt>

<span id="base.binding_hints"></span><span id="BASE.BINDING_HINTS"></span>**Automagic-Hinweise**
</dt> <dd>

Informationen, die an einen automagic-Anbieter bereitgestellt werden, um die Konfiguration des logischen LUN-Blocks zu steuern. Hinweise enthalten Informationen zur gewünschten Fehlertoleranz, zur physischen Atomarität und zum beabsichtigten E/A-Zugriffsmuster.

</dd> <dt>

<span id="base.basic_disk"></span><span id="BASE.BASIC_DISK"></span>**Basisdatenträger**
</dt> <dd>

Ein Datenträger, der vom einfachsten softwareanbieter verwaltet wird. Der Basisdatenträgeranbieter unterstützt nur Volumes, die Partitionskonfigurationsdatenstrukturen direkt zugeordnet werden.

</dd> <dt>

<span id="base.binding"></span><span id="BASE.BINDING"></span>**Bindung**
</dt> <dd>

Auswählen eines Satzes von Zuordnungen zu physischen Ressourcen.

</dd> <dt>

<span id="base.convert"></span><span id="BASE.CONVERT"></span>**Konvertieren**
</dt> <dd>

Der Prozess der Konvertierung eines Basisdatenträgers in einen dynamischen Datenträger.

</dd> <dt>

<span id="base.configuration"></span><span id="BASE.CONFIGURATION"></span>**Konfiguration**
</dt> <dd>

Eine Auflistung der Betriebsparameter, die die Zuordnung von einem Volume oder einer LUN zu physischen Ressourcen bereitstellen.

</dd> <dt>

<span id="base.controller"></span><span id="BASE.CONTROLLER"></span>**Controller**
</dt> <dd>

Ein Softwareprogramm, das die Laufzeitintelligenz für einen Hardwareanbieter enthält.

</dd> <dt>

<span id="base.disk"></span><span id="BASE.DISK"></span>**Datenträger**
</dt> <dd>

Ein physischer Datenträger oder eine HARDWARE-RAID-LUN. Datenträger sind Ziele für die E/A-Last des Laufzeitspeichers. Plug & Play (PNP) unterscheidet nicht zwischen JBOD und LUNs.

</dd> <dt>

<span id="base.disk_platter"></span><span id="BASE.DISK_PLATTER"></span>**Disk-8000-Datenträger**
</dt> <dd>

Eine Teilmenge eines Pakets, das zum Exportieren oder Importieren von Volumes aus einem Paket verwendet wird.

</dd> <dt>

<span id="base.disk_pack"></span><span id="BASE.DISK_PACK"></span>**Datenträgerpaket**
</dt> <dd>

Weitere Informationen finden Sie *unter pack*.

</dd> <dt>

<span id="base.drive"></span><span id="BASE.DRIVE"></span>**Laufwerk**
</dt> <dd>

Eine physische Datenträgerspindel innerhalb eines Hardware-RAID-Subsystems. Laufwerke werden durch das Subsystem an LUNs gebunden.

</dd> <dt>

<span id="base.dynamic_disk"></span><span id="BASE.DYNAMIC_DISK"></span>**Dynamischer Datenträger**
</dt> <dd>

Ein Datenträger, der von einem Software-RAID-Anbieter mit Unterstützung für die flexible Volume-Neukonfiguration verwaltet wird. Ein dynamischer Datenträger verwendet eine Partition als Container für Volumes. es gibt keine garantierte Zuordnung.

</dd> <dt>

<span id="base.explicit_configuration"></span><span id="BASE.EXPLICIT_CONFIGURATION"></span>**Explizite Konfiguration**
</dt> <dd>

Eine Konfiguration mit den Parametern, einschließlich des Volumetyps und des genauen Layouts, für eine Sammlung von Zielvolumes.

</dd> <dt>

<span id="base.export"></span><span id="BASE.EXPORT"></span>**Exportieren**
</dt> <dd>

Das Verschieben eines Datenträgers und aller darin enthaltenen Volumes aus einem Paket.

</dd> <dt>

<span id="base.extent"></span><span id="BASE.EXTENT"></span>**Umfang**
</dt> <dd>

Ein zusammenhängender Bereich logischer Sektoren, die zu einem einzelnen Volume oder Datenträger beitragen. Ein Bereich kann auch ein Bereich von nicht zugeordneten Sektoren sein. In der Regel zeigt ein Dateisystem die Erweiterungsdetails für einen Endbenutzer an.

</dd> <dt>

<span id="base.guid_partition_table_gpt"></span><span id="BASE.GUID_PARTITION_TABLE_GPT"></span>**GUID-Partitionstabelle (GPT)**
</dt> <dd>

Von der EFI-Firmware verwendete Strukturen. GPT ist eines von zwei Softwarekonfigurationsdatenformaten der untersten Ebene, die von der Plattformfirmware verwendet werden, um ein startbares Betriebssystem oder ein anderes ausführbares Image zu finden.

</dd> <dt>

<span id="base.hardware_provider"></span><span id="BASE.HARDWARE_PROVIDER"></span>**Hardwareanbieter**
</dt> <dd>

Eine Sammlung von Software, die auf dem Host, einem Busadapter und möglicherweise einem externen Speichersubsystem ausgeführt wird, das zusammen raid-LUNs aufweist und verwaltet. Hardwareanbieter für die meisten externen Speichersubsysteme enthalten nur hostbasierte Software im Benutzermodus.

</dd> <dt>

<span id="base.health"></span><span id="BASE.HEALTH"></span>**Gesundheit**
</dt> <dd>

Der aktuelle Fehlerverwaltungsstatus eines Volumes oder einer LUN.

</dd> <dt>

<span id="base.hot_spotting"></span><span id="BASE.HOT_SPOTTING"></span>**Hot Sparing**
</dt> <dd>

Vorübergehendes Hinzufügen eines Volumeplexs zu einem Volume.

</dd> <dt>

<span id="base.import"></span><span id="BASE.IMPORT"></span>**Importieren**
</dt> <dd>

Das Verschieben eines Datenträgers und aller zugehörigen Volumes in ein vorhandenes Paket.

</dd> <dt>

<span id="base.JBOD"></span><span id="base.jbod"></span><span id="BASE.JBOD"></span>**nur eine Reihe von Datenträgern (JBOD)**
</dt> <dd>

Eine Sammlung physischer Spindeln ohne die koordinierte Steuerung, die von einem Hardware-RAID-Gerät bereitgestellt wird.

</dd> <dt>

<span id="base.logical_block_number_LBN"></span><span id="base.logical_block_number_lbn"></span><span id="BASE.LOGICAL_BLOCK_NUMBER_LBN"></span>**Logische Blocknummer (Logical Block Number, LBN)**
</dt> <dd>

Die kleinste adressierbare Einheit von Speicherdaten. LBN wird mit E/A-Befehlsprotokollen verwendet.

</dd> <dt>

<span id="base.logical_block_mapping"></span><span id="BASE.LOGICAL_BLOCK_MAPPING"></span>**Logische Blockzuordnung**
</dt> <dd>

Die Transformation der logischen Blöcke, die einem Anbieter für diejenigen angezeigt werden, die vom Anbieter verfügbar gemacht werden.

</dd> <dt>

<span id="base.logical_Unit_Number_LUN"></span><span id="base.logical_unit_number_lun"></span><span id="BASE.LOGICAL_UNIT_NUMBER_LUN"></span>**Logische Einheitennummer (LUN)**
</dt> <dd>

Eine physisch adressierbare Speichereinheit, die von einem Hardware-RAID-Subsystem verfügbar ist. Dieser Begriff kann auch auf den SCSI-Bezeichner für die Speichereinheit verweisen.

</dd> <dt>

<span id="base.LUN_number"></span><span id="base.lun_number"></span><span id="BASE.LUN_NUMBER"></span>**LUN-Nummer**
</dt> <dd>

Eine Zahl, die ein VDS-Hardwareanbieter einer LUN in einem Array zuweist. Dies entspricht nicht der "logischen Einheitennummer" in der SCSI-Adresse des Datenträgers.

</dd> <dt>

<span id="base.management_service"></span><span id="BASE.MANAGEMENT_SERVICE"></span>**Verwaltungsdienst**
</dt> <dd>

Ein Softwareprogramm, das nach Bedarf ausgeführt wird, um Volumekonfiguration, Überwachung oder Fehlerbehandlung durchzuführen.

</dd> <dt>

<span id="base.mapping"></span><span id="BASE.MAPPING"></span>**Zuordnung**
</dt> <dd>

Ein Volume, das für das Betriebssystem verfügbar gemacht wird und über einen zugeordneten Volumenamen (laufwerkbuchstabe) verfügt. Auf ein Volume kann von einem Dateisystem zugegriffen werden.

</dd> <dt>

<span id="base.masking"></span><span id="BASE.MASKING"></span>**Maskierung**
</dt> <dd>

Ein Datenträger, der vom Betriebssystem nicht erkannt wird. Ein Datenträger kann durch das Hardware-RAID-Subsystem, den Switch, die SCSI-RESERVE durch einen anderen Computerhost oder software im Datenträgerstapel maskiert werden.

</dd> <dt>

<span id="base.master_Boot_Record_partitioning_MBR"></span><span id="base.master_boot_record_partitioning_mbr"></span><span id="BASE.MASTER_BOOT_RECORD_PARTITIONING_MBR"></span>**Partitionierung von Masterstartdatensätzen (MBR)**
</dt> <dd>

MBR ist eines von zwei Softwarekonfigurationsdatenformaten der untersten Ebene und wird von der BIOS-Firmware verwendet, um ein startbares Betriebssystemabbild zu finden.

</dd> <dt>

<span id="base.member"></span><span id="BASE.MEMBER"></span>**Mitglied**
</dt> <dd>

Eine Auflistung verketteter Datenträger-Erweiterungen, die auf einem weiteren Datenträger enthalten sind. Ein Datenträger kann nur zu einem Mitglied eines Volumes beitragen.

</dd> <dt>

<span id="base.mirror"></span><span id="BASE.MIRROR"></span>**Spiegel**
</dt> <dd>

Eine Volume- oder Datenträgerzuordnung, die zwei oder mehr identische Datenkopien beibehält. Der Typ der Zuordnung wird auch als RAID-Ebene 1 bezeichnet.

</dd> <dt>

<span id="base.pack"></span><span id="BASE.PACK"></span>**Pack**
</dt> <dd>

Eine Sammlung logischer Volumes und zugrunde liegender Datenträger. Ein Paket ist die Einheit des transitiven Abschlusses für ein Volume. Dynamische Datenträgerpakete und Datenträgergruppen sind Begriffe für dasselbe Element.

</dd> <dt>

<span id="base.parity_stripe"></span><span id="BASE.PARITY_STRIPE"></span>**Paritätsstreifen**
</dt> <dd>

Eine Volume- oder Datenträgerzuordnung, die Informationen zur Paritätsprüfung sowie Daten verwaltet. Jeder Anbieter stellt das genaue Zuordnungs- und Schutzschema zur Verfügung. Umfasst RAID 3, 4, 5 und 6.

</dd> <dt>

<span id="base.partially_directed_configuration"></span><span id="BASE.PARTIALLY_DIRECTED_CONFIGURATION"></span>**Teilweise gerichtete Konfiguration**
</dt> <dd>

Ein Volume oder eine Datenträgerkonfiguration, die nicht vollständig explizit ist. Der Bindungstyp und eine Auflistung von Zielressourcen werden angegeben. das tatsächliche Layout ist dies nicht. Die teilweise gerichtete Konfiguration ist die gängigste Volumekonfiguration.

</dd> <dt>

<span id="base.partition"></span><span id="BASE.PARTITION"></span>**Partition**
</dt> <dd>

Ein zusammenhängender Bereich logischer Sektoren, der durch einen einzelnen Eintrag in der MBR- oder GPT-Struktur beschrieben wird. Auf Basisdatenträgern entsprechen Partitionen direkt einfachen Volumes. Partitionsstrukturen werden von der BIOS- oder EFI-Plattformfirmware und einem Betriebssystem oder einem anderen startbaren Image gemeinsam genutzt.

</dd> <dt>

<span id="base.path"></span><span id="BASE.PATH"></span>**Pfad**
</dt> <dd>

Der Zugriffspfad von einem Computer zu einem Datenträger oder einer externen Hardware-LUN.

</dd> <dt>

<span id="base.plex"></span><span id="BASE.PLEX"></span>**Plex**
</dt> <dd>

Ein Member eines gespiegelten Volumes oder einer LUN.

</dd> <dt>

<span id="base.port"></span><span id="BASE.PORT"></span>**Hafen**
</dt> <dd>

Der Endpunkt eines Pfads auf einem Datenträger.

</dd> <dt>

<span id="base.redundant_array_of_independent_disks_RAID"></span><span id="base.redundant_array_of_independent_disks_raid"></span><span id="BASE.REDUNDANT_ARRAY_OF_INDEPENDENT_DISKS_RAID"></span>**Redundantes Array unabhängiger Datenträger (RAID)**
</dt> <dd>

Eine Sammlung von Techniken zum Verwalten mehrerer Datenträger.

</dd> <dt>

<span id="base.runtime_service"></span><span id="BASE.RUNTIME_SERVICE"></span>**Laufzeitdienst**
</dt> <dd>

Ein Softwareprogramm, das auf E/A-Anforderungsbasis ausgeführt wird.

</dd> <dt>

<span id="base.simple_disk"></span><span id="BASE.SIMPLE_DISK"></span>**einfacher Datenträger**
</dt> <dd>

Eine Spindel, die nicht mit einem Hardware-RAID-Controller verbunden ist. Siehe auch Just a Bunch Of Disks (JBOD).

</dd> <dt>

<span id="base.software_provider"></span><span id="BASE.SOFTWARE_PROVIDER"></span>**Softwareanbieter**
</dt> <dd>

Hostbasierte Software, die logische Volumes verfügbar macht und auf Datenträgern betrieben wird. Ein Softwareanbieter umfasst Laufzeitdienste im Kernelmodus, Konfigurationsdaten und Verwaltungsdienste im Benutzermodus.

</dd> <dt>

<span id="base.span"></span><span id="BASE.SPAN"></span>**Span**
</dt> <dd>

Eine lineare Zuordnung mehrerer diskontinuerlicher Datenträger- oder Laufwerksdehnungen auf einem Volume oder Datenträger. Die Erweiterungen können sich auf einer oder mehreren Spindeln oder LUNs benn.

</dd> <dt>

<span id="base.spindle"></span><span id="BASE.SPINDLE"></span>**Spindel**
</dt> <dd>

Eine physische Einheit des Datenträgerspeichers.

</dd> <dt>

<span id="base.stacking"></span><span id="BASE.STACKING"></span>**Stapeln**
</dt> <dd>

Das Erstellen eines Volumes oder einer LUN durch Ausführen von mehr als einem logischen Blockzuordnungsvorgang. Ein Beispiel ist ein gespiegeltes Stripesetvolume. Die gängigste Stapelung tritt auf, wenn Software-RAID über LUNs hinweg verwendet wird, die von Hardware-RAID erstellt werden.

</dd> <dt>

<span id="base.stripe"></span><span id="BASE.STRIPE"></span>**Streifen**
</dt> <dd>

Eine Volume- oder Datenträgerzuordnung, die zusammenhängende Erweiterungen über mehrere Volumes, Datenträger oder Laufwerke verteilt. Diese Zuordnung wird auch als RAID 0 bezeichnet.

</dd> <dt>

<span id="base.status"></span><span id="BASE.STATUS"></span>**Status**
</dt> <dd>

Die aktuelle Verfügbarkeit eines Volumes, Datenträgers oder Laufwerks.

</dd> <dt>

<span id="base.subsystem"></span><span id="BASE.SUBSYSTEM"></span>**Subsystem**
</dt> <dd>

Die Instanziierung von Hardwareanbietersoftware. Ein Subsystem enthält mindestens einen Controller und ein Laufwerk. Wenn sich das Subsystem außerhalb des Computers befindet, verbinden mindestens ein Netzwerkpfad das Subsystem mit dem Computer.

</dd> <dt>

<span id="base.jello"></span><span id="BASE.JELLO"></span>**Übergangszustand**
</dt> <dd>

Status der logischen zu physischen Zuordnung, die geändert wird.

</dd> <dt>

<span id="base.uninitialized_disk"></span><span id="BASE.UNINITIALIZED_DISK"></span>**Nicht initialisierter Datenträger**
</dt> <dd>

Ein Datenträger, der kein Mitglied eines Pakets ist.

</dd> <dt>

<span id="base.unmasked_disk"></span><span id="BASE.UNMASKED_DISK"></span>**Datenträger ohne Maskierung**
</dt> <dd>

Ein Datenträger, der für das Betriebssystem sichtbar ist. Der Inhalt eines datenträgers ohne Maskierung ist für Softwarevolume-Manager, Dateisysteme usw. sichtbar.

</dd> <dt>

<span id="base.volume"></span><span id="BASE.VOLUME"></span>**Volumen**
</dt> <dd>

Eine Reihe von Datenträgerblöcken, die an einen praktisch zusammenhängenden Bereich logischer Blöcke gebunden sind. Auf ein Volume kann über einen Laufwerkbuchstaben, einen bereitgestellten Ordner oder einen Volume-GUID-Pfad zugegriffen werden.

</dd> </dl>

 

 
