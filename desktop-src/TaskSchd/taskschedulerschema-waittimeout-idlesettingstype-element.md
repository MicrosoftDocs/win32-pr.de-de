---
title: WaitTimeout-Element (idleSettingsType)
description: Gibt die Zeitspanne an, die der Taskplaner auf das Auftreten einer Leerlaufbedingung wartet.
ms.assetid: 6a4cc80d-adc2-47a7-946f-a9f12eeb35a4
keywords:
- WaitTimeout-Element Taskplaner
topic_type:
- apiref
api_name:
- WaitTimeout
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4d078acecf39f9bd4848cabaa8b203787049ca8a66e565e6183b8b1998389ad8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118610395"
---
# <a name="waittimeout-idlesettingstype-element"></a>WaitTimeout-Element (idleSettingsType)

Gibt die Zeitspanne an, die der Taskplaner auf das Auftreten einer Leerlaufbedingung wartet. Wenn für dieses Element kein Wert angegeben wird, wartet der Taskplaner-Dienst unbegrenzt, bis eine Leerlaufbedingung auftritt. Das Format für diese Zeichenfolge lautet PnYnMnDTnHnMnS, wobei nY die Anzahl der Jahre, nM die Anzahl der Monate, nD die Anzahl der Tage, "T" das Datums-/Uhrzeittrennzeichen, nH die Anzahl der Stunden, nM die Anzahl der Minuten und nS die Anzahl von Sekunden ist (z. B. PT5M gibt 5 Minuten an, und P1M4DT2H5M gibt einen Monat, vier Tage, zwei Stunden und fünf Minuten an). Weitere Informationen zum Dauertyp finden Sie unter <https://go.microsoft.com/fwlink/p/?linkid=106886> . Die zulässige Mindestzeit beträgt 1 Minute.

``` syntax
<xs:element name="WaitTimeout"
    default="PT1H"
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



| Element                                                                       | Abgeleitet von                                                                 | Beschreibung                                                                                       |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md) | [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) | Gibt an, wie der Taskplaner Aufgaben ausführt, wenn sich der Computer im Leerlauf befindet.<br/> |



## <a name="remarks"></a>Hinweise

Für die Skriptentwicklung wird diese Leerlaufeinstellung mithilfe der [**IdleSettings.WaitTimeout-Eigenschaft**](idlesettings-waittimeout.md) angegeben.

Für die C++-Entwicklung wird diese Leerlaufeinstellung mithilfe der [**IIdleSettings::WaitTimeout-Eigenschaft**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_waittimeout) angegeben.

## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert eine Leerlaufeinstellung, die 24 Stunden wartet, bis eine Leerlaufbedingung auftritt.


```XML
<IdleSettings>
    <WaitTimeout>PT24H</WaitTimeout>
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

 

 





