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
# <a name="virtual-disk-service-glossary"></a><span data-ttu-id="cabe9-103">Glossar zum Dienst für virtuelle Datenträger</span><span class="sxs-lookup"><span data-stu-id="cabe9-103">Virtual Disk Service Glossary</span></span>

<span data-ttu-id="cabe9-104">\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [virtuellen Festplatten Dienstanbieter](virtual-disk-service-portal.md) durch die [Windows-Speicherverwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)ersetzt.\]</span><span class="sxs-lookup"><span data-stu-id="cabe9-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="cabe9-105">Dieser Abschnitt enthält ein Glossar der technischen Begriffe, die in der Dokumentation zu Virtual Disk Service (VDS) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cabe9-105">This section provides a glossary of technical terms used in the Virtual Disk Service (VDS) documentation.</span></span>

<dl> <dt>

<span data-ttu-id="cabe9-106"><span id="base.automagic_configuration"></span><span id="BASE.AUTOMAGIC_CONFIGURATION"></span>**automagationskonfiguration**</span><span class="sxs-lookup"><span data-stu-id="cabe9-106"><span id="base.automagic_configuration"></span><span id="BASE.AUTOMAGIC_CONFIGURATION"></span>**automagic configuration**</span></span>
</dt> <dd>

<span data-ttu-id="cabe9-107">Der Hardware-RAID-Anbieter, der eine Reihe von Regeln zur Auswahl eines logischen LUN-Blocks basierend auf einfachen Attributen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="cabe9-107">Hardware RAID provider that supplies a set of rules for choosing LUN logical block remapping based on simple attributes.</span></span> <span data-ttu-id="cabe9-108">Automaginganbieter können die Zuordnung für die Leistung oder Fehler Verwaltung auch dynamisch ändern.</span><span class="sxs-lookup"><span data-stu-id="cabe9-108">Automagic providers can also dynamically alter the mapping for performance or fault management.</span></span>

</dd> <dt>

<span data-ttu-id="cabe9-109"><span id="base.binding_hints"></span><span id="BASE.BINDING_HINTS"></span>**automagandeutungen**</span><span class="sxs-lookup"><span data-stu-id="cabe9-109"><span id="base.binding_hints"></span><span id="BASE.BINDING_HINTS"></span>**automagic hints**</span></span>
</dt> <dd>

<span data-ttu-id="cabe9-110">Informationen, die für einen automischen Anbieter bereitgestellt werden, um die Konfiguration der logischen LUN-Blöcke zu steuern</span><span class="sxs-lookup"><span data-stu-id="cabe9-110">Information supplied to an automagic provider to guide the LUN logical block configuration.</span></span> <span data-ttu-id="cabe9-111">Hinweise enthalten Informationen zu der gewünschten Fehlertoleranz, der physischen Atomizität und dem beabsichtigten e/a-Zugriffsmuster.</span><span class="sxs-lookup"><span data-stu-id="cabe9-111">Hints include information as to the desired fault tolerance, physical atomicity, and intended I/O access pattern.</span></span>

</dd> <dt>

<span data-ttu-id="cabe9-112"><span id="base.basic_disk"></span><span id="BASE.BASIC_DISK"></span>**Basis Festplatte**</span><span class="sxs-lookup"><span data-stu-id="cabe9-112"><span id="base.basic_disk"></span><span id="BASE.BASIC_DISK"></span>**basic disk**</span></span>
</dt> <dd>

<span data-ttu-id="cabe9-113">Ein Datenträger, der vom einfachsten möglichen Softwareanbieter verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="cabe9-113">A disk managed by the simplest possible software provider.</span></span> <span data-ttu-id="cabe9-114">Der Basic-Datenträger Anbieter unterstützt nur Volumes, die den Partitions Konfigurationsdaten Strukturen direkt zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="cabe9-114">The basic disk provider supports only volumes that directly map to partition configuration data structures.</span></span>

</dd> <dt>

<span data-ttu-id="cabe9-115"><span id="base.binding"></span><span id="BASE.BINDING"></span>**lichere**</span><span class="sxs-lookup"><span data-stu-id="cabe9-115"><span id="base.binding"></span><span id="BASE.BINDING"></span>**binding**</span></span>
</dt> <dd>

<span data-ttu-id="cabe9-116">Auswählen eines Satzes von Zuordnungen zu physischen Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="cabe9-116">Selecting for a set of mappings to physical resources.</span></span>

</dd> <dt>

<span data-ttu-id="cabe9-117"><span id="base.convert"></span><span id="BASE.CONVERT"></span>**umgebaut**</span><span class="sxs-lookup"><span data-stu-id="cabe9-117"><span id="base.convert"></span><span id="BASE.CONVERT"></span>**convert**</span></span>
</dt> <dd>

<span data-ttu-id="cabe9-118">Der Prozess, bei dem ein Basis Datenträger in einen dynamischen Datenträger umwandelt.</span><span class="sxs-lookup"><span data-stu-id="cabe9-118">The process of converting a basic disk to a dynamic disk.</span></span>

</dd> <dt>

<span data-ttu-id="cabe9-119"><span id="base.configuration"></span><span id="BASE.CONFIGURATION"></span>**konfiguri**</span><span class="sxs-lookup"><span data-stu-id="cabe9-119"><span id="base.configuration"></span><span id="BASE.CONFIGURATION"></span>**configuration**</span></span>
</dt> <dd>

<span data-ttu-id="cabe9-120">Eine Auflistung der Betriebsparameter, die die Zuordnung von einem Volume oder einer LUN zu physischen Ressourcen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="cabe9-120">A collection of the operating parameters that supply the mapping from a volume, or LUN, to physical resources.</span></span>

</dd> <dt>

