---
title: RegistrationTrigger.Delay-Eigenschaft
description: Ruft für die Skripterstellung die Zeitspanne zwischen der Registrierung des Tasks und dem Start des Tasks ab oder legt diese fest.
ms.assetid: 33b8f212-66eb-4396-b21f-eeb1a5175efc
keywords:
- Taskplaner der Delay-Eigenschaft
- Delay-Eigenschaft Taskplaner , RegistrationTrigger-Objekt
- RegistrationTrigger-Objekt Taskplaner , Delay-Eigenschaft
topic_type:
- apiref
api_name:
- RegistrationTrigger.Delay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd5b2176f6274ad0e4b0f413edbe595d97c95ecef6d48b076b9ae9a5ff81c0fd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072630"
---
# <a name="registrationtriggerdelay-property"></a>RegistrationTrigger.Delay-Eigenschaft

Ruft für die Skripterstellung die Zeitspanne zwischen der Registrierung des Tasks und dem Start des Tasks ab oder legt diese fest. Das Format für diese Zeichenfolge lautet PnYnMnDTnHnMnS, wobei nY die Anzahl der Jahre, nM die Anzahl der Monate, nD die Anzahl der Tage, "T" das Datums-/Uhrzeittrennzeichen, nH die Anzahl der Stunden, nM die Anzahl der Minuten und nS die Anzahl von Sekunden ist (z. B. PT5M gibt 5 Minuten an, und P1M4DT2H5M gibt einen Monat, vier Tage, zwei Stunden und fünf Minuten an).

## <a name="syntax"></a>Syntax


```VB
RegistrationTrigger.Delay As String
```



## <a name="property-value"></a>Eigenschaftswert

Die Zeitspanne zwischen der Registrierung des Systems und dem Start des Tasks.

## <a name="remarks"></a>Hinweise

Beim Lesen oder Schreiben von XML für eine Aufgabe wird die Startverzögerung mithilfe des [**Delay-Elements**](taskschedulerschema-delay-registrationtriggertype-element.md) des Taskplaner Schemas angegeben.

Wenn eine Aufgabe mit einem verzögerten Registrierungstrigger registriert wird und der Computer, auf dem der Task registriert ist, während der Verzögerung heruntergefahren oder neu gestartet wird, bevor der Task ausgeführt wird, wird der Task nicht ausgeführt, und die Verzögerung geht verloren.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





