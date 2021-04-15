---
title: Repetitionpattern. Interval (Eigenschaft)
description: Ruft bei der Skripterstellung die Zeitspanne zwischen den einzelnen Neustarts der Aufgabe ab oder legt diese fest.
ms.assetid: c48bd304-21f3-435e-99f5-3b2da0078bb8
keywords:
- Intervall Eigenschaft Taskplaner
- Interval-Eigenschaft Taskplaner, repetitionpattern-Objekt
- Repetitionpattern-Objekt Taskplaner, Intervall Eigenschaft
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
ms.openlocfilehash: 1d62bb821f4c5e61d344e21fafa4ba1265c73470
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518215"
---
# <a name="repetitionpatterninterval-property"></a>Repetitionpattern. Interval (Eigenschaft)

Ruft bei der Skripterstellung die Zeitspanne zwischen den einzelnen Neustarts der Aufgabe ab oder legt diese fest.

## <a name="syntax"></a>Syntax


```VB
RepetitionPattern.Interval As String
```



## <a name="property-value"></a>Eigenschaftswert

Die Zeitspanne zwischen den einzelnen Neustarts der Aufgabe. Das Format für diese Zeichenfolge ist P <days> dt <hours> H <minutes> M <seconds> S ("PT5M" ist beispielsweise 5 Minuten, "PT1H" ist 1 Stunde, und "PT20M" beträgt 20 Minuten). Die maximal zulässige Dauer beträgt 31 Tage, und die zulässige Mindestanzahl beträgt 1 Minute.

## <a name="remarks"></a>Bemerkungen

Wenn Sie eine Wiederholungs Dauer für eine Aufgabe angeben, müssen Sie auch das Wiederholungsintervall angeben.

Beim Lesen oder Schreiben von XML für eine Aufgabe wird das Wiederholungsintervall im [**Interval**](taskschedulerschema-interval-repetitiontype-element.md) -Element des Taskplaner Schemas angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





