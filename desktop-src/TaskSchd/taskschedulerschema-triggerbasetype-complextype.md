---
title: komplexer triggerbasetype-Typ
description: Definiert das Attribut, die untergeordneten Basiselemente und die Sequenzierungs Informationen für alle komplexen Auslösertypen.
ms.assetid: 1a2d004a-6f52-42b7-b0d0-ace8d27e9166
keywords:
- komplexer triggerbasetype-Typ Taskplaner
topic_type:
- apiref
api_name:
- triggerBaseType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 56602e4a7e6599b7b756ff6bc109376dddc63ac0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341297"
---
# <a name="triggerbasetype-complex-type"></a>komplexer triggerbasetype-Typ

Definiert das Attribut, die untergeordneten Basiselemente und die Sequenzierungs Informationen für alle komplexen Auslösertypen.

``` syntax
<xs:complexType name="triggerBaseType"
    abstract="true"
>
    <xs:sequence>
        <xs:element name="Enabled"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="StartBoundary"
            type="dateTime"
            minOccurs="0"
         />
        <xs:element name="EndBoundary"
            type="dateTime"
            minOccurs="0"
         />
        <xs:element name="Repetition"
            type="repetitionType"
            minOccurs="0"
         />
        <xs:element name="ExecutionTimeLimit"
            type="duration"
            minOccurs="0"
         />
    </xs:sequence>
    <xs:attribute name="id"
        type="ID"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                                      | type                                                                     | BESCHREIBUNG                                                                                                            |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**Aktiviert**](taskschedulerschema-enabled-triggerbasetype-element.md)                       | boolean                                                                  | Gibt an, dass der-Wert aktiviert ist.<br/>                                                                      |
| [**Endgrenze**](taskschedulerschema-endboundary-triggerbasetype-element.md)               | dateTime                                                                 | Das Datum und die Uhrzeit der Deaktivierung des Auslösers.<br/>                                                          |
| [**Executiontimelimit**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | duration                                                                 | Gibt das Intervall an, in dem der-Task den Task starten kann.<br/>                                                 |
| [**Wiederholen**](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [**Wiederholungstyp**](taskschedulerschema-repetitiontype-complextype.md) | Gibt an, wie oft die Aufgabe ausgeführt wird und wie lange das Wiederholungsmuster nach dem Auslösen des Triggers wiederholt wird.<br/> |
| [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md)           | dateTime                                                                 | Das Datum und die Uhrzeit der Aktivierung des Auslösers.<br/>                                                            |



## <a name="attributes"></a>Attributes



| Name | type | BESCHREIBUNG                           |
|------|------|---------------------------------------|
| id   | id   | Der Bezeichner des Auslösers.<br/> |



## <a name="remarks"></a>Bemerkungen

Zu den komplexen Auslösertypen zählen die folgenden.

-   [**boottriggertype**](taskschedulerschema-boottriggertype-complextype.md)
-   [**calendartriggertype**](taskschedulerschema-calendartriggertype-complextype.md)
-   [**eventtriggertype**](taskschedulerschema-eventtriggertype-complextype.md)
-   [**idletriggertype**](taskschedulerschema-idletriggertype-complextype.md)
-   [**logontriggertype**](taskschedulerschema-logontriggertype-complextype.md)
-   [**registrationtriggertype**](taskschedulerschema-registrationtriggertype-complextype.md)
-   [**timetriggertype**](taskschedulerschema-timetriggertype-complextype.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Komplexe Typen von Taskplaner Schemas](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





