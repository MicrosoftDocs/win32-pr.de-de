---
title: LogFiles.Item-Eigenschaft
description: Ruft die angegebene LogFileItem-Instanz aus der Auflistung ab.
ms.assetid: 518c1343-f659-4434-910c-958c09ffab6a
keywords:
- Elementeigenschaft SysMon
- Item-Eigenschaft SysMon , LogFiles-Klasse
- LogFiles-Klasse SysMon , Item-Eigenschaft
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
ms.openlocfilehash: b2441575ec45c3d914fef80d5a7c6655b76597c094e319f5f0b01dbb62190e19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118882281"
---
# <a name="logfilesitem-property"></a>LogFiles.Item-Eigenschaft

Ruft die angegebene [**LogFileItem-Instanz**](logfileitem.md) aus der Auflistung ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```VB
Property Item( _
  ByVal index As Object _
) As LogFileItem
```



## <a name="property-value"></a>Eigenschaftswert

[**LogFileItem-Instanz,**](logfileitem.md) die dem angegebenen Indexwert entspricht.

## <a name="remarks"></a>Hinweise

Dies ist die Standardeigenschaft des [**LogFiles-Objekts.**](systemmonitor-logfiles.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[LogFiles](logfiles.md)
</dt> <dt>

[**LogFileItem**](logfileitem.md)
</dt> <dt>

[**LogFiles**](systemmonitor-logfiles.md)
</dt> </dl>

 

 





