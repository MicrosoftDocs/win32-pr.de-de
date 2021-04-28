---
description: 'PageFault_TransitionFault Klasse: Diese Klasse ist die Ereignistypklasse für Seitenfehlerereignisse. Die folgende Syntax wird durch MOF-Code vereinfacht.'
ms.assetid: cc2b7a93-6974-4872-98f3-d6cb81861ae5
title: PageFault_TransitionFault-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PageFault_TransitionFault
- PageFault_TransitionFault.VirtualAddress
- PageFault_TransitionFault.ProgramCounter
api_type:
- NA
api_location: ''
ms.openlocfilehash: 6c8ee12cf201b9ee83d231bf1f5e499550aa3cd6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106458"
---
# <a name="pagefault_transitionfault-class"></a>PageFault \_ TransitionFault-Klasse

Diese Klasse ist die Ereignistypklasse für Seitenfehlerereignisse.

Die folgende Syntax wird durch MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[EventType{10, 11, 12, 13, 14}, EventTypeName{"TransitionFault", "DemandZeroFault", "CopyOnWrite", "GuardPageFault", "HardPageFault"}]
class PageFault_TransitionFault : PageFault_V2
{
  uint32 VirtualAddress;
  uint32 ProgramCounter;
};
```

## <a name="members"></a>Member

Die **PageFault \_ TransitionFault-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **PageFault \_ TransitionFault-Klasse** verfügt über diese Eigenschaften.

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

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**PageFault \_ V2**](pagefault-v2.md)
</dt> </dl>

 

 




