---
title: Auslöse Objekt
description: Skript Objekt, das die allgemeinen Eigenschaften bereitstellt, die von allen auslöserobjekten geerbt werden.
ms.assetid: dfc4cb36-8bdb-4aec-963e-5f1ec1ff85aa
keywords:
- Trigger Taskplaner, Triggerobjekt
- Auslöse Objekt Taskplaner
- Taskplaner des Auslösers Objekts, beschrieben
topic_type:
- apiref
api_name:
- Trigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f4a7edc6eff0bb04c81ba3bff3bb86ec0455b25
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858766"
---
# <a name="trigger-object"></a>Auslöse Objekt

Skript Objekt, das die allgemeinen Eigenschaften bereitstellt, die von allen auslöserobjekten geerbt werden.

## <a name="members"></a>Member

Das **Auslöserobjekt** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **Auslöserobjekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                            | Zugriffstyp           | BESCHREIBUNG                                                                                                                                         |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Aktiviert**](trigger-enabled.md)<br/>                       | Lesen/Schreiben<br/> | Ruft einen booleschen Wert ab, der angibt, ob der-Wert aktiviert ist, oder legt ihn fest.<br/>                                                              |
| [**Endgrenze**](trigger-endboundary.md)<br/>               | Lesen/Schreiben<br/> | Ruft das Datum und die Uhrzeit der Deaktivierung des Auslösers ab oder legt diese fest. Der-Vorgang kann die Aufgabe nicht starten, nachdem Sie deaktiviert wurde.<br/>               |
| [**Executiontimelimit**](trigger-executiontimelimit.md)<br/> | Lesen/Schreiben<br/> | Ruft die maximale Zeitspanne ab, die der vom-Aufruf gestartete Task ausgeführt werden darf, oder legt diese fest.<br/>                                         |
| [**Name**](trigger-id.md)<br/>                                 | Lesen/Schreiben<br/> | Ruft den Bezeichner für den-Typ ab oder legt ihn fest.<br/>                                                                                             |
| [**Wiederholen**](trigger-repetition.md)<br/>                 | Lesen/Schreiben<br/> | Ruft einen Wert ab, der angibt, wie oft die Aufgabe ausgeführt wird und wie lange das Wiederholungsmuster nach dem Start der Aufgabe wiederholt wird, oder legt diesen Wert fest.<br/> |
| [**StartBoundary**](trigger-startboundary.md)<br/>           | Lesen/Schreiben<br/> | Ruft das Datum und die Uhrzeit der Aktivierung des Auslösers ab oder legt diese fest. Der-Vorgang kann die Aufgabe starten, nachdem der-Vorgang aktiviert wurde.<br/>             |
| [**type**](trigger-type.md)<br/>                             |                       | Ruft den Typ des Auslösers ab.<br/>                                                                                                            |



 

## <a name="remarks"></a>Bemerkungen

Der Taskplaner stellt die folgenden einzelnen Objekte für die verschiedenen Trigger bereit, die von einem Task verwendet werden können:

-   [**Boottrigger**](boottrigger.md)
-   [**Dailylöst**](dailytrigger.md)
-   [**EventTrigger**](eventtrigger.md)
-   [**Idle-Auslösung**](idletrigger.md)
-   [**Logonauslöst**](logontrigger.md)
-   [**Monthlydowlöst**](monthlydowtrigger.md)
-   [**Monthly-auslöst**](monthlytrigger.md)
-   [**Registration-Auslösers**](registrationtrigger.md)
-   [**TimeTrigger**](timetrigger.md)
-   [**Weeklyauslösers**](weeklytrigger.md)
-   [**Sessionstatechange-Auslösers**](sessionstatechangetrigger.md)

Beim Lesen oder Schreiben von XML werden die Trigger einer Aufgabe im [**Trigger**](taskschedulerschema-triggers-tasktype-element.md) -Element des Taskplaner Schemas angegeben.

## <a name="examples"></a>Beispiele

Weitere Informationen und Beispielcode für dieses Skript Objekt finden Sie unter [time-auslöserbeispiel (Skripterstellung)](time-trigger-example--scripting-.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**TriggerCollection**](triggercollection.md)
</dt> </dl>

 

 





