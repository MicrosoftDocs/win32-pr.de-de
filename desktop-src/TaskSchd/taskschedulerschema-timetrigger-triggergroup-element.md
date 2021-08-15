---
title: TimeTrigger -Element (triggerGroup)
description: Gibt einen Trigger an, der eine Aufgabe startet, wenn der Trigger aktiviert wird.
ms.assetid: bb467f36-47cd-4db4-97c4-60c09937caac
keywords:
- TimeTrigger-Element Taskplaner
topic_type:
- apiref
api_name:
- TimeTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d6b766a64f87b43feb23200176c5d23e254638a0022ea4d77b64264ca1d507d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118355847"
---
# <a name="timetrigger-triggergroup-element"></a>TimeTrigger -Element (triggerGroup)

Gibt einen Trigger an, der eine Aufgabe startet, wenn der Trigger aktiviert wird.

``` syntax
<xs:element name="TimeTrigger"
    type="timeTriggerType"
 />
```

Das **TimeTrigger-Element** wird durch die [**triggerGroup definiert.**](taskschedulerschema-triggergroup-group.md)

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                           | Abgeleitet von                                                         | BESCHREIBUNG                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [**Trigger**](taskschedulerschema-triggers-tasktype-element.md) | [**triggersType**](taskschedulerschema-triggerstype-complextype.md) | Gibt die Trigger an, die die Aufgabe starten.<br/> |



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                                                        | type                                                                     | BESCHREIBUNG                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Aktiviert (triggerBaseType)**](taskschedulerschema-enabled-triggerbasetype-element.md)                       | boolean                                                                  | Gibt an, dass der Trigger aktiviert ist.<br/>                                                                                  |
| [**EndBoundary (triggerBaseType)**](taskschedulerschema-endboundary-triggerbasetype-element.md)               | dateTime                                                                 | Gibt das Datum und die Uhrzeit der Deaktivierung des Triggers an. Der Trigger kann die Aufgabe nicht starten, nachdem sie deaktiviert wurde.<br/> |
| [**ExecutionTimeLimit (triggerBaseType)**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | duration                                                                 | Gibt die maximale Zeitdauer an, in der der Task vom Trigger gestartet werden kann.<br/>                                   |
| [**Wiederholung (triggerBaseType)**](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [**wiederholungstyp**](taskschedulerschema-repetitiontype-complextype.md) | Gibt an, wie oft der Task ausgeführt wird und wie lange das Wiederholungsmuster wiederholt wird, nachdem der Task gestartet wurde.<br/>          |
| [**StartBoundary (triggerBaseType)**](taskschedulerschema-startboundary-triggerbasetype-element.md)           | dateTime                                                                 | Gibt das Datum und die Uhrzeit der Aktivierung des Triggers an. Dieses Element ist erforderlich.<br/>                                    |



## <a name="attributes"></a>Attributes



| Name | type       | BESCHREIBUNG                               |
|------|------------|-------------------------------------------|
| Id   | **string** | Der Bezeichner des Triggers.<br/> |



## <a name="remarks"></a>Hinweise

Das [**StartBoundary-Element**](taskschedulerschema-startboundary-triggerbasetype-element.md) ist ein erforderliches Element für Zeit- und Kalendertrigger (**TimeTrigger** und [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md)).

Für die Skriptentwicklung wird ein Zeittrigger mithilfe des [**TimeTrigger-Objekts**](timetrigger.md) angegeben.

Für die C++-Entwicklung wird ein Zeittrigger mithilfe der [**ITimeTrigger-Schnittstelle**](/windows/desktop/api/taskschd/nn-taskschd-itimetrigger) angegeben.

Die oben aufgeführten untergeordneten Elemente werden durch die [**komplexen TriggerBaseType-Elementtypen**](taskschedulerschema-triggerbasetype-complextype.md) definiert. Diese Elemente müssen in der unten gezeigten Reihenfolge hinzugefügt werden.

-   [**StartBoundary (triggerBaseType)**](taskschedulerschema-startboundary-triggerbasetype-element.md)
-   [**EndBoundary (triggerBaseType)**](taskschedulerschema-endboundary-triggerbasetype-element.md)
-   [**Aktiviert (triggerBaseType)**](taskschedulerschema-enabled-triggerbasetype-element.md)
-   [**Wiederholung (triggerBaseType)**](taskschedulerschema-repetition-triggerbasetype-element.md)
-   [**ExecutionTimeLimit (triggerBaseType)**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md)

## <a name="examples"></a>Beispiele

Ein vollständiges Beispiel für den XML-Code für einen Task, der einen Zeittrigger angibt, finden Sie unter [Time Trigger Example (XML) (Beispiel für Zeittrigger (XML)).](time-trigger-example--xml-.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





