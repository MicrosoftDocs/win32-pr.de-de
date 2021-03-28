---
description: Diese Klasse ist die Ereignistyp Klasse für Ereignisse für die Konfiguration von physischen Datenträgern.
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
ms.openlocfilehash: d868e3943f22a71b4513f4f77841ddea9204ffea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977480"
---
# <a name="systemconfig_phydisk-class"></a>SystemConfig- \_ Klasse "phydisk"

Diese Klasse ist die Ereignistyp Klasse für Ereignisse für die Konfiguration von physischen Datenträgern.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

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

Die Klasse " **SystemConfig \_ phydisk** " verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die Klasse " **SystemConfig \_ phydisk** " verfügt über diese Eigenschaften.

<dl> <dt>

**Bootdriveletter**
</dt> <dd> <dl> <dt>

Datentyp: **char16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (14), **Max** (3), **Format ("s")**
</dt> </dl>

Laufwerk Buchstabe des Start Laufwerks in der Form " <letter> :".

</dd> <dt>

**Bytespersektor**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (2)
</dt> </dl>

Anzahl von Bytes in den einzelnen Sektoren für das physische Laufwerk.

</dd> <dt>

**Rad**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (5)
</dt> </dl>

Die Gesamtanzahl der Zylinder auf dem physischen Laufwerk. Hinweis: der Wert für diese Eigenschaft wird durch erweiterte Funktionen der BIOS-Interruptzeit 13 h abgerufen. Der Wert kann ungenau sein, wenn das Laufwerk ein Übersetzungs Schema verwendet, um Datenträger Größen mit hoher Kapazität zu unterstützen. Informieren Sie sich beim Hersteller über genaue Laufwerk Spezifikationen.

</dd> <dt>

**Disknumber**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (1)
</dt> </dl>

Index Nummer des Datenträgers, der diese Partition enthält.

</dd> <dt>

**Manufacturer**
</dt> <dd> <dl> <dt>

Datentyp: **char16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (10), **Max** (256), **Format ("s")**
</dt> </dl>

Der Name des Laufwerks Herstellers.

</dd> <dt>

**Pad**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (13)
</dt> </dl>

Nicht verwendet.

</dd> <dt>

**PartitionCount**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (11)
</dt> </dl>

Anzahl der Partitionen auf diesem physischen Laufwerk, die vom Betriebssystem erkannt werden.

</dd> <dt>

**Scsilun**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (9)
</dt> </dl>

SCSI-logische Gerätenummer (LUN) des SCSI-Adapters.

</dd> <dt>

**Scsipath**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (7)
</dt> </dl>

SCSI-Busnummer des SCSI-Adapters.

</dd> <dt>

**SCSIPort**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (6)
</dt> </dl>

SCSI-Nummer des SCSI-Adapters.

</dd> <dt>

**Scsitarget**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (8)
</dt> </dl>

Enthält die Nummer des Zielgeräts.

</dd> <dt>

**Sector-Spur**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (3)
</dt> </dl>

Anzahl der Sektoren in jeder Spur für dieses physische Laufwerk.

</dd> <dt>

**Schonen**
</dt> <dd> <dl> <dt>

Datentyp: **char16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (15), **Max** (2), **Format ("s")**
</dt> </dl>

Nicht verwendet.

</dd> <dt>

**TracksPerCylinder**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (4)
</dt> </dl>

Anzahl der Spuren in jedem Zylinder auf dem physischen Laufwerk. Hinweis: der Wert für diese Eigenschaft wird durch erweiterte Funktionen der BIOS-Interruptzeit 13 h abgerufen. Der Wert kann ungenau sein, wenn das Laufwerk ein Übersetzungs Schema verwendet, um Datenträger Größen mit hoher Kapazität zu unterstützen. Informieren Sie sich beim Hersteller über genaue Laufwerk Spezifikationen.

</dd> <dt>

**Schreibzugriff aktiviert**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (12)
</dt> </dl>

True, wenn der Schreib Cache aktiviert ist.

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

 

 




