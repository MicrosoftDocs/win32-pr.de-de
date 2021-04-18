---
title: WaitTimeout (idlesettingstype)-Element
description: Gibt die Zeitspanne an, die der Taskplaner auf das Eintreten einer Leerlauf Bedingung wartet.
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
ms.openlocfilehash: 16f71a014358a8e0520274d1ff853cf6146aa05d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518479"
---
# <a name="waittimeout-idlesettingstype-element"></a>WaitTimeout (idlesettingstype)-Element

Gibt die Zeitspanne an, die der Taskplaner auf das Eintreten einer Leerlauf Bedingung wartet. Wenn für dieses Element kein Wert angegeben wird, wartet der Taskplaner-Dienst unbegrenzt, bis eine Leerlauf Bedingung auftritt. Das Format dieser Zeichenfolge lautet pnynmndtnhnmns. dabei ist "NY" die Anzahl der Jahre, "nm" die Anzahl von Monaten, "ND" die Anzahl der Tage, "t" ist das Trennzeichen für Datum/Uhrzeit, "NH" die Anzahl von Stunden, "nm" die Anzahl der Minuten und "NS" die Anzahl von Sekunden (z Weitere Informationen zum Duration-Typ finden Sie unter <https://go.microsoft.com/fwlink/p/?linkid=106886> . Die zulässige minimal Zeit beträgt 1 Minute.

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

Das-Element wird durch den komplexen Typ [**idlesettingstype**](taskschedulerschema-idlesettingstype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                       | Abgeleitet von                                                                 | BESCHREIBUNG                                                                                       |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**Idlesettings**](taskschedulerschema-idlesettings-settingstype-element.md) | [**idlesettingstype**](taskschedulerschema-idlesettingstype-complextype.md) | Gibt an, wie die Taskplaner Aufgaben ausführt, wenn sich der Computer im Leerlauf befindet.<br/> |



## <a name="remarks"></a>Bemerkungen

Bei der Skript Entwicklung wird diese Einstellung für den Leerlauf mithilfe der [**idlesettings. WaitTimeout**](idlesettings-waittimeout.md) -Eigenschaft angegeben.

Bei der C++-Entwicklung wird diese Einstellung für den Leerlauf mithilfe der [**iidlesettings:: WaitTimeout**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_waittimeout) -Eigenschaft angegeben.

## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert eine Leerlauf Einstellung, die 24 Stunden wartet, bis eine Leerlauf Bedingung auftritt.


```XML
<IdleSettings>
    <WaitTimeout>PT24H</WaitTimeout>
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

 

 





