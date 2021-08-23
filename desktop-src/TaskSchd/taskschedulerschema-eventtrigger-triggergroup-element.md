---
title: EventTrigger (triggerGroup)-Element
description: Gibt einen Trigger an, der eine Aufgabe startet, wenn ein Systemereignis auftritt.
ms.assetid: 8faffc04-1ad2-499d-bcdf-bc28f64b8aa8
keywords:
- Ereignistrigger Taskplaner , -Element
- EventTrigger-Element Taskplaner
topic_type:
- apiref
api_name:
- EventTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 555c8683933b2242d119fc00f29c6d0a33188f6404ca48a00e8a127dd59aa791
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119424470"
---
# <a name="eventtrigger-triggergroup-element"></a>EventTrigger (triggerGroup)-Element

Gibt einen Trigger an, der eine Aufgabe startet, wenn ein Systemereignis auftritt.

``` syntax
<xs:element name="EventTrigger"
    type="eventTriggerType"
 />
```

Das **EventTrigger-Element** wird von [**triggerGroup**](taskschedulerschema-triggergroup-group.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                           | Abgeleitet von                                                         | Beschreibung                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [**Trigger**](taskschedulerschema-triggers-tasktype-element.md) | [**triggersType**](taskschedulerschema-triggerstype-complextype.md) | Gibt die Trigger an, die den Task starten.<br/> |



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                                              | Typ                                                                     | Beschreibung                                                                                                                        |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Delay (eventTriggerType)**](taskschedulerschema-delay-eventtriggertype-element.md)               | duration                                                                 | Gibt die Zeitspanne zwischen dem Eintreten des Ereignisses und dem Start des Tasks an.<br/>                                |
| [**Aktiviert (triggerBaseType)**](taskschedulerschema-enabled-triggerbasetype-element.md)             | boolean                                                                  | Gibt an, dass der Trigger aktiviert ist.<br/>                                                                                  |
| [**EndBoundary (triggerBaseType)**](taskschedulerschema-endboundary-triggerbasetype-element.md)     | dateTime                                                                 | Gibt das Datum und die Uhrzeit der Deaktivierung des Triggers an. Der Trigger kann die Aufgabe nicht starten, nachdem sie deaktiviert wurde.<br/> |
| [**Wiederholung (triggerBaseType)**](taskschedulerschema-repetition-triggerbasetype-element.md)       | [**wiederholungstyp**](taskschedulerschema-repetitiontype-complextype.md) | Gibt an, wie oft der Task ausgeführt wird und wie lange das Wiederholungsmuster wiederholt wird, nachdem der Task gestartet wurde.<br/>          |
| [**StartBoundary (triggerBaseType)**](taskschedulerschema-startboundary-triggerbasetype-element.md) | dateTime                                                                 | Gibt das Datum und die Uhrzeit der Aktivierung des Triggers an.<br/>                                                              |
| [**Abonnement (eventTriggerType)**](taskschedulerschema-subscription-eventtriggertype-element.md) | Zeichenfolge                                                                   | Gibt die XPath-Abfrage an, die das Ereignis identifiziert, das den Trigger auslöst.<br/>                                             |



## <a name="attributes"></a>Attributes



| Name | Typ | BESCHREIBUNG                           |
|------|------|---------------------------------------|
| Id   | ID   | Bezeichner des Triggers.<br/> |



## <a name="remarks"></a>Hinweise

Es können maximal 500 Aufgaben mit Ereignisabonnements erstellt werden. Ein Ereignisabonnement, das eine Vielzahl von Ereignissen abfragt, kann verwendet werden, um eine Aufgabe auszulösen, die die gleiche Aktion als Reaktion auf die protokollierten Ereignisse verwendet.

Für die Skriptentwicklung wird ein Ereignistrigger durch das [**EventTrigger-Objekt**](eventtrigger.md) definiert.

Für die C++-Entwicklung wird ein Ereignistrigger durch die [**IEventTrigger-Schnittstelle**](/windows/desktop/api/taskschd/nn-taskschd-ieventtrigger) definiert.

## <a name="examples"></a>Beispiele

Ein vollständiges Beispiel für den XML-Code für eine Aufgabe, die einen Ereignistrigger verwendet, finden Sie unter [Ereignistriggerbeispiel (XML).](/previous-versions//aa446889(v=vs.85))

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

