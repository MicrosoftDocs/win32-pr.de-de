---
title: EventTrigger.Delay-Eigenschaft
description: Ruft für die Skripterstellung einen Wert ab, der die Zeitspanne zwischen dem Eintreten des Ereignisses und dem Start der Aufgabe angibt, oder legt diesen fest.
ms.assetid: 6f8b5e25-ad53-466e-adab-fe3c968e941b
keywords:
- Delay-Eigenschaft Taskplaner
- Delay-Eigenschaft Taskplaner , EventTrigger-Objekt
- EventTrigger-Objekt Taskplaner , Delay-Eigenschaft
topic_type:
- apiref
api_name:
- EventTrigger.Delay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 402ddb8e55f6eb22a4e2c106b64cbec3ed1afa6d0b58f38a2a8923f5bd8dfa4a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959590"
---
# <a name="eventtriggerdelay-property"></a>EventTrigger.Delay-Eigenschaft

Ruft für die Skripterstellung einen Wert ab, der die Zeitspanne zwischen dem Eintreten des Ereignisses und dem Start der Aufgabe angibt, oder legt diesen fest. Das Format für diese Zeichenfolge lautet PnYnMnDTnHnMnS, wobei nY die Anzahl der Jahre, nM die Anzahl der Monate, nD die Anzahl der Tage, "T" das Datums-/Uhrzeittrennzeichen, nH die Anzahl der Stunden, nM die Anzahl der Minuten und nS die Anzahl von Sekunden ist (z. B. PT5M gibt 5 Minuten an, und P1M4DT2H5M gibt einen Monat, vier Tage, zwei Stunden und fünf Minuten an).

## <a name="syntax"></a>Syntax


```VB
EventTrigger.Delay As String
```



## <a name="property-value"></a>Eigenschaftswert

Ein -Wert, der die Zeitspanne zwischen dem Eintreten des Ereignisses und dem Start der Aufgabe angibt.

## <a name="remarks"></a>Hinweise

Beim Lesen oder Schreiben eigener XML-Daten für eine Aufgabe wird die Ereignisverzögerung mithilfe des [**Delay-Elements**](taskschedulerschema-delay-eventtriggertype-element.md) des Taskplaner Schemas angegeben.

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

[**EventTrigger**](eventtrigger.md)
</dt> </dl>

 

 





