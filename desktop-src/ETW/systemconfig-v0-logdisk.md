---
description: 'SystemConfig_V0_LogDisk-Klasse: Diese Klasse ist die Ereignistypklasse für Logische Datenträgerkonfigurationsereignisse.'
ms.assetid: 3fa5f2e4-f6fa-4c10-9634-04908783cd28
title: SystemConfig_V0_LogDisk-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_LogDisk
- SystemConfig_V0_LogDisk.StartOffset
- SystemConfig_V0_LogDisk.PartitionSize
- SystemConfig_V0_LogDisk.DiskNumber
- SystemConfig_V0_LogDisk.Size
- SystemConfig_V0_LogDisk.DriveType
- SystemConfig_V0_LogDisk.DriveLetterString
- SystemConfig_V0_LogDisk.Pad
- SystemConfig_V0_LogDisk.PartitionNumber
- SystemConfig_V0_LogDisk.SectorsPerCluster
- SystemConfig_V0_LogDisk.BytesPerSector
- SystemConfig_V0_LogDisk.NumberOfFreeClusters
- SystemConfig_V0_LogDisk.TotalNumberOfClusters
- SystemConfig_V0_LogDisk.FileSystem
- SystemConfig_V0_LogDisk.VolumeExt
api_type:
- NA
api_location: ''
ms.openlocfilehash: 42b17cf31dcb3830cd35f046a7fcbad1858f8ae4f728fc1417339962a4be4441
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927520"
---
# <a name="systemconfig_v0_logdisk-class"></a>SystemConfig \_ V0 \_ LogDisk-Klasse

Diese Klasse ist die Ereignistypklasse für Konfigurationsereignisse des logischen Datenträgers.

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[EventType(12), EventTypeName("LogDisk")]
class SystemConfig_V0_LogDisk : SystemConfig_V0
{
  uint64 StartOffset;
  uint64 PartitionSize;
  uint32 DiskNumber;
  uint32 Size;
  uint32 DriveType;
  char16 DriveLetterString[];
  uint32 Pad;
  uint32 PartitionNumber;
  uint32 SectorsPerCluster;
  uint32 BytesPerSector;
  sint64 NumberOfFreeClusters;
  sint64 TotalNumberOfClusters;
  char16 FileSystem;
  uint32 VolumeExt;
};
```

## <a name="members"></a>Member

Die **SystemConfig \_ V0 \_ LogDisk-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **SystemConfig \_ V0 \_ LogDisk-Klasse** verfügt über diese Eigenschaften.

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

Qualifizierer: **WmiDataId** (6), **Max** (4)
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

Qualifizierer: **WmiDataId** (13), **Max** (16)
</dt> </dl>

Dateisystem auf dem logischen Datenträger, z. B. NTFS.

</dd> <dt>

**NumberOfFreeClusters**
</dt> <dd> <dl> <dt>

Datentyp: **sint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (11)
</dt> </dl>

Anzahl der freien Cluster im angegebenen Volume.

</dd> <dt>

**Pad**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (7)
</dt> </dl>

Reserviert.

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

Qualifizierer: **WmiDataId** (12)
</dt> </dl>

Anzahl der verwendeten und freien Cluster im Volume.

</dd> <dt>

**VolumeExt**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (14)
</dt> </dl>

Reserviert.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SystemConfig \_ V0**](systemconfig-v0.md)
</dt> </dl>

 

 




