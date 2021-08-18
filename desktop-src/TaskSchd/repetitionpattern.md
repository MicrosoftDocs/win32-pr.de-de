---
title: RepetitionPattern-Objekt
description: Skripterstellungsobjekt, das definiert, wie oft der Task ausgeführt wird und wie lange das Wiederholungsmuster wiederholt wird, nachdem der Task gestartet wurde.
ms.assetid: a4e63da7-78ab-46a9-9b55-8460355753cf
keywords:
- triggers Taskplaner , Wiederholungsmusterobjekt
- Wiederholungsmuster Taskplaner , Objekt
- RepetitionPattern-Taskplaner
- RepetitionPattern-Objekt Taskplaner , beschrieben
topic_type:
- apiref
api_name:
- RepetitionPattern
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06583aaef7f41a2752ace9c67599c1d299b72f87cb9984674994ede10d89525b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872394"
---
# <a name="repetitionpattern-object"></a>RepetitionPattern-Objekt

Skripterstellungsobjekt, das definiert, wie oft der Task ausgeführt wird und wie lange das Wiederholungsmuster wiederholt wird, nachdem der Task gestartet wurde.

## <a name="members"></a>Member

Das **RepetitionPattern-Objekt** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **RepetitionPattern-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                                    | Zugriffstyp           | Beschreibung                                                                                                                                        |
|:----------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Duration**](repetitionpattern-duration.md)<br/>                   | Lesen/Schreiben<br/> | Ruft ab oder legt fest, wie lange das Muster wiederholt wird.<br/>                                                                                          |
| [**Intervall**](repetitionpattern-interval.md)<br/>                   | Lesen/Schreiben<br/> | Ruft die Zeit zwischen jedem Neustart der Aufgabe ab oder legt diese fest.<br/>                                                                       |
| [**StopAtDurationEnd**](repetitionpattern-stopatdurationend.md)<br/> | Lesen/Schreiben<br/> | Ruft einen booleschen Wert ab, der angibt, ob eine ausgeführte Instanz der Aufgabe am Ende der Wiederholungsmusterdauer beendet wird, oder legt diesen fest.<br/> |



 

## <a name="remarks"></a>Hinweise

Wenn Sie eine Wiederholungsdauer für eine Aufgabe angeben, müssen Sie auch das Wiederholungsintervall angeben.

Wenn Sie eine Aufgabe registrieren, die einen Trigger mit einem Wiederholungsintervall von einer Minute und einer Wiederholungsdauer von vier Minuten enthält, wird die Aufgabe fünfmal gestartet. Die fünf Wiederholungen können nach folgendem Muster definiert werden.

1.  Eine Aufgabe beginnt am Anfang der ersten Minute.
2.  Die nächste Aufgabe beginnt am Ende der ersten Minute.
3.  Die nächste Aufgabe beginnt am Ende der zweiten Minute.
4.  Die nächste Aufgabe beginnt am Ende der dritten Minute.
5.  Die nächste Aufgabe beginnt am Ende der vierten Minute.

**Windows Server 2003, Windows XP und Windows 2000:** Wenn Sie eine Aufgabe registrieren, die einen Trigger mit einem Wiederholungsintervall von einer Minute und einer Wiederholungsdauer von vier Minuten enthält, wird die Aufgabe viermal gestartet.

Beim Lesen oder Schreiben von XML für eine [](taskschedulerschema-repetition-triggerbasetype-element.md) Aufgabe wird das Wiederholungsmuster mithilfe des Wiederholungselements des Taskplaner angegeben.

## <a name="examples"></a>Beispiele

Weitere Informationen und Beispielcode für diese Eigenschaft finden Sie unter [Daily Trigger Example (Scripting) (Beispiel für tägliche Trigger (Skripterstellung)).](daily-trigger-example--scripting-.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Taskplaner Objekte](task-scheduler-objects.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





