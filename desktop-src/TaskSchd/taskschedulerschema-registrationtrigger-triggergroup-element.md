---
title: RegistrationTrigger (triggerGroup)-Element
description: Gibt einen Trigger an, der eine Aufgabe startet, wenn die Aufgabe registriert wird.
ms.assetid: 8f028ed0-93e6-4423-be2f-9a02be99122b
keywords:
- Registrierungstrigger Taskplaner , XML-Element
- RegistrationTrigger-Element Taskplaner
topic_type:
- apiref
api_name:
- RegistrationTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 548ffec6bf5982aac407905d944d029b222b741c0c03fe66645f68e771c87342
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099970"
---
# <a name="registrationtrigger-triggergroup-element"></a>RegistrationTrigger (triggerGroup)-Element

Gibt einen Trigger an, der eine Aufgabe startet, wenn die Aufgabe registriert wird.

``` syntax
<xs:element name="RegistrationTrigger"
    type="registrationTriggerType"
 />
```

Das **RegistrationTrigger-Element** wird durch den komplexen [**RegistrationTriggerType-Typ**](taskschedulerschema-registrationtriggertype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                           | Abgeleitet von                                                         | BESCHREIBUNG                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [**Auslöser**](taskschedulerschema-triggers-tasktype-element.md) | [**triggersType**](taskschedulerschema-triggerstype-complextype.md) | Gibt die Trigger an, die die Aufgabe starten.<br/> |



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                                                        | type                                                                     | BESCHREIBUNG                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Delay (registrationTriggerType)**](taskschedulerschema-delay-boottriggertype-element.md)                   | duration                                                                 | Gibt die Zeit zwischen dem Zeitpunkt der Registrierung und dem Start der Aufgabe an.<br/>                          |
| [**Aktiviert (triggerBaseType)**](taskschedulerschema-enabled-triggerbasetype-element.md)                       | boolean                                                                  | Gibt an, dass der Trigger aktiviert ist.<br/>                                                                                  |
| [**EndBoundary (triggerBaseType)**](taskschedulerschema-endboundary-triggerbasetype-element.md)               | dateTime                                                                 | Gibt das Datum und die Uhrzeit der Deaktivierung des Triggers an. Der Trigger kann die Aufgabe nicht starten, nachdem sie deaktiviert wurde.<br/> |
| [**ExecutionTimeLimit (triggerBaseType)**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | duration                                                                 | Gibt die maximale Zeitdauer an, in der der Task vom Trigger gestartet werden kann.<br/>                                   |
| [**Wiederholung (triggerBaseType)**](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [**wiederholungstyp**](taskschedulerschema-repetitiontype-complextype.md) | Gibt an, wie oft der Task ausgeführt wird und wie lange das Wiederholungsmuster wiederholt wird, nachdem der Task gestartet wurde.<br/>          |
| [**StartBoundary (triggerBaseType)**](taskschedulerschema-startboundary-triggerbasetype-element.md)           | dateTime                                                                 | Gibt das Datum und die Uhrzeit der Aktivierung des Triggers an.<br/>                                                              |



## <a name="attributes"></a>Attributes



| Name | type | BESCHREIBUNG                           |
|------|------|---------------------------------------|
| Id   | ID   | Bezeichner des Triggers.<br/> |



## <a name="remarks"></a>Hinweise

Für die Skriptentwicklung wird ein Registrierungstrigger mithilfe des [**RegistrationTrigger-Objekts**](registrationtrigger.md) angegeben.

Für die C++-Entwicklung wird ein Registrierungstrigger mithilfe der [**IRegistrationTrigger-Schnittstelle**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger) angegeben.

Die oben aufgeführten untergeordneten Elemente werden durch die [**komplexen Elementtypen triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) und [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md) definiert. Diese Elemente müssen in der unten gezeigten Reihenfolge hinzugefügt werden.

-   [**StartBoundary (triggerBaseType)**](taskschedulerschema-startboundary-triggerbasetype-element.md)
-   [**EndBoundary (triggerBaseType)**](taskschedulerschema-endboundary-triggerbasetype-element.md)
-   [**Aktiviert (triggerBaseType)**](taskschedulerschema-enabled-triggerbasetype-element.md)
-   [**Wiederholung (triggerBaseType)**](taskschedulerschema-repetition-triggerbasetype-element.md)
-   [**ExecutionTimeLimit (triggerBaseType)**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md)
-   [**Delay (registrationTriggerType)**](taskschedulerschema-delay-boottriggertype-element.md)

## <a name="examples"></a>Beispiele

Ein vollständiges Beispiel für den XML-Code für eine Aufgabe, die einen Starttrigger angibt, finden Sie unter Registration Trigger Example (XML) ( Beispiel für [Registrierungstrigger (XML)).](registration-trigger-example--xml-.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Taskplaner Schemaelemente](task-scheduler-schema-elements.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