<span data-ttu-id="cabe9-121"><span id="base.controller"></span><span id="BASE.CONTROLLER"></span>**ern**</span><span class="sxs-lookup"><span data-stu-id="cabe9-121"><span id="base.controller"></span><span id="BASE.CONTROLLER"></span>**controller**</span></span>
</dt> <dd>

<span data-ttu-id="cabe9-122">Ein Softwareprogramm, das die Lauf Zeit Intelligenz für einen Hardware Anbieter enthält.</span><span class="sxs-lookup"><span data-stu-id="cabe9-122">A software program that contains the runtime intelligence for a hardware provider.</span></span>

</dd> <dt>

<span data-ttu-id="cabe9-123"><span id="base.disk"></span><span id="BASE.DISK"></span>**Diskette**</span><span class="sxs-lookup"><span data-stu-id="cabe9-123"><span id="base.disk"></span><span id="BASE.DISK"></span>**disk**</span></span>
</dt> <dd>

<span data-ttu-id="cabe9-124">Ein physischer Datenträger oder eine Hardware-RAID-LUN.</span><span class="sxs-lookup"><span data-stu-id="cabe9-124">A physical disk or hardware RAID LUN.</span></span> <span data-ttu-id="cabe9-125">Datenträger sind Ziele für die Laufzeitspeicher-e/a-Last. Plug & Play (PNP) unterscheidet nicht zwischen JBOD und LUNs.</span><span class="sxs-lookup"><span data-stu-id="cabe9-125">Disks are targets for runtime storage I/O load; Plug and Play (PNP) does not distinguish between JBOD and LUNs.</span></span>

</dd> <dt>

<span data-ttu-id="cabe9-126"><span id="base.disk_platter"></span><span id="BASE.DISK_PLATTER"></span>**Datenträger Platte**</span><span class="sxs-lookup"><span data-stu-id="cabe9-126"><span id="base.disk_platter"></span><span id="BASE.DISK_PLATTER"></span>**disk platter**</span></span>
</dt> <dd>

<span data-ttu-id="cabe9-127">Eine Teilmenge eines Pakets, das zum Exportieren oder Importieren von Volumes aus einem Paket verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cabe9-127">A subset of a pack used for exporting or importing volumes from a pack.</span></span>

</dd> <dt>

<span data-ttu-id="cabe9-128"><span id="base.disk_pack"></span><span id="BASE.DISK_PACK"></span>**Disk Pack**</span><span class="sxs-lookup"><span data-stu-id="cabe9-128"><span id="base.disk_pack"></span><span id="BASE.DISK_PACK"></span>**disk pack**</span></span>
</dt> <dd>

<span data-ttu-id="cabe9-129">Siehe *Paket*.</span><span class="sxs-lookup"><span data-stu-id="cabe9-129">See *pack*.</span></span>

</dd> <dt>

<span data-ttu-id="cabe9-130"><span id="base.drive"></span><span id="BASE.DRIVE"></span>**Antrie**</span><span class="sxs-lookup"><span data-stu-id="cabe9-130"><span id="base.drive"></span><span id="BASE.DRIVE"></span>**drive**</span></span>
</dt> <dd>

<span data-ttu-id="cabe9-131">Eine physische Datenträger Spindel innerhalb eines Hardware-RAID-Subsystems.</span><span class="sxs-lookup"><span data-stu-id="cabe9-131">A physical disk spindle within a hardware RAID subsystem.</span></span> <span data-ttu-id="cabe9-132">Laufwerke werden vom-Subsystem an LUNs gebunden.</span><span class="sxs-lookup"><span data-stu-id="cabe9-132">Drives are bound into LUNs by the subsystem.</span></span>

</dd> <dt>

<span data-ttu-id="cabe9-133"><span id="base.dynamic_disk"></span><span id="BASE.DYNAMIC_DISK"></span>**dynamischer Datenträger**</span><span class="sxs-lookup"><span data-stu-id="cabe9-133"><span id="base.dynamic_disk"></span><span id="BASE.DYNAMIC_DISK"></span>**dynamic disk**</span></span>
</dt> <dd>

<span data-ttu-id="cabe9-134">Ein von einem Software-RAID-Anbieter verwalteter Datenträger mit Unterstützung für eine flexible Neukonfiguration von Volumes.</span><span class="sxs-lookup"><span data-stu-id="cabe9-134">A disk managed by a software RAID provider with support for flexible volume reconfiguration.</span></span> <span data-ttu-id="cabe9-135">Ein dynamischer Datenträger verwendet eine Partition als Container für Volumes. Es ist keine garantierte Zuordnung vorhanden.</span><span class="sxs-lookup"><span data-stu-id="cabe9-135">A dynamic disk uses a partition as a container for volumes; there is no guaranteed mapping.</span></span>

</dd> <dt>

<span data-ttu-id="cabe9-136"><span id="base.explicit_configuration"></span><span id="BASE.EXPLICIT_CONFIGURATION"></span>**explizite Konfiguration**</span><span class="sxs-lookup"><span data-stu-id="cabe9-136"><span id="base.explicit_configuration"></span><span id="BASE.EXPLICIT_CONFIGURATION"></span>**explicit configuration**</span></span>
</dt> <dd>

<span data-ttu-id="cabe9-137">Eine Konfiguration mit den Parametern, einschließlich des Volumetyps und dem exakten Layout, für eine Auflistung von Zielvolumes.</span><span class="sxs-lookup"><span data-stu-id="cabe9-137">A configuration with the parameters, including the volume type and the exact layout, for a collection of target volumes.</span></span>

</dd> <dt>

<span data-ttu-id="cabe9-138"><span id="base.export"></span><span id="BASE.EXPORT"></span>**Exports**</span><span class="sxs-lookup"><span data-stu-id="cabe9-138"><span id="base.export"></span><span id="BASE.EXPORT"></span>**export**</span></span>
</dt> <dd>

