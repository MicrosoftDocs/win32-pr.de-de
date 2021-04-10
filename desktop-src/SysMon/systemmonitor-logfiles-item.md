---
title: Logfiles. Item (Eigenschaft)
description: Ruft die angegebene logfileitem-Instanz aus der Auflistung ab.
ms.assetid: 518c1343-f659-4434-910c-958c09ffab6a
keywords:
- Element Eigenschaften-sysmon
- Element Eigenschaft sysmon, Logfiles-Klasse
- Logfiles-Klasse (Sysmon), Item-Eigenschaft
topic_type:
- apiref
api_name:
- LogFiles.Item
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85af003cd6c0291ec90d17906f249726dfd526f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040340"
---
# <a name="logfilesitem-property"></a>Logfiles. Item (Eigenschaft)

Ruft die angegebene [**logfileitem**](logfileitem.md) -Instanz aus der Auflistung ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```VB
Property Item( _
  ByVal index As Object _
) As LogFileItem
```



## <a name="property-value"></a>Eigenschaftswert

[**Logfileitem**](logfileitem.md) -Instanz, die dem angegebenen Indexwert entspricht.

## <a name="remarks"></a>Bemerkungen

Dies ist die Standard Eigenschaft des [**Logfiles**](systemmonitor-logfiles.md) -Objekts.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[LogFiles](logfiles.md)
</dt> <dt>

[**Logfileitem**](logfileitem.md)
</dt> <dt>

[**LogFiles**](systemmonitor-logfiles.md)
</dt> </dl>

 

 





