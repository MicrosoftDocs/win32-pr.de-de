---
title: Delay (bootTriggerType)-Element
description: Gibt die Zeitspanne zwischen dem Start des Systems und dem Start des Tasks an.
ms.assetid: 2a583069-ad38-43b4-bcf2-f7c9101f1927
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
ms.openlocfilehash: 91789b22b992af163e9676ef156a2a72f4316ac49b9b47b30ae5599446918bed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119334600"
---
# <a name="delay-boottriggertype-element"></a>Delay (bootTriggerType)-Element

Gibt die Zeitspanne zwischen dem Start des Systems und dem Start des Tasks an. Das Format für diese Zeichenfolge lautet PnYnMnDTnHnMnS, wobei nY die Anzahl der Jahre, nM die Anzahl der Monate, nD die Anzahl der Tage, "T" das Datums-/Uhrzeittrennzeichen, nH die Anzahl der Stunden, nM die Anzahl der Minuten und nS die Anzahl von Sekunden ist (z. B. PT5M gibt 5 Minuten an, und P1M4DT2H5M gibt einen Monat, vier Tage, zwei Stunden und fünf Minuten an). Weitere Informationen zum Dauertyp finden Sie unter <https://go.microsoft.com/fwlink/p/?linkid=106886> .

``` syntax
<xs:element name="Delay"
    type="duration"
 />
```

Das **Delay-Element** wird vom komplexen [**BootTriggerType-Typ**](taskschedulerschema-boottriggertype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                     | Abgeleitet von                                                               | Beschreibung                                                                  |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md) | [**bootTriggerType**](taskschedulerschema-boottriggertype-complextype.md) | Gibt einen Trigger an, der eine Aufgabe startet, wenn das System gestartet wird.<br/> |



## <a name="remarks"></a>Hinweise

Für die Skriptentwicklung wird die Ereignistriggerverzögerung durch die [**BootTrigger.Delay-Eigenschaft**](boottrigger-delay.md) angegeben.

Für die C++-Entwicklung wird die Ereignistriggerverzögerung durch die [**IBootTrigger::D elay-Eigenschaft**](/windows/desktop/api/taskschd/nf-taskschd-iboottrigger-get_delay) angegeben.

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

 

 





