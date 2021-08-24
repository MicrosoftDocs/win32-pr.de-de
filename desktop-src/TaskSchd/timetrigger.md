---
title: TimeTrigger-Objekt (Windows.applicationmodel.background.h)
description: Skripterstellungsobjekt, das einen Trigger darstellt, der eine Aufgabe zu einem bestimmten Datum und einer bestimmten Uhrzeit startet.
ms.assetid: 3c277827-8e70-42e7-a849-773ecc997a93
keywords:
- Zeittrigger Taskplaner , Objekt
- TimeTrigger-Objekt Taskplaner
- TimeTrigger-Objekt Taskplaner beschrieben
topic_type:
- apiref
api_name:
- TimeTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40f0fb6f5eaff5101f3cc1f5c4aeb2245335e4f65b27d2fafb364df2d05618ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119771980"
---
# <a name="timetrigger-object"></a>TimeTrigger-Objekt

Skripterstellungsobjekt, das einen Trigger darstellt, der eine Aufgabe zu einem bestimmten Datum und einer bestimmten Uhrzeit startet.

## <a name="members"></a>Member

Das **TimeTrigger-Objekt** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **TimeTrigger-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                            | Zugriffstyp           | Beschreibung                                                                                                                                                                      |
|:--------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Aktiviert**](trigger-enabled.md)<br/>                       | Lesen/Schreiben<br/> | Geerbt vom [**Trigger**](trigger.md). Ruft einen booleschen Wert ab, der angibt, ob der Trigger aktiviert ist, oder legt diesen fest.<br/>                                                |
| [**EndBoundary**](trigger-endboundary.md)<br/>               | Lesen/Schreiben<br/> | Geerbt vom [**Trigger**](trigger.md). Ruft das Datum und die Uhrzeit der Deaktivierung des Triggers ab oder legt diese fest. Der Trigger kann die Aufgabe nicht starten, nachdem sie deaktiviert wurde.<br/> |
| [**ExecutionTimeLimit**](trigger-executiontimelimit.md)<br/> | Lesen/Schreiben<br/> | Geerbt vom [**Trigger**](trigger.md). Ruft die maximale Zeit ab, die der vom Trigger gestartete Task ausführen darf, oder legt diese fest.<br/>                           |
| [**Id**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | Lesen/Schreiben<br/> | Geerbt vom [**Trigger**](trigger.md). Ruft den Bezeichner für den Trigger ab oder legt den Bezeichner fest.<br/>                                                                               |
| [**RandomDelay**](dailytrigger-randomdelay.md)<br/>          | Lesen/Schreiben<br/> | Ruft eine Verzögerungszeit ab, die der Startzeit des Triggers zufällig hinzugefügt wird, oder legt diese fest.<br/>                                                                                    |
| [**Wiederholen**](trigger-repetition.md)<br/>                 | Lesen/Schreiben<br/> | Geerbt vom [**Trigger**](trigger.md). Ruft ab oder legt fest, wie oft der Task ausgeführt wird und wie lange das Wiederholungsmuster wiederholt wird, nachdem der Task gestartet wurde.<br/>          |
| [**StartBoundary**](trigger-startboundary.md)<br/>           | Lesen/Schreiben<br/> | Geerbt vom [**Trigger**](trigger.md). Ruft das Datum und die Uhrzeit der Aktivierung des Triggers ab oder legt diese fest. Dieses Element ist erforderlich.<br/>                                    |
| [**Typ**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | Schreibgeschützt<br/>  | Geerbt vom [**Trigger**](trigger.md). Ruft den Typ des Triggers ab.<br/>                                                                                              |



 

## <a name="remarks"></a>Hinweise

Das [**StartBoundary-Element**](taskschedulerschema-startboundary-triggerbasetype-element.md) ist ein erforderliches Element für Zeit- und Kalendertrigger ([**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) und [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md)).

Beim Lesen oder Schreiben von XML für eine Aufgabe wird ein Leerlauftrigger mithilfe des [**TimeTrigger-Elements**](taskschedulerschema-timetrigger-triggergroup-element.md) des Taskplaner Schemas angegeben.

## <a name="examples"></a>Beispiele

Weitere Informationen und Beispielcode für dieses Skriptobjekt finden Sie unter [Time Trigger Example (Scripting) (Zeittriggerbeispiel (Skripterstellung)).](time-trigger-example--scripting-.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                             |
| Header<br/>                   | <dl> <dt>Windows.applicationmodel.background.h</dt> </dl> |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl>                          |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Trigger**](trigger.md)
</dt> <dt>

[**Triggercollection**](triggercollection.md)
</dt> <dt>

[**TriggerCollection.Create**](triggercollection-create.md)
</dt> </dl>

 

 