<span data-ttu-id="cabe9-139">Das Verschieben einer Datenträger Platte und aller Volumes, die auf dieser Platte enthalten sind, aus einem Paket.</span><span class="sxs-lookup"><span data-stu-id="cabe9-139">The act of moving a disk platter and all volumes contained on that platter out of a pack.</span></span>

</dd> <dt>

<span data-ttu-id="cabe9-140"><span id="base.extent"></span><span id="BASE.EXTENT"></span>**Ausdehnung**</span><span class="sxs-lookup"><span data-stu-id="cabe9-140"><span id="base.extent"></span><span id="BASE.EXTENT"></span>**extent**</span></span>
</dt> <dd>

<span data-ttu-id="cabe9-141">Ein zusammenhängender Bereich logischer Sektoren, die zu einem einzelnen Volume oder Datenträger beitragen.</span><span class="sxs-lookup"><span data-stu-id="cabe9-141">A contiguous range of logical sectors contributing to a single volume or disk.</span></span> <span data-ttu-id="cabe9-142">Ein Block kann auch der Bereich nicht zugeordneter Sektoren sein.</span><span class="sxs-lookup"><span data-stu-id="cabe9-142">An extent can also be range of unallocated sectors.</span></span> <span data-ttu-id="cabe9-143">Häufig werden einem Endbenutzer in einem Dateisystem Details zu den Details angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cabe9-143">Commonly, a file system displays the extent details to an end-user.</span></span>

</dd> <dt>

<span data-ttu-id="cabe9-144"><span id="base.guid_partition_table_gpt"></span><span id="BASE.GUID_PARTITION_TABLE_GPT"></span>**GUID-Partitionstabelle (GPT)**</span><span class="sxs-lookup"><span data-stu-id="cabe9-144"><span id="base.guid_partition_table_gpt"></span><span id="BASE.GUID_PARTITION_TABLE_GPT"></span>**GUID Partition Table (GPT)**</span></span>
</dt> <dd>

<span data-ttu-id="cabe9-145">Von EFI-Firmware verwendete Strukturen.</span><span class="sxs-lookup"><span data-stu-id="cabe9-145">Structures used by EFI firmware.</span></span> <span data-ttu-id="cabe9-146">GPT ist eines von zwei Datenformaten für die Softwarekonfiguration auf niedrigster Ebene, die von der Platt Form Firmware verwendet werden, um ein Start fähiges Betriebssystem oder ein anderes ausführbares Image</span><span class="sxs-lookup"><span data-stu-id="cabe9-146">GPT is one of two lowest level software configuration data formats used by platform firmware to locate a bootable operating system or other executable image.</span></span>

</dd> <dt>

<span data-ttu-id="cabe9-147"><span id="base.hardware_provider"></span><span id="BASE.HARDWARE_PROVIDER"></span>**Hardware Anbieter**</span><span class="sxs-lookup"><span data-stu-id="cabe9-147"><span id="base.hardware_provider"></span><span id="BASE.HARDWARE_PROVIDER"></span>**hardware provider**</span></span>
</dt> <dd>

<span data-ttu-id="cabe9-148">Eine Sammlung von Software, die auf dem Host ausgeführt wird, ein Busadapter und möglicherweise ein externes Speichersubsystem, das zusammenarbeitet, um RAID-LUNs zu verwalten und zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="cabe9-148">A collection of software that executes on the host, a bus adapter, and possibly an external storage subsystem that works together to surface and manage RAID LUNs.</span></span> <span data-ttu-id="cabe9-149">Hardware Anbieter für die meisten externen Speicher Subsysteme enthalten nur Host basierte Software im Benutzermodus.</span><span class="sxs-lookup"><span data-stu-id="cabe9-149">Hardware providers for most external storage subsystems contain only user-mode, host-based software.</span></span>

</dd> <dt>

<span data-ttu-id="cabe9-150"><span id="base.health"></span><span id="BASE.HEALTH"></span>**gesundheitliche**</span><span class="sxs-lookup"><span data-stu-id="cabe9-150"><span id="base.health"></span><span id="BASE.HEALTH"></span>**health**</span></span>
</dt> <dd>

<span data-ttu-id="cabe9-151">Der aktuelle Fehler Verwaltungsstatus eines Volumes oder einer LUN.</span><span class="sxs-lookup"><span data-stu-id="cabe9-151">The current fault-management status of a volume or a LUN.</span></span>

</dd> <dt>

<span data-ttu-id="cabe9-152"><span id="base.hot_spotting"></span><span id="BASE.HOT_SPOTTING"></span>**heiß sparsam**</span><span class="sxs-lookup"><span data-stu-id="cabe9-152"><span id="base.hot_spotting"></span><span id="BASE.HOT_SPOTTING"></span>**hot sparing**</span></span>
</dt> <dd>

<span data-ttu-id="cabe9-153">Temporäres Hinzufügen eines volumeplex zu einem Volume.</span><span class="sxs-lookup"><span data-stu-id="cabe9-153">Temporarily adding a volume plex to a volume.</span></span>

</dd> <dt>

<span data-ttu-id="cabe9-154"><span id="base.import"></span><span id="BASE.IMPORT"></span>**Importieren**</span><span class="sxs-lookup"><span data-stu-id="cabe9-154"><span id="base.import"></span><span id="BASE.IMPORT"></span>**import**</span></span>
</dt> <dd>

<span data-ttu-id="cabe9-155">Das Verschieben einer Datenträger Platte und sämtlicher Volumes in ein vorhandenes Paket.</span><span class="sxs-lookup"><span data-stu-id="cabe9-155">The act of moving a disk platter and all its volumes into an existing pack.</span></span>

