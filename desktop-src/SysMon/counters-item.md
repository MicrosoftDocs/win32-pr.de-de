---
title: Counters. Item (Eigenschaft)
description: Ruft die angegebene-Instanz aus der Auflistung ab.
ms.assetid: bf503371-c8bd-4e0d-ab8d-58de3f8fac5f
keywords:
- Element Eigenschaften-sysmon
- Item-Eigenschaft (Sysmon), counters-Klasse
- Indikatorenklasse "sysmon", Element Eigenschaft
topic_type:
- apiref
api_name:
- Counters.Item
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 251a645f0a4ceacdbfb4e2ab7e650f41e44dd508
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475825"
---
# <a name="countersitem-property"></a>Counters. Item (Eigenschaft)

Ruft [**die angegebene-**](counteritem.md) Instanz aus der Auflistung ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```VB
Property Item( _
  ByVal index As Object _
) As CounterItem
```



## <a name="property-value"></a>Eigenschaftswert

Die Instanz des [**rattritem**](counteritem.md) , die dem angegebenen Indexwert entspricht.

## <a name="exceptions"></a>Ausnahmen



| Ausnahmetyp                                  | Bedingung                         |
|-------------------------------------------------|-----------------------------------|
| **System. Runtime. InteropServices. COMException** | Der angegebene Index ist ungültig. |



 

## <a name="remarks"></a>Bemerkungen

Dies ist die Standard Eigenschaft des [**Counters**](counters.md) -Objekts.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ratteritem**](counteritem.md)
</dt> <dt>

[**Counters**](counters.md)
</dt> </dl>

 

 





