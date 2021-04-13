---
title: Boottrigger-Element (triggergroup)
description: Gibt einen-Fehler an, mit dem eine Aufgabe gestartet wird, wenn das System gestartet wird.
ms.assetid: c6833547-0daf-4e8a-b8c5-b422827b1d96
keywords:
- Taskplaner des Start Auslösers, XML-Element
- Boottrigger-Element Taskplaner
topic_type:
- apiref
api_name:
- BootTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eb6ccf590893e19340662fd4c47e4aa68047b29d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340948"
---
# <a name="boottrigger-triggergroup-element"></a>Boottrigger-Element (triggergroup)

Gibt einen-Fehler an, mit dem eine Aufgabe gestartet wird, wenn das System gestartet wird.

``` syntax
<xs:element name="BootTrigger"
    type="bootTriggerType"
 />
```

Das **boottrigger** -Element wird durch den komplexen [**boottriggertype**](taskschedulerschema-boottriggertype-complextype.md) -Typ definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                           | Abgeleitet von                                                         | BESCHREIBUNG                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [**Trigger**](taskschedulerschema-triggers-tasktype-element.md) | [**triggerstype**](taskschedulerschema-triggerstype-complextype.md) | Gibt die Trigger an, die den Task starten.<br/> |



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                                                        | type                                                                     | BESCHREIBUNG                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Verzögerung (boottriggertype)**](taskschedulerschema-delay-boottriggertype-element.md)                           | duration                                                                 | Gibt den Zeitraum zwischen dem Start des Systems und dem Start der Aufgabe an.<br/>                            |
| [**Aktiviert (triggerbasetype)**](taskschedulerschema-enabled-triggerbasetype-element.md)                       | boolean                                                                  | Gibt an, dass der-Wert aktiviert ist.<br/>                                                                                  |
| [**Endboundary (triggerbasetype)**](taskschedulerschema-endboundary-triggerbasetype-element.md)               | dateTime                                                                 | Gibt das Datum und die Uhrzeit der Deaktivierung des Auslösers an. Der-Vorgang kann die Aufgabe nicht starten, nachdem Sie deaktiviert wurde.<br/> |
| [**Executiontimelimit (triggerbasetype)**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | duration                                                                 | Gibt die maximale Zeitspanne an, in der der Task vom-Vorgang gestartet werden kann.<br/>                                   |
| [**Wiederholung (triggerbasetype)**](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [**Wiederholungstyp**](taskschedulerschema-repetitiontype-complextype.md) | Gibt an, wie oft die Aufgabe ausgeführt wird und wie lange das Wiederholungsmuster nach dem Start der Aufgabe wiederholt wird.<br/>          |
| [**StartBoundary (triggerbasetype)**](taskschedulerschema-startboundary-triggerbasetype-element.md)           | dateTime                                                                 | Gibt das Datum und die Uhrzeit der Aktivierung des Auslösers an.<br/>                                                              |



## <a name="attributes"></a>Attributes



| Name | type       | BESCHREIBUNG                               |
|------|------------|-------------------------------------------|
| Id   | **string** | Der Bezeichner des Auslösers.<br/> |



## <a name="remarks"></a>Bemerkungen

Bei der Skript Entwicklung wird ein Start-ausgelöst, der vom [**boottrigger**](boottrigger.md) -Objekt definiert wird.

Bei der C++-Entwicklung wird ein Start-- [**Debugger durch das iboottrigger**](/windows/desktop/api/taskschd/nn-taskschd-iboottrigger) -Objekt definiert.

## <a name="examples"></a>Beispiele

Ein umfassendes Beispiel für den XML-Code für eine Aufgabe, die einen Start--Auslösers angibt, finden Sie unter Beispiel für den [Start-Beispiel](boot-trigger-example--xml-.md)

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

 

 





