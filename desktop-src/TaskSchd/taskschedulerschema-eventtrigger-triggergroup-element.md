---
title: Event Trigger-Element (triggergroup)
description: Gibt einen-Fehler an, der einen Task startet, wenn ein System Ereignis auftritt.
ms.assetid: 8faffc04-1ad2-499d-bcdf-bc28f64b8aa8
keywords:
- Taskplaner des Ereignis Auslösers, Element
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
ms.openlocfilehash: 3cecf46250fface0f716adbf287cda3269b86f04
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478180"
---
# <a name="eventtrigger-triggergroup-element"></a>Event Trigger-Element (triggergroup)

Gibt einen-Fehler an, der einen Task startet, wenn ein System Ereignis auftritt.

``` syntax
<xs:element name="EventTrigger"
    type="eventTriggerType"
 />
```

Das **EventTrigger** -Element wird von [**triggergroup**](taskschedulerschema-triggergroup-group.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                           | Abgeleitet von                                                         | BESCHREIBUNG                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [**Trigger**](taskschedulerschema-triggers-tasktype-element.md) | [**triggerstype**](taskschedulerschema-triggerstype-complextype.md) | Gibt die Trigger an, die den Task starten.<br/> |



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                                              | type                                                                     | BESCHREIBUNG                                                                                                                        |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Delay (eventtriggertype)**](taskschedulerschema-delay-eventtriggertype-element.md)               | duration                                                                 | Gibt die Zeitspanne zwischen dem Auftreten des Ereignisses und dem Start der Aufgabe an.<br/>                                |
| [**Aktiviert (triggerbasetype)**](taskschedulerschema-enabled-triggerbasetype-element.md)             | boolean                                                                  | Gibt an, dass der-Wert aktiviert ist.<br/>                                                                                  |
| [**Endboundary (triggerbasetype)**](taskschedulerschema-endboundary-triggerbasetype-element.md)     | dateTime                                                                 | Gibt das Datum und die Uhrzeit der Deaktivierung des Auslösers an. Der-Vorgang kann die Aufgabe nicht starten, nachdem Sie deaktiviert wurde.<br/> |
| [**Wiederholung (triggerbasetype)**](taskschedulerschema-repetition-triggerbasetype-element.md)       | [**Wiederholungstyp**](taskschedulerschema-repetitiontype-complextype.md) | Gibt an, wie oft die Aufgabe ausgeführt wird und wie lange das Wiederholungsmuster nach dem Start der Aufgabe wiederholt wird.<br/>          |
| [**StartBoundary (triggerbasetype)**](taskschedulerschema-startboundary-triggerbasetype-element.md) | dateTime                                                                 | Gibt das Datum und die Uhrzeit der Aktivierung des Auslösers an.<br/>                                                              |
| [**Abonnement (eventtriggertype)**](taskschedulerschema-subscription-eventtriggertype-element.md) | Zeichenfolge                                                                   | Gibt die XPath-Abfrage an, die das Ereignis identifiziert, das den-Triggern auslöst.<br/>                                             |



## <a name="attributes"></a>Attributes



| Name | type | BESCHREIBUNG                           |
|------|------|---------------------------------------|
| Id   | id   | Der Bezeichner des Auslösers.<br/> |



## <a name="remarks"></a>Bemerkungen

Es können maximal 500 Tasks mit Ereignis Abonnements erstellt werden. Ein Ereignis Abonnement, das Abfragen für eine Vielzahl von Ereignissen verwendet, kann verwendet werden, um eine Aufgabe zu initiieren, die dieselbe Aktion als Reaktion auf die protokollierten Ereignisse verwendet.

Bei der Skript Entwicklung wird ein Ereignis Trigger durch das [**EventTrigger**](eventtrigger.md) -Objekt definiert.

Bei der C++-Entwicklung wird ein Ereignis-von der [**IEvent-auslöserschnittstelle**](/windows/desktop/api/taskschd/nn-taskschd-ieventtrigger) definiert.

## <a name="examples"></a>Beispiele

Ein umfassendes Beispiel für den XML-Code für eine Aufgabe, die einen Ereignis Auslösers verwendet, finden Sie unter [Event-auslöserbeispiel (XML)](/previous-versions//aa446889(v=vs.85)).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

