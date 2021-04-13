---
title: Logonauslöst. Delay (Eigenschaft)
description: Ruft bei der Skripterstellung einen Wert ab oder legt einen Wert fest, der angibt, wie lange der Benutzer sich anmeldet und wann die Aufgabe gestartet wird.
ms.assetid: 42198357-18e9-4fff-a8bf-f2da36148dc8
keywords:
- Verzögerte Eigenschaften Taskplaner
- Delay-Eigenschaft Taskplaner, LOGON-Auslöserobjekt
- Logon-Auslöserobjekt Taskplaner, Delay-Eigenschaft
topic_type:
- apiref
api_name:
- LogonTrigger.Delay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce709b5095ffaeb9fdb5a4532f496ffa34c24e5b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391637"
---
# <a name="logontriggerdelay-property"></a>Logonauslöst. Delay (Eigenschaft)

Ruft bei der Skripterstellung einen Wert ab oder legt einen Wert fest, der angibt, wie lange der Benutzer sich anmeldet und wann die Aufgabe gestartet wird.

## <a name="syntax"></a>Syntax


```VB
LogonTrigger.Delay As String
```



## <a name="property-value"></a>Eigenschaftswert

Ein-Wert, der die Zeitspanne zwischen dem Zeitpunkt, an dem der Benutzer sich anmeldet, und dem Start der Aufgabe angibt. Das Format dieser Zeichenfolge lautet pnynmndtnhnmns. dabei ist "NY" die Anzahl der Jahre, "nm" die Anzahl von Monaten, "ND" die Anzahl der Tage, "t" ist das Trennzeichen für Datum/Uhrzeit, "NH" die Anzahl von Stunden, "nm" die Anzahl der Minuten und "NS" die Anzahl von Sekunden (z

## <a name="remarks"></a>Bemerkungen

Beim Lesen oder Schreiben von XML für eine Aufgabe wird die Verzögerung des LOGON-Auslösers mit dem [**Delay**](taskschedulerschema-delay-logontriggertype-element.md) -Element des Taskplaner-Schemas angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Logonauslöst**](logontrigger.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





