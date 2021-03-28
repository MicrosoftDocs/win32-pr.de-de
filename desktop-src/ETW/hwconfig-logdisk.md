---
description: Die Klasse hwconfig \_ logdisk ist die Ereignistyp Klasse für Konfigurations Ereignisse logischer Datenträger. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 2b7038fa-2f20-4bb5-bac1-76b272b3421c
title: HWConfig_LogDisk-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HWConfig_LogDisk
- HWConfig_LogDisk.DiskNumber
- HWConfig_LogDisk.Pad
- HWConfig_LogDisk.StartOffset
- HWConfig_LogDisk.PartitionSize
api_type:
- NA
api_location: ''
ms.openlocfilehash: dce4faed913d01f76ff23177b2dad42ea74e5c08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529885"
---
# <a name="hwconfig_logdisk-class"></a>Hwconfig \_ logdisk-Klasse

Die Klasse **hwconfig \_ logdisk** ist die Ereignistyp Klasse für Konfigurations Ereignisse logischer Datenträger.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[EventType(12), EventTypeName("LogDisk")]
class HWConfig_LogDisk : HWConfig
{
  uint32 DiskNumber;
  uint32 Pad;
  uint64 StartOffset;
  uint64 PartitionSize;
};
```

## <a name="members"></a>Member

Die Klasse " **hwconfig \_ logdisk** " verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **hwconfig \_ logdisk** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

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

Pad
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (2)
</dt> </dl>

Reserviert.

</dd> <dt>

PartitionSize
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (4)
</dt> </dl>

Gesamtgröße der Partition in Bytes.

</dd> <dt>

Starto ffset
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (3)
</dt> </dl>

Start Offset (in Bytes) der Partition vom Anfang des Datenträgers.

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

 

 




