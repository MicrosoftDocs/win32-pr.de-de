---
title: Delay-Element (registrationTriggerType)
description: Gibt die Zeit zwischen dem Zeitpunkt der Registrierung und dem Start der Aufgabe an.
ms.assetid: 8955d86c-8306-45e7-93cf-eacf50e10075
keywords:
- Delay-Taskplaner
topic_type:
- apiref
api_name:
- Delay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cd7ba3e9fd0fb71da628ee15bc0f1bdf6281e74ef20f259faf7a5a63504a6f12
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118131849"
---
# <a name="delay-registrationtriggertype-element"></a>Delay-Element (registrationTriggerType)

Gibt die Zeit zwischen dem Zeitpunkt der Registrierung und dem Start der Aufgabe an. Das Format für diese Zeichenfolge ist PnYnMnDTnHnMnS, Dabei steht nY für die Anzahl von Jahren, nM für die Anzahl der Monate, nD für die Anzahl von Tagen, "T" für das Datums-/Uhrzeittrennzeichen, nH für die Anzahl von Stunden, nM für die Anzahl von Minuten und nS für die Anzahl von Sekunden (pt5M gibt beispielsweise 5 Minuten an, und P1M4DT2H5M gibt einen Monat, vier Tage, zwei Stunden und fünf Minuten an). Weitere Informationen zum Dauertyp finden Sie unter <https://go.microsoft.com/fwlink/p/?linkid=106886> .

``` syntax
<xs:element name="Delay"
    type="duration"
 />
```

Das **Delay-Element** wird durch den komplexen [**RegistrationTriggerType-Typ**](taskschedulerschema-registrationtriggertype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                                     | Abgeleitet von                                                                               | BESCHREIBUNG                                                                    |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md) | Gibt einen Trigger an, der eine Aufgabe startet, wenn die Aufgabe registriert wird.<br/> |



## <a name="remarks"></a>Hinweise

Für die Skriptentwicklung wird die Verzögerung des Registrierungstriggers mithilfe der [**RegistrationTrigger.Delay-Eigenschaft**](registrationtrigger-delay.md) angegeben.

Für die C++-Entwicklung wird die Verzögerung des Registrierungstriggers mithilfe der [**IRegistrationTrigger::D elay-Eigenschaft**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationtrigger-get_delay) angegeben.

## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert eine Verzögerung des Registrierungstriggers, die eine Verzögerung von 5 Minuten zwischen der Registrierung des Task und dem Start des Task zulässt.


```XML
<BootTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T08:00:00</EndBoundary>
    <Enabled></Enabled>
    <Repetition></Repetition>
    <ExecutionTimeLimit></ExecutionTimeLimit>
    <Delay>PT5M<Delay>
 </BootTrigger>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Taskplaner Schemaelemente](task-scheduler-schema-elements.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





