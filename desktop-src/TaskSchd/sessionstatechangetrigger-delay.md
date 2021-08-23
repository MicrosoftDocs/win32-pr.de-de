---
title: SessionStateChangeTrigger.Delay-Eigenschaft
description: Für die Skripterstellung ruft einen Wert ab, der angibt, wie lange eine Verzögerung vor dem Starten eines Task nach dem Erkennen einer Änderung des Sitzungszustands eines Terminalservers dauert, oder legt diesen fest.
ms.assetid: 3a17884f-fd74-491a-99dc-dce300a2cc77
keywords:
- Verzögerungseigenschaft Taskplaner
- Delay-Taskplaner , SessionStateChangeTrigger-Objekt
- SessionStateChangeTrigger-Objekt Taskplaner , Delay-Eigenschaft
topic_type:
- apiref
api_name:
- SessionStateChangeTrigger.Delay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26767aeca55af5ae208791f42b5973fa38df507a84f08f3d2d1fe8db28965b52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139353"
---
# <a name="sessionstatechangetriggerdelay-property"></a>SessionStateChangeTrigger.Delay-Eigenschaft

Für die Skripterstellung ruft einen Wert ab, der angibt, wie lange eine Verzögerung vor dem Starten eines Task nach dem Erkennen einer Änderung des Sitzungszustands eines Terminalservers dauert, oder legt diesen fest. Das Format für diese Zeichenfolge ist PnYnMnDTnHnMnS, Dabei steht nY für die Anzahl von Jahren, nM für die Anzahl der Monate, nD für die Anzahl von Tagen, "T" für das Datums-/Uhrzeittrennzeichen, nH für die Anzahl von Stunden, nM für die Anzahl von Minuten und nS für die Anzahl von Sekunden (pt5M gibt beispielsweise 5 Minuten an, und P1M4DT2H5M gibt einen Monat, vier Tage, zwei Stunden und fünf Minuten an).

## <a name="syntax"></a>Syntax


```VB
SessionStateChangeTrigger.Delay As String
```



## <a name="property-value"></a>Eigenschaftswert

Die Verzögerung, die stattfindet, bevor ein Task gestartet wird, nachdem eine Änderung des Sitzungszustands des Terminalservers erkannt wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





