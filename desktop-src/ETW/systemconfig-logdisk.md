---
description: Diese Klasse ist die Ereignistyp Klasse für Konfigurations Ereignisse logischer Datenträger.
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
ms.openlocfilehash: d3bff1cf526dfb7bf1ddd36fcb887e8a4b837be4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977585"
---
# <a name="systemconfig_logdisk-class"></a>SystemConfig \_ logdisk-Klasse

Diese Klasse ist die Ereignistyp Klasse für Konfigurations Ereignisse logischer Datenträger.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

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

Die **SystemConfig \_ logdisk** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **SystemConfig \_ logdisk** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Bytespersektor**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (10)
</dt> </dl>

Anzahl von Bytes in den einzelnen Sektoren für das physische Laufwerk.

</dd> <dt>

**Disknumber**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (3)
</dt> </dl>

Index Nummer des Datenträgers, der diese Partition enthält.

</dd> <dt>

**Driveletterstring**
</dt> <dd> <dl> <dt>

Datentyp: **char16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (6), **Max** (4), **Format ("s")**
</dt> </dl>

Laufwerk Buchstabe des Datenträgers in der Form " <letter> :".

</dd> <dt>

**DriveType**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (5)
</dt> </dl>

Der Typ des Laufwerks. Dabei sind folgende Werte möglich:



| Wert                                                                        | Bedeutung                                         |
|------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>1</dt> </dl> | Partition<br/>                            |
| <dl> <dt>2</dt> </dl> | Volume<br/>                               |
| <dl> <dt>3</dt> </dl> | Erweiterte Partition auf mehreren Datenträgern<br/> |



 

</dd> <dt>

**Verwendet**
</dt> <dd> <dl> <dt>

Datentyp: **char16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (14), **Max** (16), **Format ("s")**
</dt> </dl>

Dateisystem auf dem logischen Datenträger, z. b. NTFS.

</dd> <dt>

**"Numoffreeclusters"**
</dt> <dd> <dl> <dt>

Datentyp: **sint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (12)
</dt> </dl>

Anzahl der freien Cluster im angegebenen Volume.

</dd> <dt>

**Pad1**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (7)
</dt> </dl>

Nicht verwendet.

</dd> <dt>

**Pad2**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (11)
</dt> </dl>

Nicht verwendet.

</dd> <dt>

**Pad3**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (16)
</dt> </dl>

Nicht verwendet.

</dd> <dt>

**PartitionNumber**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (8)
</dt> </dl>

Index Nummer der Partition.

</dd> <dt>

**PartitionSize**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (2)
</dt> </dl>

Gesamtgröße der Partition in Bytes.

</dd> <dt>

**Sector-Cluster**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (9)
</dt> </dl>

Anzahl der Sektoren auf dem Volume.

</dd> <dt>

**Größe**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (4)
</dt> </dl>

Größe des Laufwerks in Bytes.

</dd> <dt>

**Starto ffset**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (1)
</dt> </dl>

Start Offset (in Bytes) der Partition vom Anfang des Datenträgers.

</dd> <dt>

**Totalnummeriofclusters**
</dt> <dd> <dl> <dt>

Datentyp: **sint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (13)
</dt> </dl>

Anzahl der verwendeten und freien Cluster im Volume.

</dd> <dt>

**Volumeext**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (15)
</dt> </dl>

Reserviert.

</dd> </dl>

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**SystemConfig**](systemconfig.md)
</dt> </dl>

 

 




