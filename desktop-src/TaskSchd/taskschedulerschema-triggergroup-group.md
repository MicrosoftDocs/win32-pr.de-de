---
title: triggergroup-Gruppe
description: Definiert die auslösergruppe.
ms.assetid: e07e6999-d982-405b-adfd-2976707b999f
keywords:
- triggergroup-Taskplaner
topic_type:
- apiref
api_name:
- triggerGroup
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ce0203cd9515808891f93223dd7b3ebaf2642103
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106341"
---
# <a name="triggergroup-group"></a>triggergroup-Gruppe

Definiert die auslösergruppe.

``` syntax
<xs:group name="triggerGroup">
    <xs:choice>
        <xs:element name="BootTrigger"
            type="bootTriggerType"
            minOccurs="0"
         />
        <xs:element name="RegistrationTrigger"
            type="registrationTriggerType"
            minOccurs="0"
         />
        <xs:element name="IdleTrigger"
            type="idleTriggerType"
            minOccurs="0"
         />
        <xs:element name="TimeTrigger"
            type="timeTriggerType"
            minOccurs="0"
         />
        <xs:element name="EventTrigger"
            type="eventTriggerType"
            minOccurs="0"
         />
        <xs:element name="LogonTrigger"
            type="logonTriggerType"
            minOccurs="0"
         />
        <xs:element name="SessionStateChangeTrigger"
            type="sessionStateChangeTriggerType"
            minOccurs="0"
         />
        <xs:element name="CalendarTrigger"
            type="calendarTriggerType"
            minOccurs="0"
         />
    </xs:choice>
</xs:group>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                                                 | type                                                                                                   | BESCHREIBUNG                                                                                                       |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [**Boottrigger**](taskschedulerschema-boottrigger-triggergroup-element.md)                             | [**boottriggertype**](taskschedulerschema-boottriggertype-complextype.md)                             | Ein-Fehler, mit dem eine Aufgabe gestartet wird, wenn das System gestartet wird.<br/>                                                |
| [**Calendarausgelöst**](taskschedulerschema-calendartrigger-triggergroup-element.md)                     | [**calendartriggertype**](taskschedulerschema-calendartriggertype-complextype.md)                     | Ein-Vorgang, bei dem eine Aufgabe auf Grundlage eines täglichen, wöchentlichen, monatlichen oder monatlichen Zeitplans (Day-of-week, Dow) gestartet wird.<br/> |
| [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md)                           | [**eventtriggertype**](taskschedulerschema-eventtriggertype-complextype.md)                           | Ein-Fehler, der eine Aufgabe startet, wenn ein System Ereignis auftritt.<br/>                                               |
| [**Idle-Auslösung**](taskschedulerschema-idletrigger-triggergroup-element.md)                             | [**idletriggertype**](taskschedulerschema-idletriggertype-complextype.md)                             | Ein-Vorgang, der einen Task startet, wenn der Computer in den Leerlauf wechselt.<br/>                                |
| [**Logonauslöst**](taskschedulerschema-logontrigger-triggergroup-element.md)                           | [**logontriggertype**](taskschedulerschema-logontriggertype-complextype.md)                           | Ein-Vorgang, der einen Task startet, wenn sich ein Benutzer anmeldet.<br/>                                                      |
| [**Registration-Auslösers**](taskschedulerschema-registrationtrigger-triggergroup-element.md)             | [**registrationtriggertype**](taskschedulerschema-registrationtriggertype-complextype.md)             | Ein-Vorgang, der einen Task startet, wenn der Task registriert wird.<br/>                                              |
| [**Sessionstatechange-Auslösers**](taskschedulerschema-sessionstatechangetrigger-triggergroup-element.md) | [**sessionstatechangetriggertype**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) | Ein-Vorgang, der einen Task startet, wenn sich der Status einer Terminal Server Sitzung ändert.<br/>                             |
| [**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md)                             | [**timetriggertype**](taskschedulerschema-timetriggertype-complextype.md)                             | Ein-Vorgang, der einen Task startet, wenn der-Auslösers aktiviert ist.<br/>                                            |



## <a name="remarks"></a>Bemerkungen

Beim Lesen oder Schreiben von XML sind die Elemente, die von dieser Gruppe definiert werden, die untergeordneten [**Elemente des Triggers-Elements.**](taskschedulerschema-triggers-tasktype-element.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





