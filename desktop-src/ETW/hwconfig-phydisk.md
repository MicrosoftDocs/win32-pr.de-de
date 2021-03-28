---
description: Die Klasse hwconfig \_ phydisk ist die Ereignistyp Klasse für Ereignisse für die Konfiguration von physischen Datenträgern. Die folgende Syntax wird durch den MOF-Code vereinfacht.
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
ms.openlocfilehash: 453f06ae11bb8b1e11c9efddd6f63bffd38540e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977656"
---
# <a name="hwconfig_phydisk-class"></a>Hwconfig- \_ Klasse "phydisk"

Die Klasse **hwconfig \_ phydisk** ist die Ereignistyp Klasse für Ereignisse für die Konfiguration von physischen Datenträgern.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

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

Die Klasse **hwconfig \_ phydisk** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die Klasse **hwconfig \_ phydisk** verfügt über diese Eigenschaften.

<dl> <dt>

Bytespersektor
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (2)
</dt> </dl>

Anzahl von Bytes in den einzelnen Sektoren für das physische Laufwerk.

</dd> <dt>

Rad
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (5)
</dt> </dl>

Die Gesamtanzahl der Zylinder auf dem physischen Laufwerk. Hinweis: der Wert für diese Eigenschaft wird durch erweiterte Funktionen der BIOS-Interruptzeit 13 h abgerufen. Der Wert kann ungenau sein, wenn das Laufwerk ein Übersetzungs Schema verwendet, um Datenträger Größen mit hoher Kapazität zu unterstützen. Informieren Sie sich beim Hersteller über genaue Laufwerk Spezifikationen.

</dd> <dt>

Disknumber
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (1)
</dt> </dl>

Index Nummer des Datenträgers, der diese Partition enthält.

</dd> <dt>

Hersteller
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (10), stringbeendigung ("nullterminiert"), Format ("w")
</dt> </dl>

Der Name des Laufwerks Herstellers.

</dd> <dt>

Scsilun
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (9)
</dt> </dl>

SCSI-logische Gerätenummer (LUN) des SCSI-Adapters.

</dd> <dt>

Scsipath
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (7)
</dt> </dl>

SCSI-Busnummer des SCSI-Adapters.

</dd> <dt>

SCSIPort
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (6)
</dt> </dl>

SCSI-Nummer des SCSI-Adapters.

</dd> <dt>

Scsitarget
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (8)
</dt> </dl>

Enthält die Nummer des Zielgeräts.

</dd> <dt>

Sector-Spur
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (3)
</dt> </dl>

Anzahl der Sektoren in jeder Spur für dieses physische Laufwerk.

</dd> <dt>

TracksPerCylinder
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (4)
</dt> </dl>

Anzahl der Spuren in jedem Zylinder auf dem physischen Laufwerk. Hinweis: der Wert für diese Eigenschaft wird durch erweiterte Funktionen der BIOS-Interruptzeit 13 h abgerufen. Der Wert kann ungenau sein, wenn das Laufwerk ein Übersetzungs Schema verwendet, um Datenträger Größen mit hoher Kapazität zu unterstützen. Informieren Sie sich beim Hersteller über genaue Laufwerk Spezifikationen.

</dd> </dl>

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Hwconfig**](hwconfig.md)
</dt> </dl>

 

 




