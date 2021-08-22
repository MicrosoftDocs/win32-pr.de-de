---
title: IdleSettings.StopOnIdleEnd (Eigenschaft)
description: Für die Skripterstellung ruft einen booleschen Wert ab, der angibt, dass der Taskplaner die Aufgabe beendet, wenn die Leerlaufbedingung endet, bevor der Task abgeschlossen ist, oder legt diesen fest.
ms.assetid: 5908bf6b-227a-4234-a741-82cf38163171
keywords:
- StopOnIdleEnd-Taskplaner
- StopOnIdleEnd-Eigenschaft Taskplaner , IdleSettings-Objekt
- IdleSettings-Objekt Taskplaner , StopOnIdleEnd-Eigenschaft
topic_type:
- apiref
api_name:
- IdleSettings.StopOnIdleEnd
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4e34e95483d382b9fbb97596a7172c94a1a047bfbec0856a3ea17befc1459bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139433"
---
# <a name="idlesettingsstoponidleend-property"></a>IdleSettings.StopOnIdleEnd (Eigenschaft)

Für die Skripterstellung ruft einen booleschen Wert ab, der angibt, dass der Taskplaner die Aufgabe beendet, wenn die Leerlaufbedingung endet, bevor der Task abgeschlossen ist, oder legt diesen fest.

## <a name="syntax"></a>Syntax


```VB
IdleSettings.StopOnIdleEnd As Boolean
```



## <a name="property-value"></a>Eigenschaftswert

Ein boolescher Wert, der angibt, dass Taskplaner Aufgabe beendet, wenn die Leerlaufbedingung vor Abschluss der Aufgabe endet.

## <a name="remarks"></a>Hinweise

Beim Lesen oder Schreiben von XML für eine Aufgabe wird diese Einstellung im [**StopOnIdleEnd-Element**](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) des Taskplaner angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> <dt>

[**IdleSettings**](idlesettings.md)
</dt> </dl>

 

 





