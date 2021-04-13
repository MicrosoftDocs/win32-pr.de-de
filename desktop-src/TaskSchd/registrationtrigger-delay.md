---
title: Registrationauslöst. Delay (Eigenschaft)
description: Ruft bei der Skripterstellung die Zeitspanne zwischen dem Registrieren der Aufgabe und dem Start der Aufgabe ab oder legt diese fest.
ms.assetid: 33b8f212-66eb-4396-b21f-eeb1a5175efc
keywords:
- Verzögerte Eigenschaften Taskplaner
- Delay-Eigenschaft Taskplaner, Registration-Auslöserobjekt
- Registration-Auslöserobjekt Taskplaner, Delay-Eigenschaft
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
ms.openlocfilehash: ad86017547ac4476f430e13e2566ddd6d3494226
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518602"
---
# <a name="registrationtriggerdelay-property"></a>Registrationauslöst. Delay (Eigenschaft)

Ruft bei der Skripterstellung die Zeitspanne zwischen dem Registrieren der Aufgabe und dem Start der Aufgabe ab oder legt diese fest. Das Format dieser Zeichenfolge lautet pnynmndtnhnmns. dabei ist "NY" die Anzahl der Jahre, "nm" die Anzahl von Monaten, "ND" die Anzahl der Tage, "t" ist das Trennzeichen für Datum/Uhrzeit, "NH" die Anzahl von Stunden, "nm" die Anzahl der Minuten und "NS" die Anzahl von Sekunden (z

## <a name="syntax"></a>Syntax


```VB
RegistrationTrigger.Delay As String
```



## <a name="property-value"></a>Eigenschaftswert

Die Zeitspanne zwischen dem Registrieren des Systems und dem Start des Tasks.

## <a name="remarks"></a>Bemerkungen

Beim Lesen oder Schreiben von XML für eine Aufgabe wird die Startverzögerung mit dem [**Delay**](taskschedulerschema-delay-registrationtriggertype-element.md) -Element des Taskplaner-Schemas angegeben.

Wenn eine Aufgabe mit einem verzögerten Registrierungs Ausfall registriert ist und der Computer, auf dem der Task registriert ist, während der Verzögerung heruntergefahren oder neu gestartet wird, bevor der Task ausgeführt wird, wird der Task nicht ausgeführt, und die Verzögerung geht verloren.

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
</dt> </dl>

 

 





