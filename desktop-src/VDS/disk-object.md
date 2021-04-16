---
description: Disk-Objekt
ms.assetid: 65e14273-8127-4667-b5c8-362ad54b4782
title: Disk-Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d629f642d83c9e2c6954a4f09fe09091a2bbce9
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2021
ms.locfileid: "104562202"
---
# <a name="disk-object"></a>Disk-Objekt

\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [virtuellen Festplatten Dienstanbieter](virtual-disk-service-portal.md) durch die [Windows-Speicherverwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)ersetzt.\]

Ein Datenträger Objekt modelliert einen Host basierten, physischen Datenträger. Der auf dem lokalen Host ausgeführt Softwareanbieter kann auf eine LUN als Datenträger zugreifen, wenn das LUN-Objekt für den lokalen Host unmaskiert ist. Weitere Informationen über die LUN-Maskierung finden Sie unter dem [LUN-Objekt](lun-object.md).

Jedes Datenträger Objekt trägt zu genau einem Paket Objekt bei. ein Datenträger kann jedoch Blöcke zu einer beliebigen Anzahl von Volumes innerhalb eines Pakets beitragen. Sie können einen Datenträger als Hotspare festlegen.

## <a name="partition-to-volume-mapping"></a>Zuordnung von Partitionen zu Volumes

Das Betriebssystem unterstützt sowohl grundlegende als auch dynamische Datenträger. VDS bietet einen grundlegenden Anbieter und einen dynamischen Anbieter zum Verwalten dieser Datenträger Typen. Basis Datenträger sind nie fehlertolerant. Dynamische Datenträger können fehlertolerant sein, wenn das Betriebssystem eine solche volumebindung zulässt. Basis-und dynamische Datenträger können Partitionen enthalten, die gemäß einem der folgenden Partitions Stile strukturiert sind: Master Boot Record (MBR) oder GUID-Partitionstabelle (GPT). Die MBR-Partitionierung verfügt über bis zu vier primäre Partitionen oder drei primäre Partitionen sowie eine erweiterte Partition mit unbegrenzten logischen Laufwerken. Die GPT-Partitionierung ermöglicht bis zu 128 primäre Partitionen.

Die Beschreibung, die folgt, ist allgemein. Es zeigt die typische Beziehung zwischen Partitionen und Volumes, auf die mehrere Ausnahmen vorhanden sind. Eine ausführliche Beschreibung der Zuordnung von Partitionen zu Volumes finden Sie unter der [**ivdsadvanceddisk**](/windows/desktop/api/Vds/nn-vds-ivdsadvanceddisk) -Schnittstelle. Die Zuordnung von Partitionen zu Volumes variiert abhängig vom Typ des Datenträgers, von Basic oder dynamisch.

-   Basisfestplatten

    Eine Partition auf einem Basis Datenträger wird in den meisten Fällen direkt einem Volume zugeordnet und kann als MBR-oder GPT-Partition formatiert werden. Die folgende Abbildung zeigt die Zuordnung für beide Versionen von MBR-Partitionen. Im ersten Fall werden Partitionen (P1 bis P4) direkt den Volumes (V1 bis V4) zugeordnet. Eine erweiterte Partition (ext) ersetzt P4 im zweiten MBR-Stil. Die Anzahl logischer Laufwerke in der erweiterten Partition, die Volumes zugeordnet sind, ist unbegrenzt.

    ![Zeigt zwei Mapping-Optionen für M B-R-Partitionen an.](images/vdsbasicmapping.png)

    Die GPT-Partitionen (P1 bis P128) in der nächsten Abbildung werden direkt den Volumes (V1 bis V128) zugeordnet, wenn alle verfügbaren Partitionen verwendet werden. Ein GPT-Datenträger verwendet keine erweiterte Partition, um die Benutzerfreundlichkeit zu verbessern.

    ![Zeigt eine GPT-Partition an.](images/vdsbasicmappinggpt.png)

