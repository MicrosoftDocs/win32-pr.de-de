---
description: Die HWConfig \_ PhyDisk-Klasse ist die Ereignistypklasse für Physische Datenträgerkonfigurationsereignisse. Die folgende Syntax wird durch einen MOF-Code vereinfacht.
ms.assetid: b134ab45-b161-452f-be84-ccbdfa3fe4af
title: HWConfig_PhyDisk-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HWConfig_PhyDisk
- HWConfig_PhyDisk.DiskNumber
- HWConfig_PhyDisk.BytesPerSector
- HWConfig_PhyDisk.SectorsPerTrack
- HWConfig_PhyDisk.TracksPerCylinder
- HWConfig_PhyDisk.Cylinders
- HWConfig_PhyDisk.SCSIPort
- HWConfig_PhyDisk.SCSIPath
- HWConfig_PhyDisk.SCSITarget
- HWConfig_PhyDisk.SCSILun
- HWConfig_PhyDisk.Manufacturer
api_type:
- NA
api_location: ''
ms.openlocfilehash: ee8a578154e2acedb5d5c8ca6d5eea4f79737e5a2cfb89b0cb658526094fd09c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086400"
---
# <a name="hwconfig_phydisk-class"></a>HWConfig \_ PhyDisk-Klasse

Die **HWConfig \_ PhyDisk-Klasse** ist die Ereignistypklasse für Physische Datenträgerkonfigurationsereignisse.

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[EventType(11), EventTypeName("PhyDisk")]
class HWConfig_PhyDisk : HWConfig
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
  string Manufacturer;
};
```

## <a name="members"></a>Member

Die **HWConfig \_ PhyDisk-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **HWConfig \_ PhyDisk-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

BytesPerSector
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(2)
</dt> </dl>

Anzahl der Bytes in jedem Sektor für das physische Laufwerk.

</dd> <dt>

Zylinder
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(5)
</dt> </dl>

Gesamtanzahl der Zylinder auf dem physischen Laufwerk. Hinweis: Der Wert für diese Eigenschaft wird über erweiterte Funktionen des BIOS-Interrupts 13h abgerufen. Der Wert kann ungenau sein, wenn das Laufwerk ein Übersetzungsschema verwendet, um Datenträgergrößen mit hoher Kapazität zu unterstützen. Wenden Sie sich an den Hersteller, um genaue Laufwerkspezifikationen zu erhalten.

</dd> <dt>

DiskNumber
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(1)
</dt> </dl>

Indexnummer des Datenträgers, der diese Partition enthält.

</dd> <dt>

Hersteller
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(10), StringTermination("NullTerminated"), Format("w")
</dt> </dl>

Name des Laufwerkherstellers.

</dd> <dt>

SCSILun
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(9)
</dt> </dl>

SCSI Logical Unit Number (LUN) des SCSI-Adapters.

</dd> <dt>

SCSIPath
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(7)
</dt> </dl>

SCSI-Busnummer des SCSI-Adapters.

</dd> <dt>

SCSIPort
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(6)
</dt> </dl>

SCSI-Nummer des SCSI-Adapters.

</dd> <dt>

SCSITarget
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(8)
</dt> </dl>

Enthält die Nummer des Zielgeräts.

</dd> <dt>

SectorsPerTrack
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(3)
</dt> </dl>

Anzahl der Sektoren in jeder Spur für dieses physische Laufwerk.

</dd> <dt>

TracksPerCylinder
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(4)
</dt> </dl>

Anzahl der Spuren in jedem Zylinder auf dem physischen Laufwerk. Hinweis: Der Wert für diese Eigenschaft wird über erweiterte Funktionen des BIOS-Interrupts 13h abgerufen. Der Wert kann ungenau sein, wenn das Laufwerk ein Übersetzungsschema verwendet, um Datenträgergrößen mit hoher Kapazität zu unterstützen. Wenden Sie sich an den Hersteller, um genaue Laufwerkspezifikationen zu erhalten.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**HWConfig**](hwconfig.md)
</dt> </dl>

 

 




