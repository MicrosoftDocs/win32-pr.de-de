---
description: Datenträgerobjekt
ms.assetid: 65e14273-8127-4667-b5c8-362ad54b4782
title: Datenträgerobjekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5979e6e2e25ee6ded15b987ddbcda0c5c135f92452174853577d7781475c5d03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137227"
---
# <a name="disk-object"></a>Datenträgerobjekt

\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [Virtual Disk Service](virtual-disk-service-portal.md) durch die Windows Storage Verwaltungs-API. [](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)\]

Ein Datenträgerobjekt modelliert einen hostbasierten physischen Datenträger. Der Softwareanbieter, der auf dem lokalen Host ausgeführt wird, kann auf eine LUN als Datenträger zugreifen, wenn das LUN-Objekt dem lokalen Host entmaskiert wird. Weitere Informationen zur LUN-Maskierung finden Sie unter [LUN-Objekt.](lun-object.md)

Jedes Datenträgerobjekt trägt zu genau einem Paketobjekt bei. Ein Datenträger kann jedoch zu einer beliebigen Anzahl von Volumes innerhalb eines Pakets beitragen. Sie können einen Datenträger als Hotspare festlegen.

## <a name="partition-to-volume-mapping"></a>Partition-zu-Volume-Zuordnung

Das Betriebssystem unterstützt sowohl Basisdatenträger als auch dynamische Datenträger. VDS bietet einen Basisanbieter und einen dynamischen Anbieter zum Verwalten dieser Datenträgertypen. Basisdatenträger sind nie fehlertolerant. Dynamische Datenträger können fehlertolerant sein, wenn das Betriebssystem eine solche Volumebindung zu lässt. Basisdatenträger und dynamische Datenträger können Partitionen enthalten, die nach einem der folgenden Partitionsstile strukturiert sind: MASTER BOOT RECORD (MBR) oder GUID-Partitionstabelle (GPT). Die MBR-Partitionierung verfügt über bis zu vier primäre Partitionen oder drei primäre Partitionen sowie eine erweiterte Partition mit unendlichen logischen Laufwerken. Die GPT-Partitionierung bietet bis zu 128 primäre Partitionen.

Die folgende Beschreibung ist allgemein. Es zeigt die typische Beziehung zwischen Partitionen und Volumes, für die es mehrere Ausnahmen gibt. Eine ausführliche Beschreibung der Zuordnung von Partition zu Volume finden Sie unter [**IVdsAdvancedDisk-Schnittstelle.**](/windows/desktop/api/Vds/nn-vds-ivdsadvanceddisk) Die Zuordnung von Partition zu Volume variiert je nach Typ des Datenträgers (einfach oder dynamisch).

-   Basisfestplatten

    Eine Partition auf einem Basisdatenträger wird in den meisten Fällen direkt einem Volume zuteil und kann als MBR- oder GPT-Partition formatiert werden. Die folgende Abbildung zeigt die Zuordnung für beide Versionen von MBR-Partitionen. Im ersten Fall werden Partitionen (P1 bis P4) direkt Volumes (V1 bis V4) zuordnen. Eine erweiterte Partition (Ext) ersetzt P4 im zweiten MBR-Stil. Die Anzahl der logischen Laufwerke innerhalb der erweiterten Partition, die Volumes zuordnen, ist unbegrenzt.

    ![Zeigt zwei Zuordnungsoptionen für M B R-Partitionen an.](images/vdsbasicmapping.png)

    Die GPT-Partitionen (P1 bis P128) in der nächsten Abbildung sind volumes (V1 bis V128) direkt zuordnen, wenn alle verfügbaren Partitionen verwendet werden. Ein GPT-Datenträger nutzt keine erweiterte Partition, um die Benutzerfreundlichkeit zu verbessern.

    ![Zeigt eine GPT-Partition an.](images/vdsbasicmappinggpt.png)

