---
title: Registrationtrigger (triggergroup)-Element
description: Gibt einen-Typ an, der einen Task startet, wenn der Task registriert wird.
ms.assetid: 8f028ed0-93e6-4423-be2f-9a02be99122b
keywords:
- Registrierungs-auslöserTaskplaner, XML-Element
- Registration-Auslöserelement Taskplaner
topic_type:
- apiref
api_name:
- RegistrationTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 90960f81d252b0b0a8d1de3ab5cc1465003467a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344688"
---
# <a name="registrationtrigger-triggergroup-element"></a>Registrationtrigger (triggergroup)-Element

Gibt einen-Typ an, der einen Task startet, wenn der Task registriert wird.

``` syntax
<xs:element name="RegistrationTrigger"
    type="registrationTriggerType"
 />
```

Das **registrationtrigger** -Element wird durch den komplexen Typ [**registrationtriggertype**](taskschedulerschema-registrationtriggertype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                           | Abgeleitet von                                                         | BESCHREIBUNG                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [**Trigger**](taskschedulerschema-triggers-tasktype-element.md) | [**triggerstype**](taskschedulerschema-triggerstype-complextype.md) | Gibt die Trigger an, die den Task starten.<br/> |



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                                                        | type                                                                     | BESCHREIBUNG                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Delay (registrationtriggertype)**](taskschedulerschema-delay-boottriggertype-element.md)                   | duration                                                                 | Gibt die Zeitspanne zwischen dem Registrieren der Aufgabe und dem Start der Aufgabe an.<br/>                          |
| [**Aktiviert (triggerbasetype)**](taskschedulerschema-enabled-triggerbasetype-element.md)                       | boolean                                                                  | Gibt an, dass der-Wert aktiviert ist.<br/>                                                                                  |
| [**Endboundary (triggerbasetype)**](taskschedulerschema-endboundary-triggerbasetype-element.md)               | dateTime                                                                 | Gibt das Datum und die Uhrzeit der Deaktivierung des Auslösers an. Der-Vorgang kann die Aufgabe nicht starten, nachdem Sie deaktiviert wurde.<br/> |
| [**Executiontimelimit (triggerbasetype)**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | duration                                                                 | Gibt die maximale Zeitspanne an, in der der Task vom-Vorgang gestartet werden kann.<br/>                                   |
| [**Wiederholung (triggerbasetype)**](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [**Wiederholungstyp**](taskschedulerschema-repetitiontype-complextype.md) | Gibt an, wie oft die Aufgabe ausgeführt wird und wie lange das Wiederholungsmuster nach dem Start der Aufgabe wiederholt wird.<br/>          |
| [**StartBoundary (triggerbasetype)**](taskschedulerschema-startboundary-triggerbasetype-element.md)           | dateTime                                                                 | Gibt das Datum und die Uhrzeit der Aktivierung des Auslösers an.<br/>                                                              |



## <a name="attributes"></a>Attributes



| Name | type | BESCHREIBUNG                           |
|------|------|---------------------------------------|
| Id   | id   | Der Bezeichner des Auslösers.<br/> |



## <a name="remarks"></a>Bemerkungen

Bei der Entwicklung von Skripts wird ein Registrierungs-Assistent mithilfe des [**Registration-auslöserobjekts**](registrationtrigger.md) angegeben.

Bei der C++-Entwicklung wird ein Registrierungs-Assistent mithilfe der [**iregistration-auslöserschnittstelle**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger) angegeben.

Die oben aufgeführten untergeordneten Elemente werden von den komplexen Elementtypen [**triggerbasetype**](taskschedulerschema-triggerbasetype-complextype.md) und [**registrationtriggertype**](taskschedulerschema-registrationtriggertype-complextype.md) definiert. Diese Elemente müssen in der unten gezeigten Sequenz hinzugefügt werden.

-   [**StartBoundary (triggerbasetype)**](taskschedulerschema-startboundary-triggerbasetype-element.md)
-   [**Endboundary (triggerbasetype)**](taskschedulerschema-endboundary-triggerbasetype-element.md)
-   [**Aktiviert (triggerbasetype)**](taskschedulerschema-enabled-triggerbasetype-element.md)
-   [**Wiederholung (triggerbasetype)**](taskschedulerschema-repetition-triggerbasetype-element.md)
-   [**Executiontimelimit (triggerbasetype)**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md)
-   [**Delay (registrationtriggertype)**](taskschedulerschema-delay-boottriggertype-element.md)

## <a name="examples"></a>Beispiele

Ein umfassendes Beispiel für den XML-Code für eine Aufgabe, die einen Start--Auslösers angibt, finden Sie unter [Beispiel für Registrierungs Beispiel (XML)](registration-trigger-example--xml-.md).

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

 

 





