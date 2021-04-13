---
title: Logontrigger-Element (triggergroup)
description: Gibt einen-Vorgang an, der einen Task startet, wenn sich ein Benutzer anmeldet.
ms.assetid: c3edee50-e053-4813-a1b2-bf1e7b575ff7
keywords:
- Logon-, XML-Element
- Logon-Auslöserelement Taskplaner
topic_type:
- apiref
api_name:
- LogonTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c89d0e593277f1c854850017412b49c22d8ac436
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340547"
---
# <a name="logontrigger-triggergroup-element"></a>Logontrigger-Element (triggergroup)

Gibt einen-Vorgang an, der einen Task startet, wenn sich ein Benutzer anmeldet.

``` syntax
<xs:element name="LogonTrigger"
    type="logonTriggerType"
 />
```

Das **logontrigger** -Element wird von [**triggergroup**](taskschedulerschema-triggergroup-group.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                           | Abgeleitet von                                                         | BESCHREIBUNG                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [**Trigger**](taskschedulerschema-triggers-tasktype-element.md) | [**triggerstype**](taskschedulerschema-triggerstype-complextype.md) | Gibt die Trigger an, die den Task starten.<br/> |



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                                                        | type                                                                     | BESCHREIBUNG                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Delay (logontriggertype)**](taskschedulerschema-delay-logontriggertype-element.md)                         | duration                                                                 | Zeitraum zwischen dem Zeitpunkt, an dem sich der Benutzer anmeldet, und dem Start der Aufgabe.<br/>                                              |
| [**Aktiviert (triggerbasetype)**](taskschedulerschema-enabled-triggerbasetype-element.md)                       | boolean                                                                  | Gibt an, dass der-Wert aktiviert ist.<br/>                                                                                  |
| [**Endboundary (triggerbasetype)**](taskschedulerschema-endboundary-triggerbasetype-element.md)               | dateTime                                                                 | Gibt das Datum und die Uhrzeit der Deaktivierung des Auslösers an. Der-Vorgang kann die Aufgabe nicht starten, nachdem Sie deaktiviert wurde.<br/> |
| [**Executiontimelimit (triggerbasetype)**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | duration                                                                 | Gibt die maximale Zeitspanne an, in der der Task vom-Vorgang gestartet werden kann.<br/>                                   |
| [**Wiederholung (triggerbasetype)**](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [**Wiederholungstyp**](taskschedulerschema-repetitiontype-complextype.md) | Gibt an, wie oft die Aufgabe ausgeführt wird und wie lange das Wiederholungsmuster nach dem Start der Aufgabe wiederholt wird.<br/>          |
| [**StartBoundary (triggerbasetype)**](taskschedulerschema-startboundary-triggerbasetype-element.md)           | dateTime                                                                 | Gibt das Datum und die Uhrzeit der Aktivierung des Auslösers an.<br/>                                                              |
| [**UserID (logontriggertype)**](taskschedulerschema-userid-logontriggertype-element.md)                       | Zeichenfolge                                                                   | Der Bezeichner des Benutzers. Der Task wird gestartet, wenn sich dieser Benutzer auf dem Computer anmeldet.<br/>                                      |



## <a name="remarks"></a>Bemerkungen

Bei der Skripterstellung wird ein LOGON-Ereignis mithilfe des [**Logon-auslöserobjekts**](logontrigger.md) angegeben.

Bei der C++-Entwicklung wird ein LOGON-Ereignis mithilfe der [**iLogon-**](/windows/desktop/api/taskschd/nn-taskschd-ilogontrigger) Schnittstelle angegeben.

Die oben aufgeführten untergeordneten Elemente werden von den komplexen Elementtypen [**triggerbasetype**](taskschedulerschema-triggerbasetype-complextype.md) und [**logontriggertype**](taskschedulerschema-logontriggertype-complextype.md) definiert. Diese Elemente müssen in der unten gezeigten Sequenz hinzugefügt werden.

-   [**StartBoundary (triggerbasetype)**](taskschedulerschema-startboundary-triggerbasetype-element.md)
-   [**Endboundary (triggerbasetype)**](taskschedulerschema-endboundary-triggerbasetype-element.md)
-   [**Aktiviert (triggerbasetype)**](taskschedulerschema-enabled-triggerbasetype-element.md)
-   [**Wiederholung (triggerbasetype)**](taskschedulerschema-repetition-triggerbasetype-element.md)
-   [**Executiontimelimit (triggerbasetype)**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md)
-   [**UserID (logontriggertype)**](taskschedulerschema-userid-logontriggertype-element.md)
-   [**Delay (logontriggertype)**](taskschedulerschema-delay-logontriggertype-element.md)

### <a name="attributes"></a>Attribute

Das unten aufgeführte Attribut wird von den komplexen [**triggerbasetype**](taskschedulerschema-triggerbasetype-complextype.md) -Elementtypen definiert.

-   ID: der Bezeichner des Auslösers.

## <a name="examples"></a>Beispiele

Ein umfassendes Beispiel für den XML-Code für eine Aufgabe, die einen Logon-Auslösers verwendet, finden Sie unter [Logon-Beispiel Beispiel (XML)](logon-trigger-example--xml-.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Schema Elemente Taskplaner](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





