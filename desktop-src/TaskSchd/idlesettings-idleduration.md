---
title: Idlesettings. idleduration-Eigenschaft
description: Ruft bei der Skripterstellung einen Wert ab, der angibt, wie lange sich der Computer im Leerlauf befinden muss, bevor der Task ausgeführt wird, oder legt ihn fest.
ms.assetid: 32b9a14e-e37e-4e3a-81eb-041387f2017b
keywords:
- Idleduration-Eigenschaft Taskplaner
- Idleduration-Eigenschaft Taskplaner, idlesettings-Objekt
- Idlesettings-Objekt Taskplaner, idleduration-Eigenschaft
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
ms.openlocfilehash: f6eeed4fef540b3a9e13d0f52e3ce1934cb9e220
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742456"
---
# <a name="idlesettingsidleduration-property"></a>Idlesettings. idleduration-Eigenschaft

Ruft bei der Skripterstellung einen Wert ab, der angibt, wie lange sich der Computer im Leerlauf befinden muss, bevor der Task ausgeführt wird, oder legt ihn fest.

## <a name="syntax"></a>Syntax


```VB
IdleSettings.IdleDuration As String
```



## <a name="property-value"></a>Eigenschaftswert

Ein-Wert, der die Zeitspanne angibt, in der sich der Computer im Leerlauf befinden muss, bevor der Task ausgeführt wird.) Das Format dieser Zeichenfolge lautet pnynmndtnhnmns. dabei ist "NY" die Anzahl der Jahre, "nm" die Anzahl von Monaten, "ND" die Anzahl der Tage, "t" ist das Trennzeichen für Datum/Uhrzeit, "NH" die Anzahl von Stunden, "nm" die Anzahl der Minuten und "NS" die Anzahl von Sekunden (z Der Mindestwert ist eine Minute. Wenn dieser Wert **null** ist, wird die Verzögerung auf den Standardwert von 10 Minuten festgelegt.

## <a name="remarks"></a>Bemerkungen

Beim Lesen oder Schreiben von XML für eine Aufgabe wird diese Einstellung im [**Duration**](taskschedulerschema-duration-idlesettingstype-element.md) -Element des Taskplaner-Schemas angegeben.

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

 

 