-   Dynamische Datenträger

    Ein spezieller Partitionstyp auf einem dynamischen Datenträger ist einer großen Anzahl von Volumes zugeordnet. Informationen zu einem geschätzten Grenzwert, der vom dynamischen Anbieter vorgegeben wird, finden Sie im [Pack-Objekt](pack-object.md). Wie die folgende Abbildung zeigt, kann eine beliebige Anzahl von Blöcken in P1 vorhanden sein, die Volumes zugeordnet sind.

    ![Zeigt einen speziellen Partitionstyp auf einem dynamischen Datenträger an.](images/vdsdynamicmapping.png)

Unabhängig vom Datenträger Datenträger kann ein Datenträger einen oder mehrere Datenträger Blöcke enthalten. Ein Datenträger Block ist ein zusammenhängender Bereich logischer Blöcke, die vom Datenträger verfügbar gemacht werden. Beispielsweise kann ein Datenträger Block ein gesamtes Volume, einen Teil eines übergreifenden Volumes, ein Mitglied eines Stripesetvolumes oder einen Plex eines gespiegelten Volumes darstellen.

### <a name="working-with-disks"></a>Arbeiten mit Datenträgern

Verwenden Sie die [**ivdspack:: adddisk**](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk) -Methode zum Hinzufügen eines Datenträgers zu einem vorhandenen Paket. Aufrufer können einen Zeiger auf einen bestimmten Datenträger abrufen, indem Sie das gewünschte Datenträger Objekt aus der-Enumeration auswählen, das von der [**ivdspack:: querydisks**](/windows/desktop/api/Vds/nf-vds-ivdspack-querydisks) -Methode zurückgegeben wird. Ebenso können Sie die [**ivdsdisk:: getpack**](/windows/desktop/api/Vds/nf-vds-ivdsdisk-getpack) -Methode aufrufen, um zu bestimmen, welches Paket einen bestimmten Datenträger enthält.

Sie können einen Datenträger von einem Paket in einen anderen verschieben, indem Sie die [**ivdspack:: MigrateDisks**](/windows/desktop/api/Vds/nf-vds-ivdspack-migratedisks) -Methode aufrufen. (VDS unterstützt nicht die Migration eines Basis Datenträgers zwischen vom Basic-Anbieter kontrollierten Paketen.) Sie können ein Paket auch auf einen anderen Host verschieben, indem Sie alle Datenträger im Paket physisch auf den neuen Host verschieben. Das Paket wird mit den Datenträgern verschoben und als fremd Paket auf dem neuen Host angezeigt. Anweisungen hierzu finden [Sie unter Hinzufügen von fremden Datenträgern zu einem Paket](adding-foreign-disks-to-a-pack.md).

Zusätzlich zu einem Objekt Bezeichner, einem Namen, einer Adresse, einem Gerätetyp und einem Medientyp enthalten die Eigenschaften des Datenträger Objekts den Datenträger Status, den Zustand und die Flags. die Größe in Bytes, Bytes pro Sektor, Sektoren pro Spur und Spuren pro Zylinder. und den Bus-und Partitionstyp.

In der folgenden Tabelle werden verwandte Schnittstellen, Enumerationen und Strukturen aufgelistet.



