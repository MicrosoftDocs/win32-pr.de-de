---
title: Delay (logonTriggerType)-Element
description: Die Zeitspanne zwischen der Anmeldung des Benutzers und dem Start der Aufgabe.
ms.assetid: daab29f7-5d05-4e6d-a0c0-7b83b4d0b941
keywords:
- Delay-Element Taskplaner
topic_type:
- apiref
api_name:
- Delay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1bd18652630ad14f9b888db6a810d8da1eb42a18fb9d2caa6726414aa9054702
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118357136"
---
# <a name="delay-logontriggertype-element"></a>Delay (logonTriggerType)-Element

Die Zeitspanne zwischen der Anmeldung des Benutzers und dem Start der Aufgabe. Das Format für diese Zeichenfolge lautet PnYnMnDTnHnMnS, wobei nY die Anzahl der Jahre, nM die Anzahl der Monate, nD die Anzahl der Tage, "T" das Datums-/Uhrzeittrennzeichen, nH die Anzahl der Stunden, nM die Anzahl der Minuten und nS die Anzahl von Sekunden ist (z. B. PT5M gibt 5 Minuten an, und P1M4DT2H5M gibt einen Monat, vier Tage, zwei Stunden und fünf Minuten an). Weitere Informationen zum Dauertyp finden Sie unter <https://go.microsoft.com/fwlink/p/?linkid=106886> .

``` syntax
<xs:element name="Delay"
    type="duration"
 />
```

Das **Delay-Element** wird durch den [**komplexen LogonTriggerType-Typ**](taskschedulerschema-logontriggertype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                       | Abgeleitet von                                                                 | BESCHREIBUNG                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md) | [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md) | Gibt einen Trigger an, der eine Aufgabe startet, wenn sich ein Benutzer anmeldet.<br/> |



## <a name="remarks"></a>Hinweise

Für die Skriptentwicklung wird die Verzögerung des Anmeldetriggers mithilfe der [**LogonTrigger.Delay-Eigenschaft**](logontrigger-delay.md) angegeben.

Für die C++-Entwicklung wird der Benutzerbezeichner für den Anmeldetrigger mithilfe der [**ILogonTrigger::D elay-Eigenschaft**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_delay) angegeben.

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

 

 





