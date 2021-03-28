---
description: Diese Klasse ist die Ereignistyp Klasse, die den Anfang der Datenträger-e/a-Lese-, Schreib-und Lösch Ereignisse markiert. Die folgende Syntax wird durch den MOF-Code vereinfacht.
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
ms.openlocfilehash: ea08f32106c935be628bcdcd22e39ab92a0566e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525262"
---
# <a name="diskio_typegroup2-class"></a>Diskio \_ TypeGroup2-Klasse

Diese Klasse ist die Ereignistyp Klasse, die den Anfang der Datenträger-e/a-Lese-, Schreib-und Lösch Ereignisse markiert.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

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

Die **diskio \_ TypeGroup2** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **diskio \_ TypeGroup2** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**IRP**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**wmidataid**](event-tracing-mof-qualifiers.md) (1), [**Zeiger**](event-tracing-mof-qualifiers.md)
</dt> </dl>

E/a-Anforderungspaket. Diese Eigenschaft identifiziert die e/a-Aktivität.

</dd> <dt>

**Issuingthreadid**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**wmidataid**](event-tracing-mof-qualifiers.md) (2)
</dt> </dl>

Der Bezeichner des ausstellenden Threads.

**Windows Server 2008 R2, Windows Server 2008, Windows 7 und Windows Vista:** Diese Eigenschaft wird nicht unterstützt.

</dd> </dl>

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Sowie**](diskio.md)
</dt> </dl>

 

 




