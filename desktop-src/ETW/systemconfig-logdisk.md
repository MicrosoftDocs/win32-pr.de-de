---
description: 'SystemConfig_LogDisk-Klasse: Diese Klasse ist die Ereignistypklasse für Konfigurationsereignisse für logische Datenträger.'
ms.assetid: a11a8245-8ace-4061-b6c7-938002d8b9fc
title: SystemConfig_LogDisk-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_LogDisk
- SystemConfig_LogDisk.StartOffset
- SystemConfig_LogDisk.PartitionSize
- SystemConfig_LogDisk.DiskNumber
- SystemConfig_LogDisk.Size
- SystemConfig_LogDisk.DriveType
- SystemConfig_LogDisk.DriveLetterString
- SystemConfig_LogDisk.Pad1
- SystemConfig_LogDisk.PartitionNumber
- SystemConfig_LogDisk.SectorsPerCluster
- SystemConfig_LogDisk.BytesPerSector
- SystemConfig_LogDisk.Pad2
- SystemConfig_LogDisk.NumberOfFreeClusters
- SystemConfig_LogDisk.TotalNumberOfClusters
- SystemConfig_LogDisk.FileSystem
- SystemConfig_LogDisk.VolumeExt
- SystemConfig_LogDisk.Pad3
api_type:
- NA
api_location: ''
ms.openlocfilehash: c24ce209c51e0ac2d6167ae76d3f8289d73aa0fffa9ce607e51c8566cbb37c36
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119582230"
---
# <a name="systemconfig_logdisk-class"></a>SystemConfig \_ LogDisk-Klasse

Diese Klasse ist die Ereignistypklasse für Konfigurationsereignisse des logischen Datenträgers.

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[EventType(12), EventTypeName("LogDisk")]
class SystemConfig_LogDisk : SystemConfig
{
  uint64 StartOffset;
  uint64 PartitionSize;
  uint32 DiskNumber;
  uint32 Size;
  uint32 DriveType;
  char16 DriveLetterString[];
  uint32 Pad1;
  uint32 PartitionNumber;
  uint32 SectorsPerCluster;
  uint32 BytesPerSector;
  uint32 Pad2;
  sint64 NumberOfFreeClusters;
  sint64 TotalNumberOfClusters;
  char16 FileSystem;
  uint32 VolumeExt;
  uint32 Pad3;
};
```

## <a name="members"></a>Member

Die **SystemConfig \_ LogDisk-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **SystemConfig \_ LogDisk-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**BytesPerSector**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (10)
</dt> </dl>

Anzahl der Bytes in jedem Sektor für das physische Laufwerk.

</dd> <dt>

**DiskNumber**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (3)
</dt> </dl>

Indexnummer des Datenträgers, der diese Partition enthält.

</dd> <dt>

**DriveLetterString**
</dt> <dd> <dl> <dt>

Datentyp: **char16-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (6), **Max** (4), **Format(s)**
</dt> </dl>

Laufwerkbuchstabe des Datenträgers im Format <letter> ":".

</dd> <dt>

**DriveType**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (5)
</dt> </dl>

Typ des Laufwerks. Mögliche Werte:



| Wert                                                                        | Bedeutung                                         |
|------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>1</dt> </dl> | Partition<br/>                            |
| <dl> <dt>2</dt> </dl> | Volume<br/>                               |
| <dl> <dt>3</dt> </dl> | Erweiterte Partition auf mehreren Datenträgern<br/> |



 

</dd> <dt>

**Dateisystem**
</dt> <dd> <dl> <dt>

Datentyp: **char16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (14), Max(16), **Format(s)** 
</dt> </dl>

Dateisystem auf dem logischen Datenträger, z. B. NTFS.

</dd> <dt>

**NumberOfFreeClusters**
</dt> <dd> <dl> <dt>

Datentyp: **sint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (12)
</dt> </dl>

Anzahl der freien Cluster im angegebenen Volume.

</dd> <dt>

**Pad1**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (7)
</dt> </dl>

Wird nicht verwendet.

</dd> <dt>

**Pad2**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (11)
</dt> </dl>

Wird nicht verwendet.

</dd> <dt>

**Pad3**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (16)
</dt> </dl>

Wird nicht verwendet.

</dd> <dt>

**PartitionNumber**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (8)
</dt> </dl>

Indexnummer der Partition.

</dd> <dt>

**PartitionSize**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (2)
</dt> </dl>

Gesamtgröße der Partition in Bytes.

</dd> <dt>

**SectorsPerCluster**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (9)
</dt> </dl>

Anzahl der Sektoren im Volume.

</dd> <dt>

**Größe**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (4)
</dt> </dl>

Größe des Laufwerks in Bytes.

</dd> <dt>

**StartOffset**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (1)
</dt> </dl>

Startoffset (in Bytes) der Partition vom Anfang des Datenträgers.

</dd> <dt>

**TotalNumberOfClusters**
</dt> <dd> <dl> <dt>

Datentyp: **sint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (13)
</dt> </dl>

Anzahl der verwendeten und kostenlosen Cluster im Volume.

</dd> <dt>

**VolumeExt**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (15)
</dt> </dl>

Reserviert.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SystemConfig**](systemconfig.md)
</dt> </dl>

 

 