-   Dynamische Datenträger

    Ein spezieller Partitionstyp auf einem dynamischen Datenträger wird einer großen Anzahl von Volumes angezeigt. Einen geschätzten Grenzwert, der vom dynamischen Anbieter erzwingt wird, finden Sie im [Paketobjekt](pack-object.md). Wie die folgende Abbildung zeigt, kann es eine beliebige Anzahl von Extents in P1 geben, die Volumes zuordnen.

    ![Zeigt einen speziellen Partitionstyp auf einem dynamischen Datenträger an.](images/vdsdynamicmapping.png)

Unabhängig vom Datenträgertyp kann ein Datenträger einen oder mehrere Datenträgerdungen enthalten. Ein Datenträgerbereich ist ein zusammenhängender Bereich logischer Blöcke, die vom Datenträger verfügbar gemacht werden. Ein Datenträgerbereich kann beispielsweise ein gesamtes Volume, einen Teil eines übergreifenden Volumes, ein Member eines Striping-Volumes oder einen Plex eines gespiegelten Volumes darstellen.

### <a name="working-with-disks"></a>Arbeiten mit Datenträgern

Verwenden Sie [**die IVdsPack::AddDisk-Methode,**](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk) um einem vorhandenen Paket einen Datenträger hinzuzufügen. Aufrufer können einen Zeiger auf einen bestimmten Datenträger erhalten, indem sie das gewünschte Datenträgerobjekt aus der Enumeration auswählen, die von der [**IVdsPack::QueryDisks-Methode zurückgegeben**](/windows/desktop/api/Vds/nf-vds-ivdspack-querydisks) wird. Ebenso können Sie die [**IVdsDisk::GetPack-Methode**](/windows/desktop/api/Vds/nf-vds-ivdsdisk-getpack) aufrufen, um zu bestimmen, welches Paket einen bestimmten Datenträger enthält.

Sie können einen Datenträger von einem Paket in ein anderes verschieben, indem Sie die [**IVdsPack::MigrateDisks-Methode**](/windows/desktop/api/Vds/nf-vds-ivdspack-migratedisks) aufrufen. (VDS unterstützt nicht die Migration eines Basisdatenträgers zwischen Paketen, die vom Basic-Anbieter gesteuert werden.) Sie können ein Paket auch auf einen anderen Host verschieben, indem Sie alle Datenträger im Paket physisch auf den neuen Host verschieben. Das Paket wird mit den Datenträgern bewegt und als Fremdpaket auf dem neuen Host angezeigt. Anweisungen finden Sie unter [Hinzufügen von Fremddatenträgern zu einem Paket.](adding-foreign-disks-to-a-pack.md)

Zusätzlich zu einem Objektbezeichner, einem Namen, einer Adresse, einem Gerätetyp und einem Medientyp enthalten Datenträgerobjekteigenschaften den Datenträgerstatus, die Integrität und flags. die Größe in Bytes, Bytes pro Sektor, Sektoren pro Spur und Spuren pro Zylinder; und den Bus- und Partitionstyp.

In der folgenden Tabelle sind verwandte Schnittstellen, Enumerationen und Strukturen aufgeführt.



