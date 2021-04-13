---
title: Timetrigger-Element (triggergroup)
description: Gibt einen-Auslösers an, der einen Task startet, wenn der--ausgelöst wird
ms.assetid: bb467f36-47cd-4db4-97c4-60c09937caac
keywords:
- Time-Auslöserelement Taskplaner
topic_type:
- apiref
api_name:
- TimeTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 83d3b0a63a8be70af7eba4edb90e49db71892f5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478162"
---
# <a name="timetrigger-triggergroup-element"></a>Timetrigger-Element (triggergroup)

Gibt einen-Auslösers an, der einen Task startet, wenn der--ausgelöst wird

``` syntax
<xs:element name="TimeTrigger"
    type="timeTriggerType"
 />
```

Das **timetrigger** -Element wird von [**triggergroup**](taskschedulerschema-triggergroup-group.md) definiert.

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
| [**StartBoundary (triggerbasetype)**](taskschedulerschema-startboundary-triggerbasetype-element.md)           | dateTime                                                                 | Gibt das Datum und die Uhrzeit der Aktivierung des Auslösers an. Dieses Element ist erforderlich.<br/>                                    |



## <a name="attributes"></a>Attributes



| Name | type       | BESCHREIBUNG                               |
|------|------------|-------------------------------------------|
| Id   | **string** | Der Bezeichner des Auslösers.<br/> |



## <a name="remarks"></a>Bemerkungen

Das [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) -Element ist ein erforderliches Element für Zeit-und Kalender Trigger (**timetrigger** und [**calendartrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md)).

Bei der Skripterstellung wird ein Zeit-und Zeit Auslöserwert mit dem [**time-Auslöserobjekt**](timetrigger.md)

Bei der C++-Entwicklung wird mithilfe der [**Itime-auslöserschnittstelle**](/windows/desktop/api/taskschd/nn-taskschd-itimetrigger) ein Zeit-und ein Zeit--

Die oben aufgeführten untergeordneten Elemente werden von den komplexen [**triggerbasetype**](taskschedulerschema-triggerbasetype-complextype.md) -Elementtypen definiert. Diese Elemente müssen in der unten gezeigten Sequenz hinzugefügt werden.

-   [**StartBoundary (triggerbasetype)**](taskschedulerschema-startboundary-triggerbasetype-element.md)
-   [**Endboundary (triggerbasetype)**](taskschedulerschema-endboundary-triggerbasetype-element.md)
-   [**Aktiviert (triggerbasetype)**](taskschedulerschema-enabled-triggerbasetype-element.md)
-   [**Wiederholung (triggerbasetype)**](taskschedulerschema-repetition-triggerbasetype-element.md)
-   [**Executiontimelimit (triggerbasetype)**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md)

## <a name="examples"></a>Beispiele

Ein umfassendes Beispiel für den XML-Code für eine Aufgabe, die einen Zeit--Timeout angibt, finden Sie unter [time-auslöserbeispiel (XML)](time-trigger-example--xml-.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





