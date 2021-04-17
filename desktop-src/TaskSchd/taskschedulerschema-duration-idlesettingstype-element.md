---
title: Duration (idlesettingstype)-Element
description: Gibt an, wie lange sich der Computer im Leerlauf befinden muss, bevor der Task ausgeführt wird.
ms.assetid: 89584694-0685-44e2-b8b7-69e47ee28d5d
keywords:
- Duration-Element Taskplaner
topic_type:
- apiref
api_name:
- Duration
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 31ad092693c72dcc33357f4b7e21436e2cba8af8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517564"
---
# <a name="duration-idlesettingstype-element"></a>Duration (idlesettingstype)-Element

Gibt an, wie lange sich der Computer im Leerlauf befinden muss, bevor der Task ausgeführt wird. Das Format dieser Zeichenfolge lautet pnynmndtnhnmns. dabei ist "NY" die Anzahl der Jahre, "nm" die Anzahl von Monaten, "ND" die Anzahl der Tage, "t" ist das Trennzeichen für Datum/Uhrzeit, "NH" die Anzahl von Stunden, "nm" die Anzahl der Minuten und "NS" die Anzahl von Sekunden (z Der Mindestwert ist eine Minute. Weitere Informationen zum Duration-Typ finden Sie unter <https://go.microsoft.com/fwlink/p/?linkid=106886> .

``` syntax
<xs:element name="Duration"
    default="PT10M"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="duration"
        >
            <xs:minInclusive
                value="PT1M"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

Das-Element wird durch den komplexen Typ [**idlesettingstype**](taskschedulerschema-idlesettingstype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                       | Abgeleitet von                                                                 | BESCHREIBUNG                                                                                       |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**Idlesettings**](taskschedulerschema-idlesettings-settingstype-element.md) | [**idlesettingstype**](taskschedulerschema-idlesettingstype-complextype.md) | Gibt an, wie die Taskplaner Aufgaben ausführt, wenn sich der Computer im Leerlauf befindet.<br/> |



## <a name="remarks"></a>Bemerkungen

Bei der Skriptprogrammierung wird diese Einstellung für den Leerlauf mithilfe der [**idlesettings. idleduration**](idlesettings-idleduration.md) -Eigenschaft angegeben.

Bei der C++-Programmierung wird diese Einstellung für den Leerlauf mithilfe der [**iidlesettings:: idleduration**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_idleduration) -Eigenschaft angegeben.

## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert eine Leerlauf Einstellung, die 5 Minuten für den Start der Aufgabe zulässt.


```XML
<IdleSettings>
    <Duration>PT5M</Duration>
</IdleSettings>
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

 

 





