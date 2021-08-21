---
title: TimeTrigger.RandomDelay-Eigenschaft
description: Für die Skripterstellung ruft eine Verzögerungszeit ab, die zufällig zur Startzeit des Triggers hinzugefügt wird, oder legt diese fest. | TimeTrigger.RandomDelay-Eigenschaft
ms.assetid: ee55dd85-9696-4872-8670-f919fca7481d
keywords:
- RandomDelay-Taskplaner
- RandomDelay-Eigenschaft Taskplaner , TimeTrigger-Objekt
- TimeTrigger-Objekt Taskplaner , RandomDelay-Eigenschaft
topic_type:
- apiref
api_name:
- TimeTrigger.RandomDelay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cdbe297ace4fd34c2b5bf88db132e0573afd208052b50331ab571881b85831f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118354762"
---
# <a name="timetriggerrandomdelay-property"></a>TimeTrigger.RandomDelay-Eigenschaft

Für die Skripterstellung ruft eine Verzögerungszeit ab, die zufällig zur Startzeit des Triggers hinzugefügt wird, oder legt diese fest.

## <a name="syntax"></a>Syntax


```VB
TimeTrigger.RandomDelay As String
```



## <a name="property-value"></a>Eigenschaftswert

Die Verzögerungszeit, die zufällig zur Startzeit des Triggers hinzugefügt wird. Das Format für diese Zeichenfolge ist PnYnMnDTnHnMnS, Dabei steht nY für die Anzahl von Jahren, nM für die Anzahl der Monate, nD für die Anzahl von Tagen, "T" für das Datums-/Uhrzeittrennzeichen, nH für die Anzahl von Stunden, nM für die Anzahl von Minuten und nS für die Anzahl von Sekunden (pt5M gibt beispielsweise 5 Minuten an, und P1M4DT2H5M gibt einen Monat, vier Tage, zwei Stunden und fünf Minuten an).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