</dd> <dt>

<span data-ttu-id="cabe9-156"><span id="base.JBOD"></span><span id="base.jbod"></span><span id="BASE.JBOD"></span>**nur eine Reihe von Datenträgern (JBOD)**</span><span class="sxs-lookup"><span data-stu-id="cabe9-156"><span id="base.JBOD"></span><span id="base.jbod"></span><span id="BASE.JBOD"></span>**just a bunch of disks (JBOD)**</span></span>
</dt> <dd>

<span data-ttu-id="cabe9-157">Eine Auflistung physischer Spindeln ohne das koordinierte Steuerelement, das von einem Hardware-RAID-Gerät bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="cabe9-157">A collection of physical spindles without the coordinated control provided by a hardware RAID device.</span></span>

</dd> <dt>

<span data-ttu-id="cabe9-158"><span id="base.logical_block_number_LBN"></span><span id="base.logical_block_number_lbn"></span><span id="BASE.LOGICAL_BLOCK_NUMBER_LBN"></span>**logische Block Nummer (LBN)**</span><span class="sxs-lookup"><span data-stu-id="cabe9-158"><span id="base.logical_block_number_LBN"></span><span id="base.logical_block_number_lbn"></span><span id="BASE.LOGICAL_BLOCK_NUMBER_LBN"></span>**logical block number (LBN)**</span></span>
</dt> <dd>

<span data-ttu-id="cabe9-159">Die kleinste adressierbare Einheit von Speicherdaten.</span><span class="sxs-lookup"><span data-stu-id="cabe9-159">The smallest addressable unit of storage data.</span></span> <span data-ttu-id="cabe9-160">LBN wird mit e/a-Befehls Protokollen verwendet.</span><span class="sxs-lookup"><span data-stu-id="cabe9-160">LBN is used with I/O command protocols.</span></span>

</dd> <dt>

<span data-ttu-id="cabe9-161"><span id="base.logical_block_mapping"></span><span id="BASE.LOGICAL_BLOCK_MAPPING"></span>**logische Block Zuordnung**</span><span class="sxs-lookup"><span data-stu-id="cabe9-161"><span id="base.logical_block_mapping"></span><span id="BASE.LOGICAL_BLOCK_MAPPING"></span>**logical block mapping**</span></span>
</dt> <dd>

<span data-ttu-id="cabe9-162">Die Transformation der logischen Blöcke, die einem Anbieter für die vom Anbieter bereitgestellten logischen Blöcke angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="cabe9-162">The transformation of the logical blocks presented to a provider to those exposed by the provider.</span></span>

</dd> <dt>

<span data-ttu-id="cabe9-163"><span id="base.logical_Unit_Number_LUN"></span><span id="base.logical_unit_number_lun"></span><span id="BASE.LOGICAL_UNIT_NUMBER_LUN"></span>**logische Gerätenummer (LUN)**</span><span class="sxs-lookup"><span data-stu-id="cabe9-163"><span id="base.logical_Unit_Number_LUN"></span><span id="base.logical_unit_number_lun"></span><span id="BASE.LOGICAL_UNIT_NUMBER_LUN"></span>**logical unit number (LUN)**</span></span>
</dt> <dd>

<span data-ttu-id="cabe9-164">Eine physisch adressierbare Speichereinheit, die von einem Hardware-RAID-Subsystem bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="cabe9-164">A physically addressable storage unit as surfaced by a hardware RAID subsystem.</span></span> <span data-ttu-id="cabe9-165">Dieser Begriff kann sich auch auf den SCSI-Bezeichner für die Speichereinheit beziehen.</span><span class="sxs-lookup"><span data-stu-id="cabe9-165">This term can also refer to the SCSI identifier for the storage unit.</span></span>

</dd> <dt>

<span data-ttu-id="cabe9-166"><span id="base.LUN_number"></span><span id="base.lun_number"></span><span id="BASE.LUN_NUMBER"></span>**LUN-Nummer**</span><span class="sxs-lookup"><span data-stu-id="cabe9-166"><span id="base.LUN_number"></span><span id="base.lun_number"></span><span id="BASE.LUN_NUMBER"></span>**LUN number**</span></span>
</dt> <dd>

<span data-ttu-id="cabe9-167">Eine Zahl, die ein VDS-Hardware Anbieter einer LUN in einem Array zuweist.</span><span class="sxs-lookup"><span data-stu-id="cabe9-167">A number that a VDS hardware provider assigns to a LUN in an array.</span></span> <span data-ttu-id="cabe9-168">Dies entspricht nicht der "logischen Gerätenummer" in der SCSI-Adresse des Datenträgers.</span><span class="sxs-lookup"><span data-stu-id="cabe9-168">This is not the same as the "logical unit number" in the disk's SCSI address.</span></span>

</dd> <dt>

<span data-ttu-id="cabe9-169"><span id="base.management_service"></span><span id="BASE.MANAGEMENT_SERVICE"></span>**Verwaltungsdienst**</span><span class="sxs-lookup"><span data-stu-id="cabe9-169"><span id="base.management_service"></span><span id="BASE.MANAGEMENT_SERVICE"></span>**management service**</span></span>
</dt> <dd>

<span data-ttu-id="cabe9-170">Ein Softwareprogramm, das nach Bedarf ausgeführt wird, um die Volumekonfiguration, Überwachung oder Fehlerbehandlung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="cabe9-170">A software program that executes as needed to perform volume configuration, monitoring, or fault handling.</span></span>

</dd> <dt>

<span data-ttu-id="cabe9-171"><span id="base.mapping"></span><span id="BASE.MAPPING"></span>**Mapping**</span><span class="sxs-lookup"><span data-stu-id="cabe9-171"><span id="base.mapping"></span><span id="BASE.MAPPING"></span>**mapping**</span></span>
</dt> <dd>

