---
description: 'PageFault_TypeGroup1 Klasse: Diese Klasse ist die Ereignistypklasse für Seitenfehlerereignisse. Die folgende Syntax wird durch MOF-Code vereinfacht.'
ms.assetid: 59cb1091-af21-4fe6-87b8-17a262cc4467
title: PageFault_TypeGroup1-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PageFault_TypeGroup1
- PageFault_TypeGroup1.VirtualAddress
- PageFault_TypeGroup1.ProgramCounter
api_type:
- NA
api_location: ''
ms.openlocfilehash: 4a69e74a086ecd594d83c932beea4fd7d62724db
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106408"
---
# <a name="pagefault_typegroup1-class"></a>PageFault \_ TypeGroup1-Klasse

Diese Klasse ist die Ereignistypklasse für Seitenfehlerereignisse.

Die folgende Syntax wird durch MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[EventType{10, 11, 12, 13, 14, 15}, EventTypeName{"TransitionFault", "DemandZeroFault", "CopyOnWrite", "GuardPageFault", "HardPageFault", "AccessViolation"}]
class PageFault_TypeGroup1 : PageFault_V2
{
  uint32 VirtualAddress;
  uint32 ProgramCounter;
};
```

## <a name="members"></a>Member

Die **PageFault \_ TypeGroup1-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **PageFault \_ TypeGroup1-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

ProgramCounter
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(2), Zeiger
</dt> </dl>

Zeiger auf die aktuelle Anweisung, die ausgeführt wird.

</dd> <dt>

VirtualAddress
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(1), Zeiger
</dt> </dl>

Virtuelle Adresse der Seite, die den Seitenfehler verursacht hat.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Ein Seitenfehler tritt auf, wenn eine seite, die im Arbeitsspeichercache gesucht wird, dort nicht gefunden wird und von einer anderen Stelle im Arbeitsspeicher (ein weicher Fehler) oder vom Datenträger (ein harter Fehler) abgerufen werden muss.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**PageFault \_ V2**](pagefault-v2.md)
</dt> </dl>

 

 




