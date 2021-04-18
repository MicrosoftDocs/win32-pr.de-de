---
title: Repetitionpattern. Duration (Eigenschaft)
description: Ruft bei der Skripterstellung ab oder legt fest, wie lange das Muster wiederholt wird.
ms.assetid: 41a56414-981b-440a-b51a-228125baf303
keywords:
- Duration-Eigenschaft Taskplaner
- Duration-Eigenschaft Taskplaner, repetitionpattern-Objekt
- Repetitionpattern-Objekt Taskplaner, Duration-Eigenschaft
topic_type:
- apiref
api_name:
- RepetitionPattern.Duration
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51ff18330fd69bb54fdfb489b72f9470f707aed8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345310"
---
# <a name="repetitionpatternduration-property"></a>Repetitionpattern. Duration (Eigenschaft)

Ruft bei der Skripterstellung ab oder legt fest, wie lange das Muster wiederholt wird.

## <a name="syntax"></a>Syntax


```VB
RepetitionPattern.Duration As String
```



## <a name="property-value"></a>Eigenschaftswert

Gibt an, wie lange das Muster wiederholt wird. Das Format dieser Zeichenfolge lautet pnynmndtnhnmns. dabei ist "NY" die Anzahl der Jahre, "nm" die Anzahl von Monaten, "ND" die Anzahl der Tage, "t" ist das Trennzeichen für Datum/Uhrzeit, "NH" die Anzahl von Stunden, "nm" die Anzahl der Minuten und "NS" die Anzahl von Sekunden (z Die zulässige minimal Dauer beträgt eine Minute.

Wenn für die Dauer kein Wert angegeben wird, wird das Muster unbegrenzt wiederholt.

## <a name="remarks"></a>Bemerkungen

Wenn Sie eine Wiederholungs Dauer für eine Aufgabe angeben, müssen Sie auch das Wiederholungsintervall angeben.

Beim Lesen oder Schreiben von XML für eine Aufgabe wird die Wiederholungs Dauer im [**Duration**](taskschedulerschema-duration-repetitiontype-element.md) -Element des Taskplaner-Schemas angegeben.

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

 

 