<span data-ttu-id="cabe9-172">Ein Volume, das für das Betriebssystem verfügbar gemacht wird und über einen zugeordneten Volumenamen (Laufwerk Buchstabe) verfügt.</span><span class="sxs-lookup"><span data-stu-id="cabe9-172">A volume that is exposed to the operating system and has an associated volume name (a drive letter).</span></span> <span data-ttu-id="cabe9-173">Ein Dateisystem kann auf ein Volume zugreifen.</span><span class="sxs-lookup"><span data-stu-id="cabe9-173">A volume is accessible by a file system.</span></span>

</dd> <dt>

<span data-ttu-id="cabe9-174"><span id="base.masking"></span><span id="BASE.MASKING"></span>**maskiert**</span><span class="sxs-lookup"><span data-stu-id="cabe9-174"><span id="base.masking"></span><span id="BASE.MASKING"></span>**masking**</span></span>
</dt> <dd>

<span data-ttu-id="cabe9-175">Ein Datenträger, der vom Betriebssystem nicht erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="cabe9-175">A disk not recognized by the operating system.</span></span> <span data-ttu-id="cabe9-176">Ein Datenträger kann mit dem Hardware-RAID-Subsystem, dem Switch, der SCSI-Reserve eines anderen Computer Hosts oder der Software im Datenträger Stapel maskiert werden.</span><span class="sxs-lookup"><span data-stu-id="cabe9-176">A disk can be masked by the hardware RAID subsystem, switch, SCSI RESERVE by another computer host, or software in the disk stack.</span></span>

</dd> <dt>

<span data-ttu-id="cabe9-177"><span id="base.master_Boot_Record_partitioning_MBR"></span><span id="base.master_boot_record_partitioning_mbr"></span><span id="BASE.MASTER_BOOT_RECORD_PARTITIONING_MBR"></span>**Master Boot Record Partitionierung (MBR)**</span><span class="sxs-lookup"><span data-stu-id="cabe9-177"><span id="base.master_Boot_Record_partitioning_MBR"></span><span id="base.master_boot_record_partitioning_mbr"></span><span id="BASE.MASTER_BOOT_RECORD_PARTITIONING_MBR"></span>**master boot record partitioning (MBR)**</span></span>
</dt> <dd>

<span data-ttu-id="cabe9-178">MBR ist eines von zwei Datenformaten für die Softwarekonfiguration auf niedrigster Ebene und wird von der BIOS-Firmware verwendet, um ein Start fähiges Betriebssystem Abbild zu suchen.</span><span class="sxs-lookup"><span data-stu-id="cabe9-178">MBR is one of two lowest level software configuration data formats, and is used by BIOS firmware to locate a bootable operating system image.</span></span>

</dd> <dt>

<span data-ttu-id="cabe9-179"><span id="base.member"></span><span id="BASE.MEMBER"></span>**Kollege**</span><span class="sxs-lookup"><span data-stu-id="cabe9-179"><span id="base.member"></span><span id="BASE.MEMBER"></span>**member**</span></span>
</dt> <dd>

<span data-ttu-id="cabe9-180">Eine Auflistung verketter Datenträger Blöcke, die auf einem oder mehreren Datenträgern enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="cabe9-180">A collection of concatenated disk extents contained on one more disks.</span></span> <span data-ttu-id="cabe9-181">Ein Datenträger kann nur zu einem Mitglied eines Volumes beitragen.</span><span class="sxs-lookup"><span data-stu-id="cabe9-181">A disk can contribute to only one member of a volume.</span></span>

</dd> <dt>

<span data-ttu-id="cabe9-182"><span id="base.mirror"></span><span id="BASE.MIRROR"></span>**OL**</span><span class="sxs-lookup"><span data-stu-id="cabe9-182"><span id="base.mirror"></span><span id="BASE.MIRROR"></span>**mirror**</span></span>
</dt> <dd>

<span data-ttu-id="cabe9-183">Ein Volume oder eine Datenträger Zuordnung, das mindestens zwei identische Datenkopien verwaltet.</span><span class="sxs-lookup"><span data-stu-id="cabe9-183">A volume or disk mapping that maintains two or more identical data copies.</span></span> <span data-ttu-id="cabe9-184">Der Typ der Zuordnung wird auch als RAID-Stufe 1 bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="cabe9-184">The type of mapping is also called RAID Level 1.</span></span>

</dd> <dt>

<span data-ttu-id="cabe9-185"><span id="base.pack"></span><span id="BASE.PACK"></span>**ru**</span><span class="sxs-lookup"><span data-stu-id="cabe9-185"><span id="base.pack"></span><span id="BASE.PACK"></span>**pack**</span></span>
</dt> <dd>

<span data-ttu-id="cabe9-186">Eine Auflistung logischer Volumes und zugrunde liegender Datenträger.</span><span class="sxs-lookup"><span data-stu-id="cabe9-186">A collection of logical volumes and underlying disks.</span></span> <span data-ttu-id="cabe9-187">Ein Paket ist die Einheit des transitiven Abschlusses für ein Volume.</span><span class="sxs-lookup"><span data-stu-id="cabe9-187">A pack is the unit of transitive closure for a volume.</span></span> <span data-ttu-id="cabe9-188">Dynamische Festplatten Pakete und Datenträger Gruppen sind Begriffe für dasselbe Element.</span><span class="sxs-lookup"><span data-stu-id="cabe9-188">Dynamic disk packs and disk groups are terms for the same item.</span></span>

</dd> <dt>

<span data-ttu-id="cabe9-189"><span id="base.parity_stripe"></span><span id="BASE.PARITY_STRIPE"></span>**Paritäts Streifen**</span><span class="sxs-lookup"><span data-stu-id="cabe9-189"><span id="base.parity_stripe"></span><span id="BASE.PARITY_STRIPE"></span>**parity stripe**</span></span>
</dt> <dd>

