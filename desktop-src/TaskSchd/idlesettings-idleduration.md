---
title: IdleSettings.IdleDuration-Eigenschaft
description: Ruft für die Skripterstellung einen Wert ab, der angibt, wie lange sich der Computer im Leerlauf befinden muss, bevor der Task ausgeführt wird, oder legt diesen fest.
ms.assetid: 32b9a14e-e37e-4e3a-81eb-041387f2017b
keywords:
- IdleDuration-Eigenschaft Taskplaner
- IdleDuration-Eigenschaft Taskplaner , IdleSettings-Objekt
- IdleSettings-Objekt Taskplaner , IdleDuration-Eigenschaft
topic_type:
- apiref
api_name:
- IdleSettings.IdleDuration
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30a78210202579d517410a2d82f1c5566d947f1ceb76cbd92538a0266b7b81ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002438"
---
# <a name="idlesettingsidleduration-property"></a>IdleSettings.IdleDuration-Eigenschaft

Ruft für die Skripterstellung einen Wert ab, der angibt, wie lange sich der Computer im Leerlauf befinden muss, bevor der Task ausgeführt wird, oder legt diesen fest.

## <a name="syntax"></a>Syntax


```VB
IdleSettings.IdleDuration As String
```



## <a name="property-value"></a>Eigenschaftswert

Ein -Wert, der angibt, wie lange sich der Computer im Leerlauf befinden muss, bevor der Task ausgeführt wird. Das Format für diese Zeichenfolge lautet PnYnMnDTnHnMnS, wobei nY die Anzahl der Jahre, nM die Anzahl der Monate, nD die Anzahl der Tage, "T" das Datums-/Uhrzeittrennzeichen, nH die Anzahl der Stunden, nM die Anzahl der Minuten und nS die Anzahl von Sekunden ist (z. B. PT5M gibt 5 Minuten an, und P1M4DT2H5M gibt einen Monat, vier Tage, zwei Stunden und fünf Minuten an). Der Mindestwert beträgt eine Minute. Wenn dieser Wert **NULL** ist, wird die Verzögerung auf den Standardwert von 10 Minuten festgelegt.

## <a name="remarks"></a>Hinweise

Beim Lesen oder Schreiben von XML für eine Aufgabe wird diese Einstellung im [**Duration-Element**](taskschedulerschema-duration-idlesettingstype-element.md) des Taskplaner Schemas angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> <dt>

[**IdleSettings**](idlesettings.md)
</dt> </dl>

 

 





