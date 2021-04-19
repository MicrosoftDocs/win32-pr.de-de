---
title: Count. Value-Eigenschaft
description: Ruft den letzten samplingwert des Zählers ab.
ms.assetid: c5aeaa00-e185-484d-8a7a-d45a21690e20
keywords:
- Eigenschafts-sysmon
- Value-Eigenschaft (Sysmon), ratteritem-Klasse
- Namteritem Class sysmon, Value-Eigenschaft
topic_type:
- apiref
api_name:
- CounterItem.Value
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62c0d6bd9e1751e34c980bc95f790314017eeb49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342215"
---
# <a name="counteritemvalue-property"></a>Count. Value-Eigenschaft

Ruft den letzten samplingwert des Zählers ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```VB
Property Value As Double
```



## <a name="property-value"></a>Eigenschaftswert

Der zuletzt erfasste Wert des Zählers. Der Wert ist-1, wenn ein Fehler auftritt.

## <a name="remarks"></a>Bemerkungen

Dies ist die Standard Eigenschaft des [**ratteritem**](counteritem.md) -Objekts.

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

[**"Count. GetValue"**](counteritem-getvalue.md)
</dt> </dl>

 

 