| type                                              | Element                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Schnittstellen, die von diesem Objekt immer verfügbar gemacht werden | [**IVdsDisk**](/windows/desktop/api/Vds/nn-vds-ivdsdisk), [**IVdsDiskOnline**](/windows/desktop/api/Vds/nn-vds-ivdsdiskonline), [**IVdsAdvancedDisk**](/windows/desktop/api/Vds/nn-vds-ivdsadvanceddisk), [**IVdsAdvancedDisk2**](/windows/desktop/api/Vds/nn-vds-ivdsadvanceddisk2), [**IVdsDiskPartitionMF**](/windows/desktop/api/Vds/nn-vds-ivdsdiskpartitionmf), [**IVdsDiskPartitionMF2**](/windows/desktop/api/Vds/nn-vds-ivdsdiskpartitionmf2)und [**IVdsCreatePartitionEx**](/windows/desktop/api/Vds/nn-vds-ivdscreatepartitionex). **Windows Server 2008:** Die [**IVdsDiskPartitionMF2-Schnittstelle**](/windows/desktop/api/Vds/nn-vds-ivdsdiskpartitionmf2) wird nicht unterstützt.<br/> **Windows Vista:** Die [**IVdsDiskOnline-Schnittstelle**](/windows/desktop/api/Vds/nn-vds-ivdsdiskonline) wird erst nach Windows Vista mit Service Pack 1 (SP1) unterstützt. Verwenden [**Sie stattdessen IVdsDisk2.**](/windows/desktop/api/Vds/nn-vds-ivdsdisk2) Die [**IVdsDiskPartitionMF2-Schnittstelle**](/windows/desktop/api/Vds/nn-vds-ivdsdiskpartitionmf2) wird nicht unterstützt.<br/> **Windows Server 2003:** Die [**Schnittstellen IVdsAdvancedDisk2,**](/windows/desktop/api/Vds/nn-vds-ivdsadvanceddisk2) [**IVdsDisk2,**](/windows/desktop/api/Vds/nn-vds-ivdsdisk2) [**IVdsDiskOnline,**](/windows/desktop/api/Vds/nn-vds-ivdsdiskonline) [**IVdsDiskPartitionMF**](/windows/desktop/api/Vds/nn-vds-ivdsdiskpartitionmf)und [**IVdsDiskPartitionMF2**](/windows/desktop/api/Vds/nn-vds-ivdsdiskpartitionmf2) werden nicht unterstützt.<br/> |
| Schnittstellen, die von diesem Objekt verfügbar gemacht werden können     | [**IVdsRemovable**](/windows/desktop/api/Vds/nn-vds-ivdsremovable). (Weitere [Schnittstellen, die verfügbar gemacht](lun-object.md) werden, wenn der Datenträger eine LUN ist, finden Sie unter LUN-Objekt.)<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Zugeordnete Enumerationen                           | [**VDS \_ \_DATENTRÄGERFLAG,**](/windows/desktop/api/Vds/ne-vds-vds_disk_flag) [**VDS \_ DISK \_ STATUS,**](/windows/desktop/api/Vds/ne-vds-vds_disk_status) [**VDS \_ PARTITION \_ FLAG,**](/windows/desktop/api/Vds/ne-vds-vds_partition_flag) [**VDS PARTITION \_ \_ STYLE**](/windows/win32/api/vds/ne-vds-__vds_partition_style)UND [**VDS DISK EXTENT \_ \_ \_ TYPE**](/windows/desktop/api/Vds/ne-vds-vds_disk_extent_type).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Zugeordnete Strukturen                             | [**VDS \_ \_DATENTRÄGERPROP,**](/windows/desktop/api/Vds/ns-vds-vds_disk_prop) [**VDS \_ DISK \_ NOTIFICATION,**](/windows/desktop/api/Vds/ns-vds-vds_disk_notification)VDS INPUT [**\_ \_ DISK,**](/windows/desktop/api/Vds/ns-vds-vds_input_disk) [**VDS PARTITION \_ \_ PROP,**](/windows/desktop/api/Vds/ns-vds-vds_partition_prop) [**VDS PARTITION INFO \_ \_ \_ GPT,**](/windows/desktop/api/Vds/ns-vds-vds_partition_info_gpt) [**VDS PARTITION \_ INFO \_ \_ MBR**](/windows/desktop/api/Vds/ns-vds-vds_partition_info_mbr)UND [**VDS DISK \_ \_ EXTENT**](/windows/desktop/api/Vds/ns-vds-vds_disk_extent).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Softwareanbieterobjekte](software-provider-objects.md)
</dt> <dt>

[Pack-Objekt](pack-object.md)
</dt> <dt>

[LUN-Objekt](lun-object.md)
</dt> <dt>

[Hinzufügen von Fremddatenträgern zu einem Paket](adding-foreign-disks-to-a-pack.md)
</dt> </dl>

 

