---
description: Diese Klasse ist die Ereignistypklasse, die den Anfang der Datenträger-E/A-Lese-, Schreib- und Leerungsereignisse markiert. Die folgende Syntax wird durch einen MOF-Code vereinfacht.
ms.assetid: 96543ef9-cc2b-4d9a-86a8-f2458439e4d8
title: DiskIo_TypeGroup2-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskIo_TypeGroup2
- DiskIo_TypeGroup2.Irp
- DiskIo_TypeGroup2.IssuingThreadId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 60c1f2be2e90ddb8b3d7a396bfa925f0b7e83181effe7fb8c947bd911133f441
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963140"
---
# <a name="diskio_typegroup2-class"></a>DiskIo \_ TypeGroup2-Klasse

Diese Klasse ist die Ereignistypklasse, die den Anfang der Datenträger-E/A-Lese-, Schreib- und Leerungsereignisse markiert.

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[EventType{12, 13, 15}, EventTypeName{"ReadInit", "WriteInit", "FlushInit"}]
class DiskIo_TypeGroup2 : DiskIo
{
  uint32 Irp;
  uint32 IssuingThreadId;
};
```

## <a name="members"></a>Member

Die **DiskIo \_ TypeGroup2-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **DiskIo \_ TypeGroup2-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Irp**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**WmiDataId**](event-tracing-mof-qualifiers.md) (1), [**Zeiger**](event-tracing-mof-qualifiers.md)
</dt> </dl>

E/A-Anforderungspaket. Diese Eigenschaft identifiziert die E/A-Aktivität.

</dd> <dt>

**IssuingThreadId**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**WmiDataId**](event-tracing-mof-qualifiers.md) (2)
</dt> </dl>

Der Bezeichner des ausstellenden Threads.

**Windows Server 2008 R2, Windows Server 2008, Windows 7 und Windows Vista:** Diese Eigenschaft wird nicht unterstützt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DiskIo**](diskio.md)
</dt> </dl>

 

 




