---
title: Time-Auslöserobjekt (Windows. applicationmodel. Background. h)
description: Skript Objekt, das einen-Auslösers darstellt, der eine Aufgabe zu einem bestimmten Datum und einer bestimmten Uhrzeit startet.
ms.assetid: 3c277827-8e70-42e7-a849-773ecc997a93
keywords:
- Zeit Auslöse Taskplaner, Objekt
- Time-Auslöserobjekt Taskplaner
- Time-Auslöserobjekt Taskplaner, beschrieben
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
ms.openlocfilehash: 1a8403b93e1c5292ade9f6f402b7e41994339140
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340878"
---
# <a name="timetrigger-object"></a>Timeauslöserobjekt

Skript Objekt, das einen-Auslösers darstellt, der eine Aufgabe zu einem bestimmten Datum und einer bestimmten Uhrzeit startet.

## <a name="members"></a>Member

Das **time-Auslöserobjekt** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **time-Auslöserobjekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                            | Zugriffstyp           | BESCHREIBUNG                                                                                                                                                                      |
|:--------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Aktiviert**](trigger-enabled.md)<br/>                       | Lesen/Schreiben<br/> | Geerbt von [**einem**](trigger.md)-Auslösung. Ruft einen booleschen Wert ab, der angibt, ob der-Wert aktiviert ist, oder legt ihn fest.<br/>                                                |
| [**Endgrenze**](trigger-endboundary.md)<br/>               | Lesen/Schreiben<br/> | Geerbt von [**einem**](trigger.md)-Auslösung. Ruft das Datum und die Uhrzeit der Deaktivierung des Auslösers ab oder legt diese fest. Der-Vorgang kann die Aufgabe nicht starten, nachdem Sie deaktiviert wurde.<br/> |
| [**Executiontimelimit**](trigger-executiontimelimit.md)<br/> | Lesen/Schreiben<br/> | Geerbt von [**einem**](trigger.md)-Auslösung. Ruft die maximale Zeitspanne ab, die der vom-Aufruf gestartete Task ausgeführt werden darf, oder legt diese fest.<br/>                           |
| [**Name**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | Lesen/Schreiben<br/> | Geerbt von [**einem**](trigger.md)-Auslösung. Ruft den Bezeichner für den-Typ ab oder legt ihn fest.<br/>                                                                               |
| [**Randomdelay**](dailytrigger-randomdelay.md)<br/>          | Lesen/Schreiben<br/> | Ruft eine Verzögerungszeit ab, die der Startzeit des Auslösers zufällig hinzugefügt wird, oder legt diese fest.<br/>                                                                                    |
| [**Wiederholen**](trigger-repetition.md)<br/>                 | Lesen/Schreiben<br/> | Geerbt von [**einem**](trigger.md)-Auslösung. Ruft ab oder legt fest, wie oft die Aufgabe ausgeführt wird und wie lange das Wiederholungsmuster wiederholt wird, nachdem die Aufgabe gestartet wurde.<br/>          |
| [**StartBoundary**](trigger-startboundary.md)<br/>           | Lesen/Schreiben<br/> | Geerbt von [**einem**](trigger.md)-Auslösung. Ruft das Datum und die Uhrzeit der Aktivierung des Auslösers ab oder legt diese fest. Dieses Element ist erforderlich.<br/>                                    |
| [**type**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | Schreibgeschützt<br/>  | Geerbt von [**einem**](trigger.md)-Auslösung. Ruft den Typ des Auslösers ab.<br/>                                                                                              |



 

## <a name="remarks"></a>Bemerkungen

Das [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) -Element ist ein erforderliches Element für Zeit-und Kalender Trigger ([**timetrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) und [**calendartrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md)).

Beim Lesen oder Schreiben von XML für eine Aufgabe wird ein Leerlauf-Auslösung mithilfe des [**time-Auslöserelements**](taskschedulerschema-timetrigger-triggergroup-element.md) des Taskplaner Schemas angegeben.

## <a name="examples"></a>Beispiele

Weitere Informationen und Beispielcode für dieses Skript Objekt finden Sie unter [time-auslöserbeispiel (Skripterstellung)](time-trigger-example--scripting-.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                             |
| Header<br/>                   | <dl> <dt>Windows. applicationmodel. Background. h</dt> </dl> |
| Typbibliothek<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl>                          |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Trigger**](trigger.md)
</dt> <dt>

[**TriggerCollection**](triggercollection.md)
</dt> <dt>

[**TriggerCollection. Create**](triggercollection-create.md)
</dt> </dl>

 

 





