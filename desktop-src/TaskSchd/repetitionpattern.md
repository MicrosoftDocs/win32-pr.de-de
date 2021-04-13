---
title: Repetitionpattern-Objekt
description: Skript Objekt, das definiert, wie oft die Aufgabe ausgeführt wird und wie lange das Wiederholungsmuster wiederholt wird, nachdem die Aufgabe gestartet wurde.
ms.assetid: a4e63da7-78ab-46a9-9b55-8460355753cf
keywords:
- Trigger Taskplaner, Wiederholungsmuster Objekt
- Wiederholungsmuster Taskplaner, Objekt
- Repetitionpattern-Objekt Taskplaner
- Wiederholungpattern-Objekt Taskplaner, beschrieben
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
ms.openlocfilehash: 84b88588238c9a7e4158fe21bca8904bf6f39b51
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475975"
---
# <a name="repetitionpattern-object"></a>Repetitionpattern-Objekt

Skript Objekt, das definiert, wie oft die Aufgabe ausgeführt wird und wie lange das Wiederholungsmuster wiederholt wird, nachdem die Aufgabe gestartet wurde.

## <a name="members"></a>Member

Das **wiederholungpattern** -Objekt verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **repetitionpattern** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                                                    | Zugriffstyp           | BESCHREIBUNG                                                                                                                                        |
|:----------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Duration**](repetitionpattern-duration.md)<br/>                   | Lesen/Schreiben<br/> | Ruft ab oder legt fest, wie lange das Muster wiederholt wird.<br/>                                                                                          |
| [**Intervall**](repetitionpattern-interval.md)<br/>                   | Lesen/Schreiben<br/> | Ruft die Zeitspanne zwischen den einzelnen Neustarts der Aufgabe ab oder legt diese fest.<br/>                                                                       |
| [**Stopatdurationend**](repetitionpattern-stopatdurationend.md)<br/> | Lesen/Schreiben<br/> | Ruft einen booleschen Wert ab, der angibt, ob eine laufende Instanz der Aufgabe am Ende der Wiederholungsmuster Dauer beendet wird, oder legt diesen fest.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Wenn Sie eine Wiederholungs Dauer für eine Aufgabe angeben, müssen Sie auch das Wiederholungsintervall angeben.

Wenn Sie eine Aufgabe registrieren, die einen-Auslösers mit einem Wiederholungsintervall von einer Minute und einer Wiederholungs Dauer von vier Minuten enthält, wird die Aufgabe fünfmal gestartet. Die fünf Wiederholungen können mithilfe des folgenden Musters definiert werden.

1.  Eine Aufgabe beginnt am Anfang der ersten Minute.
2.  Die nächste Aufgabe beginnt am Ende der ersten Minute.
3.  Die nächste Aufgabe beginnt am Ende der zweiten Minute.
4.  Die nächste Aufgabe beginnt am Ende der dritten Minute.
5.  Die nächste Aufgabe beginnt am Ende der vierten Minute.

**Windows Server 2003, Windows XP und Windows 2000:** Wenn Sie eine Aufgabe registrieren, die einen-Auslösers mit einem Wiederholungsintervall von einer Minute und einer Wiederholungs Dauer von vier Minuten enthält, wird die Aufgabe viermal gestartet.

Beim Lesen oder Schreiben von XML für eine Aufgabe wird das Wiederholungsmuster mithilfe des [**Wiederholungs**](taskschedulerschema-repetition-triggerbasetype-element.md) Elements des Taskplaner Schemas angegeben.

## <a name="examples"></a>Beispiele

Weitere Informationen und Beispielcode für diese Eigenschaft finden Sie unter [Beispiel für den täglichen Beispiel (Skripterstellung)](daily-trigger-example--scripting-.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Taskplaner Objekte](task-scheduler-objects.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





