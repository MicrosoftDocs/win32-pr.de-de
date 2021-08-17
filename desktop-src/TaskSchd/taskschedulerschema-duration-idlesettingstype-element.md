---
title: Duration (idleSettingsType)-Element
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
ms.openlocfilehash: 46523caa10f96d7dd76947540932107106ad0d5c8a4b7f26fc6f6d5bebb40325
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118356567"
---
# <a name="duration-idlesettingstype-element"></a>Duration (idleSettingsType)-Element

Gibt an, wie lange sich der Computer im Leerlauf befinden muss, bevor der Task ausgeführt wird. Das Format für diese Zeichenfolge lautet PnYnMnDTnHnMnS, wobei nY die Anzahl der Jahre, nM die Anzahl der Monate, nD die Anzahl der Tage, "T" das Datums-/Uhrzeittrennzeichen, nH die Anzahl der Stunden, nM die Anzahl der Minuten und nS die Anzahl von Sekunden ist (z. B. PT5M gibt 5 Minuten an, und P1M4DT2H5M gibt einen Monat, vier Tage, zwei Stunden und fünf Minuten an). Der Mindestwert beträgt eine Minute. Weitere Informationen zum Dauertyp finden Sie unter <https://go.microsoft.com/fwlink/p/?linkid=106886> .

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

Das Element wird durch den komplexen [**idleSettingsType-Typ**](taskschedulerschema-idlesettingstype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                       | Abgeleitet von                                                                 | BESCHREIBUNG                                                                                       |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md) | [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) | Gibt an, wie der Taskplaner Aufgaben ausführt, wenn sich der Computer im Leerlauf befindet.<br/> |



## <a name="remarks"></a>Hinweise

Für die Skriptprogrammierung wird diese Leerlaufeinstellung mithilfe der [**IdleSettings.IdleDuration-Eigenschaft**](idlesettings-idleduration.md) angegeben.

Für die C++-Programmierung wird diese Leerlaufeinstellung mithilfe der [**IIdleSettings::IdleDuration-Eigenschaft**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_idleduration) angegeben.

## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert eine Leerlaufeinstellung, die 5 Minuten für den Start der Aufgabe zulässt.


```XML
<IdleSettings>
    <Duration>PT5M</Duration>
</IdleSettings>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Taskplaner Schemaelemente](task-scheduler-schema-elements.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





