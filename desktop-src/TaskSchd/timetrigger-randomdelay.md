---
title: Timeauslöst. randomdelay-Eigenschaft
description: Ruft bei der Skripterstellung eine Verzögerungszeit ab, die der Startzeit des Auslösers zufällig hinzugefügt wird, oder legt diese fest. | Timeauslöst. randomdelay-Eigenschaft
ms.assetid: ee55dd85-9696-4872-8670-f919fca7481d
keywords:
- Randomdelay-Eigenschaft Taskplaner
- Randomdelay-Eigenschaft Taskplaner, Time-Auslöserobjekt
- Time-Auslöserobjekt Taskplaner, randomdelay-Eigenschaft
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
ms.openlocfilehash: 39c4acf4f38670332e723ac0824276695919cb1d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106365260"
---
# <a name="timetriggerrandomdelay-property"></a>Timeauslöst. randomdelay-Eigenschaft

Ruft bei der Skripterstellung eine Verzögerungszeit ab, die der Startzeit des Auslösers zufällig hinzugefügt wird, oder legt diese fest.

## <a name="syntax"></a>Syntax


```VB
TimeTrigger.RandomDelay As String
```



## <a name="property-value"></a>Eigenschaftswert

Die Verzögerungszeit, die der Startzeit des Auslösers nach dem Zufallsprinzip hinzugefügt wird. Das Format dieser Zeichenfolge lautet pnynmndtnhnmns. dabei ist "NY" die Anzahl der Jahre, "nm" die Anzahl von Monaten, "ND" die Anzahl der Tage, "t" ist das Trennzeichen für Datum/Uhrzeit, "NH" die Anzahl von Stunden, "nm" die Anzahl der Minuten und "NS" die Anzahl von Sekunden (z

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





