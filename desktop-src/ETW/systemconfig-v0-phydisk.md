---
description: 'SystemConfig_V0_PhyDisk Klasse: Diese Klasse ist die Ereignistypklasse für physische Datenträgerkonfigurationsereignisse.'
ms.assetid: 90ca3089-de5c-4e15-8abf-eaab9aafff06
title: SystemConfig_V0_PhyDisk-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_PhyDisk
- SystemConfig_V0_PhyDisk.DiskNumber
- SystemConfig_V0_PhyDisk.BytesPerSector
- SystemConfig_V0_PhyDisk.SectorsPerTrack
- SystemConfig_V0_PhyDisk.TracksPerCylinder
- SystemConfig_V0_PhyDisk.Cylinders
- SystemConfig_V0_PhyDisk.SCSIPort
- SystemConfig_V0_PhyDisk.SCSIPath
- SystemConfig_V0_PhyDisk.SCSITarget
- SystemConfig_V0_PhyDisk.SCSILun
- SystemConfig_V0_PhyDisk.Manufacturer
- SystemConfig_V0_PhyDisk.PartitionCount
- SystemConfig_V0_PhyDisk.WriteCacheEnabled
- SystemConfig_V0_PhyDisk.BootDriveLetter
api_type:
- NA
api_location: ''
ms.openlocfilehash: c18a198934b7234121da02900896d67c39a3ab3c
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880726"
---
# <a name="systemconfig_v0_phydisk-class"></a>SystemConfig \_ V0 \_ PhyDisk-Klasse

Diese Klasse ist die Ereignistypklasse für physische Datenträgerkonfigurationsereignisse.

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[EventType(11), EventTypeName("PhyDisk")]
class SystemConfig_V0_PhyDisk : SystemConfig_V0
{
  uint32  DiskNumber;
  uint32  BytesPerSector;
  uint32  SectorsPerTrack;
  uint32  TracksPerCylinder;
  uint64  Cylinders;
  uint32  SCSIPort;
  uint32  SCSIPath;
  uint32  SCSITarget;
  uint32  SCSILun;
  char16  Manufacturer[];
  uint32  PartitionCount;
  boolean WriteCacheEnabled;
  char16  BootDriveLetter[];
};
```

## <a name="members"></a>Member

Die **SystemConfig \_ V0 \_ PhyDisk-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **SystemConfig \_ V0 \_ PhyDisk-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**BootDriveLetter**
</dt> <dd> <dl> <dt>

Datentyp: **char16-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (13), **Max** (3)
</dt> </dl>

Laufwerkbuchstaben des Startlaufwerks im Folgenden: &lt; "Letter &gt; :".

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

Qualifizierer: **WmiDataId** (10), **Max** (256)
</dt> </dl>

Name des Laufwerkherstellers.

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

SCSI-LUN (Logical Unit Number) des SCSI-Adapters.

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

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (12)
</dt> </dl>

True, wenn der Schreibcache aktiviert ist.

</dd> </dl>

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**SystemConfig \_ V0**](systemconfig-v0.md)
</dt> </dl>

 

 




