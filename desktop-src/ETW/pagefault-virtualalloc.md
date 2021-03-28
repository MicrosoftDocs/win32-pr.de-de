---
description: Diese Klasse ist die Ereignistyp Klasse für virtuelle Zuordnungs Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
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
ms.openlocfilehash: f9e754bc3dc09f492682d5a522a6489cfde27ceb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343999"
---
# <a name="pagefault_virtualalloc-class"></a>Pagefault- \_ virtualzuweisung-Klasse

Diese Klasse ist die Ereignistyp Klasse für virtuelle Zuordnungs Ereignisse.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

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

Die **Pagefault- \_ virtualordc** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Pagefault- \_ virtualordc** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**BaseAddress**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (1), Zeiger
</dt> </dl>

Die Startadresse, an der der Arbeitsspeicher zugeordnet oder freigegeben wurde.

</dd> <dt>

**Flags**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (4), Format ("x")
</dt> </dl>

Der Typ der Speicher Belegung, der ausgeführt wurde. Mögliche Werte finden Sie unter der *fltypcationtype* -Parameter der [**virtualzuweisung**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) -Funktion.

</dd> <dt>

**ProcessID**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (3)
</dt> </dl>

Der Prozess, der den Arbeitsspeicher besaß (kann sich von dem Thread unterscheiden, der die Zuordnung durchgeführt hat).

</dd> <dt>

**Regionsize**
</dt> <dd> <dl> <dt>

Datentyp: **Object**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: wmidataid (2), Erweiterung ("sizet")
</dt> </dl>

Die Größe (in Bytes) des Arbeitsspeichers, der zugeordnet oder freigegeben wurde.

</dd> </dl>

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Pagefault \_ v2**](pagefault-v2.md)
</dt> </dl>

 

 
