---
title: Idletrigger-Element (triggergroup)
description: Gibt einen-Auslösers an, der einen Task startet, wenn der Computer in den Leerlauf wechselt.
ms.assetid: c3e317b5-d1a7-46de-ace5-e066452583d3
keywords:
- Leerlauf-, XML-Element
- Idle-Auslöserelement Taskplaner
topic_type:
- apiref
api_name:
- IdleTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 221d272145670b9514cde5ffbe8b02e5ddcd6e0c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040282"
---
# <a name="idletrigger-triggergroup-element"></a>Idletrigger-Element (triggergroup)

Gibt einen-Auslösers an, der einen Task startet, wenn der Computer in den Leerlauf wechselt. Informationen zu Bedingungen im Leerlauf finden Sie unter [Aufgaben im Leerlauf](task-idle-conditions.md).

``` syntax
<xs:element name="IdleTrigger"
    type="idleTriggerType"
 />
```

Das **idletrigger** -Element wird von [**triggergroup**](taskschedulerschema-triggergroup-group.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                           | Abgeleitet von                                                         | BESCHREIBUNG                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [**Trigger**](taskschedulerschema-triggers-tasktype-element.md) | [**triggerstype**](taskschedulerschema-triggerstype-complextype.md) | Gibt die Trigger an, die den Task starten.<br/> |



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                                                        | type                                                                     | BESCHREIBUNG                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Aktiviert (triggerbasetype)**](taskschedulerschema-enabled-triggerbasetype-element.md)                       | boolean                                                                  | Gibt an, dass der-Wert aktiviert ist.<br/>                                                                                  |
| [**Endboundary (triggerbasetype)**](taskschedulerschema-endboundary-triggerbasetype-element.md)               | dateTime                                                                 | Gibt das Datum und die Uhrzeit der Deaktivierung des Auslösers an. Der-Vorgang kann die Aufgabe nicht starten, nachdem Sie deaktiviert wurde.<br/> |
| [**Executiontimelimit (triggerbasetype)**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | duration                                                                 | Gibt die maximale Zeitspanne an, in der der Task vom-Vorgang gestartet werden kann.<br/>                                   |
| [**Wiederholung (triggerbasetype)**](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [**Wiederholungstyp**](taskschedulerschema-repetitiontype-complextype.md) | Gibt an, wie oft die Aufgabe ausgeführt wird und wie lange das Wiederholungsmuster nach dem Start der Aufgabe wiederholt wird.<br/>          |
| [**StartBoundary (triggerbasetype)**](taskschedulerschema-startboundary-triggerbasetype-element.md)           | dateTime                                                                 | Gibt das Datum und die Uhrzeit der Aktivierung des Auslösers an.<br/>                                                              |



## <a name="attributes"></a>Attributes



| Name | type   | BESCHREIBUNG                               |
|------|--------|-------------------------------------------|
| Id   | string | Der Bezeichner des Auslösers.<br/> |



## <a name="remarks"></a>Bemerkungen

Bei der Skripterstellung wird ein Leerlauf--Auslösung mithilfe des [**Idle-auslöserobjekts**](idletrigger.md) angegeben.

Bei der C++-Entwicklung wird mithilfe der [**iidletimeout**](/windows/win32/api/taskschd/nn-taskschd-iidletrigger) -Schnittstelle ein Leerlauf-Auslösers angegeben.

Die oben aufgeführten untergeordneten Elemente werden von den komplexen [**triggerbasetype**](taskschedulerschema-triggerbasetype-complextype.md) -Elementtypen definiert. Diese Elemente müssen in der unten gezeigten Sequenz hinzugefügt werden.

-   [**StartBoundary (triggerbasetype)**](taskschedulerschema-startboundary-triggerbasetype-element.md)
-   [**Endboundary (triggerbasetype)**](taskschedulerschema-endboundary-triggerbasetype-element.md)
-   [**Aktiviert (triggerbasetype)**](taskschedulerschema-enabled-triggerbasetype-element.md)
-   [**Wiederholung (triggerbasetype)**](taskschedulerschema-repetition-triggerbasetype-element.md)
-   [**Executiontimelimit (triggerbasetype)**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md)

## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert einen Leerlauf-Auslösung.


```XML
<IdleTrigger>
    <StartBoundary>2005-01-01T00:08:00</StartBoundary>
    <EndBounadry>2007-01-01T00:08:00</EndBoundary>
    <Enabled></Enabled>
    <Repetition></Repetition>
    <ExecutionTimeLimit></ExecutionTimeLimit>
</IdleTrigger>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Schema Elemente Taskplaner](task-scheduler-schema-elements.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

