---
description: 'SystemConfig_PhyDisk Klasse: Diese Klasse ist die Ereignistypklasse für physische Datenträgerkonfigurationsereignisse.'
ms.assetid: 850a6b2c-69e6-47ae-95ff-585fcc70c1c8
title: SystemConfig_PhyDisk-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_PhyDisk
- SystemConfig_PhyDisk.DiskNumber
- SystemConfig_PhyDisk.BytesPerSector
- SystemConfig_PhyDisk.SectorsPerTrack
- SystemConfig_PhyDisk.TracksPerCylinder
- SystemConfig_PhyDisk.Cylinders
- SystemConfig_PhyDisk.SCSIPort
- SystemConfig_PhyDisk.SCSIPath
- SystemConfig_PhyDisk.SCSITarget
- SystemConfig_PhyDisk.SCSILun
- SystemConfig_PhyDisk.Manufacturer
- SystemConfig_PhyDisk.PartitionCount
- SystemConfig_PhyDisk.WriteCacheEnabled
- SystemConfig_PhyDisk.Pad
- SystemConfig_PhyDisk.BootDriveLetter
- SystemConfig_PhyDisk.Spare
api_type:
- NA
api_location: ''
ms.openlocfilehash: 52ab249ab5087a1528317687d90f6d8fa665bc1a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106098"
---
# <a name="systemconfig_phydisk-class"></a>SystemConfig \_ PhyDisk-Klasse

Diese Klasse ist die Ereignistypklasse für physische Datenträgerkonfigurationsereignisse.

Die folgende Syntax wird durch MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[EventType(11), EventTypeName("PhyDisk")]
class SystemConfig_PhyDisk : SystemConfig
{
  uint32 DiskNumber;
  uint32 BytesPerSector;
  uint32 SectorsPerTrack;
  uint32 TracksPerCylinder;
  uint64 Cylinders;
  uint32 SCSIPort;
  uint32 SCSIPath;
  uint32 SCSITarget;
  uint32 SCSILun;
  char16 Manufacturer[];
  uint32 PartitionCount;
  uint8  WriteCacheEnabled;
  uint8  Pad;
  char16 BootDriveLetter[];
  char16 Spare[];
};
```

## <a name="members"></a>Member

Die **SystemConfig \_ PhyDisk-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **SystemConfig \_ PhyDisk-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**BootDriveLetter**
</dt> <dd> <dl> <dt>

Datentyp: **char16-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (14), **Max** (3), **Format("s")**
</dt> </dl>

Laufwerkbuchstaben des Startlaufwerks im Folgenden: <letter> ":".

</dd> <dt>

**BytesPerSector**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (2)
</dt> </dl>

Anzahl von Bytes in jedem Sektor für das physische Laufwerk.

</dd> <dt>

**Zylinder**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (5)
</dt> </dl>

Gesamtanzahl der Zylinder auf dem physischen Laufwerk. Hinweis: Der Wert für diese Eigenschaft wird über erweiterte Funktionen des BIOS-Interrupts 13h ermittelt. Der Wert kann ungenau sein, wenn das Laufwerk ein Übersetzungsschema verwendet, um Datenträgergrößen mit hoher Kapazität zu unterstützen. Wenden Sie sich an den Hersteller, um genaue Laufwerkspezifikationen zu erhalten.

</dd> <dt>

**DiskNumber**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (1)
</dt> </dl>

Indexnummer des Datenträgers, der diese Partition enthält.

</dd> <dt>

**Manufacturer**
</dt> <dd> <dl> <dt>

Datentyp: **char16-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (10), **Max** (256), **Format(s)**
</dt> </dl>

Name des Laufwerkherstellers.

</dd> <dt>

**Pad**
</dt> <dd> <dl> <dt>

Datentyp: **uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (13)
</dt> </dl>

Nicht verwendet.

</dd> <dt>

**PartitionCount**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (11)
</dt> </dl>

Anzahl der Partitionen auf diesem physischen Laufwerk, die vom Betriebssystem erkannt werden.

</dd> <dt>

**SCSILun**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (9)
</dt> </dl>

SCSI Logical Unit Number (LUN) des SCSI-Adapters.

</dd> <dt>

**SCSIPath**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (7)
</dt> </dl>

SCSI-Busnummer des SCSI-Adapters.

</dd> <dt>

**SCSIPort**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (6)
</dt> </dl>

SCSI-Nummer des SCSI-Adapters.

</dd> <dt>

**SCSITarget**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (8)
</dt> </dl>

Enthält die Nummer des Zielgeräts.

</dd> <dt>

**SectorsPerTrack**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (3)
</dt> </dl>

Anzahl der Sektoren in jeder Spur für dieses physische Laufwerk.

</dd> <dt>

**Ersatz**
</dt> <dd> <dl> <dt>

Datentyp: **char16-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (15), **Max** (2), **Format("s")**
</dt> </dl>

Nicht verwendet.

</dd> <dt>

**TracksPerCylinder**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (4)
</dt> </dl>

Anzahl der Spuren in jedem Zylinder auf dem physischen Laufwerk. Hinweis: Der Wert für diese Eigenschaft wird über erweiterte Funktionen des BIOS-Interrupts 13h ermittelt. Der Wert kann ungenau sein, wenn das Laufwerk ein Übersetzungsschema verwendet, um Datenträgergrößen mit hoher Kapazität zu unterstützen. Wenden Sie sich an den Hersteller, um genaue Laufwerkspezifikationen zu erhalten.

</dd> <dt>

**WriteCacheEnabled**
</dt> <dd> <dl> <dt>

Datentyp: **uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (12)
</dt> </dl>

True, wenn der Schreibcache aktiviert ist.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**SystemConfig**](systemconfig.md)
</dt> </dl>

 

 




