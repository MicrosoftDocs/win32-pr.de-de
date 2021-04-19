---
title: EventTrigger. Delay (Eigenschaft)
description: Ruft bei der Skripterstellung einen Wert ab oder legt einen Wert fest, der die Zeitspanne zwischen dem Auftreten des Ereignisses und dem Start der Aufgabe angibt.
ms.assetid: 6f8b5e25-ad53-466e-adab-fe3c968e941b
keywords:
- Verzögerte Eigenschaften Taskplaner
- Delay-Eigenschaft Taskplaner, EventTrigger-Objekt
- EventTrigger-Objekt Taskplaner, Delay-Eigenschaft
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
ms.openlocfilehash: fcb67ca7ef12ca023bcb6c0d9d83880d4abb94af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341392"
---
# <a name="eventtriggerdelay-property"></a>EventTrigger. Delay (Eigenschaft)

Ruft bei der Skripterstellung einen Wert ab oder legt einen Wert fest, der die Zeitspanne zwischen dem Auftreten des Ereignisses und dem Start der Aufgabe angibt. Das Format dieser Zeichenfolge lautet pnynmndtnhnmns. dabei ist "NY" die Anzahl der Jahre, "nm" die Anzahl von Monaten, "ND" die Anzahl der Tage, "t" ist das Trennzeichen für Datum/Uhrzeit, "NH" die Anzahl von Stunden, "nm" die Anzahl der Minuten und "NS" die Anzahl von Sekunden (z

## <a name="syntax"></a>Syntax


```VB
EventTrigger.Delay As String
```



## <a name="property-value"></a>Eigenschaftswert

Ein-Wert, der die Zeitspanne zwischen dem Auftreten des Ereignisses und dem Start der Aufgabe angibt.

## <a name="remarks"></a>Bemerkungen

Beim Lesen oder schreiben Ihrer eigenen XML-Daten für eine Aufgabe wird die Ereignis Verzögerung mit dem [**Delay**](taskschedulerschema-delay-eventtriggertype-element.md) -Element des Taskplaner-Schemas angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> <dt>

[**EventTrigger**](eventtrigger.md)
</dt> </dl>

 

 





