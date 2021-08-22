---
title: Triggerobjekt
description: Skriptobjekt, das die allgemeinen Eigenschaften bereitstellt, die von allen Triggerobjekten geerbt werden.
ms.assetid: dfc4cb36-8bdb-4aec-963e-5f1ec1ff85aa
keywords:
- Trigger Taskplaner , Triggerobjekt
- Triggerobjekt Taskplaner
- Triggerobjekt Taskplaner beschrieben
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
ms.openlocfilehash: 3b27427bf77465be119fc678cb4babf85254fa437b350c54d4409c0cd5b28024
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002008"
---
# <a name="trigger-object"></a>Triggerobjekt

Skriptobjekt, das die allgemeinen Eigenschaften bereitstellt, die von allen Triggerobjekten geerbt werden.

## <a name="members"></a>Member

Das **Trigger-Objekt** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **Trigger-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                            | Zugriffstyp           | Beschreibung                                                                                                                                         |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Aktiviert**](trigger-enabled.md)<br/>                       | Lesen/Schreiben<br/> | Ruft einen booleschen Wert ab, der angibt, ob der Trigger aktiviert ist, oder legt diesen fest.<br/>                                                              |
| [**EndBoundary**](trigger-endboundary.md)<br/>               | Lesen/Schreiben<br/> | Ruft das Datum und die Uhrzeit der Deaktivierung des Triggers ab oder legt diese fest. Der Trigger kann die Aufgabe nicht starten, nachdem sie deaktiviert wurde.<br/>               |
| [**ExecutionTimeLimit**](trigger-executiontimelimit.md)<br/> | Lesen/Schreiben<br/> | Ruft die maximale Zeit ab, die der vom Trigger gestartete Task ausführen darf, oder legt diese fest.<br/>                                         |
| [**Id**](trigger-id.md)<br/>                                 | Lesen/Schreiben<br/> | Ruft den Bezeichner für den Trigger ab oder legt den Bezeichner fest.<br/>                                                                                             |
| [**Wiederholen**](trigger-repetition.md)<br/>                 | Lesen/Schreiben<br/> | Ruft einen Wert ab, der angibt, wie oft der Task ausgeführt wird und wie lange das Wiederholungsmuster nach dem Starten der Aufgabe wiederholt wird, oder legt diesen fest.<br/> |
| [**StartBoundary**](trigger-startboundary.md)<br/>           | Lesen/Schreiben<br/> | Ruft das Datum und die Uhrzeit der Aktivierung des Triggers ab oder legt diese fest. Der Trigger kann die Aufgabe starten, nachdem der Trigger aktiviert wurde.<br/>             |
| [**type**](trigger-type.md)<br/>                             |                       | Ruft den Typ des Triggers ab.<br/>                                                                                                            |



 

## <a name="remarks"></a>Hinweise

Der Taskplaner stellt die folgenden einzelnen Objekte für die verschiedenen Trigger bereit, die eine Aufgabe verwenden kann:

-   [**BootTrigger**](boottrigger.md)
-   [**DailyTrigger**](dailytrigger.md)
-   [**EventTrigger**](eventtrigger.md)
-   [**IdleTrigger**](idletrigger.md)
-   [**LogonTrigger**](logontrigger.md)
-   [**MonthlyDOWTrigger**](monthlydowtrigger.md)
-   [**MonthlyTrigger**](monthlytrigger.md)
-   [**RegistrationTrigger**](registrationtrigger.md)
-   [**TimeTrigger**](timetrigger.md)
-   [**WeeklyTrigger**](weeklytrigger.md)
-   [**SessionStateChangeTrigger**](sessionstatechangetrigger.md)

Beim Lesen oder Schreiben von XML werden die Trigger einer Aufgabe im [**Triggers-Element**](taskschedulerschema-triggers-tasktype-element.md) des Taskplaner Schemas angegeben.

## <a name="examples"></a>Beispiele

Weitere Informationen und Beispielcode für dieses Skriptobjekt finden Sie unter [Time Trigger Example (Scripting) (Zeittriggerbeispiel (Skripterstellung)).](time-trigger-example--scripting-.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Triggercollection**](triggercollection.md)
</dt> </dl>

 

 





