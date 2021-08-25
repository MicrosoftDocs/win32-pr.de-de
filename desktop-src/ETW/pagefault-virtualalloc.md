---
description: Diese Klasse ist die Ereignistypklasse für virtuelle Zuordnungsereignisse. Die folgende Syntax wird durch einen MOF-Code vereinfacht.
ms.assetid: 037d33e0-da94-4834-bc02-814c1cae1d8d
title: PageFault_VirtualAlloc-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PageFault_VirtualAlloc
- PageFault_VirtualAlloc.BaseAddress
- PageFault_VirtualAlloc.RegionSize
- PageFault_VirtualAlloc.ProcessId
- PageFault_VirtualAlloc.Flags
api_type:
- NA
api_location: ''
ms.openlocfilehash: fa3dd8eb53e9c1a79cf38edde0d9c4dba93ea85b0994bfb316b97064f211f26e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927570"
---
# <a name="pagefault_virtualalloc-class"></a>PageFault \_ VirtualAlloc-Klasse

Diese Klasse ist die Ereignistypklasse für virtuelle Zuordnungsereignisse.

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[EventType{98, 99}, EventTypeName{"VirtualAlloc", "VirtualFree"}]
class PageFault_VirtualAlloc : PageFault_V2
{
  uint32 BaseAddress;
  object RegionSize;
  uint32 ProcessId;
  uint32 Flags;
};
```

## <a name="members"></a>Member

Die **PageFault \_ VirtualAlloc-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **PageFault \_ VirtualAlloc-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**BaseAddress**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(1), Zeiger
</dt> </dl>

Die Startadresse, an der Arbeitsspeicher belegt oder freigegeben wurde.

</dd> <dt>

**Flags**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(4), Format("x")
</dt> </dl>

Der Typ der Speicherbelegung, die ausgeführt wurde. Mögliche Werte finden Sie im *flAllocationType-Parameter* der [**VirtualAllocEx-Funktion.**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex)

</dd> <dt>

**Processid**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(3)
</dt> </dl>

Der Prozess, der den Arbeitsspeicher besitzt (kann sich von dem Thread unterscheiden, der die Zuordnung ausgeführt hat).

</dd> <dt>

**RegionSize**
</dt> <dd> <dl> <dt>

Datentyp: **object**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(2), Extension("SizeT")
</dt> </dl>

Die Größe des belegten oder freigegebenen Arbeitsspeichers in Bytes.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**PageFault \_ V2**](pagefault-v2.md)
</dt> </dl>

 

 
