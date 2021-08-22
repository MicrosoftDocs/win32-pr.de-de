---
title: IdleSettings.WaitTimeout-Eigenschaft
description: Ruft für die Skripterstellung einen Wert ab, der angibt, wie lange der Taskplaner auf das Auftreten einer Leerlaufbedingung wartet, oder legt diesen fest.
ms.assetid: 1be1c62b-bab0-41f8-9f64-e778aba4891f
keywords:
- Taskplaner der WaitTimeout-Eigenschaft
- WaitTimeout-Eigenschaft Taskplaner , IdleSettings-Objekt
- IdleSettings-Objekt Taskplaner , WaitTimeout-Eigenschaft
topic_type:
- apiref
api_name:
- IdleSettings.WaitTimeout
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5359f25b93921dbcaeed13941a675bc89cc4d79dcb3a36d2228ebf992ca955a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118859618"
---
# <a name="idlesettingswaittimeout-property"></a>IdleSettings.WaitTimeout-Eigenschaft

Ruft für die Skripterstellung einen Wert ab, der angibt, wie lange der Taskplaner auf das Auftreten einer Leerlaufbedingung wartet, oder legt diesen fest. Wenn für diese Eigenschaft kein Wert angegeben ist, wartet der Taskplaner-Dienst unbegrenzt, bis eine Leerlaufbedingung auftritt.

## <a name="syntax"></a>Syntax


```VB
IdleSettings.WaitTimeout As String
```



## <a name="property-value"></a>Eigenschaftswert

Ein -Wert, der die Zeitspanne angibt, die der Taskplaner auf das Auftreten einer Leerlaufbedingung wartet. Das Format für diese Zeichenfolge lautet PnYnMnDTnHnMnS, wobei nY die Anzahl der Jahre, nM die Anzahl der Monate, nD die Anzahl der Tage, "T" das Datums-/Uhrzeittrennzeichen, nH die Anzahl der Stunden, nM die Anzahl der Minuten und nS die Anzahl von Sekunden ist (z. B. PT5M gibt 5 Minuten an, und P1M4DT2H5M gibt einen Monat, vier Tage, zwei Stunden und fünf Minuten an). Die zulässige Mindestzeit beträgt 1 Minute. Wenn dieser Wert **NULL** ist, wird die Verzögerung auf den Standardwert 1 Stunde festgelegt.

## <a name="remarks"></a>Hinweise

Beim Lesen oder Schreiben von XML für eine Aufgabe wird diese Einstellung im [**WaitTimeout-Element**](taskschedulerschema-waittimeout-idlesettingstype-element.md) des Taskplaner Schemas angegeben.

Wenn eine Aufgabe durch einen Leerlauftrigger ausgelöst wird, wird die **IdleSettings.WaitTimeout-Eigenschaft** ignoriert.

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

 

 