<span data-ttu-id="cabe9-190">Ein Volume oder eine Datenträger Zuordnung, das Informationen zur Paritäts Überprüfung sowie Daten verwaltet.</span><span class="sxs-lookup"><span data-stu-id="cabe9-190">A volume or disk mapping that maintains parity check information as well as data.</span></span> <span data-ttu-id="cabe9-191">Jeder Lieferant liefert das genaue Mapping-und Schutzschema.</span><span class="sxs-lookup"><span data-stu-id="cabe9-191">Each vendor supplies the exact mapping and protection scheme.</span></span> <span data-ttu-id="cabe9-192">Umfasst RAID 3, 4, 5 und 6.</span><span class="sxs-lookup"><span data-stu-id="cabe9-192">Includes RAID 3, 4, 5, and 6.</span></span>

</dd> <dt>

<span data-ttu-id="cabe9-193"><span id="base.partially_directed_configuration"></span><span id="BASE.PARTIALLY_DIRECTED_CONFIGURATION"></span>**teilweise gesteuerte Konfiguration**</span><span class="sxs-lookup"><span data-stu-id="cabe9-193"><span id="base.partially_directed_configuration"></span><span id="BASE.PARTIALLY_DIRECTED_CONFIGURATION"></span>**partially directed configuration**</span></span>
</dt> <dd>

<span data-ttu-id="cabe9-194">Ein Volume oder eine Datenträger Konfiguration, das nicht vollständig explizit ist.</span><span class="sxs-lookup"><span data-stu-id="cabe9-194">A volume or disk configuration that is not fully explicit.</span></span> <span data-ttu-id="cabe9-195">Der Bindungstyp und eine Auflistung von Ziel Ressourcen werden angegeben. das tatsächliche Layout ist nicht.</span><span class="sxs-lookup"><span data-stu-id="cabe9-195">The binding type and a collection of target resources are specified; the actual layout is not.</span></span> <span data-ttu-id="cabe9-196">Die teilweise gesteuerte Konfiguration ist die gängigste Volumekonfiguration.</span><span class="sxs-lookup"><span data-stu-id="cabe9-196">Partially directed configuration is the most common volume configuration.</span></span>

</dd> <dt>

<span data-ttu-id="cabe9-197"><span id="base.partition"></span><span id="BASE.PARTITION"></span>**spaltet**</span><span class="sxs-lookup"><span data-stu-id="cabe9-197"><span id="base.partition"></span><span id="BASE.PARTITION"></span>**partition**</span></span>
</dt> <dd>

<span data-ttu-id="cabe9-198">Ein zusammenhängender Bereich logischer Sektoren, der durch einen einzelnen Eintrag in der MBR-oder GPT-Struktur beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="cabe9-198">A contiguous range of logical sectors described by a single entry in the MBR or GPT structure.</span></span> <span data-ttu-id="cabe9-199">Auf Basis Datenträgern entsprechen Partitionen direkt einfachen Volumes.</span><span class="sxs-lookup"><span data-stu-id="cabe9-199">On basic disks, partitions directly correspond to simple volumes.</span></span> <span data-ttu-id="cabe9-200">Partitions Strukturen werden von der BIOS-oder EFI-Platt Form Firmware und einem Betriebssystem oder einem anderen Start baren Image gemeinsam genutzt.</span><span class="sxs-lookup"><span data-stu-id="cabe9-200">Partition structures are shared between the BIOS or EFI platform firmware and an operating system or other bootable image.</span></span>

</dd> <dt>

<span data-ttu-id="cabe9-201"><span id="base.path"></span><span id="BASE.PATH"></span>**ADS**</span><span class="sxs-lookup"><span data-stu-id="cabe9-201"><span id="base.path"></span><span id="BASE.PATH"></span>**path**</span></span>
</dt> <dd>

<span data-ttu-id="cabe9-202">Der Zugriffs Pfad von einem Computer auf einen Datenträger oder eine externe Hardware-LUN.</span><span class="sxs-lookup"><span data-stu-id="cabe9-202">The access path from a computer to a disk or external hardware LUN.</span></span>

</dd> <dt>

<span data-ttu-id="cabe9-203"><span id="base.plex"></span><span id="BASE.PLEX"></span>**Plex**</span><span class="sxs-lookup"><span data-stu-id="cabe9-203"><span id="base.plex"></span><span id="BASE.PLEX"></span>**plex**</span></span>
</dt> <dd>

<span data-ttu-id="cabe9-204">Ein Member eines gespiegelten Volumes oder einer gespiegelten LUN.</span><span class="sxs-lookup"><span data-stu-id="cabe9-204">One member of a mirrored volume or LUN.</span></span>

</dd> <dt>

<span data-ttu-id="cabe9-205"><span id="base.port"></span><span id="BASE.PORT"></span>**Port**</span><span class="sxs-lookup"><span data-stu-id="cabe9-205"><span id="base.port"></span><span id="BASE.PORT"></span>**port**</span></span>
</dt> <dd>

<span data-ttu-id="cabe9-206">Der Endpunkt eines Pfads auf einem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="cabe9-206">The endpoint of a path at a disk.</span></span>

</dd> <dt>

<span data-ttu-id="cabe9-207"><span id="base.redundant_array_of_independent_disks_RAID"></span><span id="base.redundant_array_of_independent_disks_raid"></span><span id="BASE.REDUNDANT_ARRAY_OF_INDEPENDENT_DISKS_RAID"></span>**redundantes Array von unabhängigen Datenträgern (RAID)**</span><span class="sxs-lookup"><span data-stu-id="cabe9-207"><span id="base.redundant_array_of_independent_disks_RAID"></span><span id="base.redundant_array_of_independent_disks_raid"></span><span id="BASE.REDUNDANT_ARRAY_OF_INDEPENDENT_DISKS_RAID"></span>**redundant array of independent disks (RAID)**</span></span>
</dt> <dd>

