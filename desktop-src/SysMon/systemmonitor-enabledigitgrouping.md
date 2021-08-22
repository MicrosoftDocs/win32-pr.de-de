---
title: SystemMonitor.EnableDigitGrouping-Eigenschaft
description: Ruft einen Wert ab, der bestimmt, ob SYSMON beim Anzeigen numerischer Werte die Zifferngruppierung verwendet, oder legt diesen fest.
ms.assetid: 6a277960-fd01-423c-af2a-b35ed46c6d9a
keywords:
- EnableDigitGrouping-Eigenschaft SysMon
- EnableDigitGrouping-Eigenschaft SysMon , SystemMonitor-Objekt
- SystemMonitor-Objekt SysMon , EnableDigitGrouping-Eigenschaft
topic_type:
- apiref
api_name:
- SystemMonitor.EnableDigitGrouping
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d910e479cc0a957ea5f1332d7fead0f93badd797bfe2d90b26f9914f0c3d863a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118882605"
---
# <a name="systemmonitorenabledigitgrouping-property"></a>SystemMonitor.EnableDigitGrouping-Eigenschaft

Ruft einen Wert ab, der bestimmt, ob SYSMON beim Anzeigen numerischer Werte die Zifferngruppierung verwendet, oder legt diesen fest.

## <a name="syntax"></a>Syntax


```VB
Property EnableDigitGrouping As Boolean
```



## <a name="property-value"></a>Eigenschaftswert

True gibt an, dass SYSMON Ziffern gruppiert, wenn numerische Werte angezeigt werden, z.B. 1.214. False gibt an, dass numerische Werte nicht gruppiert werden, z. B. 1214. True ist die Standardeinstellung.

## <a name="remarks"></a>Hinweise

Das Symbol für die Zifferngruppierung ist lokalisiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



 

 





