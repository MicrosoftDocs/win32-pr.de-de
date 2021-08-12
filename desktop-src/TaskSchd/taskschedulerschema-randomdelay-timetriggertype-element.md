---
title: RandomDelay (timeTriggerType) -Element
description: Enthält die Verzögerungszeit, die zufällig zur Startzeit des Triggers hinzugefügt wird. | RandomDelay (timeTriggerType) -Element
ms.assetid: 84dffd18-651d-4e81-8c02-6cee9759a9b9
keywords:
- RandomDelay-Element Taskplaner
topic_type:
- apiref
api_name:
- RandomDelay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c4c9fde8a0f88ed7e87b5a0d3ccc252f141f6b677f535adf853ef0aca9499b4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118611506"
---
# <a name="randomdelay-timetriggertype-element"></a>RandomDelay (timeTriggerType) -Element

Enthält die Verzögerungszeit, die zufällig zur Startzeit des Triggers hinzugefügt wird. Das Format für diese Zeichenfolge ist PnYnMnDTnHnMnS, Dabei steht nY für die Anzahl von Jahren, nM für die Anzahl von Monaten, nD für die Anzahl von Tagen, "T" für das Datums-/Uhrzeittrennzeichen, nH für die Anzahl von Stunden, nM für die Anzahl von Minuten und nS für die Anzahl von Sekunden (PT5M gibt beispielsweise 5 Minuten an, und P1M4DT2H5M gibt einen Monat, vier Tage, zwei Stunden und fünf Minuten an). Weitere Informationen zum Dauertyp finden Sie unter <https://go.microsoft.com/fwlink/p/?linkid=106886> .

``` syntax
<xs:element name="RandomDelay"
    type="duration"
    default="PT0M"
    minOccurs="0"
 />
```

Das -Element wird durch den komplexen [**timeTriggerType-Typ**](taskschedulerschema-timetriggertype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                                    | Abgeleitet von                                                               | Beschreibung                                                                      |
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [**TimeTrigger (triggerGroup)**](taskschedulerschema-timetrigger-triggergroup-element.md) | [**timeTriggerType**](taskschedulerschema-timetriggertype-complextype.md) | Gibt einen Trigger an, der eine Aufgabe startet, wenn der Trigger aktiviert wird.<br/> |



## <a name="remarks"></a>Hinweise

Informationen zur C++-Entwicklung finden Sie unter [**RandomDelay-Eigenschaft von ITimeTrigger.**](/windows/desktop/api/taskschd/nf-taskschd-itimetrigger-get_randomdelay)

Informationen zur Skriptentwicklung finden Sie unter [**TimeTrigger.RandomDelay**](timetrigger-randomdelay.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 