<span data-ttu-id="cabe9-208">Eine Sammlung von Techniken zum Verwalten mehrerer Datenträger.</span><span class="sxs-lookup"><span data-stu-id="cabe9-208">A collection of techniques for managing multiple disks.</span></span>

</dd> <dt>

<span data-ttu-id="cabe9-209"><span id="base.runtime_service"></span><span id="BASE.RUNTIME_SERVICE"></span>**Lauf Zeit Dienst**</span><span class="sxs-lookup"><span data-stu-id="cabe9-209"><span id="base.runtime_service"></span><span id="BASE.RUNTIME_SERVICE"></span>**runtime service**</span></span>
</dt> <dd>

<span data-ttu-id="cabe9-210">Ein Softwareprogramm, das auf einer e/a-Anforderung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cabe9-210">A software program that executes on an I/O-request basis.</span></span>

</dd> <dt>

<span data-ttu-id="cabe9-211"><span id="base.simple_disk"></span><span id="BASE.SIMPLE_DISK"></span>**einfache Festplatte**</span><span class="sxs-lookup"><span data-stu-id="cabe9-211"><span id="base.simple_disk"></span><span id="BASE.SIMPLE_DISK"></span>**simple disk**</span></span>
</dt> <dd>

<span data-ttu-id="cabe9-212">Eine Spindel, die nicht mit einem Hardware-RAID-Controller verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="cabe9-212">A spindle that is not connected to a hardware RAID controller.</span></span> <span data-ttu-id="cabe9-213">Siehe auch nur eine Reihe von Datenträgern (JBOD).</span><span class="sxs-lookup"><span data-stu-id="cabe9-213">See also Just a Bunch Of Disks (JBOD).</span></span>

</dd> <dt>

<span data-ttu-id="cabe9-214"><span id="base.software_provider"></span><span id="BASE.SOFTWARE_PROVIDER"></span>**Softwareanbieter**</span><span class="sxs-lookup"><span data-stu-id="cabe9-214"><span id="base.software_provider"></span><span id="BASE.SOFTWARE_PROVIDER"></span>**software provider**</span></span>
</dt> <dd>

<span data-ttu-id="cabe9-215">Host basierte Software, die logische Volumes verfügbar macht und auf Datenträgern arbeitet.</span><span class="sxs-lookup"><span data-stu-id="cabe9-215">Host-based software that exposes logical volumes and operates on disks.</span></span> <span data-ttu-id="cabe9-216">Ein Softwareanbieter umfasst Lauf Zeit Dienste im Kernel Modus, Konfigurationsdaten und benutzermodusverwaltungsdienste.</span><span class="sxs-lookup"><span data-stu-id="cabe9-216">A software provider includes kernel-mode runtime services, configuration data, and user-mode management services.</span></span>

</dd> <dt>

<span data-ttu-id="cabe9-217"><span id="base.span"></span><span id="BASE.SPAN"></span>**Spanne**</span><span class="sxs-lookup"><span data-stu-id="cabe9-217"><span id="base.span"></span><span id="BASE.SPAN"></span>**span**</span></span>
</dt> <dd>

<span data-ttu-id="cabe9-218">Eine lineare Zuordnung von Volumes oder Datenträgern mehrerer diskontinuierlichen Datenträger-oder Laufwerks Blöcke.</span><span class="sxs-lookup"><span data-stu-id="cabe9-218">A volume or disk linear mapping of multiple discontinuous disk or drive extents.</span></span> <span data-ttu-id="cabe9-219">Die Blöcke können sich auf einem oder mehreren Spindeln oder LUNs befinden.</span><span class="sxs-lookup"><span data-stu-id="cabe9-219">The extents can be on one or more spindles or LUNs.</span></span>

</dd> <dt>

<span data-ttu-id="cabe9-220"><span id="base.spindle"></span><span id="BASE.SPINDLE"></span>**Maschinen**</span><span class="sxs-lookup"><span data-stu-id="cabe9-220"><span id="base.spindle"></span><span id="BASE.SPINDLE"></span>**spindle**</span></span>
</dt> <dd>

<span data-ttu-id="cabe9-221">Eine physische Einheit von Datenträger Speicher.</span><span class="sxs-lookup"><span data-stu-id="cabe9-221">A physical unit of disk storage.</span></span>

</dd> <dt>

<span data-ttu-id="cabe9-222"><span id="base.stacking"></span><span id="BASE.STACKING"></span>**Staffeln**</span><span class="sxs-lookup"><span data-stu-id="cabe9-222"><span id="base.stacking"></span><span id="BASE.STACKING"></span>**stacking**</span></span>
</dt> <dd>

<span data-ttu-id="cabe9-223">Der Vorgang des Erstellens eines Volumes oder einer LUN durch Ausführen mehrerer logischer Block Mapping-Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="cabe9-223">The act of constructing a volume or LUN by performing more than one logical block mapping operation.</span></span> <span data-ttu-id="cabe9-224">Ein Beispiel hierfür ist ein gespiegeltes Stripeset.</span><span class="sxs-lookup"><span data-stu-id="cabe9-224">An example is a mirrored striped volume.</span></span> <span data-ttu-id="cabe9-225">Das häufigste Stapeln tritt auf, wenn Software-RAID für LUNs verwendet wird, die von Hardware-RAID erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="cabe9-225">The most common stacking occurs when software RAID is used across LUNs constructed by hardware RAID.</span></span>

</dd> <dt>

