---
title: Delay (logontriggertype)-Element
description: Zeitraum zwischen dem Zeitpunkt, an dem sich der Benutzer anmeldet, und dem Start der Aufgabe.
ms.assetid: daab29f7-5d05-4e6d-a0c0-7b83b4d0b941
keywords:
- Verzögertes Element Taskplaner
topic_type:
- apiref
api_name:
- Delay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a820bad3d68cfb0a697f795a9fd7326c9e52abe9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478903"
---
# <a name="delay-logontriggertype-element"></a>Delay (logontriggertype)-Element

Zeitraum zwischen dem Zeitpunkt, an dem sich der Benutzer anmeldet, und dem Start der Aufgabe. Das Format dieser Zeichenfolge lautet pnynmndtnhnmns. dabei ist "NY" die Anzahl der Jahre, "nm" die Anzahl von Monaten, "ND" die Anzahl der Tage, "t" ist das Trennzeichen für Datum/Uhrzeit, "NH" die Anzahl von Stunden, "nm" die Anzahl der Minuten und "NS" die Anzahl von Sekunden (z Weitere Informationen zum Duration-Typ finden Sie unter <https://go.microsoft.com/fwlink/p/?linkid=106886> .

``` syntax
<xs:element name="Delay"
    type="duration"
 />
```

Das **Delay** -Element wird durch den komplexen [**logontriggertype**](taskschedulerschema-logontriggertype-complextype.md) -Typ definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                       | Abgeleitet von                                                                 | BESCHREIBUNG                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**Logonauslöst**](taskschedulerschema-logontrigger-triggergroup-element.md) | [**logontriggertype**](taskschedulerschema-logontriggertype-complextype.md) | Gibt einen-Vorgang an, der einen Task startet, wenn sich ein Benutzer anmeldet.<br/> |



## <a name="remarks"></a>Bemerkungen

Bei der Skripterstellung wird die Verzögerung des LOGON-Auslösers mithilfe der [**LOGON-Eigenschaft. Delay**](logontrigger-delay.md) angegeben.

Bei der C++-Entwicklung wird die Benutzer-ID für den Logon-Auslösers mithilfe der [**iLogon-:D Elay**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_delay) -Eigenschaft angegeben.

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

 

 





