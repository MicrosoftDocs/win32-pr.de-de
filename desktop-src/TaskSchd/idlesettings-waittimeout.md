---
title: Idlesettings. WaitTimeout (Eigenschaft)
description: Ruft bei der Skripterstellung einen Wert ab oder legt einen Wert fest, der die Zeitspanne angibt, die der Taskplaner auf das Eintreten einer Leerlauf Bedingung wartet.
ms.assetid: 1be1c62b-bab0-41f8-9f64-e778aba4891f
keywords:
- WaitTimeout-Eigenschaft Taskplaner
- WaitTimeout-Eigenschaft Taskplaner, idlesettings-Objekt
- Idlesettings-Objekt Taskplaner, WaitTimeout-Eigenschaft
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
ms.openlocfilehash: fbb8e2abbd200b2c10eaefeafe2082a00be636a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040710"
---
# <a name="idlesettingswaittimeout-property"></a>Idlesettings. WaitTimeout (Eigenschaft)

Ruft bei der Skripterstellung einen Wert ab oder legt einen Wert fest, der die Zeitspanne angibt, die der Taskplaner auf das Eintreten einer Leerlauf Bedingung wartet. Wenn für diese Eigenschaft kein Wert angegeben wird, wartet der Taskplaner-Dienst unbegrenzt, bis eine Leerlauf Bedingung auftritt.

## <a name="syntax"></a>Syntax


```VB
IdleSettings.WaitTimeout As String
```



## <a name="property-value"></a>Eigenschaftswert

Ein-Wert, der die Zeitspanne angibt, die der Taskplaner auf das Eintreten einer Leerlauf Bedingung wartet. Das Format dieser Zeichenfolge lautet pnynmndtnhnmns. dabei ist "NY" die Anzahl der Jahre, "nm" die Anzahl von Monaten, "ND" die Anzahl der Tage, "t" ist das Trennzeichen für Datum/Uhrzeit, "NH" die Anzahl von Stunden, "nm" die Anzahl der Minuten und "NS" die Anzahl von Sekunden (z Die zulässige minimal Zeit beträgt 1 Minute. Wenn dieser Wert **null** ist, wird die Verzögerung auf den Standardwert von einer Stunde festgelegt.

## <a name="remarks"></a>Bemerkungen

Beim Lesen oder Schreiben von XML für eine Aufgabe wird diese Einstellung im [**WaitTimeout**](taskschedulerschema-waittimeout-idlesettingstype-element.md) -Element des Taskplaner-Schemas angegeben.

Wenn eine Aufgabe durch einen Leerlauf Trigger ausgelöst wird, wird die **idlesettings. WaitTimeout** -Eigenschaft ignoriert.

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

[**Idlesettings**](idlesettings.md)
</dt> </dl>

 

 