<span data-ttu-id="cabe9-226"><span id="base.stripe"></span><span id="BASE.STRIPE"></span>**Reifen**</span><span class="sxs-lookup"><span data-stu-id="cabe9-226"><span id="base.stripe"></span><span id="BASE.STRIPE"></span>**stripe**</span></span>
</dt> <dd>

<span data-ttu-id="cabe9-227">Ein Volume oder eine Datenträger Zuordnung, das zusammenhängende Blöcke über mehrere Volumes, Datenträger oder Laufwerke hinweg überlappt.</span><span class="sxs-lookup"><span data-stu-id="cabe9-227">A volume or disk mapping that interleaves contiguous extents across multiple volumes, disks, or drives.</span></span> <span data-ttu-id="cabe9-228">Diese Zuordnung wird auch als RAID 0 bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="cabe9-228">This mapping is also called RAID 0.</span></span>

</dd> <dt>

<span data-ttu-id="cabe9-229"><span id="base.status"></span><span id="BASE.STATUS"></span>**Stands**</span><span class="sxs-lookup"><span data-stu-id="cabe9-229"><span id="base.status"></span><span id="BASE.STATUS"></span>**status**</span></span>
</dt> <dd>

<span data-ttu-id="cabe9-230">Die aktuelle Verfügbarkeit eines Volumes, einer Festplatte oder eines Laufwerks.</span><span class="sxs-lookup"><span data-stu-id="cabe9-230">The current availability of a volume, disk, or drive.</span></span>

</dd> <dt>

<span data-ttu-id="cabe9-231"><span id="base.subsystem"></span><span id="BASE.SUBSYSTEM"></span>**System**</span><span class="sxs-lookup"><span data-stu-id="cabe9-231"><span id="base.subsystem"></span><span id="BASE.SUBSYSTEM"></span>**subsystem**</span></span>
</dt> <dd>

<span data-ttu-id="cabe9-232">Die Instanziierung von Hardware Anbieter Software.</span><span class="sxs-lookup"><span data-stu-id="cabe9-232">The instantiation of hardware-provider software.</span></span> <span data-ttu-id="cabe9-233">Ein Subsystem enthält mindestens einen Controller und ein Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="cabe9-233">A subsystem contains at least one controller and one drive.</span></span> <span data-ttu-id="cabe9-234">Wenn das Subsystem für den Computer extern ist, wird von einem oder mehreren Netzwerkpfaden das Subsystem mit dem Computer verbunden.</span><span class="sxs-lookup"><span data-stu-id="cabe9-234">If the subsystem is external to the computer, one or more network paths connect the subsystem to the computer.</span></span>

</dd> <dt>

<span data-ttu-id="cabe9-235"><span id="base.jello"></span><span id="BASE.JELLO"></span>**Übergangsstatus**</span><span class="sxs-lookup"><span data-stu-id="cabe9-235"><span id="base.jello"></span><span id="BASE.JELLO"></span>**transition state**</span></span>
</dt> <dd>

<span data-ttu-id="cabe9-236">Der Status der logischen und physischen Zuordnung, die geändert wird.</span><span class="sxs-lookup"><span data-stu-id="cabe9-236">Status of the logical to physical mapping that is undergoing change.</span></span>

</dd> <dt>

<span data-ttu-id="cabe9-237"><span id="base.uninitialized_disk"></span><span id="BASE.UNINITIALIZED_DISK"></span>**nicht initialisierter Datenträger**</span><span class="sxs-lookup"><span data-stu-id="cabe9-237"><span id="base.uninitialized_disk"></span><span id="BASE.UNINITIALIZED_DISK"></span>**uninitialized disk**</span></span>
</dt> <dd>

<span data-ttu-id="cabe9-238">Ein Datenträger, der kein Mitglied eines Pakets ist.</span><span class="sxs-lookup"><span data-stu-id="cabe9-238">A disk that is not a member of a pack.</span></span>

</dd> <dt>

<span data-ttu-id="cabe9-239"><span id="base.unmasked_disk"></span><span id="BASE.UNMASKED_DISK"></span>**unmaskierte Festplatte**</span><span class="sxs-lookup"><span data-stu-id="cabe9-239"><span id="base.unmasked_disk"></span><span id="BASE.UNMASKED_DISK"></span>**unmasked disk**</span></span>
</dt> <dd>

<span data-ttu-id="cabe9-240">Ein Datenträger, der für das Betriebssystem sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="cabe9-240">A disk that is visible to the operating system.</span></span> <span data-ttu-id="cabe9-241">Der Inhalt eines nicht maskierten Datenträgers ist für Softwareverteilungs-Manager, Dateisysteme usw. sichtbar.</span><span class="sxs-lookup"><span data-stu-id="cabe9-241">The contents of an unmasked disk are visible to software volume managers, file systems, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="cabe9-242"><span id="base.volume"></span><span id="BASE.VOLUME"></span>**Handels**</span><span class="sxs-lookup"><span data-stu-id="cabe9-242"><span id="base.volume"></span><span id="BASE.VOLUME"></span>**volume**</span></span>
</dt> <dd>

<span data-ttu-id="cabe9-243">Eine Reihe von Datenträger Blöcke, die an einen praktisch zusammenhängenden Bereich logischer Blöcke gebunden sind.</span><span class="sxs-lookup"><span data-stu-id="cabe9-243">A number of disk extents bound into a virtually contiguous range of logical blocks.</span></span> <span data-ttu-id="cabe9-244">Auf ein Volume kann über einen Laufwerk Buchstaben, einen bereitgestellten Ordner oder einen VolumeGuid-Pfad zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="cabe9-244">A volume can be accessed through a drive letter, a mounted folder, or a volume GUID path.</span></span>

</dd> </dl>

 

 
