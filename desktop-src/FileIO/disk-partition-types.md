---
description: Gültige Partitionstypen, die von Datenträger Treibern verwendet werden.
ms.assetid: b2e15b93-a02b-4d6f-b242-b5ec9a30c97b
title: Datenträger-Partitionstypen (winioctl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4109d4386d4892ca695fe8876b61501110cef455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359470"
---
# <a name="disk-partition-types"></a>Datenträger-Partitionstypen

In der folgenden Tabelle sind die gültigen Partitionstypen aufgeführt, die von Datenträger Treibern verwendet werden.



| Konstante/Wert                                                                                                                                                                                                                                      | BESCHREIBUNG                                                                                                                                                |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PARTITION_ENTRY_UNUSED"></span><span id="partition_entry_unused"></span><dl> <dt>**Partition \_ Eintrag nicht \_ verwendet**</dt> <dt>0x00</dt> </dl> | Eine nicht verwendete Eintrag-Partition.<br/>                                                                                                                      |
| <span id="PARTITION_EXTENDED"></span><span id="partition_extended"></span><dl> <dt>**Partition \_ Erweitert**</dt> <dt>0x05</dt> </dl>              | Eine erweiterte Partition.<br/>                                                                                                                          |
| <span id="PARTITION_FAT_12"></span><span id="partition_fat_12"></span><dl> <dt>**Partition \_ FAT \_ 12**</dt> <dt>0x01</dt> </dl>                   | Eine FAT12-Dateisystem Partition.<br/>                                                                                                                  |
| <span id="PARTITION_FAT_16"></span><span id="partition_fat_16"></span><dl> <dt>**Partition \_ FAT \_ 16**</dt> <dt>0x04</dt> </dl>                   | Eine FAT16-Dateisystem Partition.<br/>                                                                                                                  |
| <span id="PARTITION_FAT32"></span><span id="partition_fat32"></span><dl> <dt>**Partition \_ FAT32**</dt> <dt>0x0B</dt> </dl>                       | Eine FAT32-Dateisystem Partition.<br/>                                                                                                                  |
| <span id="PARTITION_IFS"></span><span id="partition_ifs"></span><dl> <dt>**Partition \_ IFS**</dt> <dt>0x07</dt> </dl>                             | Eine IFS-Partition.<br/>                                                                                                                               |
| <span id="PARTITION_LDM"></span><span id="partition_ldm"></span><dl> <dt>**Partition \_ LDM**</dt> <dt>0x42</dt> </dl>                             | Eine LDM-Partition (Logical Disk Manager).<br/>                                                                                                         |
| <span id="PARTITION_NTFT"></span><span id="partition_ntft"></span><dl> <dt>**Partition \_ NTFT**</dt> <dt>0x80</dt> </dl>                          | Eine NTFT-Partition.<br/>                                                                                                                              |
| <span id="VALID_NTFT"></span><span id="valid_ntft"></span><dl> <dt>**Gültig \_ NTFT**</dt> <dt>0xC0</dt> </dl>                                      | Eine gültige NTFT-Partition.<br/> Das hohe Bit eines Partitionstyp Codes gibt an, dass eine Partition Teil eines NTFT-Spiegels oder Stripesetarrays ist.<br/> |



## <a name="remarks"></a>Bemerkungen

Es gibt mehrere Makros, mit denen Sie den Partitionstyp erkennen können: **iscontainerpartition**, **isftpartition** und **iserkenzedpartition**. Weitere Informationen finden Sie unter winioctl. h.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winioctl. h (Include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Partitions \_ Informationen \_ Ex**](/windows/desktop/api/WinIoCtl/ns-winioctl-partition_information_ex)
</dt> <dt>

[**Partitions \_ Informationen \_ MBR**](/windows/desktop/api/WinIoCtl/ns-winioctl-partition_information_mbr)
</dt> <dt>

[**\_Partitions \_ Informationen festlegen**](/windows/desktop/api/WinIoCtl/ns-winioctl-set_partition_information)
</dt> </dl>

 

 