| type                                              | Element                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Schnittstellen, die von diesem Objekt immer verfügbar gemacht werden | [**Ivdsdisk**](/windows/desktop/api/Vds/nn-vds-ivdsdisk), [**ivdsdiskonline**](/windows/desktop/api/Vds/nn-vds-ivdsdiskonline), [**ivdsadvanceddisk**](/windows/desktop/api/Vds/nn-vds-ivdsadvanceddisk), [**IVdsAdvancedDisk2**](/windows/desktop/api/Vds/nn-vds-ivdsadvanceddisk2), [**ivdsdiskpartitionmf**](/windows/desktop/api/Vds/nn-vds-ivdsdiskpartitionmf), [**IVdsDiskPartitionMF2**](/windows/desktop/api/Vds/nn-vds-ivdsdiskpartitionmf2)und [**ivdscreatepartitionex**](/windows/desktop/api/Vds/nn-vds-ivdscreatepartitionex). **Windows Server 2008:** Die [**IVdsDiskPartitionMF2**](/windows/desktop/api/Vds/nn-vds-ivdsdiskpartitionmf2) -Schnittstelle wird nicht unterstützt.<br/> **Windows Vista:** Die [**ivdsdiskonline**](/windows/desktop/api/Vds/nn-vds-ivdsdiskonline) -Schnittstelle wird erst ab Windows Vista mit Service Pack 1 (SP1) unterstützt. Verwenden Sie stattdessen [**IVdsDisk2**](/windows/desktop/api/Vds/nn-vds-ivdsdisk2) . Die [**IVdsDiskPartitionMF2**](/windows/desktop/api/Vds/nn-vds-ivdsdiskpartitionmf2) -Schnittstelle wird nicht unterstützt.<br/> **Windows Server 2003:** Die Schnittstellen [**IVdsAdvancedDisk2**](/windows/desktop/api/Vds/nn-vds-ivdsadvanceddisk2), [**IVdsDisk2**](/windows/desktop/api/Vds/nn-vds-ivdsdisk2), [**ivdsdiskonline**](/windows/desktop/api/Vds/nn-vds-ivdsdiskonline), [**ivdsdiskpartitionmf**](/windows/desktop/api/Vds/nn-vds-ivdsdiskpartitionmf)und [**IVdsDiskPartitionMF2**](/windows/desktop/api/Vds/nn-vds-ivdsdiskpartitionmf2) werden nicht unterstützt.<br/> |
| Schnittstellen, die von diesem Objekt verfügbar gemacht werden können     | [**Ivdswechsel**](/windows/desktop/api/Vds/nn-vds-ivdsremovable). (Siehe [LUN-Objekt](lun-object.md) für zusätzliche Schnittstellen, die verfügbar gemacht werden, wenn der Datenträger eine LUN ist.)<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Zugehörige Enumerationen                           | [**VDS \_ \_**](/windows/desktop/api/Vds/ne-vds-vds_disk_flag)Datenträgerflag, VDS-Datenträger [**\_ \_ Status**](/windows/desktop/api/Vds/ne-vds-vds_disk_status), [**VDS- \_ \_ partitionsflag**](/windows/desktop/api/Vds/ne-vds-vds_partition_flag), [**VDS- \_ Partitions \_ Stil**](/windows/win32/api/vds/ne-vds-__vds_partition_style)und [**VDS \_ \_ \_**](/windows/desktop/api/Vds/ne-vds-vds_disk_extent_type)-Datenträger Block.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Zugeordnete Strukturen                             | [**VDS \_ Daten \_ Träger Stütze**](/windows/desktop/api/Vds/ns-vds-vds_disk_prop), VDS-Datenträger [**\_ \_ Benachrichtigung**](/windows/desktop/api/Vds/ns-vds-vds_disk_notification), [**VDS- \_ Eingabe \_**](/windows/desktop/api/Vds/ns-vds-vds_input_disk)Datenträger, [**VDS- \_ Partitions \_ Stütze**](/windows/desktop/api/Vds/ns-vds-vds_partition_prop), [**VDS- \_ Partitions \_ Info- \_ GPT**](/windows/desktop/api/Vds/ns-vds-vds_partition_info_gpt), [**VDS- \_ Partitions \_ Informationen \_ MBR**](/windows/desktop/api/Vds/ns-vds-vds_partition_info_mbr)und VDS-Datenträger Block [**\_ \_**](/windows/desktop/api/Vds/ns-vds-vds_disk_extent).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Software Anbieter Objekte](software-provider-objects.md)
</dt> <dt>

[Pack-Objekt](pack-object.md)
</dt> <dt>

[LUN-Objekt](lun-object.md)
</dt> <dt>

[Hinzufügen von fremden Datenträgern zu einem Paket](adding-foreign-disks-to-a-pack.md)
</dt> </dl>

 

