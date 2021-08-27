---
title: RepetitionPattern.Interval-Eigenschaft
description: Ruft für Skripts die Zeitspanne zwischen jedem Neustart der Aufgabe ab oder legt sie fest.
ms.assetid: c48bd304-21f3-435e-99f5-3b2da0078bb8
keywords:
- Taskplaner der Interval-Eigenschaft
- Interval-Eigenschaft Taskplaner , RepetitionPattern-Objekt
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
ms.openlocfilehash: cc6efcaa56d2c251b5e044c87091bc646c21f8691aa384ad522b6062014fd496
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072620"
---
# <a name="repetitionpatterninterval-property"></a>RepetitionPattern.Interval-Eigenschaft

Ruft für Skripts die Zeitspanne zwischen jedem Neustart der Aufgabe ab oder legt sie fest.

## <a name="syntax"></a>Syntax


```VB
RepetitionPattern.Interval As String
```



## <a name="property-value"></a>Eigenschaftswert

Die Zeitspanne zwischen jedem Neustart der Aufgabe. Das Format für diese Zeichenfolge lautet `P<days>DT<hours>H<minutes>M<seconds>S` (z. B. "PT5M" ist 5 Minuten, "PT1H" ist 1 Stunde und "PT20M" ist 20 Minuten). Die maximal zulässige Zeit beträgt 31 Tage, und die zulässige Mindestzeit beträgt 1 Minute.

## <a name="remarks"></a>Hinweise

Wenn Sie eine Wiederholungsdauer für eine Aufgabe angeben, müssen Sie auch das Wiederholungsintervall angeben.

Beim Lesen oder Schreiben von XML für eine Aufgabe wird das Wiederholungsintervall im [**Interval-Element**](taskschedulerschema-interval-repetitiontype-element.md) des Taskplaner Schemas angegeben.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





