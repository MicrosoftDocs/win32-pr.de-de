---
title: Idle-Auslöserobjekt
description: Skript Objekt, das einen-Fehler darstellt, der einen Task startet, wenn eine Leerlauf Bedingung auftritt.
ms.assetid: 627d83cf-27bd-47ce-a647-fa1e9af5263e
keywords:
- Leerlauf-auslöserTaskplaner, Objekt
- Idle-Auslöserobjekt Taskplaner
- Idle-Auslöserobjekt Taskplaner, beschrieben
topic_type:
- apiref
api_name:
- IdleTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e72288827fec34257bf4f54a152031ef37068790
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342877"
---
# <a name="idletrigger-object"></a>Idle-Auslöserobjekt

Skript Objekt, das einen-Fehler darstellt, der einen Task startet, wenn eine Leerlauf Bedingung auftritt. Informationen zu Bedingungen im Leerlauf finden Sie unter [Aufgaben im Leerlauf](task-idle-conditions.md).

## <a name="members"></a>Member

Das **Idle-Auslöserobjekt** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **Idle-Auslöserobjekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                            | Zugriffstyp           | BESCHREIBUNG                                                                                                                                                                                               |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Aktiviert**](trigger-enabled.md)<br/>                       | Lesen/Schreiben<br/> | Wird vom- [**Auslöserobjekt**](trigger.md) geerbt. Ruft einen booleschen Wert ab, der angibt, ob der-Wert aktiviert ist, oder legt ihn fest.<br/>                                                              |
| [Endgrenze](trigger-endboundary.md)<br/>                   | Lesen/Schreiben<br/> | Wird vom- [**Auslöserobjekt**](trigger.md) geerbt. Ruft das Datum und die Uhrzeit der Deaktivierung des Auslösers ab oder legt diese fest. Der-Vorgang kann die Aufgabe nicht starten, nachdem Sie deaktiviert wurde.<br/>               |
| [**Executiontimelimit**](trigger-executiontimelimit.md)<br/> | Lesen/Schreiben<br/> | Wird vom- [**Auslöserobjekt**](trigger.md) geerbt. Ruft den maximalen Zeitraum ab, in dem der Task vom-Vorgang gestartet werden kann, oder legt diesen fest.<br/>                                                 |
| [**Name**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | Lesen/Schreiben<br/> | Wird vom- [**Auslöserobjekt**](trigger.md) geerbt. Ruft den Bezeichner für den-Typ ab oder legt ihn fest.<br/>                                                                                             |
| [**Wiederholen**](trigger-repetition.md)<br/>                 | Lesen/Schreiben<br/> | Wird vom- [**Auslöserobjekt**](trigger.md) geerbt. Ruft einen Wert ab, der angibt, wie oft die Aufgabe ausgeführt wird und wie lange das Wiederholungsmuster nach dem Start der Aufgabe wiederholt wird, oder legt diesen Wert fest.<br/> |
| [**StartBoundary**](trigger-startboundary.md)<br/>           | Lesen/Schreiben<br/> | Wird vom- [**Auslöserobjekt**](trigger.md) geerbt. Ruft das Datum und die Uhrzeit der Aktivierung des Auslösers ab oder legt diese fest.<br/>                                                                            |
| [**type**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | Schreibgeschützt<br/>  | Wird vom- [**Auslöserobjekt**](trigger.md) geerbt. Ruft den Typ des Auslösers ab.<br/>                                                                                                            |



 

## <a name="remarks"></a>Bemerkungen

Ein Leerlauf-Triggervorgang löst nur dann eine Task Aktion aus, wenn der Computer nach der Start Grenze des Auslösers in den Leerlauf wechselt.

Beim Lesen oder Schreiben von XML für eine Aufgabe wird mit dem [**Idle-Auslöserelement**](taskschedulerschema-idletrigger-triggergroup-element.md) des Taskplaner Schemas ein Leerlauf--Auslöserwert angegeben.

Wenn eine Aufgabe durch einen Leerlauf Trigger ausgelöst wird, wird die [**idlesettings. WaitTimeout**](idlesettings-waittimeout.md) -Eigenschaft ignoriert.

Wenn die anfängliche Instanz eines Tasks mit einem Leerlauf-ausgelöst wird, wird die Aufgabe nur einmal ohne Wiederholungen gestartet, auch wenn in der [**Wiederholungs**](trigger-repetition.md) Eigenschaft mehrfache Wiederholung definiert ist. Dieses Verhalten tritt nicht auf, wenn der Task von sich selbst beendet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Trigger**](trigger.md)
</dt> <dt>

[Taskplaner Objekte](task-scheduler-objects.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





