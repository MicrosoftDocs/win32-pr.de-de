---
title: RepetitionPattern.Interval-Eigenschaft
description: Bei der Skripterstellung ruft die Zeit zwischen jedem Neustart der Aufgabe ab oder legt diese fest.
ms.assetid: c48bd304-21f3-435e-99f5-3b2da0078bb8
keywords:
- Interval-Taskplaner
- Interval-Taskplaner , RepetitionPattern-Objekt
- RepetitionPattern-Objekt Taskplaner , Interval-Eigenschaft
topic_type:
- apiref
api_name:
- RepetitionPattern.Interval
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1e81920fffe5c9fd58dd36a028b924f54ebe6dd
ms.sourcegitcommit: b3a9abea47dea7374eac0f9a95a652ac6977fb2e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/20/2021
ms.locfileid: "107734175"
---
# <a name="repetitionpatterninterval-property"></a>RepetitionPattern.Interval-Eigenschaft

Bei der Skripterstellung ruft die Zeit zwischen jedem Neustart der Aufgabe ab oder legt diese fest.

## <a name="syntax"></a>Syntax


```VB
RepetitionPattern.Interval As String
```



## <a name="property-value"></a>Eigenschaftswert

Die Zeit zwischen jedem Neustart der Aufgabe. Das Format für diese Zeichenfolge ist (z. B. `P<days>DT<hours>H<minutes>M<seconds>S` ist "PT5M" 5 Minuten, "PT1H" ist 1 Stunde und "PT20M" beträgt 20 Minuten). Die maximal zulässige Zeit beträgt 31 Tage, und die zulässige Mindestzeit beträgt 1 Minute.

## <a name="remarks"></a>Bemerkungen

Wenn Sie eine Wiederholungsdauer für eine Aufgabe angeben, müssen Sie auch das Wiederholungsintervall angeben.

Beim Lesen oder Schreiben von XML für eine Aufgabe wird das Wiederholungsintervall im [**Interval-Element**](taskschedulerschema-interval-repetitiontype-element.md) des Taskplaner angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





