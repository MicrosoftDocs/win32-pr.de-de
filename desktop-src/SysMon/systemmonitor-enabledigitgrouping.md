---
title: Systemmonitor. enabledigitgruppierung (Eigenschaft)
description: Ruft einen Wert ab, der bestimmt, ob sysmon eine Ziffern Gruppierung verwendet, wenn numerische Werte angezeigt werden, oder legt ihn fest.
ms.assetid: 6a277960-fd01-423c-af2a-b35ed46c6d9a
keywords:
- Enabledigitgruppierung-Eigenschaft (Sysmon)
- Enabledigitgruppierungseigenschaft (Sysmon), Systemmonitor-Objekt
- Systemmonitor-Objekt "sysmon", enabledigitgruppierung (Eigenschaft)
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
ms.openlocfilehash: 66da0ad5ade7f3e01f58ef29bbd1094634c01b37
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391941"
---
# <a name="systemmonitorenabledigitgrouping-property"></a>Systemmonitor. enabledigitgruppierung (Eigenschaft)

Ruft einen Wert ab, der bestimmt, ob sysmon eine Ziffern Gruppierung verwendet, wenn numerische Werte angezeigt werden, oder legt ihn fest.

## <a name="syntax"></a>Syntax


```VB
Property EnableDigitGrouping As Boolean
```



## <a name="property-value"></a>Eigenschaftswert

True gibt an, dass sysmon Ziffern beim Anzeigen numerischer Werte gruppiert, z. b. 1.214. False gibt an, dass numerische Werte nicht gruppiert werden, z. b. 1214. Der Standardwert ist "true".

## <a name="remarks"></a>Bemerkungen

Das Ziffern Gruppierungs Symbol ist lokalisiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



 

 





